# Charity Fundraising Analysis
Analyzing a fundraising dataset to evaluate data quality, supporter behaviour, and fundraising performance.<br/><br/>
**Skills:** Data Cleaning, Data Visualization, Data Analysis. <br>
**Tools:** Microsoft Excel, Microsoft Powerpoint.

## Scenario
The fundraising team from an environmental charity would like to understand more about the quality of their data, the supporters they have and their giving behaviour, and the performance of the charity’s fundraising activities. My task is to explore the data, analyse and extract key insights from the data and present my findings.

### Definitions & Clarifications
* A ‘Fund’ is an allocation of funds to a particular purpose, ie. how that money can be spent by the charity.
* A ‘Campaign’ is a broad categorisation of fundraising activities. A single Campaign can have multiple Appeals associated with it.
* An ‘Appeal’ is a more granular categorisation of fundraising activities. Each Appeal is associated with one Campaign.

> [!NOTE]
> The dataset was provided with limited context, based only on the information outlined in this section.

## Analysis
### 1. Methodology
>_Tools used and their applications_

#### 1.1 Usage of MS Excel
Why?
* Familiarity and comfort over SQL
* Alternatives better suited for other purposes
  
How?
* Usage of Power Pivot add-on
* Utilizing Pivot Tables for analysis and visuals’ creation
* Using helper columns and formulas where necessary

#### 1.2 Data Cleaning
Dates in Transactions[date] not in standardized form –
* 8th Apr 2025
* 16th Mar 2025

Data Type Conversion from ‘Text’ to ‘Currency’ for –
* Campaigns[goal_amount]
* Appeals[goal_amount]
* Transactions[amount]

#### 1.3 Relationships between tables
![1.3 Relationships between tables](/images/1.3%20Relationships%20between%20tables.jpg)

Establishing correct relationships –
* Allows pivot tables to connect and aggregate data seamlessly across multiple tables.
* Ensure data accuracy and consistency in analysis.

