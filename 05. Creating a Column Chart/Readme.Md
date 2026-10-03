# Power BI Column Chart

## 📊 Overview

A **Column Chart** in Power BI is used to compare numerical values
across different categories. It is especially useful when you want to
clearly see which category has a higher or lower value.

In this project, a **Stacked Column Chart** is created using sales data
to compare **Sales by Segment**, while also showing the contribution of
each **Region**.

------------------------------------------------------------------------

## 🎯 When Should You Use a Column Chart?

A column chart is a good choice when:

-   You want to compare values across **different categories**.
-   The X-axis contains **categorical data**.
-   The Y-axis contains a **numeric measure** such as Sales, Profit,
    Quantity, or Revenue.
-   You want to identify the **highest and lowest performing
    categories**.
-   You need a simple visual for comparing groups.

### Common examples

  Category     Numeric Measure   Example
  ------------ ----------------- ---------------------------
  Product      Sales             Sales by Product
  Region       Profit            Profit by Region
  Department   Employees         Employees by Department
  Segment      Revenue           Revenue by Segment
  Category     Quantity          Quantity Sold by Category

------------------------------------------------------------------------

## 📁 What Kind of Dataset Is Required?

Column charts generally work best with datasets containing:

### 1. Categorical Column

This is the field used on the **X-axis**.

Examples:

-   Category
-   Segment
-   Region
-   Product Name
-   Department
-   Country
-   Customer Type

### 2. Numerical Column

This is the field used on the **Y-axis**.

Examples:

-   Sales
-   Profit
-   Revenue
-   Quantity
-   Cost
-   Salary

### 3. Optional Grouping Column

You can add another categorical column to the **Legend** to create a
**Stacked Column Chart** or **Clustered Column Chart**.

Examples:

-   Region
-   Product Category
-   Customer Type
-   Year
-   Department

------------------------------------------------------------------------

## 🗂️ Dataset Structure Example

A dataset could look like this:

  Segment     Region       Sales   Profit   Quantity
  ----------- --------- -------- -------- ----------
  Consumer    Central     250000    45000       1200
  Consumer    East        350000    62000       1500
  Consumer    South       200000    38000        900
  Consumer    West        360000    70000       1600
  Corporate   Central     160000    30000        700
  Corporate   East        200000    42000        850
  Corporate   South       120000    24000        500
  Corporate   West        230000    48000        950

This type of dataset is suitable because it contains:

-   **Segment** → Category
-   **Sales** → Numerical value
-   **Region** → Grouping/Legend

------------------------------------------------------------------------

# 🛠️ Creating a Column Chart in Power BI

## Step 1: Load the Dataset

Open **Power BI Desktop** and load your dataset.

You can import data from:

-   Excel
-   CSV
-   SQL Server
-   MySQL
-   PostgreSQL
-   Web
-   Other supported data sources

Go to:

**Home → Get Data**

Select your required data source and load the dataset.

------------------------------------------------------------------------

## Step 2: Select the Column Chart

In the **Visualizations** pane, select:

**Stacked Column Chart**

You can also choose:

-   Clustered Column Chart
-   100% Stacked Column Chart

Choose the chart type according to the analysis you want to perform.

------------------------------------------------------------------------

## Step 3: Add Fields

For this example:

### X-axis

Add:

`Segment`

This creates categories such as:

-   Consumer
-   Corporate
-   Home Office

### Y-axis

Add:

`Sales`

Power BI will automatically aggregate the values, normally as:

**Sum of Sales**

### Legend

Add:

`Region`

This divides each column into different regional sections.

The configuration is:

``` text
X-axis  → Segment
Y-axis  → Sales
Legend  → Region
```

------------------------------------------------------------------------

## 📸 Column Chart Created

![Power BI Column Chart](Images/column_chart.png)

**Figure:** Stacked Column Chart showing Sales by Segment and Region.

------------------------------------------------------------------------

# 🎨 Formatting the Column Chart

After creating the chart, select the visual and open the **Format
visual** pane.

You can customize several properties.

------------------------------------------------------------------------

## 1. Title

Go to:

**Format visual → General → Title**

You can change the title to something meaningful, for example:

**Sales by Segment and Region**

A good title should clearly explain what the chart represents.

------------------------------------------------------------------------

## 2. Data Labels

Go to:

**Format visual → Visual → Data labels**

Turn **Data labels ON**.

This displays the numerical value directly on each section of the
column.

Data labels are useful when the audience needs to see the actual values
instead of estimating them from the axis.

------------------------------------------------------------------------

## 3. X-axis

The X-axis contains the categories.

In this example:

``` text
Consumer
Corporate
Home Office
```

You can modify:

-   Text size
-   Font
-   Color
-   Title
-   Concatenation
-   Label density

------------------------------------------------------------------------

## 4. Y-axis

The Y-axis represents the numerical measure.

In this example:

``` text
Sum of Sales
```

You can change:

-   Display units
-   Decimal places
-   Text size
-   Title
-   Gridlines

For large sales values, display units such as **Thousands (K)** or
**Millions (M)** can make the chart easier to read.

------------------------------------------------------------------------

## 5. Legend

The legend identifies the different groups represented by the stacked
sections.

In this project:

``` text
Region
```

The regions include:

-   Central
-   East
-   South
-   West

The legend makes it possible to compare the contribution of each region
within every segment.

------------------------------------------------------------------------

## 6. Data Colors

You can customize the colors of the individual categories shown in the
chart.

For example, you can assign different colors to:

-   Central
-   East
-   South
-   West

Choose colors that provide good contrast and remain easy to read.

------------------------------------------------------------------------

## 7. Gridlines

Gridlines can help users estimate values from the Y-axis.

You can enable or disable them depending on the design of your report.

Avoid adding too many visual elements because they can make the
dashboard harder to understand.

------------------------------------------------------------------------

# 📊 Types of Column Charts in Power BI

## 1. Clustered Column Chart

Used to compare multiple values side by side.

Example:

``` text
Sales by Region
```

Useful when you want to compare categories directly.

------------------------------------------------------------------------

## 2. Stacked Column Chart

Used when you want to show both:

-   Total value
-   Contribution of subcategories

Example:

``` text
Sales by Segment
    + Region
```

This is the chart used in this project.

------------------------------------------------------------------------

## 3. 100% Stacked Column Chart

Used to compare the **percentage contribution** of each category.

Example:

``` text
Percentage of Sales by Region within each Segment
```

Every column has the same height of 100%.

------------------------------------------------------------------------

# 🔍 What Can We Analyze From This Chart?

A column chart can help answer questions such as:

-   Which segment has the highest sales?
-   Which segment has the lowest sales?
-   Which region contributes the most sales?
-   How do regions contribute to each segment?
-   Which categories need further investigation?
-   Are there significant differences between categories?

For the displayed example, the chart allows the viewer to compare total
sales across **Consumer, Corporate, and Home Office**, while the stacked
sections show how the regions contribute to those totals.

------------------------------------------------------------------------

# 💡 Best Practices

### ✅ Use a Column Chart When:

-   You are comparing categories.
-   Your X-axis contains categorical values.
-   Your Y-axis contains numerical values.
-   You have a manageable number of categories.
-   You want quick visual comparison.

### ❌ Avoid Using It When:

-   You have hundreds of categories.
-   The category names are extremely long.
-   You are mainly analyzing a continuous time trend.

For time-based trends such as monthly or yearly sales, a **Line Chart**
is often more appropriate.

------------------------------------------------------------------------

# 📌 Recommended Dataset Fields

A simple column-chart dataset can follow this structure:

``` text
Category → X-axis
Measure  → Y-axis
Group    → Legend (optional)
```

Example:

``` text
Segment → X-axis
Sales   → Y-axis
Region  → Legend
```

------------------------------------------------------------------------

# 🚀 Skills Demonstrated

This Power BI project demonstrates:

-   Data Import
-   Data Visualization
-   Column Charts
-   Stacked Column Charts
-   Aggregation
-   Data Comparison
-   Visual Formatting
-   Dashboard Design
-   Business Data Analysis

------------------------------------------------------------------------

## 📷 Column Chart Screenshot

![Column Chart Screenshot](https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/06.%20Creating%20a%20Pie%20%26%20Donut%20Chart/images/image07.png)

------------------------------------------------------------------------

## 👨‍💻 Column Chart Summary

This  demonstrates how to create and format a **Stacked Column
Chart in Microsoft Power BI** using sales data. The visualization
compares sales across different customer segments and shows the
contribution of individual regions.

It is a useful beginner-level Power BI project for understanding
**categorical comparison, aggregation, legends, data labels, and visual
formatting**.

------------------------------------------------------------------------

## ⭐ Conclusion

A column chart is one of the most useful Power BI visuals for comparing
categorical data. By combining a category, numerical measure, and
optional grouping field, you can create clear and meaningful business
visualizations.

**Example configuration:**

``` text
X-axis  → Segment
Y-axis  → Sum of Sales
Legend  → Region
```

This simple structure can be adapted to many real-world business
scenarios such as **sales analysis, profit analysis, employee analysis,
product performance, customer analysis, and regional performance**.
