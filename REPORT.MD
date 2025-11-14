# Project Overview
This project analyzes consumer complaints data related to the Bank of America. The goal is to uncover insights into customer issues, response effectiveness, and complaint resolution trends. Using Power BI, the project visualizes key metrics and patterns that can help the bank improve service delivery and customer satisfaction.

## Objectives
- Identify the most common complaint types and their frequencies.
- Analyze complaint resolution statuses and response timeliness.
- Assess customer satisfaction levels through complaint outcomes.
- Enable data-driven decision-making with interactive dashboards. 

## Data Overview
The dataset used in this analysis was obtained from the Consumer Financial Protection Bureau (CFPB).
It contains details on:
- Complaint ID
- Submission Channels (e.g., Web, Phone, Email)
- Product/Service Type
- Company Response to Consumer
- Complaint Status (In Progress, Closed, Closed with Response, Not Started)
- Date Received & Date Sent to Company
- Timely Response (Yes/No)
- Consumer Dispute Information

## Process and Methodology
This is the process I took to analyze the dataset:
- Identifyimg the business problem, stakeholders, business questions, and recommended insights 
- Identifying Issues and the dataset and cleaning the dataset
- Analysing and visualizing the dataset
### Step 1: Identifyimg the business problem, stakeholders, business questions, and recommended insights 
**BUSINESS PROBLEM**

From the Consumer Complaints dataset, we can see that the consumers face a number of issues when using the Bank of America’s products such as mortgage, debt collection, checkings or savings, credit reporting and so on. Some of the issues the customers encounter are: lost or stolen check, applying for a mortgage or refinancing an existing mortgage, attempts to collect debts not owed, trouble during payment process, and so on. 

**STAKEHOLDERS**

This dataset is useful to a wide range of people within and outside Bank of America. Each group can use the information in diverse ways to improve customer experience, ensure compliance, gain more customers, make better decisions, and so on. The stakeholders who will benefit from this dataset are:

- **Bank leaders, Managers, Investors, and Stakeholders:** Seeing what customers are complaining about the most will enable them spot big problems, fix them quickly, and keep customers happy.

- **Customer Service Team:** The customer service team can use this dataset to understand what customers are complaining about and how quickly these issues are resolved. The insights gained will help them improve how they communicate with the customers, train staff, reduce repeated complaints, and make the overall complaint-handling process faster and more effective.

- **Data Analytics & Business Intelligence Team:** This team can turn the dataset into easy to understand reports and dashboards that can be used to discover trends and patterns like which product has the most issues.

- **Product Managers:** The product managers can use the insights gotten from this dataset to improve product features in order to reduce customer complaints and improve customer satisfaction.

- **Legal Team:** The legal team can use this dataset to ensure that the company’s response to complaints are in line with CFPB regulations and other legal standards.

- **Public Relations (PR)** & Communications Teams: They can use it to prepare public statements based on recurring complaint themes.

- **Government Agencies & Regulators:** Government agencies and regulators can use this data to monitor the bank’s compliance with consumer protection laws and issue penalties if necessary.

- **Researchers & Policy Analysts:** Researchers can use this dataset in their research on consumer behaviour, consumer protection and systemic issues in the banking sector.

**BUSINESS QUESTIONS**

Based on the business problem, these are some of the questions we need to address: 

- What bank products have the most issues/complaints? 
- What issues occur the most? 
- What is the most used method for complaint submission by the customers? 
- How often are issues resolved on time by the bank? 
- What states have the highest number of complaints. 
- Which year, month or day did the bank receive the most complaints?
- What states have the highest on-time response rate? 
- How does the bank respond to/close consumer complaints? 
- What is the complaints resolution rate for each product? 

**RECOMMENDED INSIGHTS**

Having considered the business problem, stakeholders and business questions, the recommended insights are as follows:

- **Top N Products With Most Issues:** To identify which bank products generate the most complaints. 

- **Top N Most Frequent Issues:** To analyze which specific issues customers report the most.

- **Regional Hotspots:** To identify the states where complaints are concentrated.

- **Top N Submission Channels:** To identify which submission channels are mostly used by the customers to submit their complaints.

- **Top N States with Most Complaints:** To highlight states that generate the most complaints.

- **Complaints Trend Overtime:** To identify patterns and trends in complaints submission by the customers.

- **Customer Feedback:** To gauge how the customers feel their issues are being resolved. Do they feel that the responses to their complaints are timely or not?

- **Top 5 States with Highest On-Time Response Rate:** To show the top 5 states with the highest on-time response rate.

- **Company Response to Consumers Count Distribution:** To show how the bank responds to complaints and the most complaint resolution strategy.

- **Complaints Resolution Rate Per Product:** To Identify which product teams perform best at handling issues.

### Step 2: Identifying Issues and the dataset and cleaning the dataset
**TOOL USED**

I used Microsoft Power BI to clean the dataset.

**ISSUES FOUND**

1. The “State” column was in the text format which is correct. However, the data category was Uncategorized.
2. The “Complaint ID” column was in the whole number format.
3. There were null values in some key columns such as; the “Sub-issue”, “Company public response”, and “Timely response?” columns.
4. The “timely response?” column name is in a question format and this could interfere in or obstruct queries or formulas in some data analytics tools.

**STEPS TAKEN TO CLEAN THE DATASET**

1. I changed the data type of the “Complaint ID” column from “Whole Number” to “Text” since an ID is unique data and is not a number.
2. For the “State” column, I retained the data type as “Text” but changed the data category from “Uncategorized” to “State or Province”.
3. For the “Timely Response?” column, I changed the column name to “Responded on time” because it is easy to understand and does not contain special or misleading characters.
4. For the key columns with null values, I replaced the null values with “Unknown” to show that the values were not specified.

**CHANGES MADE TO THE COLUMN NAMES OR STRUCTURE**

1. I changed the column name of the “Timely response?” column to “Responded on time” because it is easy to understand and does not contain special or misleading characters. The “Timely response?” column name had a special character (?) that could pose some problems in some data analytics tools.
2. I changed the data type of the “Complaint ID” column from “Whole Number” to “Text”.

By implementing the steps above, the dataset is now clean and ready for analysis. We can be sure that whatever insights derived from this dataset is correct and can be trusted.

### Step 3: Analysing and visualizing the dataset
**METHOD OF ANALYSIS**

The analysis was carried out using Power BI, focusing on visual techniques to answer the key business questions.

To determine which bank products have the most complaints, I used a bar chart visual showing the count of complaints by product, based on the Complaint ID and Product columns. I applied a Top 5 filter in the filters pane to highlight the five products with the highest number of complaints.

For which issues occur the most, I used a pie chart to display the distribution of complaints by issue, utilizing the Complaint ID and Issue columns. I also applied a Top 5 filter to identify the 5 most frequent issues.

To find the most used method for complaint submission, I created a pie chart that showed the distribution of submission methods. The visual used the Complaint ID and Submitted via columns, with a Top 5 filter applied to show the 5 most common submission channels.

For how often issues are resolved on time, I analyzed the Responded on time column in a pie chart to compare the proportion of “Yes” versus “No” responses.

To identify which states have the highest number of complaints, I used a Tree map visual to display complaint distribution across states. A Top 5 filter was applied using the Complaint ID and State columns to highlight the five states with the most complaints.

To determine which year, month, or day, the bank received the most complaints, I used a line chart with the Date received and Complaint ID columns to visualize complaint trends and patterns over time.

To determine states that have the highest on-time response rate;
I Created a base measure to count the total number of complaints in the dataset: Total Complaints = COUNTROWS(Data)
I created a measure to determine the number of on-time responses: On-Time Responses = CALCULATE([Total Complaints], Data[On-Time] = “Yes")
I created another measure to determine the percentage of on-time responses: % On-Time Responses = DIVIDE([On-Time Responses], [Total Complaints])
Then I used a bar chart with: Y-axis: State, X-axis: % On-Time Responses 

To evaluate how effectively the bank resolves customer complaints across different products, I created a Complaint Resolution Rate by Product visual in Power BI. The goal was to measure the proportion of complaints that have been closed or resolved (i.e., not “In progress”) for each product category. 
I Created a measure to count all complaints whose status is not “In progress” (i.e., closed, closed with explanation, closed with monetary relief, Closed with non-monetary relief):
Closed = CALCULATE([Total Complaints], Data[Company response to consumer] <> "In progress")
I Calculated the percentage of closed complaints relative to the total complaints:
Closed % = DIVIDE([Closed], [Total Complaints])
Then, I Built a horizontal bar chart with: Y-axis: Product, X-axis: Closed %

To determine how the bank responds to/close consumer complaints, I used a column chart with: Y-axis: Total Complaints, X-axis: Company Response to Consumers

**INSIGHTS AND VISUALIZATIONS**

1. **Business Question:** What bank products have the most issues or complaints?

**Insight:** Checking or savings accounts recorded the highest number of complaints (24,814 complaints), followed by credit cards or prepaid cards (16,197 complaints). This indicates that customers experience more service-related issues in these core banking products.

**Chart Used:** Bar Chart – Count of Complaint ID by Product (Top 5 Products)

2. **Business Question:** What issues occur the most?

**Insight:** The most recurring issue is Managing an account, which represents nearly half of all complaints (about 50%), followed by Incorrect information on reports and Problems with a purchase shown on a statement.

**Chart Used:** Donut Chart – Count of Complaint ID by Issue (Top 5 Issues)

3. **Business Question:** What is the most used method for complaint submission by customers?

**Insight:** The Web is the most used submission channel, accounting for about 73% of total complaints, showing that most customers prefer digital channels to report issues.

**Chart Used:** Donut Chart – Submission Channels

4. **Business Question:** How often are issues resolved on time by the bank?

**Insight:** The majority of complaints (about 96%) were responded to on time, indicating a strong commitment to timely customer service and regulatory compliance.

**Chart Used:** Donut Chart – Response Timeliness

5. **Business Question:** What states have the highest number of complaints?

**Insight:** The top five states with the highest number of complaints are California (CA), Florida (FL), Texas (TX), New York (NY), and Georgia (GA). These states may represent larger customer bases or higher engagement levels with Bank of America’s products.

**Chart Used:** Tree Map – Complaint Count by State (Top 5 States)

6. **Business Question:** Which year, month, or day did the bank receive the most complaints?

**Insight:** The complaint trend shows a gradual increase over time (the year 2022 recorded the highest number of complaints), with noticeable spikes in recent years, suggesting rising customer awareness and engagement with complaint channels.

**Charts Used:** Line Chart – Top 5 States With Most Complaints 

7. **Business Question:** What states have the highest on-time response rate?

**Insight:** The chart shows that the top 5 states that have the highest on-time response rate are; South Dakota (SD), Utah (UT), Maine (ME), Louisiana (LA), and New Hampshire (NH).

**Charts Used:** Bar Chart – Top 5 States With On-Time Response Rate

8. **Business Question:** How does the bank respond to/close consumer complaints?

**Insight:** The chart shows that most of the consumer complaints were closed with explanation. The next in line is closed with monetary relief.

**Charts Used:** Column Chart – Company Responses to Consumers

9. **Business Question:** What is the complaints resolution rate for each product? 

**Insight:** The bar chart shows that the product, student loan, has a 100% complaint resolution rate. This means that all complaints for student loan have been resolved (none are currently “In progress”).

**Charts Used:** Bar Chart – Complaint Resolution Rate by Product

## Dashboard Summary
**Dashboard 1 Title:** BOA Customer Complaints Overview & Insights

**KPIs:** Total Complaints, Top Issue, Top Issue - Prod., Top Issue - State

**Visuals:** Top 5 Products with Most Complaints, Top 5 Recurring Issues, Complaints Trend Overtime, Top 5 States With Most Complaints, and Top 5 Submission Channels.


