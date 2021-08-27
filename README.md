# Kickstarter
Performing analysis on Kickstarter data to uncover trends.

This dataset will allow us to perform data analysis on many funded projects in order to uncover trends.
First, we must just familiarize ourselves with the data in order to see what we’re working with and see how we can better organize it in order to further analyze.
We can see some columns referring to the goal which tells us how much money each campaign will need to succeed, the pledged column tells us how much each campaign actually made, the outcomes column tells us if the campaign met its goal, and the country column lists the country in which the campaign was started.

### Filter
By using the filter button, we can filter one or more columns by many variables. For instance, we will later filter outcomes by “success” and “failed” to only view data with that specific outcome.

### Conditional Formatting
If we wanted to better visualize the success, failed, live, and canceled outcomes at a glance, we can apply “Conditional Formatting” and color code by each outcome. The purpose for doing this is that we can quickly see the outcomes without reading every individual row.

### Calculations
Now, we’ll add some new “Percentage Funded” data in order to better compare each row by their goal and pledge proportionately to one another.
We will first name the next empty column “Percentage Funded”, where in this column we will create a function that divides column E values by column D values, multiplying it by 100, and rounding it to the nearest whole number, giving us the percentage in donations funded.

We can also create a column for the average donations each kickstarter has been funded. In order to create that function, we can divide the pledged column by the backers column and have it rounded to the nearest hundredths.

### Errors
Now that we’ve added some columns, this average donation column may have some errors so we need to fix that in order to make sure our data is clean.
We find the error < #DIV/0! > in this new column meaning that some were divided by 0. Instead, we can input < =IFERROR(value,value_if_error) > in order to put the value of 0 in those errors and clean the data.

### Pivot Tables
Pivot tables help condense data into a summary and gives the user the ability to organize what they want to see. We can also use these tables to better visualize data and to create charts.

### Pivot Charts
Below, I've created a stacked bar graph that visualizes the outcomes of every parent category. We can clearly see that the theatre category had the most successful outcomes.

![image](https://user-images.githubusercontent.com/57331058/131051968-5f2322fe-6feb-413a-9f78-6ca096d211f8.png)

I've also created a bar graph for the subcategories and their outcomes. It's clear that plays were the most successful in the subcategories.

![image](https://user-images.githubusercontent.com/57331058/131051886-b50a6505-7936-44ef-b0fe-2ca86161de57.png)

#### Making Line Graphs
By converting the time format of the date created and date ended, we can also see how long these campaigns lasted in order to see what month these campaigns were being funded the most. These would be our "Outcome Based on Launch Date" graph.

![image](https://user-images.githubusercontent.com/57331058/131052277-077a6a0b-5cb9-4b84-965b-e5093e9d4db2.png)

### Box Plots
Box plots aid in visualization of distributions of one or more columns. Here we see the distribution between the goals and the pledged when we filter these to only in GB and the subcategory as "musicals". We can now see that half of the goals are less than £2000 and we can also see that the goals were a lot higher in general than the amounts pledged.

![image](https://user-images.githubusercontent.com/57331058/131053320-041ed26f-c2b2-405d-97cd-3fdfe1454caf.png)

