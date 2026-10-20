# KAN-125: Day 6 | Task 6 | Create Docker Networks and Test Port Conflicts

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-125
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** pranavi selvaraju
- **Created:** 2026-10-18T17:35:53.718Z
- **Updated:** 2026-10-19T16:17:44.083Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Objective: Inspect Docker networks, test container connectivity, compare bridge and host networking, and document port conflicts.

docker network ls
docker run -itd --name c1 alpine
docker run -itd --name c2 alpine
docker ps
docker inspect c2
docker inspect -f "{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}" c2
docker exec -it c1 sh

Inside c1, ping the IP address returned for c2 (if ping is available), then exit.

ping -c 3 CONTAINER_IP
exit
docker network create --driver bridge akshiv_net
docker network ls
docker network inspect akshiv_net
docker run -itd --name a1 --network akshiv_net alpine
docker run -itd --name a2 --network akshiv_net alpine
docker exec -it a1 sh

Inside a1, test automatic name resolution on the custom bridge network, then exit.

ping -c 3 a2
exit
docker network inspect akshiv_net
docker run -d --name web1 --network akshiv_net nginx
docker run -d --name web2 --network akshiv_net httpd
docker ps
docker logs web1
docker logs web2

Both servers can use internal port 80 because they have separate container network namespaces. Publish them on different host ports for external access:

docker run -d --name web3 -p 8081:80 nginx
docker run -d --name web4 -p 8082:80 httpd

On a supported Linux host, compare host networking and inspect the results:

docker run -d --network host --name hostcont1 nginx
docker run -d --network host --name hostcont2 httpd
docker ps -a
docker logs hostcont1
docker logs hostcont2
sudo ss -lntp | grep ":80"

Expected outcome: Custom bridge network is created; container-name connectivity is tested; same internal port and separate host-port mappings are demonstrated; host-network port conflicts are documented.

## Attachments

- [Screenshot 2026-10-16 at 3.47.27 PM.png](attachments/Screenshot%202026-10-16%20at%203.47.27%20PM.png)
- [Screenshot 2026-10-16 at 3.47.36 PM.png](attachments/Screenshot%202026-10-16%20at%203.47.36%20PM.png)
- [Screenshot 2026-10-16 at 3.49.53 PM.png](attachments/Screenshot%202026-10-16%20at%203.49.53%20PM.png)
- [Screenshot 2026-10-16 at 3.50.09 PM.png](attachments/Screenshot%202026-10-16%20at%203.50.09%20PM.png)
- [Screenshot 2026-10-16 at 3.50.18 PM.png](attachments/Screenshot%202026-10-16%20at%203.50.18%20PM.png)
