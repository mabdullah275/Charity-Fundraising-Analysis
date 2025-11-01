# Charity Fundraising Analysis
Analyzing a fundraising dataset to evaluate data quality, supporter behaviour, and fundraising performance.<br/><br/>
**Skills:** Data Cleaning, Data Visualization, Data Analysis. <br>
**Tools:** Microsoft Excel, Microsoft Powerpoint.

## Scenario
The fundraising team from an environmental charity would like to understand more about the quality of their data, the supporters they have and their giving behaviour, and the performance of the charity’s fundraising activities. My task is to explore the data, analyse and extract key insights from the data and present my findings.

| Term | Definition & Clarification |
| :- | :- |
| Fund | An allocation of funds to a particular purpose, ie. how that money can be spent by the charity. |
| Campaign | A broad categorisation of fundraising activities. A single Campaign can have multiple Appeals associated with it. |
| Appeal | A more granular categorisation of fundraising activities. Each Appeal is associated with one Campaign. |

> [!NOTE]
> The dataset was provided with limited context, based only on the information outlined in this section.

## Analysis
### 1. Methodology
>_Tools used and their applications_

#### 1.1 Usage of Excel
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

| Table 1 | Cardinality | Filter Direction | Table 2 |
| :- | :- | :- | :- | 
| transactions[appeal_id] | Many to One | << To transactions | appeals[appeal_id] | 
| transactions[campaign_id] | Many to One | << To transactions | campaigns[campaign_id] |
| transactions[fund_id] | Many to One | << To transactions | funds[fund_id] | 
| transactions[supporter_id] | Many to One | << To transactions | supporters[constituent_id] | 

Establishing correct relationships –
* Allows pivot tables to connect and aggregate data seamlessly across multiple tables.
* Ensure data accuracy and consistency in analysis.

### 2. Supporter Insights

#### 2.1 Demographics
<img src="images/2.1%20Demographics.png">

#### 2.2 Donor Behaviour
<img src="images/2.2%20Donor%20Behaviour.png">
> [!IMPORTANT]
> Donors with at least two donations, including one in 2024 or later, are considered regular.

#### 2.3 Preferred Payment Methods
<img src="images/2.3%20Preferred%20Payment%20Methods.png">

#### 2.4 Top Supporters
<table>
<tr><th>Top 5 Individual Supporters</th><th>Top 5 Organization Supporters</th></tr>
<tr>
<td>
| Supporter ID | Full Name | Avg Donation Amount |
| :-: | :-: | :-: |
| 2749 | Richard Thompson | £112,717.24 |
| 2243 | Angela Kelly  | £83,817.38 |
| 1980 | Sandra Stewart | £71,852.93 |
| 4169 | Jessica Gilmore | £70,051.86 |
| 3905 | William Chang | £67,543.65 |
</td>
<td>
|Supporter ID| Full Name | Avg Donation Amount|
| :-: | :-: | :-: |
| 433 | Whitaker PLC | £636,840.54 |
| 465 | Lane, Brooks and Wagner | £274,361.61 |
| 480 | Rodriguez Inc | £260,868.75 |
| 203 | Garcia-Novak | £250,337.06 |
| 434 | Chambers-Strickland | £244,459.82 |
</td>
</tr> 
</table>