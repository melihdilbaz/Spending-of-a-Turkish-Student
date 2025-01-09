# Spending-of-a-Turkish-Student

I decided to choose a claim as the following (notice that I study and live in Turkey):  
**In the high inflation environment, as a student, the shift in my spending habits is not from discretionary purchases.**

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
   
    ✅ The raw data is made focused on the school terms specifically. Based on the words inside the `Açıklama` column, there detected the type of the sub category and it is assigned to the regarding transaction.
   
    ✅ Since the `Cafeteria food` is on the basis of a large **charge-up** and being served long-lasting, it needed a distributed scale of those school-id cafeteria charge-ups. Starting from the day the charg-up occurs, up until the day the same type transaction holds, every day is equally allocated a share. Only the days that `Dining out - food` is happened, are passed.

   - For some days, there shares fell short between the charge-up days, it caused very small shares a day far from the reality for the time being. To scale this up, the average cafeteria spending a day (slighly less than the average spending) is assigned to the years and if transaction money falls short on those time periods, those assigned realistic values replaced the initial shares.
   - P.S. This supposedly realistic values are determined by the first-hand experience, the prices for those times are considered.
   - P.S. Some part of categorization is handled by python code whereas 10% of all data are categorized manuelly and corrected.
     
3. All data points are merged into the day they belong to.
4. The corresponding day is mapped to the day of the week as a new field.
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



