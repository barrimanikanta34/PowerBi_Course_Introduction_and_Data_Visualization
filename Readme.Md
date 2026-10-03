# 📊 Power BI Data Visualization Collection

A complete collection of **Power BI visualizations** created to understand how different charts and visuals can be used for data analysis and reporting.

Each section contains:
- Purpose of the visual
- Suitable data types
- Important Power BI fields/settings
- When to use the visual
- A clickable image that opens the visualization directly

> **Note:** Keep the image files inside the `Images` folder and update the image filenames below if your filenames are different.

---

## 📑 Table of Contents

1. [Clustered Column Chart](images\image08.png)
2. [Clustered Bar Chart](images\image09.png)
3. [Line Chart](images\image02.png)
4. [Area Chart](images\image03.png)
5. [Ribbon Chart](images\image06.png)
6. [Line and Stacked Column Chart](images\image09.png)
7. [Line and Clustered Column Chart](images\image09.png)
8. [Scatter Plot](Images\image3.png)
9. [Bubble Map](images\image3.png)
10. [Table](images\image09.png)
11. [Matrix](images\image10.png)
12. [Funnel Chart](images\image09.png)
13. [Pie Chart](images\image07.png)
14. [Donut Chart](images\image07.png)


---

# 1. Clustered Column Chart

The **Clustered Column Chart** compares multiple measures or categories using vertical columns placed side-by-side.

### Suitable Data

Best suited for:
- Category-wise comparisons
- Sales by category
- Profit by region
- Sales by segment
- Comparing multiple groups within the same category

### Recommended Fields

- **X-axis:** Categorical column such as Category, Region, Segment
- **Y-axis:** Numerical measure such as Sales, Profit, Quantity
- **Legend:** Optional categorical field such as Segment

### Example

Sales can be compared across Technology, Furniture, and Office Supplies, with different customer segments displayed side-by-side.

### Power BI Features

Useful settings include:
- Data labels
- X-axis and Y-axis formatting
- Legend
- Gridlines
- Columns
- Zoom slider when available
- Tooltips
- Conditional formatting

### Visualization

[![Clustered Column Chart](Images/clustered-column-chart.png)](Images/clustered-column-chart.png)

---

# 2. Clustered Bar Chart

The **Clustered Bar Chart** displays horizontal bars and is useful when category names are long or when many categories need to be compared.

### Suitable Data

Best suited for:
- Sales by category
- Profit by city
- Quantity by product
- Regional comparisons
- Ranking categories

### Recommended Fields

- **Y-axis:** Category or other categorical field
- **X-axis:** Numerical measure
- **Legend:** Optional grouping field

### Power BI Features

Useful settings include:
- Data labels
- X-axis and Y-axis
- Legend
- Gridlines
- Bars
- Tooltips
- Sorting

### Visualization

[![Clustered Bar Chart](Images/clustered-bar-chart.png)](Images/clustered-bar-chart.png)

---

# 3. Line Chart

A **Line Chart** shows how a numerical value changes across an ordered category, especially time.

### Suitable Data

Best suited for:
- Sales over time
- Profit by year
- Quantity by month
- Revenue trends
- Website traffic trends

### Recommended Fields

- **X-axis:** Date, Year, Quarter, Month, or another ordered category
- **Y-axis:** Sales, Profit, Quantity, Revenue, etc.
- **Legend:** Optional category or segment

### Important Features

- Data labels
- Markers
- X-axis
- Y-axis
- Legend
- Gridlines
- Zoom slider
- Tooltips

### Visualization

[![Line Chart](Images/line-chart.png)](Images/line-chart.png)

---

# 4. Area Chart

An **Area Chart** combines a line with a filled area underneath it. It is useful for showing trends and the magnitude of values.

### Suitable Data

Use it for:
- Quantity over time
- Sales trends
- Website traffic
- Revenue trends
- Cumulative or continuous measurements

### Recommended Fields

- **X-axis:** Time or ordered category
- **Y-axis:** Numerical measure
- **Legend:** Optional

### Power BI Features

- Data labels
- X-axis
- Y-axis
- Legend
- Gridlines
- Zoom slider
- Tooltips

### Visualization

[![Area Chart](Images/area-chart.png)](Images/area-chart.png)

---

# 5. Ribbon Chart

A **Ribbon Chart** shows changes in the ranking of categories across a dimension such as time.

### Suitable Data

Useful for:
- Product rankings by year
- Category rankings by month
- Sales rankings
- Regional performance
- Segment movement

### Recommended Fields

- **X-axis:** Time or another ordered category
- **Y-axis:** Numerical measure
- **Legend:** Category used for ranking

### Important Power BI Features

- Data labels
- Legend
- X-axis
- Y-axis
- Gridlines
- Tooltips
- Sorting

### Visualization

[![Ribbon Chart](Images/ribbon-chart.png)](Images/ribbon-chart.png)

---

# 6. Line and Stacked Column Chart

The **Line and Stacked Column Chart** combines stacked columns with a line. It is useful when a total or grouped value needs to be compared with another measure.

### Suitable Data

Examples:
- Sales by ship mode and segment
- Revenue by category with profit trend
- Sales by region with margin
- Multiple segments over time

### Recommended Fields

- **X-axis:** Category or time
- **Column Y-axis:** Numerical measure
- **Line Y-axis:** Another numerical measure
- **Column series / Legend:** Grouping field

### Power BI Features

- Column formatting
- Line formatting
- Secondary Y-axis
- Data labels
- Legend
- Gridlines
- Zoom slider
- Tooltips

### Visualization

[![Line and Stacked Column Chart](Images/line-stacked-column-chart.png)](Images/line-stacked-column-chart.png)

---

# 7. Line and Clustered Column Chart

The **Line and Clustered Column Chart** compares multiple column values while displaying another measure as a line.

### Example

Sales and Quantity can be compared by year and category.

### Suitable Data

This visual works well when:
- Two or more categories need side-by-side comparison
- Another measure needs to be shown as a line
- Measures have different scales

### Recommended Fields

- **X-axis:** Year, Month, Category, etc.
- **Column Y-axis:** Sales or another numerical measure
- **Line Y-axis:** Quantity, Profit, Margin, etc.
- **Column series:** Category or Segment

### Secondary Axis

When the line measure has a very different scale from the columns, the **Secondary Y-axis** can make the comparison easier to read.

### Visualization

[![Line and Clustered Column Chart](Images/line-clustered-column-chart.png)](Images/line-clustered-column-chart.png)

---

# 8. Scatter Plot

A **Scatter Plot** displays individual observations using two numerical variables.

The example compares **Sales** and **Profit**.

### Suitable Data

Use scatter plots for:
- Sales vs Profit
- Price vs Quantity
- Advertising spend vs Revenue
- Customer value vs Orders
- Any relationship between two numerical variables

### Recommended Fields

- **X-axis:** Numerical variable such as Sales
- **Y-axis:** Numerical variable such as Profit
- **Details:** Optional field to identify individual observations
- **Legend:** Optional category
- **Size:** Optional third numerical variable

### What It Helps Identify

- Positive or negative relationships
- Clusters
- Outliers
- Concentration of observations
- Possible correlations

### Visualization

[![Scatter Plot](Images/scatter-plot.png)](Images/scatter-plot.png)

---

# 9. Map

The **Map visual** represents geographical data using locations and bubbles.

The example shows **Sales by City**.

### Suitable Data

Best suited for:
- Sales by city
- Customers by location
- Profit by country
- Store locations
- Orders by geographic area
- Regional business analysis

### Recommended Fields

Possible geographic fields:
- Country
- State
- City
- Postal Code
- Latitude
- Longitude

Numerical fields:
- Sales
- Profit
- Quantity
- Customer Count

### Important Settings

- Map settings
- Bubbles
- Legend
- Category labels
- Heat map
- Zoom controls
- Tooltips

### Data Category

For accurate geographic plotting, assign the appropriate **Data Category** in Power BI, such as:
- Country/Region
- State or Province
- City
- Postal Code
- Latitude
- Longitude

### Visualization

[![Map - Sales by City](Images/map-sales-by-city.png)](Images/map-sales-by-city.png)

---

# 10. Table

The **Table visual** displays detailed records in a vertical tabular format.

### Suitable Data

Useful for:
- Customer details
- Product details
- Order information
- Sales transactions
- Profit records
- Detailed reports

### Example Fields

- Country
- Region
- City
- Customer Name
- Sales
- Profit
- Quantity

### Important Features

- Column sorting
- Data formatting
- Conditional formatting
- Totals
- Tooltips
- Search/filtering through report interactions

### When to Use

Use a Table when users need to see **individual records and detailed values** rather than only summarized trends.

### Visualization

[![Table Visual](Images/table-visual.png)](Images/table-visual.png)

---

# 11. Matrix

The **Matrix visual** is similar to a table but provides hierarchical rows and columns with summarized values.

### Example Structure

**Rows**
- Country
- City

**Columns**
- Region

**Values**
- Sum of Sales
- Sum of Profit

### Suitable Data

Use a Matrix for:
- Hierarchical analysis
- Region → City analysis
- Year → Quarter → Month analysis
- Category → Sub-category analysis
- Cross-tab reports

### Important Features

- Row hierarchy
- Column hierarchy
- Expand/collapse
- Drill up
- Drill down
- Subtotals
- Grand totals
- Conditional formatting
- Sorting

### Visualization

[![Matrix Visual](Images/matrix-visual.png)](Images/matrix-visual.png)

---

# 12. Funnel Chart

A **Funnel Chart** represents values across sequential stages of a process.

The example shows the number of customers at different stages:

**Prospects → Leads → Interested Leads → Converted Leads**

### Suitable Data

Funnel charts are ideal for:
- Sales pipelines
- Recruitment stages
- Marketing conversions
- Customer journeys
- Application processes
- Lead conversion
- Order processing stages

### Recommended Fields

- **Category:** Stage
- **Values:** Count or Sum of records

### Useful Features

- Data labels
- Category labels
- Conversion rate labels
- Colors
- Tooltips

### Important Concept

The stages should normally represent a meaningful sequence, where the value can be compared from one stage to the next.

### Visualization

[![Funnel Chart](Images/funnel-chart.png)](Images/funnel-chart.png)

---

# 13. Pie Chart

A **Pie Chart** represents the contribution of categories to a whole.

### Suitable Data

Good for:
- Sales share by category
- Market share
- Customer distribution
- Revenue contribution
- Segment contribution

### Recommended Fields

- **Legend / Details:** Category
- **Values:** Sales, Profit, Quantity, or Count

### Best Used When

A pie chart is most readable when there are a relatively small number of categories and the goal is to understand **part-to-whole composition**.

### Visualization

[![Pie Chart](Images/pie-chart.png)](Images/pie-chart.png)

---

# 14. Donut Chart

A **Donut Chart** is similar to a pie chart but leaves a central area that can improve visual presentation.

### Suitable Data

Use it for:
- Category share
- Segment distribution
- Sales contribution
- Customer distribution
- Percentage breakdowns

### Recommended Fields

- **Legend:** Category
- **Values:** Numerical measure

### Power BI Features

- Detail labels
- Legend
- Data labels
- Tooltips
- Sorting

### Visualization

[![Donut Chart](Images/donut-chart.png)](Images/donut-chart.png)

---

# 15. Treemap

A **Treemap** displays hierarchical categories as nested rectangles, where rectangle size represents a numerical value.

### Suitable Data

Excellent for:
- Sales by Category and Sub-category
- Profit by Product Group
- Revenue by Department
- Market share
- Hierarchical business data

### Recommended Fields

- **Category:** Main grouping
- **Details:** Sub-category
- **Values:** Sales, Profit, Quantity, etc.

### Power BI Features

- Category labels
- Data labels
- Colors
- Hierarchy
- Tooltips

### Visualization

[![Treemap](Images/treemap.png)](Images/treemap.png)

---

# 16. Waterfall Chart

A **Waterfall Chart** shows how positive and negative changes contribute to a final total.

### Suitable Data

Useful for:
- Profit changes
- Revenue bridge analysis
- Budget vs actual
- Cost analysis
- Starting balance to ending balance
- Monthly financial changes

### Recommended Fields

- **Category:** Month, Department, Expense Type, etc.
- **Y-axis:** Numerical measure such as Profit or Revenue

### What It Shows

A waterfall can make it easier to understand:
- Starting value
- Increases
- Decreases
- Intermediate totals
- Final value

### Visualization

[![Waterfall Chart](Images/waterfall-chart.png)](Images/waterfall-chart.png)

---

# 📌 Choosing the Right Power BI Visual

| Requirement | Recommended Visual |
|---|---|
| Compare categories vertically | Clustered Column Chart |
| Compare categories horizontally | Clustered Bar Chart |
| Show trends over time | Line Chart |
| Show trend + magnitude | Area Chart |
| Show ranking changes | Ribbon Chart |
| Compare grouped values + another measure | Line & Clustered Column |
| Compare stacked groups + another measure | Line & Stacked Column |
| Analyze relationship between two numerical variables | Scatter Plot |
| Analyze geographic information | Map |
| Display detailed records | Table |
| Analyze hierarchical/cross-tab data | Matrix |
| Show sequential stages/conversion | Funnel Chart |
| Show part-to-whole composition | Pie Chart |
| Show part-to-whole with a different layout | Donut Chart |
| Show hierarchical proportions | Treemap |
| Show positive/negative contribution to a total | Waterfall Chart |

---

# 📂 Suggested Project Structure

```text
PowerBI-Data-Visualization/
│
├── README.md
│
├── Images/
│   ├── clustered-column-chart.png
│   ├── clustered-bar-chart.png
│   ├── line-chart.png
│   ├── area-chart.png
│   ├── ribbon-chart.png
│   ├── line-stacked-column-chart.png
│   ├── line-clustered-column-chart.png
│   ├── scatter-plot.png
│   ├── map-sales-by-city.png
│   ├── table-visual.png
│   ├── matrix-visual.png
│   ├── funnel-chart.png
│   ├── pie-chart.png
│   ├── donut-chart.png
│   ├── treemap.png
│   └── waterfall-chart.png
│
└── Dataset/
    └── dataset.csv
```

---

# 🧭 General Power BI Workflow

The common workflow for creating these visuals is:

1. Import the dataset into Power BI.
2. Check the data types of each column.
3. Assign correct data categories where required.
4. Select the required visual from the **Visualizations** pane.
5. Drag categorical fields into Axis, Rows, Columns, Legend, or Details.
6. Drag numerical fields into Values, X-axis, Y-axis, or other measure areas.
7. Format the visual using the **Format visual** pane.
8. Add data labels where they improve readability.
9. Configure titles, legends, axes, gridlines, and tooltips.
10. Apply filters or slicers when required.
11. Check the final visualization for readability and accuracy.

---

# 🎯 Data Selection Guide

## Categorical Columns

Examples:
- Category
- Sub-Category
- Region
- Segment
- Ship Mode
- City
- Country

These are generally useful for:
- Axis
- Legend
- Rows
- Columns
- Details
- Grouping

## Numerical Columns

Examples:
- Sales
- Profit
- Quantity
- Discount
- Customer Count

These are generally useful for:
- Values
- X-axis
- Y-axis
- Size
- Measures

## Date Columns

Examples:
- Order Date
- Ship Date

These are useful for:
- Year
- Quarter
- Month
- Day
- Time-series analysis
- Drill-down hierarchies

## Geographic Columns

Examples:
- Country
- State
- City
- Postal Code
- Latitude
- Longitude

These are useful for:
- Map visuals
- Geographic analysis
- Location-based reporting

---

# 🔍 Power BI Interactions

Power BI visuals can interact with each other through:

- Cross-filtering
- Cross-highlighting
- Tooltips
- Slicers
- Filters
- Drill-down
- Drill-through
- Sorting
- Zoom slider where supported

These features allow users to explore the report without creating a separate visual for every possible analysis.

---

# 📝 Notes

- Always select a visual according to the type of question the data needs to answer.
- Use numerical measures for quantitative analysis.
- Use categorical fields for grouping and comparison.
- Use date hierarchies when analyzing trends over time.
- Use geographic fields for location-based analysis.
- Avoid adding too many categories to a visual if it reduces readability.
- Use legends only when they provide useful grouping information.
- Use data labels when exact values are important.
- Format numbers consistently, such as K, M, currency, or percentages.
- Always verify the aggregation being used, such as **Sum, Average, Count, or Distinct Count**.

---

# 👨‍💻 Author

**Ganesh Ganga**

Power BI Data Visualization Project

---

# 📄 License

This project is created for **educational, learning, and portfolio purposes**.

The visualizations, documentation, and examples are intended to demonstrate Power BI data visualization concepts. Dataset ownership and third-party materials remain with their respective owners.

---

⭐ If this project is useful for learning Power BI, consider giving the repository a star!
