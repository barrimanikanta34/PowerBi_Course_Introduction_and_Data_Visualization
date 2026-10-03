# 📊 Power BI – Line & Clustered Column Chart

This section explains how to create, configure, format, and use a **Line and Clustered Column Chart** in Microsoft Power BI.

The example in this project uses:

- **Year** as the category on the X-axis
- **Sales** as the primary column value
- **Category** as the column series
- **Quantity** as the line value
- **Category** values such as Furniture, Office Supplies, and Technology
- A **secondary Y-axis** for Quantity because Sales and Quantity use different units/scales

---

## 🖼️ Chart Used in This Project

![Line and Clustered Column Chart](images\image09.png)

### What the chart shows

The chart combines two different visualizations in one:

- **Clustered columns** show Sales for each Category.
- **Line** shows Quantity.
- The columns use the **primary Y-axis**.
- The line uses the **secondary Y-axis**.
- Year is used as the X-axis.
- The legend identifies the different Category series and the Quantity line.

This type of visual is useful when you want to compare a value such as **Sales** with another measure such as **Quantity** across a common category or time period.

---

# 1. What Is a Line and Clustered Column Chart?

A **Line and Clustered Column Chart** combines:

1. A clustered column chart
2. A line chart

The two chart types share the same X-axis, but the line can use a separate secondary Y-axis.

### Example

| Year | Furniture Sales | Office Supplies Sales | Technology Sales | Quantity |
|---|---:|---:|---:|---:|
| 2014 | Sales value | Sales value | Sales value | Quantity |
| 2015 | Sales value | Sales value | Sales value | Quantity |
| 2016 | Sales value | Sales value | Sales value | Quantity |
| 2017 | Sales value | Sales value | Sales value | Quantity |
| 2018 | Sales value | Sales value | Sales value | Quantity |

The columns answer:

> **How much Sales were generated?**

The line answers:

> **How did Quantity change?**

---

# 2. When Should You Use This Chart?

Use this visual when you need to compare:

- A large numeric measure with another numeric measure
- Sales vs Quantity
- Revenue vs Orders
- Revenue vs Profit
- Cost vs Units Sold
- Production vs Defects
- Budget vs Actual
- Website Revenue vs Visitors
- Expenses vs Transactions

It is especially useful when the two measures have **different units or very different scales**.

### Example

If:

- Sales = ₹500,000
- Quantity = 10,000

Putting both on the same Y-axis may make the smaller measure difficult to understand.

A secondary Y-axis solves this problem.

---

# 3. Suitable Columns for This Chart

A Line and Clustered Column Chart normally requires:

### A. X-axis / Category Column

Use a **categorical or ordered column**.

Suitable examples:

- Year
- Quarter
- Month
- Date
- Product Category
- Region
- Country
- Department
- Customer Segment
- Ship Mode

For this example:

```text
X-axis → Year
```

---

### B. Column Values

Use one or more **numeric columns/measures**.

Suitable examples:

- Sales
- Revenue
- Cost
- Profit
- Quantity
- Orders
- Units Sold

For this example:

```text
Column Y-axis → Sales
```

---

### C. Column Series / Legend

Use a **categorical column** when you want multiple clustered columns.

Examples:

- Category
- Segment
- Region
- Product Type
- Department
- Ship Mode

For this example:

```text
Column series → Category
```

This creates separate columns for:

- Furniture
- Office Supplies
- Technology

---

### D. Line Values

Use a **numeric column or measure** for the line.

Examples:

- Quantity
- Profit
- Profit Margin
- Order Count
- Conversion Rate
- Average Sales

For this example:

```text
Line Y-axis → Quantity
```

---

# 4. Recommended Data Types

| Field | Recommended Data Type | Example |
|---|---|---|
| Year | Whole Number / Date | 2014, 2015 |
| Quarter | Text / Date hierarchy | Q1, Q2 |
| Month | Text / Date | January |
| Category | Text | Furniture |
| Sales | Decimal / Currency | 272K |
| Quantity | Whole Number | 12.4K |
| Profit | Decimal / Currency | 90K |
| Region | Text | East |
| Segment | Text | Consumer |

### Important

The X-axis should normally contain:

> **Categorical, chronological, or ordered data**

The Y-axis values should normally contain:

> **Numerical measures**

---

# 5. Step-by-Step: Create the Chart

## Step 1 – Load the Dataset

Open Power BI Desktop.

Go to:

```text
Home → Get Data
```

Select your data source.

For example:

```text
Excel
CSV
SQL Server
MySQL
Web
```

Load the dataset into Power BI.

---

## Step 2 – Select the Visual

In the **Visualizations** pane, select:

**Line and clustered column chart**

The visual icon looks like:

- Columns
- Combined with a line

---

## Step 3 – Add the X-axis

Drag:

```text
Year
```

into:

```text
X-axis
```

The chart will now group the values by year.

---

## Step 4 – Add Column Values

Drag:

```text
Sales
```

into:

```text
Y-axis / Column Y-axis
```

Power BI will display Sales as columns.

---

## Step 5 – Add Column Series

Drag:

```text
Category
```

into:

```text
Column series
```

This creates separate columns for each category.

Example:

```text
Furniture
Office Supplies
Technology
```

---

## Step 6 – Add the Line Measure

Drag:

```text
Quantity
```

into:

```text
Line Y-axis
```

Power BI will display Quantity as a line.

---

# 6. Understanding the Two Y-Axes

One of the most important features of this visual is the ability to use two Y-axes.

### Primary Y-axis

The primary Y-axis is used for the columns.

In this example:

```text
Sales
```

The left side of the chart represents Sales.

---

### Secondary Y-axis

The secondary Y-axis is used for the line.

In this example:

```text
Quantity
```

The right side of the chart represents Quantity.

This allows both measures to remain readable even when their numerical scales are very different.

---

# 7. Why Use a Secondary Y-axis?

Suppose:

```text
Sales = 272,000
Quantity = 12,400
```

If both values use one axis, the Quantity line could appear very small.

Using:

```text
Primary Y-axis → Sales
Secondary Y-axis → Quantity
```

allows each measure to have an appropriate scale.

### Important Best Practice

Do not use a secondary axis merely to make a chart look more dramatic.

Use it when:

- The units are different
- The scales are significantly different
- The comparison is meaningful

Always make the axis labels clear.

---

# 8. Legend

The **Legend** explains what each color or series represents.

In this example, the legend identifies:

```text
Furniture
Office Supplies
Technology
Quantity
```

### How to Format the Legend

Select the visual.

Go to:

```text
Format visual → Legend
```

You can adjust:

- Position
- Text size
- Font
- Title
- Spacing
- Marker size

### Common Legend Positions

```text
Top
Bottom
Left
Right
```

For dashboards, **Top** or **Bottom** is often easier to read when there are only a few categories.

---

# 9. Data Labels

Data labels display the numerical value directly on the visual.

For example:

```text
154K
146K
171K
12.4K
```

### Enable Data Labels

Go to:

```text
Format visual → Data labels
```

Turn:

```text
Data labels → On
```

Depending on the current Power BI version, column and line label settings may appear under separate formatting sections.

### Useful Settings

You can adjust:

- Text size
- Display units
- Decimal places
- Position
- Color
- Font
- Precision

---

# 10. Display Units

Large numbers can be difficult to read.

Instead of:

```text
272000
```

Power BI can display:

```text
272K
```

Similarly:

```text
1,500,000
```

can be displayed as:

```text
1.5M
```

Useful display units include:

```text
None
Thousands
Millions
Billions
Auto
```

For dashboards, **Auto**, **Thousands**, or **Millions** can improve readability.

---

# 11. Number Formatting

For Sales:

```text
₹272K
```

or:

```text
$272K
```

For Quantity:

```text
12.4K
```

The formatting should match the meaning of the measure.

### Examples

```text
Sales → Currency
Profit → Currency
Quantity → Whole Number
Profit Margin → Percentage
```

---

# 12. X-axis Formatting

The X-axis controls the categories or time periods.

Go to:

```text
Format visual → X-axis
```

You can modify:

- Title
- Title text
- Text size
- Font
- Label density
- Concatenation
- Scale type
- Start/end values where applicable

For this chart:

```text
X-axis → Year
```

---

# 13. Y-axis Formatting

Go to:

```text
Format visual → Y-axis
```

You can modify:

- Title
- Font size
- Text size
- Display units
- Decimal places
- Start
- End
- Gridlines
- Position

For example:

```text
Primary Y-axis → Sales
Secondary Y-axis → Quantity
```

Make sure users can easily understand which axis belongs to which measure.

---

# 14. Gridlines

Gridlines help users estimate values from the chart.

Go to:

```text
Format visual → Gridlines
```

You can change:

- On / Off
- Color
- Transparency
- Width
- Style

Avoid excessive gridlines because they can make the visual difficult to read.

---

# 15. Zoom Slider

The **Zoom slider** is useful when there are many categories or time periods.

Go to:

```text
Format visual → Zoom slider
```

Turn:

```text
Zoom slider → On
```

Users can then focus on a smaller portion of the X-axis.

### Example

If the chart contains:

```text
2010 → 2025
```

the user can zoom into:

```text
2018 → 2022
```

This is particularly useful for:

- Daily data
- Monthly data
- Long date ranges
- Many categories

---

# 16. Tooltips

Tooltips appear when the user hovers over a data point.

They can display:

```text
Year
Category
Sales
Quantity
Profit
```

Tooltips are useful because they provide additional information without overcrowding the chart.

You can also add additional fields to the **Tooltips** field well.

---

# 17. Drill Down

Power BI supports hierarchical analysis.

For a date field, you may have:

```text
Year
   ↓
Quarter
   ↓
Month
   ↓
Day
```

This allows users to move from a high-level summary to detailed information.

---

# 18. Year → Quarter → Month → Day

When using a date field such as:

```text
Order Date
```

Power BI can create a date hierarchy.

Example:

```text
Order Date
├── Year
├── Quarter
├── Month
└── Day
```

This hierarchy can be used on the X-axis.

---

# 19. Drill Down – Step by Step

Add:

```text
Order Date
```

to the X-axis.

Power BI may automatically create:

```text
Date Hierarchy
```

You can then use the drill controls at the top of the visual.

### Level 1

```text
Year
```

Example:

```text
2014
2015
2016
2017
2018
```

### Drill Down

Move from:

```text
Year
```

to:

```text
Quarter
```

You may see:

```text
Q1
Q2
Q3
Q4
```

Then continue to:

```text
Month
```

and:

```text
Day
```

---

# 20. Drill Up

**Drill Up** moves from a detailed level back to a higher level.

Example:

```text
Day
 ↓
Month
 ↓
Quarter
 ↓
Year
```

If you are currently viewing monthly data, Drill Up can return you to quarterly or yearly information.

---

# 21. Expand Next Level

Power BI also provides an option to expand a hierarchy to show the next level while keeping the current context.

For example:

```text
Year
```

can be expanded to show:

```text
2014
   Q1
   Q2
   Q3
   Q4

2015
   Q1
   Q2
   Q3
   Q4
```

This is different from simply replacing the current level with the next level.

---

# 22. Go to Next Level

The next-level option moves the visual from:

```text
Year
```

to:

```text
Quarter
```

Then:

```text
Quarter → Month
```

and:

```text
Month → Day
```

This is useful for progressively exploring a dataset.

---

# 23. Date Hierarchy vs Individual Date

Power BI can use either:

### Date Hierarchy

```text
Year
Quarter
Month
Day
```

or:

### Individual Date

```text
01-Jan-2014
02-Jan-2014
03-Jan-2014
...
```

Use a hierarchy when you want summarized time analysis.

Use individual dates when you need exact date-level analysis.

---

# 24. Sorting

You can sort the visual by:

- Year
- Sales
- Quantity
- Category

Use:

```text
More options (...) → Sort by
```

For time-series charts, normally keep:

```text
Year → Ascending
```

so that the trend reads naturally from older to newer periods.

---

# 25. Visual Filters

Filters allow you to restrict the information displayed by the chart.

Examples:

```text
Category = Technology
Region = East
Year = 2017
Segment = Consumer
```

You can apply filters at:

- Visual level
- Page level
- Report level

---

# 26. Slicers

A slicer provides an interactive filtering control.

Useful slicers include:

```text
Year
Category
Region
Segment
Ship Mode
```

For example:

```text
Year Slicer
2014
2015
2016
2017
2018
```

Selecting a year can update the chart dynamically.

---

# 27. Cross-Filtering and Interactions

Power BI visuals can interact with each other.

For example, selecting:

```text
Technology
```

in one visual can filter or highlight other visuals.

To configure this:

```text
Format → Edit interactions
```

You can choose:

- Filter
- Highlight
- None

---

# 28. Conditional Formatting

Conditional formatting can be used to emphasize important values.

Depending on the visual and Power BI version, formatting options can include:

- Data colors
- Gradient colors
- Rules
- Field-value-based colors

Example:

```text
High Sales → one color
Low Sales → another color
```

Use conditional formatting carefully so that the chart remains readable.

---

# 29. Titles

A meaningful title should explain what the chart represents.

Good example:

```text
Sales and Quantity by Year and Category
```

Avoid generic titles such as:

```text
Chart 1
Graph
Data
```

---

# 30. Subtitle

A subtitle can provide additional context.

Example:

```text
Sum of Sales and Quantity by Year and Category
```

This tells the viewer exactly what is being measured.

---

# 31. Columns vs Line

The visual is most effective when each visual type has a clear purpose.

### Columns

Use columns for:

- Comparing categories
- Comparing yearly totals
- Comparing sales
- Comparing revenue
- Comparing expenses

### Line

Use a line for:

- Trends
- Changes over time
- Quantity movement
- Profit movement
- Growth
- Performance patterns

---

# 32. Good Combinations

### Sales + Quantity

```text
Columns → Sales
Line → Quantity
```

### Revenue + Orders

```text
Columns → Revenue
Line → Order Count
```

### Revenue + Profit

```text
Columns → Revenue
Line → Profit
```

### Sales + Profit Margin

```text
Columns → Sales
Line → Profit Margin
```

For a percentage line such as Profit Margin, clearly label the secondary axis as a percentage.

---

# 33. Example DAX Measures

Instead of relying only on automatically summarized columns, you can create measures.

### Total Sales

```DAX
Total Sales =
SUM(Sheet1[Sales])
```

### Total Quantity

```DAX
Total Quantity =
SUM(Sheet1[Quantity])
```

### Total Profit

```DAX
Total Profit =
SUM(Sheet1[Profit])
```

### Profit Margin

```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)
```

Format Profit Margin as:

```text
Percentage
```

---

# 34. Example Configuration for This Chart

The visual can be configured approximately as follows:

```text
Visual:
Line and Clustered Column Chart

X-axis:
Year

Column Y-axis:
Sales

Column series:
Category

Line Y-axis:
Quantity
```

Result:

```text
             Sales Columns
                    +
                    |
                    |       Quantity Line
                    |            /\
                    |      /\   /  \
                    |     /  \_/    \
                    +----------------------
                         Year
```

---

# 35. Why Category Is Suitable for the Legend

`Category` is a categorical field.

Example:

```text
Furniture
Office Supplies
Technology
```

These are discrete groups, so they work well as clustered column series.

A numerical field such as:

```text
Sales
```

is generally not used as a category legend.

Instead, Sales is used as a measure.

---

# 36. Why Year Is Suitable for the X-axis

`Year` represents an ordered time dimension.

Example:

```text
2014 → 2015 → 2016 → 2017 → 2018
```

This makes it suitable for showing changes over time.

Other suitable ordered time fields include:

```text
Year
Quarter
Month
Date
```

---

# 37. Common Mistakes to Avoid

### ❌ Too many categories

Do not put dozens of categories into the clustered columns.

The chart can become difficult to read.

### ❌ Too many legend items

If the legend contains many categories, consider using:

- Slicers
- Filters
- Small multiples
- A bar chart

### ❌ Unrelated secondary axis

Do not add a second measure simply because Power BI supports it.

The two measures should have a meaningful analytical relationship.

### ❌ Missing axis titles

Always make it clear what each Y-axis represents.

### ❌ Excessive colors

Use a consistent color scheme.

### ❌ Too many labels

Too many data labels can create visual clutter.

---

# 38. Performance and Readability Tips

For a professional Power BI dashboard:

- Keep the title meaningful.
- Use readable fonts.
- Avoid unnecessary decimals.
- Use compact number formatting.
- Keep the legend simple.
- Use the secondary axis only when appropriate.
- Keep category names short where possible.
- Use tooltips for additional information.
- Use slicers for interactive filtering.
- Use drill-down for detailed time analysis.
- Use zoom slider when there are many X-axis values.
- Maintain consistent formatting across report pages.

---

# 39. Quick Reference

| Component | Recommended Field |
|---|---|
| Visual | Line and Clustered Column Chart |
| X-axis | Year |
| Column Y-axis | Sales |
| Column series | Category |
| Line Y-axis | Quantity |
| Primary Y-axis | Sales |
| Secondary Y-axis | Quantity |
| Legend | Category + Line measure |
| Data labels | Sales and Quantity |
| Zoom slider | Useful for many periods |
| Tooltip | Sales, Quantity, Profit |
| Drill hierarchy | Year → Quarter → Month → Day |
| Slicer | Year / Category / Region |
| Filter | Category / Region / Segment |

---

# 40. Final Summary

The **Line and Clustered Column Chart** is useful when you need to compare a categorical or time-based dimension with two different numerical measures.

In this example:

```text
Year
  ↓
Category
  ↓
Sales → Clustered Columns
Quantity → Line
```

The chart provides:

- Category comparison through columns
- Trend information through the line
- Primary and secondary Y-axes
- Legend-based category identification
- Data labels
- Tooltips
- Zoom slider
- Drill Up / Drill Down
- Year → Quarter → Month → Day analysis
- Filters and slicers
- Interactive visual relationships

This makes the visual suitable for **sales dashboards, business reports, financial analysis, operational dashboards, inventory analysis, and performance monitoring**.

---

## 📁 Project Structure

```text
PowerBI_Line_Clustered_Column_Chart/
│
├── README.md
│
└── Images/
    └── line-clustered-column-chart.png
```

---

## 🛠️ Tools Used

- Microsoft Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Interactive Visualizations
- Filters and Slicers
- Drill Down / Drill Up
- Data Hierarchies
- Line and Clustered Column Chart

---

## 👨‍💻 Learning Outcome

After completing this visualization, you should understand how to:

- Select appropriate categorical, date, and numerical columns
- Create a Line and Clustered Column Chart
- Compare two measures using primary and secondary axes
- Configure legends and data labels
- Format X-axis and Y-axis
- Use display units and number formatting
- Enable and use Zoom Slider
- Create Year → Quarter → Month → Day hierarchies
- Perform Drill Down and Drill Up
- Use filters and slicers
- Configure tooltips
- Apply sorting
- Create DAX measures
- Build interactive Power BI dashboards
