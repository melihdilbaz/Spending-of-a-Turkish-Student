# Spending-of-a-Turkish-Student

I decided to choose a claim as the following (notice that I study and live in Turkey):  
**In the high inflation environment, as a student, my spending habits shifted away from discretionary purchases.**

## Project Workflow

Firstly, I have downloaded my spending history focused on the periods when I have actively participated in the school life. In total, I got 5 school terms to analyze, which had the information for each transaction occurred in my account, being enlisted as: 
  - `Tarih`
  -  `Tutar`
  -   `Bakiye`
  -   `Açıklama`

1. **Each data point is categorized as discretionary or essential along with the following subcategories:**
   - Cafeteria food
   - Market – grocery
   - Education
   - Savings
   - Entertainment
   - Dining out - food
   - Dining out - coffee
   - Fashion
   - Transportation
   - Others
2. All data points are merged into the day they belong to.
3. The corresponding day is mapped to the day of the week as a new field.
4. Each day has a `bakiye` (remaining balance) value for the start of the day.
5. Each day has a `total tutar` (total spending) value for all transactions that day.
6. Each day has a `discretionary share` value, representing the proportion of discretionary spending over the total spending.

Secondly, I reached out to the official datas being published by TÜİK in between 2022 and 2024 for the inflation rates for annual and monthly scale (TÜFE). I tried to feed the cumulative inflation data with the datas I scraped from the TÜİK's website. Cumulative inflation along with the monthly inflation will be laid down with my own spending history and be analyzed for the claim I proposed at the beginning.

## Questions to Address
- **Does the official inflation rate reflect an increase in the volume of spending?**
  - Compare the spending volumes with inflation rates for the same months.
  - Analyze the change in spending volume over the term.
- **Is there a shift in the type of the favorite discretionary purchase?**
- **Has the share of discretionary purchases over the total daily / weekly spending decreased?**
- **Which days are more suitable for discretionary spending?**
- **Are income days and spending correlated?**

### Analysis Focus
- Show weekly/monthly spending trends and the share of both discretionary and essential categories over incomes.
- Identify the main sources of income and analyze whether they mitigate the effects of inflation:
  - Limited income
  - Reliance on allowances
  - Part-time jobs

### Key Insights
- Discretionary spending is more elastic to economic pressures, especially in a high-inflation environment.
- Analyze whether the main sources of income provide enough financial stability for a student under inflationary pressures.

## ML Modeling
- **Objective:** Possibly can be set as getting some options of spending for an entered amount of money for the day.
  - Inputs: The amount of money.
  - Outputs: Predicted list of purchases for the day.



