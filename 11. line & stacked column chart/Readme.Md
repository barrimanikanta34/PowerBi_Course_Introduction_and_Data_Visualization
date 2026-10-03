# Power BI – Line and Stacked Column Chart

## 📊 Sales and Profit by Year and Segment

This Power BI project demonstrates a **Line and Stacked Column Chart** for comparing **Sales and Profit** across different years and customer segments.

The visual shown in this project combines two chart types:

- **Stacked Column Chart** → Sales
- **Line Chart** → Profit

This combination is useful when two related measures have different scales and need to be analyzed together.

---

# 🖼️ Visualization

<p align="center">
  <img src="images\image09.png"
       alt="Power BI Line and Stacked Column Chart - Sales and Profit by Year and Segment"
       width="1000">
</p>

---

# 1. 🎯 Objective

The objective of this visualization is to understand:

- How Sales change from year to year.
- How different customer Segments contribute to Sales.
- How Profit changes over the same period.
- The relationship between Sales and Profit.
- How Power BI date hierarchies can be used.
- How to navigate from Year → Quarter → Month → Day.
- How to use drill-down and drill-up.
- How to work with a secondary Y-axis.
- How to format a combination chart professionally.

---

# 2. 📌 Chart Type Used

The visual is a:

## Line and Stacked Column Chart

It combines:

```text
Stacked Columns → Sales
Line            → Profit
```

The columns are divided according to:

```text
Segment
```

The line represents:

```text
Profit
```

Therefore, the visual can show both:

```text
Sales composition
        +
Profit trend
```

in one chart.

---

# 3. 📋 Field Configuration

The configuration represented in the screenshot is approximately:

| Power BI Field | Used As |
|---|---|
| Order Date / Date Hierarchy | X-axis |
| Sales | Column Y-axis |
| Segment | Column Legend |
| Profit | Line Y-axis / Secondary Y-axis |

The screenshot displays:

```text
X-axis       → Year
Column value → Sum of Sales
Legend       → Segment
Line value   → Sum of Profit
```

The visual uses a **secondary Y-axis** for Profit because Sales and Profit have different numerical scales.

---

# 4. 🧩 Understanding the Visual

The columns show Sales:

```text
2014
████████████████
Consumer
████████
Corporate
████
Home Office
```

The line shows Profit:

```text
Profit
   ●
  / \
 ●   ●
       \
        ●
```

This makes it possible to compare:

```text
Sales → Column height
Profit → Line position
Segment → Column color
```

---

# 5. 📊 Why Use a Combination Chart?

A combination chart is useful when you want to compare two different measures at the same time.

For example:

```text
Sales  → Large values
Profit → Smaller values
```

If both are plotted on the same scale, Profit may become difficult to see.

Power BI therefore provides a:

```text
Secondary Y-axis
```

for the line measure.

---

# 6. 🗂️ What Type of Columns Are Suitable?

Choosing the correct data type is important.

## A. X-axis – Date/Time Column

A date field is highly suitable for this type of chart.

Examples:

```text
Order Date
Ship Date
Invoice Date
Transaction Date
```

For example:

```text
Order Date
2014-01-01
2014-01-02
2014-02-15
2015-03-10
...
```

Power BI can create a date hierarchy from a proper Date/DateTime column.

---

## B. Column Y-axis – Numerical Measure

The column portion should normally use a numerical measure.

Examples:

```text
Sales
Revenue
Quantity
Cost
Expenses
Production
```

In this project:

```text
Sales
```

is used.

Power BI aggregates it as:

```text
Sum of Sales
```

---

## C. Legend – Categorical Column

A categorical column is suitable for dividing the stacked columns into multiple series.

Examples:

```text
Segment
Category
Region
Product Category
Department
Customer Type
```

In this project:

```text
Segment
```

is used.

The segments are:

```text
Consumer
Corporate
Home Office
```

---

## D. Line – Numerical Measure

The line should normally represent another numerical measure.

Examples:

```text
Profit
Profit Margin
Average Sales
Cost
Growth %
Conversion Rate
```

In this project:

```text
Profit
```

is used.

---

# 7. ✅ Suitable Column Combination

A good general structure is:

```text
Date/Time Column
        ↓
      X-axis

Numerical Measure
        ↓
   Column Y-axis

Categorical Column
        ↓
     Legend

Second Numerical Measure
        ↓
    Line Y-axis
```

Example:

```text
Order Date
    ↓
X-axis

Sales
    ↓
Column Y-axis

Segment
    ↓
Legend

Profit
    ↓
Line Y-axis
```

---

# 8. ❌ Columns That Are Usually Not Suitable

Avoid using identifiers as the main numerical measure.

Examples:

```text
Customer ID
Order ID
Product ID
Row ID
```

These are identifiers rather than meaningful measures.

Similarly, avoid using very high-cardinality columns as a legend unless there is a specific analytical reason.

For example:

```text
Customer Name
Product Name
Order ID
```

may create too many series/categories and make the chart difficult to read.

---

# 9. 📅 Power BI Date Hierarchy

One of the most important concepts demonstrated by this visual is the **date hierarchy**.

A date hierarchy commonly follows:

```text
Year
  ↓
Quarter
  ↓
Month
  ↓
Day
```

For example:

```text
2014
 ├── Q1
 │    ├── January
 │    ├── February
 │    └── March
 │
 ├── Q2
 │
 ├── Q3
 │
 └── Q4
```

This hierarchy allows you to analyze the same measure at different levels of detail.

---

# 10. 🗓️ Year Level

At the Year level, the chart displays values such as:

```text
2014
2015
2016
2017
```

This is useful for:

- Year-over-year analysis
- Long-term trends
- Annual Sales comparison
- Annual Profit comparison

Example:

```text
2014 → Sales + Profit
2015 → Sales + Profit
2016 → Sales + Profit
2017 → Sales + Profit
```

---

# 11. 📆 Quarter Level

When you move down to Quarter:

```text
Year
 ↓
Quarter
```

the chart can display:

```text
2014 Q1
2014 Q2
2014 Q3
2014 Q4

2015 Q1
2015 Q2
...
```

Quarter-level analysis is useful for:

- Seasonal analysis
- Quarterly business performance
- Comparing Q1/Q2/Q3/Q4
- Identifying changes within a year

---

# 12. 📅 Month Level

The next level is:

```text
Year
 ↓
Quarter
 ↓
Month
```

Example:

```text
2014
 ├── Q1
 │    ├── January
 │    ├── February
 │    └── March
```

Month-level analysis provides more detail than yearly analysis.

It can reveal:

- Monthly Sales trends
- Monthly Profit trends
- Seasonal patterns
- Strong and weak months

---

# 13. 📆 Day Level

The most detailed level in the standard hierarchy is:

```text
Year
 ↓
Quarter
 ↓
Month
 ↓
Day
```

Example:

```text
2014
  Q1
   January
    1
    2
    3
    4
    ...
```

Day-level analysis is useful when:

- Daily transactions matter.
- You need operational monitoring.
- You want to investigate specific dates.
- The dataset contains sufficient daily records.

However, displaying thousands of days in one visual can create clutter.

---

# 14. 🔽 Drill Down

**Drill Down** means moving from a higher level of a hierarchy to a more detailed level.

Example:

```text
Year
 ↓
Quarter
 ↓
Month
 ↓
Day
```

Suppose the chart currently shows:

```text
2014
2015
2016
2017
```

You can drill down to:

```text
2014 Q1
2014 Q2
2014 Q3
2014 Q4
...
```

Then further to:

```text
January
February
March
...
```

and eventually:

```text
Individual dates
```

---

# 15. 🔼 Drill Up

**Drill Up** is the opposite of Drill Down.

If you are viewing:

```text
Day
```

you can move back to:

```text
Month
```

then:

```text
Quarter
```

then:

```text
Year
```

Conceptually:

```text
Day
 ↑
Month
 ↑
Quarter
 ↑
Year
```

Drill Up provides a way to return to a higher-level summary.

---

# 16. 🔽🔼 Drill Down vs Drill Up

| Operation | Direction | Example |
|---|---|---|
| Drill Down | More detail | Year → Quarter |
| Drill Down | More detail | Quarter → Month |
| Drill Down | More detail | Month → Day |
| Drill Up | Less detail | Day → Month |
| Drill Up | Less detail | Month → Quarter |
| Drill Up | Less detail | Quarter → Year |

---

# 17. 🧭 Power BI Drill Controls

When a hierarchy is used, Power BI can display drill controls in the visual header.

Typical controls include:

```text
Drill Up
Go to Next Level
Expand Next Level
Drill Mode
```

The exact icons and behavior can vary with the visual and Power BI version.

---

# 18. 🔽 Go to Next Level

The **Go to next level** functionality moves the visual to the next hierarchy level.

For example:

```text
Year
 ↓
Quarter
```

Instead of manually selecting each Year, the chart can display the next level of the hierarchy.

---

# 19. ⬇️ Expand Next Level

The expand functionality can show the next hierarchy level while retaining the current level of context.

For example:

```text
2014
 ├── Q1
 ├── Q2
 ├── Q3
 └── Q4
```

This is useful when you want to see both the parent and child context.

---

# 20. 🛠️ How to Create the Chart

## Step 1 – Load Data

Open:

```text
Power BI Desktop
```

Then:

```text
Home → Get Data
```

Load your dataset.

---

## Step 2 – Verify Data Types

Open:

```text
Data View
```

Check that:

```text
Order Date → Date/DateTime
Sales      → Decimal Number / Whole Number
Profit     → Decimal Number / Whole Number
Segment    → Text
```

Correct data types are important for Power BI to create meaningful visualizations and hierarchies.

---

## Step 3 – Select the Visual

From the Visualizations pane, select:

```text
Line and Stacked Column Chart
```

---

## Step 4 – Add Order Date

Drag:

```text
Order Date
```

to:

```text
X-axis
```

Power BI can provide a date hierarchy such as:

```text
Year
Quarter
Month
Day
```

---

## Step 5 – Add Sales

Drag:

```text
Sales
```

to the column value/Y-axis field.

Power BI will typically use:

```text
Sum of Sales
```

---

## Step 6 – Add Segment

Drag:

```text
Segment
```

to:

```text
Column series / Legend
```

This creates stacked Sales columns.

---

## Step 7 – Add Profit

Drag:

```text
Profit
```

to the line Y-axis/line values field.

The visual now contains:

```text
Sales → Columns
Profit → Line
Segment → Stacked series
```

---

# 21. 📐 Secondary Y-axis

The screenshot displays two Y-axes:

```text
Left Y-axis  → Sales
Right Y-axis → Profit
```

This is called a:

```text
Secondary Y-axis
```

It is useful when the two measures have different scales.

Example:

```text
Sales:
0M → 0.8M

Profit:
50K → 90K
```

Using separate scales makes both measures easier to interpret.

---

# 22. ⚠️ Be Careful With Secondary Axes

A secondary axis can improve readability, but it can also make relationships appear stronger or weaker depending on the scales.

Therefore:

- Clearly label both axes.
- Use understandable units.
- Do not hide important scale information.
- Explain what each axis represents.
- Avoid misleading visual comparisons.

---

# 23. 📊 Column Formatting

The column portion represents:

```text
Sales
```

Formatting options can include:

- Column colors
- Transparency
- Border
- Data labels
- Display units
- Decimal places
- Spacing
- Width
- Series formatting

---

# 24. 📈 Line Formatting

The line represents:

```text
Profit
```

Possible formatting options include:

- Line color
- Line width
- Markers
- Marker size
- Data labels
- Transparency
- Style

Markers make individual points easier to identify.

---

# 25. 🏷️ Data Labels

Data labels can display values directly on the chart.

For columns:

```text
Sales values
```

For the line:

```text
Profit values
```

Use data labels when exact values are important.

Avoid excessive labels when there are many dates or categories because the visual can become crowded.

---

# 26. 📚 Legend

The legend identifies the stacked column series.

In this project:

```text
Legend → Segment
```

The legend contains:

```text
Consumer
Corporate
Home Office
Profit
```

Depending on the Power BI visual and formatting behavior, the line series may also appear in the legend.

---

# 27. 🎨 Legend Formatting

The legend can generally be configured for:

- On/Off
- Position
- Font size
- Text color
- Orientation
- Title
- Spacing

Possible positions include:

```text
Top
Bottom
Left
Right
```

Keep the legend in a location that does not interfere with the chart.

---

# 28. 🎨 Colors

Use separate colors for the Segment categories.

For example:

```text
Consumer
Corporate
Home Office
```

Use consistent colors throughout the report.

If Consumer is blue in one chart, keeping Consumer blue in other visuals makes the report easier to understand.

---

# 29. 📏 X-axis

The X-axis represents the date hierarchy.

At different levels it may display:

```text
Year
Quarter
Month
Day
```

Formatting options may include:

- Title
- Font size
- Label color
- Label density
- Concatenation
- Axis type
- Zoom slider

---

# 30. 📐 Y-axis

The primary Y-axis represents:

```text
Sales
```

Possible settings include:

- Minimum
- Maximum
- Display units
- Decimal places
- Title
- Font size
- Gridlines

---

# 31. 📐 Secondary Y-axis

The secondary Y-axis represents:

```text
Profit
```

It is displayed separately from Sales.

This allows:

```text
Sales → Left scale
Profit → Right scale
```

The axis should have a clear title so the reader knows which measure is being represented.

---

# 32. 🔍 Zoom Slider

The screenshot shows a:

```text
Zoom slider
```

option in the Format visual pane.

A zoom slider can be useful when the X-axis contains many values.

For example:

```text
2014 ─────────────────────────── 2017
```

can be narrowed to:

```text
2015 ───────────── 2016
```

This allows users to focus on a smaller section of the data.

---

# 33. 📌 When Is Zoom Slider Useful?

Zoom slider is especially useful for:

- Daily data
- Monthly data across many years
- Large time-series datasets
- Dense categories
- Long date ranges

It is less important when the visual contains only:

```text
2014
2015
2016
2017
```

---

# 34. 🛠️ Format Visual Options

The Format visual pane provides controls for customizing the chart.

Common sections include:

```text
Style presets
X-axis
Y-axis
Secondary Y-axis
Legend
Small multiples
Gridlines
Zoom slider
Columns
Lines
```

The exact sections can vary depending on the selected visual and Power BI version.

---

# 35. 🧱 Columns Formatting

The **Columns** section can be used to customize the stacked column portion.

Common settings can include:

```text
Colors
Transparency
Border
Spacing
Data labels
Series
```

---

# 36. 📈 Lines Formatting

The **Lines** section can be used to customize the Profit line.

Possible settings include:

```text
Line color
Line width
Markers
Marker size
Data labels
```

---

# 37. 📏 Gridlines

Gridlines make it easier to estimate values.

For example:

```text
0.8M ─────────────
0.6M ─────────────
0.4M ─────────────
0.2M ─────────────
0.0M ─────────────
```

Use subtle gridlines so they do not overpower the data.

---

# 38. 🖱️ Tooltips

When the user hovers over a data point, Power BI can display additional information.

For example:

```text
Year: 2016
Segment: Consumer
Sales: ...
Profit: ...
```

Tooltips are useful because they provide detail without requiring many permanent labels.

---

# 39. 🔎 Focus Mode

Focus mode enlarges the selected visual.

It is useful when:

- The chart contains many details.
- You need to inspect values.
- The report page contains multiple visuals.

---

# 40. ⋯ More Options

The visual's **More options (...)** menu can provide features such as:

- Sorting
- Export data
- Show as table
- Spotlight
- Other visual-specific commands

Available commands can vary by visual, permissions, and Power BI version.

---

# 41. 🎚️ Slicers

You can add slicers to make the chart interactive.

Useful slicer fields include:

```text
Year
Region
Category
Segment
Ship Mode
```

Example:

```text
Year

☐ 2014
☑ 2015
☐ 2016
☐ 2017
```

The chart will update based on the selected filter.

---

# 42. 🧹 Filters

Power BI supports:

```text
Visual-level filters
Page-level filters
Report-level filters
```

### Visual-level

Only the selected chart is affected.

### Page-level

All visuals on the current page are affected.

### Report-level

The filter can affect the entire report.

---

# 43. 🖱️ Visual Interactions

Power BI visuals can interact with one another.

For example:

```text
Click Consumer
        ↓
Other visuals may be
filtered/highlighted
```

This enables interactive report exploration.

---

# 44. 📊 Small Multiples

Small multiples can divide a visual into separate panels based on a category.

For example:

```text
Segment
```

could create separate panels for:

```text
Consumer
Corporate
Home Office
```

This can be useful when comparing the same trend across groups.

---

# 45. 🧮 Aggregations

Power BI can aggregate numerical columns using:

```text
Sum
Average
Minimum
Maximum
Count
Distinct Count
```

For this project:

```text
Sales → Sum
Profit → Sum
```

This produces:

```text
Sum of Sales
Sum of Profit
```

---

# 46. 🧠 Measures

For a more controlled report, create explicit DAX measures.

Example:

```DAX
Total Sales =
SUM(Sheet1[Sales])
```

and:

```DAX
Total Profit =
SUM(Sheet1[Profit])
```

Then use:

```text
Total Sales → Column values
Total Profit → Line values
```

Measures are reusable across the report.

---

# 47. 📈 Profit Margin

Instead of only showing Profit, you can also calculate Profit Margin.

Example:

```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales]
)
```

This can help answer:

```text
How profitable are Sales?
```

A percentage measure can sometimes be more informative than the absolute Profit value.

---

# 48. 📊 Year-over-Year Analysis

A date hierarchy also makes year-based analysis possible.

You can compare:

```text
2014
2015
2016
2017
```

For more advanced analysis, DAX time-intelligence functions can be used to calculate:

- Previous year
- Year-over-year growth
- Year-over-year percentage
- Running total

---

# 49. 📅 When to Use Year, Quarter, Month, and Day

| Level | Best For |
|---|---|
| Year | Long-term trends |
| Quarter | Seasonal/business performance |
| Month | Detailed trend analysis |
| Day | Operational/daily analysis |

---

# 50. ⚠️ Avoid Too Much Detail

A common mistake is displaying:

```text
Year → Quarter → Month → Day
```

all at once for a large dataset.

This can create:

- Too many labels
- Overlapping text
- Difficult navigation
- Poor readability

Use drill-down to reveal detail only when needed.

---

# 51. 📌 Date Column Requirements

For a proper date hierarchy, the date column should contain valid date values.

Good:

```text
2017-01-15
2017-02-21
2017-03-10
```

Not ideal:

```text
January
February
March
```

stored only as text when date intelligence is required.

---

# 52. 🗃️ Recommended Data Model

For larger Power BI projects, a dedicated Date table is recommended.

A typical Date table can contain:

```text
Date
Year
Quarter
Month
Month Number
Week
Day
```

Example:

```text
Date       Year   Quarter   Month
2017-01-01 2017   Q1        January
2017-01-02 2017   Q1        January
...
```

This provides better control over time-based analysis.

---

# 53. 🧭 Date Sorting

Month names should usually be sorted chronologically.

Incorrect alphabetical order:

```text
April
August
December
February
January
...
```

Correct order:

```text
January
February
March
April
...
December
```

Use a Month Number column to sort Month Name when necessary.

---

# 54. 🔄 Recommended Analysis Workflow

```text
Year
 ↓
Identify overall trend
 ↓
Drill Down
 ↓
Quarter
 ↓
Identify seasonal pattern
 ↓
Drill Down
 ↓
Month
 ↓
Investigate detailed trend
 ↓
Drill Down
 ↓
Day
 ↓
Investigate individual dates
```

Then:

```text
Drill Up
 ↓
Month
 ↓
Quarter
 ↓
Year
```

---

# 55. 🆚 Line and Stacked Column vs Other Charts

| Chart | Main Purpose |
|---|---|
| Line and Stacked Column | Compare a stacked measure with another measure/trend |
| Clustered Column | Compare categories side-by-side |
| Stacked Column | Compare composition |
| Line Chart | Show trends |
| Area Chart | Show trends with magnitude |
| Stacked Area | Show composition over an ordered axis |
| Bar Chart | Compare categories horizontally |

---

# 56. ❌ When Not to Use This Combination Chart

Avoid this chart when:

- There is only one measure.
- Both measures have almost identical purposes and scales.
- There are too many categories.
- The secondary axis may confuse users.
- The X-axis has too many unrelated categories.
- Exact values are more important than trends.
- The visual becomes overcrowded.

---

# 57. 🎯 Best Practices

### Data

- Use a valid Date/DateTime column for time analysis.
- Use numerical measures for Sales and Profit.
- Use a categorical column for the stacked series.
- Check aggregation settings.

### Chart

- Use a clear title.
- Clearly label both Y-axes.
- Keep the legend visible.
- Use meaningful colors.
- Use data labels selectively.
- Use tooltips for additional information.
- Use drill-down for detailed analysis.
- Use zoom slider for dense date ranges.

### Report

- Keep colors consistent.
- Use slicers where useful.
- Avoid excessive visual elements.
- Maintain readable fonts.
- Keep the report layout clean.

---

# 58. 🚀 Complete Power BI Workflow

```text
Load Dataset
      ↓
Check Data Types
      ↓
Create/Verify Date Column
      ↓
Create Date Hierarchy
      ↓
Select Line and Stacked Column Chart
      ↓
Add Order Date → X-axis
      ↓
Add Sales → Column Y-axis
      ↓
Add Segment → Legend
      ↓
Add Profit → Line Y-axis
      ↓
Configure Secondary Y-axis
      ↓
Configure Year/Quarter/Month/Day
      ↓
Test Drill Down
      ↓
Test Drill Up
      ↓
Format Columns
      ↓
Format Lines
      ↓
Format Legend
      ↓
Format Axes
      ↓
Configure Data Labels
      ↓
Configure Gridlines
      ↓
Configure Zoom Slider
      ↓
Configure Tooltips
      ↓
Add Slicers if Required
      ↓
Test Visual Interactions
      ↓
Review and Publish
```

---

# 59. 🧠 Key Concepts Learned

This visualization demonstrates:

- Line and Stacked Column Chart
- Stacked columns
- Line series
- X-axis
- Primary Y-axis
- Secondary Y-axis
- Legend
- Numerical measures
- Categorical columns
- Date columns
- Date hierarchy
- Year
- Quarter
- Month
- Day
- Drill Down
- Drill Up
- Go to Next Level
- Expand Next Level
- Zoom Slider
- Data Labels
- Tooltips
- Gridlines
- Sorting
- Slicers
- Filters
- Visual Interactions
- Small Multiples
- DAX Measures
- Profit Margin
- Time-series analysis

---

# 60. 📌 Quick Reference

```text
Visual:
Line and Stacked Column Chart

X-axis:
Order Date / Date Hierarchy

Column Y-axis:
Sales

Column Legend:
Segment

Line Y-axis:
Profit

Primary Axis:
Sales

Secondary Axis:
Profit

Hierarchy:
Year
 ↓
Quarter
 ↓
Month
 ↓
Day
```

---

# 61. 🎓 Learning Outcome

After completing this visualization, you should be able to:

1. Select appropriate fields for a combination chart.
2. Distinguish categorical, numerical, and date columns.
3. Create a Line and Stacked Column Chart.
4. Compare Sales and Profit.
5. Use a secondary Y-axis.
6. Add a categorical legend.
7. Create and use date hierarchies.
8. Analyze Year-level data.
9. Analyze Quarter-level data.
10. Analyze Month-level data.
11. Analyze Day-level data.
12. Perform Drill Down.
13. Perform Drill Up.
14. Use Go to Next Level.
15. Understand Expand Next Level.
16. Configure data labels.
17. Configure tooltips.
18. Use a zoom slider when appropriate.
19. Format columns and lines.
20. Use slicers and filters.
21. Create DAX measures.
22. Calculate Profit Margin.
23. Perform time-based analysis.
24. Design a professional Power BI report.

---

# 62. 🏁 Conclusion

The **Line and Stacked Column Chart** is a powerful Power BI visual when two related measures need to be analyzed together.

In this project:

```text
Sales
 ↓
Stacked Columns

Segment
 ↓
Column Categories

Profit
 ↓
Line

Order Date
 ↓
Year → Quarter → Month → Day
```

The combination allows users to understand both **Sales composition** and **Profit trends** in the same visual.

The drill hierarchy provides a structured way to move from:

```text
Year
 ↓
Quarter
 ↓
Month
 ↓
Day
```

and Drill Up provides the reverse path.

For professional reports, combine this visual with:

```text
Slicers
Filters
Tooltips
Data Labels
Secondary Y-axis
Zoom Slider
Consistent Colors
DAX Measures
```

to create an interactive and informative Power BI report.

---

# 🔗 Useful Microsoft Power BI References

- [Power BI visualization types](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a)
- [Customize Power BI visualizations](https://learn.microsoft.com/en-us/power-bi/create-reports/service-custom-visuals-format)
- [Drill down and drill up in Power BI](https://learn.microsoft.com/en-us/power-bi/consumer/end-user-drill)
- [Power BI date hierarchies](https://learn.microsoft.com/en-us/power-bi/transform-model/desktop-date-tables)
- [Power BI slicers](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers)
- [Power BI filters](https://learn.microsoft.com/en-us/power-bi/create-reports/power-bi-report-add-filter)
- [DAX](https://learn.microsoft.com/en-us/dax/)

---

## 👨‍💻 Project Information

**Project Type:** Power BI Data Visualization Practice

**Visualization:** Line and Stacked Column Chart

**Analysis:** Sales and Profit by Year and Segment

**Main Fields:**

```text
Order Date → X-axis / Date Hierarchy
Sales      → Column values
Segment    → Legend
Profit     → Line values
```

### Repository Structure

```text
PowerBI_Line_and_Stacked_Column_Chart/
│
├── README.md
│
└── Images/
    └── sales-profit-year-segment.png
```
