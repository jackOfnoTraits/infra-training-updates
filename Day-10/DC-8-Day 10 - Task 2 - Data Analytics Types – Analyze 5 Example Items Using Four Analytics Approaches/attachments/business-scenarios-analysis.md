# 5 Business Scenarios: The Four Types of Data Analytics

## 1. Declining Sales in an E-commerce Business

**Problem:** An online retail company notices that its monthly sales have dropped significantly.

### Descriptive Analysis — What happened?

Monthly sales decreased by 25% compared with the previous month. The number of completed orders also declined.

### Diagnostic Analysis — Why did it happen?

Analysis of website traffic, customer behavior, and checkout data reveals that more customers abandoned their shopping carts after shipping fees increased.

### Predictive Analysis — What might happen next?

If cart abandonment continues at the current rate, sales may decline further over the next month. A forecasting model could estimate the likely revenue impact.

### Prescriptive Analysis — What should we do?

Test free shipping above a minimum order value, offer targeted promotions, and optimize the checkout process. Compare conversion rates before and after the changes.

---

## 2. High Employee Turnover in a Company

**Problem:** A company is losing employees faster than expected, increasing recruitment and training costs.

### Descriptive Analysis — What happened?

The employee turnover rate increased from 10% to 22% over six months, with most resignations occurring among employees with less than two years of experience.

### Diagnostic Analysis — Why did it happen?

Exit interviews, salary benchmarks, engagement surveys, and promotion records indicate that below-market salaries and limited career advancement may be contributing to resignations.

### Predictive Analysis — What might happen next?

Employees in departments with low engagement and few promotion opportunities may have a higher likelihood of leaving in the next quarter.

### Prescriptive Analysis — What should we do?

Review compensation, create career development plans, train managers, and introduce retention initiatives in high-turnover departments. Measure their effectiveness while protecting employee privacy.

---

## 3. Frequent Server Outages in an IT Company

**Problem:** An online service experiences repeated outages, disrupting customers and business operations.

### Descriptive Analysis — What happened?

The production application experienced five outages in one week, resulting in 90 minutes of total downtime and failed customer requests.

### Diagnostic Analysis — Why did it happen?

Log analysis, infrastructure metrics, and incident timelines reveal that the database connection pool was exhausted during traffic spikes, preventing new requests from being served.

### Predictive Analysis — What might happen next?

Based on traffic forecasts and historical resource usage, the system may experience another outage during the next peak period if database connections remain a bottleneck.

### Prescriptive Analysis — What should we do?

Optimize database queries, tune connection pools, introduce backpressure and request timeouts, and configure autoscaling where appropriate. Add monitoring and load-test the system before peak traffic.

---

## 4. Inventory Shortages in a Retail Business

**Problem:** A retail chain frequently runs out of popular products while holding excess stock of other items.

### Descriptive Analysis — What happened?

The company experienced stockouts for 15% of its top-selling products, while slow-moving products occupied a large share of warehouse space.

### Diagnostic Analysis — Why did it happen?

Sales history, purchase orders, and supplier delivery records show that demand was underestimated for popular products and some suppliers consistently delivered late.

### Predictive Analysis — What might happen next?

Demand forecasting suggests that certain products will face shortages during upcoming holidays, while slow-moving items are likely to remain in storage.

### Prescriptive Analysis — What should we do?

Set dynamic reorder points and safety stock levels, adjust purchase quantities based on demand forecasts, and identify alternative suppliers for critical products.

---

## 5. Increasing Customer Complaints in a Telecom Company

**Problem:** A telecommunications company receives more customer complaints and notices declining customer satisfaction.

### Descriptive Analysis — What happened?

Customer complaints increased by 35% over three months, and customer satisfaction scores declined from 4.2 to 3.4 out of 5.

### Diagnostic Analysis — Why did it happen?

Complaint categories, network performance data, and support records reveal that dropped calls in certain regions and long customer service wait times account for a large proportion of complaints.

### Predictive Analysis — What might happen next?

Customers experiencing repeated service failures and unresolved complaints may be more likely to switch providers, potentially increasing customer churn.

### Prescriptive Analysis — What should we do?

Prioritize network repairs in affected regions, improve support staffing during peak hours, and proactively contact customers with unresolved issues. Track complaint rates and customer retention after the improvements.

---

## Quick Comparison: All Five Scenarios

| Business problem    | Descriptive: What happened? | Diagnostic: Why?                         | Predictive: What's next?    | Prescriptive: What to do?           |
| ------------------- | --------------------------- | ---------------------------------------- | --------------------------- | ----------------------------------- |
| E-commerce sales    | Sales fell                  | Shipping fees increased cart abandonment | Sales may fall further      | Test shipping incentives            |
| Employee turnover   | Resignations increased      | Pay and career growth concerns           | More resignations may occur | Improve retention                   |
| IT outages          | Downtime increased          | Database connections exhausted           | Outages may recur           | Optimize and monitor infrastructure |
| Inventory shortages | Stockouts and excess stock  | Poor demand estimates and late suppliers | Future shortages likely     | Optimize replenishment              |
| Telecom complaints  | Complaints increased        | Network failures and long waits          | Customer churn may rise     | Fix network and improve support     |

## Key Idea to Remember

1. **Descriptive analytics = Past:** What happened?
2. **Diagnostic analytics = Explanation:** Why did it happen?
3. **Predictive analytics = Future:** What might happen next?
4. **Prescriptive analytics = Action:** What should we do?

In practice, these four approaches work together. A business first measures a problem, investigates its causes, forecasts what may happen, and then chooses actions that are likely to produce a better outcome. Forecasts and recommendations should be validated against real data and measured results.
