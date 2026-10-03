# Power BI – Line Chart & Area Chart

## 📊 Project Overview

This Power BI practice project demonstrates two important visualization types:

1. **Line Chart**
2. **Area Chart**

Both visuals are useful for analyzing values across an ordered category or sequence. In this project, the charts analyze **Profit** and **Quantity by Ship Mode**.

The project demonstrates how to:

- Select suitable fields for Line and Area Charts
- Understand categorical and numerical data
- Configure the X-axis and Y-axis
- Create a Line Chart
- Create an Area Chart
- Add and format data labels
- Change font size
- Format chart titles
- Configure axes
- Format colors
- Configure tooltips
- Sort categories
- Format display units
- Use markers
- Configure gridlines
- Understand interactions
- Decide when to use Line vs Area Charts
- Build readable Power BI reports

---

# 📁 Dataset Used

The dataset contains sales and order-related fields such as:

| Column | Type | Example / Purpose |
|---|---|---|
| Category | Categorical | Product category |
| City | Categorical | Customer city |
| Country | Categorical | Customer country |
| Customer ID | Identifier | Unique customer |
| Customer Name | Categorical | Customer name |
| Discount | Numerical | Discount value |
| Order Date | Date | Order date |
| Order ID | Identifier | Unique order |
| Postal Code | Numerical / Categorical | Postal code |
| Product ID | Identifier | Product identifier |
| Product Name | Categorical | Product name |
| Profit | Numerical | Profit amount |
| Quantity | Numerical | Quantity sold |
| Region | Categorical | Geographic region |
| Sales | Numerical | Sales amount |
| Segment | Categorical | Customer segment |
| Ship Date | Date | Shipping date |
| Ship Mode | Categorical | Shipping method |
| State | Categorical | State |
| Sub-Category | Categorical | Product sub-category |

---

# 1. 📈 Line Chart

## What is a Line Chart?

A **Line Chart** displays values as points connected by a line.

It is especially useful when the X-axis represents an ordered sequence, such as:

- Date
- Month
- Quarter
- Year
- Ranking/order
- Ordered categories

A line chart helps users see:

- Increase
- Decrease
- Patterns
- Changes between points
- Overall movement
- Peaks and drops

---

## 🖼️ Line Chart Used in This Project

<p align="center">
  <img src="https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/08.%20Line_%26_Area_Chart/images/image02.png"
       alt="Power BI Line Chart - Profit by Ship Mode"
       width="900">
</p>

### Chart configuration

The screenshot shows:

```text
Chart Type → Line Chart
Title      → Profit by Shipmode
Category   → Ship Mode
Values     → Profit
```

The Ship Mode categories shown are:

```text
Standard Class
Second Class
First Class
Same Day
```

The approximate profit values shown are:

```text
Standard Class → 164K
Second Class   → 57K
First Class    → 49K
Same Day       → 16K
```

---

# 2. 🧩 What Data Is Suitable for a Line Chart?

A Line Chart generally requires:

### A. Ordered/Categorical or Date Field

This field determines the X-axis.

Examples:

```text
Order Date
Ship Date
Year
Month
Quarter
Ship Mode
```

### B. Numerical Field / Measure

This determines the Y-axis.

Examples:

```text
Profit
Sales
Quantity
Discount
```

### Example from this project

```text
X-axis → Ship Mode
Y-axis → Profit
```

This allows the report to compare profit across the selected Ship Mode categories.

---

# 3. ⚠️ Important Point About Line Charts

Line Charts are most naturally suited to **ordered data**, especially time-series data.

For example:

```text
Jan → Feb → Mar → Apr → May
```

or:

```text
2022 → 2023 → 2024 → 2025 → 2026
```

When using a field such as `Ship Mode`, the categories are categorical rather than naturally continuous.

Therefore, this particular chart should be understood as an **ordered categorical comparison**, based on the category order shown in the report.

For pure category-to-category comparison without meaningful ordering, a **bar or column chart** may be more appropriate.

---

# 4. 🛠️ How to Create the Line Chart

## Step 1 – Load the Dataset

1. Open **Power BI Desktop**.
2. Select **Home → Get Data**.
3. Select the required source.
4. Load the dataset.
5. Check the data types.

---

## Step 2 – Select the Line Chart

1. Open **Report View**.
2. Open the **Visualizations** pane.
3. Select the **Line Chart** visual.

A blank Line Chart will appear.

---

## Step 3 – Add Ship Mode

Drag:

```text
Ship Mode → X-axis
```

This creates categories such as:

```text
Standard Class
Second Class
First Class
Same Day
```

---

## Step 4 – Add Profit

Drag:

```text
Profit → Y-axis / Values
```

Power BI will normally aggregate the field as:

```text
Sum of Profit
```

---

# 5. 📈 Understanding the Line

The line connects the profit value for each Ship Mode.

For example:

```text
Standard Class → 164K
        ↓
Second Class   → 57K
        ↓
First Class    → 49K
        ↓
Same Day       → 16K
```

The line visually shows the movement between the values.

The chart should not be interpreted as a time trend because Ship Mode is not a time variable.

---

# 6. 🍃 Area Chart

## What is an Area Chart?

An **Area Chart** is similar to a Line Chart, but the area below the line is filled.

The filled area emphasizes the magnitude of the values.

Area Charts are useful for:

- Showing trends
- Showing magnitude
- Showing changes over an ordered axis
- Time-series analysis
- Comparing cumulative-looking visual patterns

---

# 7. 🖼️ Area Chart Used in This Project

<p align="center">
  <img src="https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/08.%20Line_%26_Area_Chart/images/image03.png"
       alt="Power BI Area Chart - Quantity by Ship Mode"
       width="900">
</p>

### Chart configuration

The screenshot shows:

```text
Chart Type → Area Chart
Title      → Quantity by Ship Mode
Category   → Ship Mode
Values     → Quantity
```

The categories are:

```text
Standard Class
Second Class
First Class
Same Day
```

The approximate values shown are:

```text
Standard Class → 22.8K
Second Class   → 7.4K
First Class    → 5.7K
Same Day       → 2.0K
```

---

# 8. 🧩 What Data Is Suitable for an Area Chart?

An Area Chart generally requires:

### A. Ordered / Date / Categorical Field

Examples:

```text
Order Date
Ship Date
Year
Month
Quarter
Ship Mode
```

### B. Numerical Field / Measure

Examples:

```text
Quantity
Sales
Profit
Revenue
```

### Example from this project

```text
X-axis → Ship Mode
Y-axis → Quantity
```

---

# 9. 🛠️ How to Create the Area Chart

## Step 1

Select the **Area Chart** visual from the Visualizations pane.

## Step 2

Add:

```text
Ship Mode → X-axis
```

## Step 3

Add:

```text
Quantity → Y-axis / Values
```

Power BI aggregates Quantity, normally as:

```text
Sum of Quantity
```

## Step 4

Format the visual according to the report requirements.

---

# 10. 📊 Line Chart vs Area Chart

| Feature | Line Chart | Area Chart |
|---|---|---|
| Shows values | ✅ | ✅ |
| Shows direction/change | ✅ | ✅ |
| Filled area | ❌ | ✅ |
| Trend analysis | ✅ | ✅ |
| Magnitude emphasis | Moderate | Strong |
| Time-series analysis | Excellent | Excellent |
| Multiple series | ✅ | ✅ |
| Data labels | ✅ | ✅ |
| Tooltips | ✅ | ✅ |
| Gridlines | ✅ | ✅ |
| Markers | ✅ | Available depending on formatting |
| Best for | Trend/change | Trend + magnitude |

---

# 11. 🎨 Formatting the Line and Area Charts

Select the visual and open:

```text
Format visual
```

The exact formatting card names can vary slightly between Power BI Desktop versions.

---

# 12. 📝 Chart Title

A title should clearly describe the analysis.

Examples from this project:

```text
Profit by Shipmode
```

and:

```text
Quantity by Ship Mode
```

A cleaner business-style title can also be:

```text
Profit by Ship Mode
```

### Steps

1. Select the visual.
2. Open **Format visual**.
3. Open the title formatting section.
4. Turn the title **On**.
5. Enter the title.
6. Adjust:
   - Font
   - Font size
   - Alignment
   - Text color
   - Background if required

---

# 13. 🏷️ Data Labels

Data labels display values directly on the chart.

Examples from the screenshots:

### Line Chart

```text
164K
57K
49K
16K
```

### Area Chart

```text
22.8K
7.4K
5.7K
2.0K
```

### Steps

1. Select the visual.
2. Open **Format visual**.
3. Find the data-label/detail-label formatting section.
4. Turn labels **On**.
5. Configure:
   - Font size
   - Position
   - Display units
   - Decimal places
   - Color

---

# 14. 🔢 Display Units

Large numbers can be displayed using compact units.

Examples:

```text
164,000 → 164K
22,800  → 22.8K
7,400   → 7.4K
```

Common display units include:

```text
None
Thousands
Millions
Billions
```

For the charts in this project, thousands are useful because the values are in the K range.

---

# 15. 🔤 Font Size

Font sizes can be adjusted for:

- Title
- X-axis labels
- Y-axis labels
- Data labels
- Legend
- Tooltip text where applicable

Use a readable font size and maintain consistency across report visuals.

---

# 16. 📐 X-Axis Formatting

The X-axis contains:

```text
Ship Mode
```

Possible formatting options include:

- Title
- Font
- Font size
- Text color
- Label density
- Concatenation
- Scale/category settings where available

For a date-based Line Chart, the X-axis can instead represent:

```text
Year
Quarter
Month
Date
```

---

# 17. 📏 Y-Axis Formatting

The Y-axis contains the numerical measure.

### Line Chart

```text
Y-axis → Profit
```

### Area Chart

```text
Y-axis → Quantity
```

Useful formatting options include:

- Axis title
- Font size
- Display units
- Decimal places
- Start value
- End value
- Gridlines

---

# 18. 📚 Legend

A legend is useful when multiple series are displayed.

For a single-series chart such as these screenshots, a legend may not be necessary.

For example, if you add:

```text
Sales
Profit
```

as separate series, a legend can identify them.

### Best practice

Do not keep an unnecessary legend when there is only one series and the visual is already clear.

---

# 19. 🎨 Line Color

To change the line color:

1. Select the Line Chart.
2. Open **Format visual**.
3. Find the series/color formatting section.
4. Select the series.
5. Choose the required color.

For the Area Chart, the same type of series/color formatting controls can be used to change the line and filled area appearance.

---

# 20. 🌊 Area Fill

The key visual difference between a Line Chart and Area Chart is the filled region below the line.

The Area Chart in this project visually emphasizes the quantity magnitude.

When formatting an Area Chart, consider:

- Fill transparency
- Line color
- Border/line visibility
- Data labels
- Gridlines

Avoid excessive opacity if labels or gridlines become difficult to read.

---

# 21. 📏 Gridlines

Gridlines help users estimate values against the Y-axis.

They can be:

```text
Enabled
Disabled
```

Use subtle gridlines so they help interpretation without dominating the visual.

---

# 22. 🖱️ Tooltips

Tooltips provide additional information when the user hovers over a data point.

For example:

```text
Ship Mode: Standard Class
Profit: 164K
```

For the Area Chart:

```text
Ship Mode: Standard Class
Quantity: 22.8K
```

Tooltips help provide details without adding excessive text to the chart.

---

# 23. 🔄 Sorting

You can sort the visual using the chart's options menu.

For example:

```text
Sort by → Profit
```

or:

```text
Sort by → Quantity
```

and then:

```text
Ascending
```

or:

```text
Descending
```

### Important

For time-series Line or Area Charts, maintain chronological order:

```text
Jan → Feb → Mar → Apr
```

Do not sort months alphabetically if the goal is to show a time trend.

---

# 24. 🖱️ Interactive Filtering

Power BI visuals support interactive behavior.

Selecting a data point can affect other visuals on the same report page.

For example:

```text
Select Standard Class
        ↓
Other visuals respond
        ↓
Related records are filtered/highlighted
```

This makes the report interactive.

---

# 25. 🔎 Drill-Down

Line and Area Charts can be configured with hierarchical fields.

For example:

```text
Order Date
    ↓
Year
    ↓
Quarter
    ↓
Month
    ↓
Day
```

Users can move from a high-level trend to more detailed information.

This is particularly useful for time-series analysis.

---

# 26. 📅 Best Use Case: Time-Series Data

Line and Area Charts are especially useful for time-based data.

Example:

```text
Order Date → X-axis
Sales      → Y-axis
```

The result can show:

```text
Sales
  ↑
  │       ╭───╮
  │   ╭───╯   ╰──╮
  │───╯           ╰──
  └────────────────────→ Time
     Jan Feb Mar Apr
```

This allows users to identify:

- Trends
- Peaks
- Drops
- Seasonal patterns
- Growth
- Decline

---

# 27. ⚠️ Important Consideration for These Screenshots

The screenshots use:

```text
Ship Mode
```

as the X-axis.

`Ship Mode` contains categories rather than dates:

```text
Standard Class
Second Class
First Class
Same Day
```

Therefore, these particular visuals should be treated as **ordered categorical comparisons**.

For a genuine trend analysis, a better configuration would usually be something like:

```text
Order Date → X-axis
Profit     → Y-axis
```

or:

```text
Order Date → X-axis
Quantity   → Y-axis
```

This would allow the Line or Area Chart to represent change over time.

---

# 28. 🧮 Aggregation

Power BI aggregates numerical fields placed in the Values/Y-axis area.

Examples:

```text
Profit   → Sum of Profit
Quantity → Sum of Quantity
Sales    → Sum of Sales
```

Other possible aggregations include:

```text
Sum
Average
Minimum
Maximum
Count
Distinct Count
```

Always verify the aggregation because changing it changes the meaning of the chart.

---

# 29. 📊 Exact Field Configuration in This Project

## Line Chart

```text
Visual:
Line Chart

X-axis:
Ship Mode

Y-axis / Values:
Profit

Aggregation:
Sum of Profit
```

## Area Chart

```text
Visual:
Area Chart

X-axis:
Ship Mode

Y-axis / Values:
Quantity

Aggregation:
Sum of Quantity
```

---

# 30. 📋 Approximate Values Shown in the Screenshots

## Profit by Ship Mode

| Ship Mode | Approx. Profit |
|---|---:|
| Standard Class | 164K |
| Second Class | 57K |
| First Class | 49K |
| Same Day | 16K |

## Quantity by Ship Mode

| Ship Mode | Approx. Quantity |
|---|---:|
| Standard Class | 22.8K |
| Second Class | 7.4K |
| First Class | 5.7K |
| Same Day | 2.0K |

These values are read from the displayed labels in the screenshots and are rounded using Power BI display units.

---

# 31. ❌ When NOT to Use a Line Chart

Avoid a Line Chart when:

- Categories have no meaningful order.
- There are many unrelated categories.
- Exact category comparison is the main goal.
- The visual becomes difficult to interpret.

For simple category comparison, consider:

```text
Bar Chart
Clustered Column Chart
```

---

# 32. ❌ When NOT to Use an Area Chart

Avoid an Area Chart when:

- The filled region creates visual clutter.
- Many series overlap.
- Exact values are more important than magnitude.
- Categories do not have a meaningful order.
- The visual contains too many categories.

A Line Chart can often be clearer when multiple trends need to be compared.

---

# 33. 🆚 Line vs Area: Practical Selection

## Choose Line Chart when:

- Trend direction is the main focus.
- You want a clean view of changes.
- Exact points are important.
- You have multiple series to compare.

## Choose Area Chart when:

- You want to emphasize magnitude.
- The filled region helps communicate the scale.
- You are showing a trend over time.
- The number of series is small.

---

# 34. 🎯 Best Practices

### Data

- Use a meaningful ordered field on the X-axis.
- Use a numerical measure on the Y-axis.
- Use date fields for genuine time-series analysis.
- Check the aggregation.

### Design

- Use clear titles.
- Keep fonts readable.
- Use appropriate display units.
- Avoid unnecessary legends.
- Keep colors consistent.
- Use gridlines carefully.
- Avoid too many data labels.

### Time-Series

For dates:

```text
Year → Quarter → Month → Day
```

Maintain chronological ordering.

### Area Charts

Avoid using too many overlapping filled series because transparency and colors can make the visual difficult to read.

---

# 35. 🚀 Recommended Power BI Workflow

```text
Load Dataset
      ↓
Check Data Types
      ↓
Clean / Transform Data
      ↓
Select Line or Area Chart
      ↓
Choose Ordered / Date Field
      ↓
Add Numerical Measure
      ↓
Check Aggregation
      ↓
Format Title
      ↓
Format X-axis
      ↓
Format Y-axis
      ↓
Format Data Labels
      ↓
Set Display Units
      ↓
Format Colors
      ↓
Configure Gridlines
      ↓
Configure Tooltips
      ↓
Check Sorting
      ↓
Test Interactions
      ↓
Review Dashboard
```

---

# 36. 🧠 Key Concepts Learned

This project demonstrates:

- Power BI data loading
- Categorical data
- Numerical data
- Measures
- Aggregations
- Line Charts
- Area Charts
- X-axis
- Y-axis
- Data labels
- Display units
- Font formatting
- Color formatting
- Gridlines
- Tooltips
- Sorting
- Cross-filtering
- Cross-highlighting
- Drill-down
- Time-series visualization
- Dashboard design

---

# 37. 🎯 Conclusion

Line Charts and Area Charts are useful for showing how a numerical measure changes across an ordered dimension.

In this project:

```text
Line Chart
Ship Mode → Profit

Area Chart
Ship Mode → Quantity
```

The Line Chart focuses on the movement of **Profit**, while the Area Chart emphasizes the magnitude of **Quantity**.

However, because `Ship Mode` is a categorical field rather than a time variable, these specific examples should be considered categorical/ordered comparisons. For genuine trend analysis, use an ordered date or time field such as `Order Date`.

The core visualization workflow is:

```text
Choose the correct data
        ↓
Choose Line or Area Chart
        ↓
Configure X-axis
        ↓
Configure Y-axis
        ↓
Check aggregation
        ↓
Format title
        ↓
Format axes
        ↓
Format labels
        ↓
Configure colors
        ↓
Add tooltips
        ↓
Check sorting
        ↓
Test interactions
        ↓
Build a clear dashboard
```

---

# 🔗 Official Microsoft Learn References

- [Power BI visualization types](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a)
- [Customize visualization titles, backgrounds, and legends](https://learn.microsoft.com/en-us/power-bi/create-reports/service-custom-visuals-format)
- [Power BI visual interactions](https://learn.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions)
- [Power BI line charts](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-line)

---

## 👨‍💻 Project Type

**Power BI Data Visualization Practice Project**

### Visualizations Used

- 📈 Line Chart
- 🌊 Area Chart

### Analysis

**Profit and Quantity by Ship Mode**

### Main Fields

```text
Ship Mode → Category / ordered field
Profit    → Numerical measure
Quantity  → Numerical measure
```

### Repository Structure

```text
PowerBI_Line_Area_Charts/
│
├── README.md
│
└── Images/
    ├── line-chart.png
    └── area-chart.png
```
