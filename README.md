# Airplane Customer Satisfaction Analysis


## About Dataset
Dataset: [Maven Analytics](https://www.mavenanalytics.io/data-playground?accessType=open&dataStructure=5wfxyeVf1etbP4TXdyPdG1) 

Customer satisfaction scores from 120,000+ airline passengers, including additional information about each passenger, their flight, and type of travel, as well as ther evaluation of different factors like cleanliness, comfort, service, and overall experience. This analysis is to analyze how each factors affects the customers satisfaction.

Data Dictionary
<table>

<tr>
<td> ID </td>
<td>Unique passenger identifier </td>
</tr>

<tr>
<td>Gender </td>
<td>Gender of the passenger (Female/Male) </td>
</tr>

<tr>
<td> Age </td>
<td> Age of the passenger </td>
</tr>
 
<tr>
<td> Customer Type </td>
<td> Type of airline customer (First-time/Returning)</td>
</tr>

<tr>
<td> Type of Travel </td>
<td>Purpose of the flight (Business/Personal) </td>
</tr>

<tr>
<td> Class </td>
<td> Travel class in the airplane for the passenger seat</td>
</tr>

<tr>
<td> Flight Distance </td>
<td>Flight distance in miles </td>
</tr>

<tr>
<td> Departure Delay </td>
<td>Flight departure delay in minutes </td>
</tr>

<tr>
<td> Arrival Delay </td>
<td>Flight arrival delay in minutes </td>
</tr>

<tr>
<td> Departure and Arrival Time Convenience </td>
<td> Satisfaction level with the convenience of the flight departure and arrival times from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td> Ease of Online Booking </td>
<td> "Satisfaction level with the online booking experience from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td> Check-in Service </td>
<td> "Satisfaction level with the check-in service from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td>Online Boarding  </td>
<td>"Satisfaction level with the online boarding experience from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td> Gate Location </td>
<td> "Satisfaction level with the gate location in the airport from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td> On-board Service </td>
<td>"Satisfaction level with the on-boarding service in the airport from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td> Seat Comfort </td>
<td>"Satisfaction level with the comfort of the airplane seat from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td>Leg Room Service  </td>
<td>"Satisfaction level with the leg room of the airplane seat from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td>Cleanliness  </td>
<td> "Satisfaction level with the cleanliness of the airplane from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td> Food and Drink </td>
<td>"Satisfaction level with the food and drinks on the airplane from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td>In-flight Service  </td>
<td> Satisfaction level with the in-flight service from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td> In-flight Wifi Service </td>
<td>"Satisfaction level with the in-flight Wifi service from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td> In-flight Entertainment </td>
<td> Satisfaction level with the in-flight entertainment from 1 (lowest) to 5 (highest) - 0 means ""not applicable"""</td>
</tr>

<tr>
<td>  Baggage Handling</td>
<td>"Satisfaction level with the baggage handling from the airline from 1 (lowest) to 5 (highest) - 0 means ""not applicable""" </td>
</tr>

<tr>
<td>  Satisfaction</td>
<td> Overall satisfaction level with the airline (Satisfied/Neutral or unsatisfied)</td>
</tr>

</table>

## Analysis Process
1. Data Exploration
2. Data Cleaning
3. Feature Engineering
4. Visualizations
5. Exploratory Data Analysis

## Data Exploration

The dataset has 129, 880 rows and 24 columns. 14 of which are ratings of services provided by the airline. Results of the exploration phase are:
- 393 missing data in `Arrival Delay`
- There are no duplicates
- `Arrival Delay` had the wrong data type
- The average customer age is 39 years
- Average arrival delay and departure delay is 15 minutes
- The average flight distance covered by the airline is 1190 miles

## Data Cleaning

Data cleaning steps taken in this ananlysis includes:
- Replacing missing values with "0" 
- Changing data types

## Feature Engineering

New features/columns were created to aid in-depth analysis of the data. The following are the new features created.
- `Total Delay`: `Arrival delay` + `Departure delay`	
- `Age_cat`: Age category for customers(0-12: Child, 13-19: Teen, 20-59: Adult, 60-100: Elder)
- `Flight_cat`: flight category for customers(0-700: Short-haul, 701-2999: Medium-haul, >3000: Long-haul)
- `Total Average Rating`: Total average across all 14 services for every customer.

## Visualizations

The visualization process involves exploring the datasets through plots and charts using seaborn and matplot libraries. The visualizations done here help create questions for the exploratory data analysis process. 
Insights from the visualizations shows that there are:
- 43% satisfied customers
- More females to males
- More Returning customers than first timers
- More Business purpose flights
- More Business class than Economy and  more Economy than Economy plus
- More Medium Haul flights to Short-haul and more Short-haul to Long-haul fights
- More Adult passengers than Elders,  Elders than teens and more teens than children.

## Exploratory Data Analysis

<b>Satisfaction Rate across Customer type, Class, Type of Travel, Age Category and and Flight category </b>

<b>Customer Type</b> 

25% of First time customers were satisfied
48% of Returning customers were satisfied

<b>Class</b>

70% of passengers who flew Business class were satisfied<br>
~25% of passengers who flew Economy Plus class were satisfied <br>
~ 20% of passengers who flew Economy class were satisfied

<b>Type of Travel</b>

~60% of passengers travelling for Business purposes were satisfied <br>
~10% of passengers travelling for Personal Reasons were satisfied

<b>Age Category</b>

~ 17% Children were satisfied with their flight <br>
~ 20% Teens were satisfied with their flight <br>
~ 49% Adults were satisfied with their flight <br>
~ 23% Elders were satisfied with their flight

<b>Flight Category</b>

~ 80% of passengers who flew Long -haul distances were satisfied <br>
~ 48% of passengers who flew Medium-haul distances were satisfied <br>
~ 31% of passengers who flew Short-haul distances were satisfied