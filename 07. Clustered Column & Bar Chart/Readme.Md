# Power BI – Clustered Column Chart & Clustered Bar Chart

## 📊 Project Overview

This Power BI practice project demonstrates two important categorical comparison visuals:

1. **Clustered Column Chart**
2. **Clustered Bar Chart**

Both visuals use the same sales dataset and compare **Sales by Category and Segment**.

The purpose of this project is to understand:

- Which data types are suitable for clustered charts
- How to configure Axis, Legend, and Values
- How to compare multiple categories and groups
- How to format titles, labels, colors, fonts, axes, and legends
- How to make Power BI visuals readable and interactive
- When to choose a clustered column chart versus a clustered bar chart

---

# 📁 Dataset Used

The dataset contains fields such as:

| Column | Type | Example / Purpose |
|---|---|---|
| Category | Categorical | Product category |
| City | Categorical | Customer city |
| Country | Categorical | Customer country |
| Customer ID | Identifier | Unique customer |
| Customer Name | Categorical | Customer name |
| Discount | Numerical | Discount amount/rate |
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

# 1. 📊 Clustered Column Chart

## What is a Clustered Column Chart?

A **Clustered Column Chart** displays multiple vertical columns side by side for each category.

It is useful when you want to compare a numerical measure across:

- Different categories
- Different groups
- Multiple series within each category

In this project, the chart compares **Sales** across product **Categories**, separated by **Segments**.

---

## 🖼️ Clustered Column Chart Used in This Project

<p align="center">
  <img src="https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/07.%20Clustered%20Column%20%26%20Bar%20Chart/images/image08.png"
       alt="Power BI Clustered Column Chart - Sales by Category and Segment"
       width="900">
</p>

### Chart shown above

The chart represents:

```text
Title / Measure → Sum of Sales
Category        → Category
Legend          → Segment
Value           → Sales
```

The categories visible in the chart are:

- Technology
- Furniture
- Office Supplies

The legend contains:

- Consumer
- Corporate
- Home Office

---

# 2. 🧩 What Data Is Suitable for a Clustered Column Chart?

A clustered column chart normally requires:

### A. Categorical Field

A categorical field is used to define the groups on the horizontal axis.

Examples:

```text
Category
Region
Segment
Country
State
Sub-Category
Ship Mode
```

### B. Numerical Field / Measure

A numerical field is used to determine the height of the columns.

Examples:

```text
Sales
Profit
Quantity
Discount
```

### C. Optional Second Categorical Field

A second categorical field can be used as the **Legend** to create multiple columns within each category.

For this project:

```text
X-Axis / Category → Category
Legend            → Segment
Y-Axis / Values   → Sales
```

This produces three segment columns for each product category.

---

# 3. 🛠️ How to Create the Clustered Column Chart

## Step 1 – Load the Dataset

1. Open **Power BI Desktop**.
2. Select **Home → Get Data**.
3. Select your data source.
4. Load the dataset.
5. Check that the columns have the correct data types.

---

## Step 2 – Select the Clustered Column Chart

1. Open the **Report** view.
2. Go to the **Visualizations** pane.
3. Select the **Clustered Column Chart** icon.

A blank visual will appear on the report canvas.

---

## Step 3 – Add the Category

Drag:

```text
Category → X-axis
```

This creates groups such as:

```text
Technology
Furniture
Office Supplies
```

---

## Step 4 – Add Sales

Drag:

```text
Sales → Y-axis / Values
```

Power BI aggregates the Sales field.

The default aggregation will commonly be:

```text
Sum of Sales
```

---

## Step 5 – Add Segment as the Legend

Drag:

```text
Segment → Legend
```

Now each category contains multiple columns:

```text
Technology
 ├── Consumer
 ├── Corporate
 └── Home Office

Furniture
 ├── Consumer
 ├── Corporate
 └── Home Office

Office Supplies
 ├── Consumer
 ├── Corporate
 └── Home Office
```

This is the key feature of a **clustered** chart.

---

# 4. 📈 Understanding the Chart

The chart allows us to compare:

### Category-to-Category

For example:

```text
Technology vs Furniture vs Office Supplies
```

### Segment-to-Segment

For example:

```text
Consumer vs Corporate vs Home Office
```

### Category + Segment

For example:

```text
Technology + Consumer
Technology + Corporate
Technology + Home Office
```

This makes clustered column charts useful when multiple groups need to be compared side by side.

---

# 5. 📊 Clustered Bar Chart

## What is a Clustered Bar Chart?

A **Clustered Bar Chart** uses horizontal bars instead of vertical columns.

The underlying concept is similar to a clustered column chart.

The major difference is the orientation:

```text
Clustered Column
      ↓
Vertical columns

Clustered Bar
      ↓
Horizontal bars
```

A horizontal bar chart can be especially useful when category names are long or when a horizontal layout makes comparisons easier to read.

---

# 6. 🖼️ Clustered Bar Chart Used in This Project

<p align="center">
  <img src="https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/07.%20Clustered%20Column%20%26%20Bar%20Chart/images/image09.png"
       alt="Power BI Clustered Bar Chart - Sales by Category and Segment"
       width="900">
</p>

### Chart shown above

The chart uses:

```text
Category → Category
Legend   → Segment
Values   → Sales
```

The categories are:

- Technology
- Furniture
- Office Supplies

The segment groups are:

- Consumer
- Corporate
- Home Office

---

# 7. 🛠️ How to Create the Clustered Bar Chart

## Step 1 – Select the Visual

In the **Visualizations** pane, select the **Clustered Bar Chart**.

---

## Step 2 – Add Category

Add:

```text
Category → Y-axis
```

Because the chart is horizontal, categories appear along the vertical axis.

---

## Step 3 – Add Sales

Add:

```text
Sales → X-axis / Values
```

The length of each horizontal bar represents the sales value.

---

## Step 4 – Add Segment

Add:

```text
Segment → Legend
```

Power BI displays separate bars for:

```text
Consumer
Corporate
Home Office
```

within each category.

---

# 8. 🆚 Clustered Column vs Clustered Bar

| Feature | Clustered Column | Clustered Bar |
|---|---|---|
| Orientation | Vertical | Horizontal |
| Category axis | X-axis | Y-axis |
| Value axis | Y-axis | X-axis |
| Best for | Vertical comparisons | Horizontal comparisons |
| Long category names | Can become crowded | Often easier to read |
| Multiple groups | ✅ | ✅ |
| Legend | ✅ | ✅ |
| Data labels | ✅ | ✅ |
| Tooltips | ✅ | ✅ |
| Sorting | ✅ | ✅ |
| Cross-filtering | ✅ | ✅ |
| Drill-down | Can be used | Can be used |

---

# 9. 🎨 Formatting the Charts

After creating either chart, select the visual and open:

```text
Format visual
```

Power BI's exact formatting card names can vary slightly between versions.

The following formatting options are commonly useful.

---

# 10. 📝 Chart Title

A clear title tells users what the visual represents.

For example:

```text
Sum of Sales
by Category and Segment
```

Or a cleaner business title:

```text
Sales by Category and Segment
```

### Steps

1. Select the visual.
2. Open **Format visual**.
3. Open the title formatting section.
4. Turn the title on.
5. Enter the required title.
6. Adjust:
   - Font
   - Font size
   - Alignment
   - Text color
   - Background, if required

---

# 11. 🏷️ Data Labels

Data labels show the numerical value directly on each column/bar.

For example:

```text
0.41M
0.25M
0.18M
```

### Steps

1. Select the chart.
2. Open **Format visual**.
3. Find **Data labels** or the corresponding label card.
4. Turn it **On**.
5. Adjust:
   - Text size
   - Display units
   - Decimal places
   - Position
   - Color

Data labels are especially useful when users need to see values without hovering over the visual.

---

# 12. 🔢 Display Units

Large numbers can be displayed using shorter units.

For example:

```text
410,000 → 0.41M
250,000 → 0.25M
```

Common display units include:

```text
None
Thousands
Millions
Billions
```

For sales dashboards, **Millions (M)** can make large values easier to read.

---

# 13. 🔤 Font Size

Font size can be adjusted for:

- Chart title
- Axis labels
- Data labels
- Legend
- Other visual text

Use readable sizes based on the report canvas.

Avoid making labels so small that users have to zoom in.

---

# 14. 📐 X-Axis and Y-Axis Formatting

Axis formatting can improve readability.

Useful options include:

- Axis title
- Font size
- Text color
- Scale
- Display units
- Decimal places
- Gridlines
- Label density
- Start/end values where appropriate

### Clustered Column Chart

```text
X-axis → Category
Y-axis → Sales
```

### Clustered Bar Chart

```text
Y-axis → Category
X-axis → Sales
```

---

# 15. 📚 Axis Titles

Axis titles explain what each axis represents.

For the column chart:

```text
X-axis → Category
Y-axis → Sales
```

For the bar chart:

```text
Y-axis → Category
X-axis → Sales
```

Clear axis titles are especially useful when the dashboard is viewed by someone unfamiliar with the dataset.

---

# 16. 🗂️ Legend Formatting

The legend explains the different series.

In this project:

```text
Consumer
Corporate
Home Office
```

### Legend formatting can include:

- Position
- Font size
- Text color
- Title
- Orientation where supported

Possible positions include:

```text
Top
Bottom
Left
Right
```

The screenshots place the legend near the bottom of the visual.

---

# 17. 🎨 Changing Series Colors

You can customize the color assigned to each segment.

Example:

```text
Consumer      → Color 1
Corporate     → Color 2
Home Office   → Color 3
```

### Steps

1. Select the visual.
2. Open **Format visual**.
3. Open the series/data-color formatting section.
4. Select the required series.
5. Choose a color.

### Best Practice

Keep category/segment colors consistent throughout the report.

For example:

```text
Consumer = same color everywhere
Corporate = same color everywhere
Home Office = same color everywhere
```

This allows users to recognize a segment quickly.

---

# 18. 📊 Sorting

Sorting can make comparisons easier.

You can sort the chart by:

- Category
- Sales
- Another available measure

For example:

```text
Sort by → Sales
```

Then choose:

```text
Ascending
```

or

```text
Descending
```

Use sorting when the order helps communicate the analysis.

---

# 19. 🖱️ Tooltips

Tooltips appear when the user hovers over a column or bar.

For example:

```text
Category: Technology
Segment: Consumer
Sales: 0.41M
```

Tooltips are useful because they provide additional information without adding too many labels to the visual.

---

# 20. 🔍 Cross-Filtering and Cross-Highlighting

Power BI visuals are interactive.

Selecting a category or segment can affect other visuals on the same report page.

For example:

```text
Select Technology
       ↓
Other visuals respond
       ↓
Only relevant data is highlighted/filtered
```

This allows users to explore relationships between different parts of the dataset.

---

# 21. 🔎 Drill-Down

Clustered charts can also be used with hierarchical fields.

For example:

```text
Category
   ↓
Sub-Category
   ↓
Product Name
```

A user can start with:

```text
Technology
```

and then drill down into:

```text
Phones
Accessories
Machines
```

when the hierarchy is configured.

Use drill-down when the data has meaningful levels of detail.

---

# 22. 🧮 Aggregation

When `Sales` is placed in the Values field, Power BI applies an aggregation.

Common aggregations include:

```text
Sum
Average
Minimum
Maximum
Count
Distinct count
```

For this project:

```text
Sales → Sum
```

Therefore the chart displays:

```text
Sum of Sales
```

Always verify that the selected aggregation matches the business question.

---

# 23. 📌 Why Category and Segment Work Well Together

The combination:

```text
Category + Segment + Sales
```

is appropriate because:

- `Category` is categorical.
- `Segment` is categorical.
- `Sales` is numerical.
- Sales can be aggregated.
- Multiple segments can be compared within each category.

This creates a clear **two-dimensional categorical comparison**.

---

# 24. ❌ When NOT to Use Clustered Column/Bar Charts

Avoid these charts when:

### Too many categories

If there are dozens of categories, the visual can become crowded.

Consider:

- Bar Chart
- Treemap
- Table
- Matrix

depending on the analysis.

### Time-series trend

For continuous trends over time, consider:

```text
Line Chart
```

Example:

```text
Sales by Month
```

### Part-to-whole analysis

If the primary question is:

> What percentage of the total does each category represent?

consider:

```text
Pie Chart
Donut Chart
100% Stacked Chart
```

depending on the number of categories and comparison needs.

---

# 25. 🆚 When Should I Use Column vs Bar?

## Use Clustered Column Chart when:

- Categories have short names.
- Vertical comparison is easy to read.
- You want a traditional column-style dashboard.
- You have a moderate number of categories.

## Use Clustered Bar Chart when:

- Category names are long.
- Horizontal comparison is easier.
- You want the category labels displayed along the left side.
- A horizontal layout fits the dashboard better.

Neither visual is universally better; the choice depends on the data and the intended presentation.

---

# 26. 📊 Understanding the Values in This Project

The screenshots show approximately:

### Technology

```text
Consumer     ≈ 0.41M
Corporate    ≈ 0.25M
Home Office  ≈ 0.18M
```

### Furniture

```text
Consumer     ≈ 0.39M
Corporate    ≈ 0.23M
Home Office  ≈ 0.12M
```

### Office Supplies

```text
Consumer     ≈ 0.36M
Corporate    ≈ 0.23M
Home Office  ≈ 0.12M
```

These values are displayed in the Power BI visuals using **millions (M)** as the display unit.

---

# 27. 📋 Field Configuration Summary

## Clustered Column Chart

```text
Visual:
Clustered Column Chart

X-axis:
Category

Y-axis / Values:
Sales

Legend:
Segment

Aggregation:
Sum of Sales
```

## Clustered Bar Chart

```text
Visual:
Clustered Bar Chart

Y-axis:
Category

X-axis / Values:
Sales

Legend:
Segment

Aggregation:
Sum of Sales
```

---

# 28. 🎯 Practical Example

Suppose the dataset contains:

| Category | Segment | Sales |
|---|---|---:|
| Technology | Consumer | 410,000 |
| Technology | Corporate | 250,000 |
| Technology | Home Office | 180,000 |
| Furniture | Consumer | 390,000 |
| Furniture | Corporate | 230,000 |
| Furniture | Home Office | 120,000 |
| Office Supplies | Consumer | 360,000 |
| Office Supplies | Corporate | 230,000 |
| Office Supplies | Home Office | 120,000 |

Power BI groups the data by:

```text
Category
    +
Segment
```

and calculates:

```text
Sum of Sales
```

The resulting visual allows direct comparison between categories and segments.

---

# 29. 🧠 Key Concepts Learned

This project demonstrates:

- Power BI data loading
- Data types
- Categorical data
- Numerical data
- Measures
- Aggregation
- Clustered Column Chart
- Clustered Bar Chart
- Axis configuration
- Legend
- Data labels
- Display units
- Number formatting
- Font formatting
- Colors
- Sorting
- Tooltips
- Cross-filtering
- Cross-highlighting
- Drill-down
- Visual interactions
- Dashboard design

---

# 30. 🚀 Recommended Power BI Workflow

```text
Load Dataset
      ↓
Check Data Types
      ↓
Clean / Transform Data
      ↓
Select Visualization
      ↓
Choose Categorical Field
      ↓
Choose Numerical Measure
      ↓
Add Second Category to Legend
      ↓
Check Aggregation
      ↓
Format Title
      ↓
Format Axis
      ↓
Format Legend
      ↓
Enable Data Labels
      ↓
Set Display Units
      ↓
Set Colors
      ↓
Configure Tooltips
      ↓
Test Interactions
      ↓
Sort if Required
      ↓
Align Visual
      ↓
Review Dashboard
```

---

# 31. ✅ Best Practices

### Data

- Use categorical fields for categories and groups.
- Use numerical measures for values.
- Verify data types before creating visuals.
- Check aggregation settings.

### Visual Design

- Keep the number of categories manageable.
- Use consistent colors.
- Use readable fonts.
- Avoid unnecessary visual effects.
- Use clear titles.
- Use appropriate display units.
- Avoid overcrowding the visual.

### Comparison

Use clustered visuals when the purpose is to compare multiple groups side by side.

### Accessibility

Use sufficient contrast and do not rely only on color to communicate meaning.

---

# 32. 🎯 Conclusion

Clustered Column Charts and Clustered Bar Charts are powerful Power BI visuals for comparing numerical values across categories and groups.

In this project:

```text
Category → Product category
Segment  → Customer segment
Sales    → Numerical measure
```

The Clustered Column Chart presents the comparison vertically, while the Clustered Bar Chart presents the same type of comparison horizontally.

The main learning process is:

```text
Choose the correct data
        ↓
Choose the appropriate visual
        ↓
Configure Axis
        ↓
Configure Legend
        ↓
Add Numerical Measure
        ↓
Format the Visual
        ↓
Add Labels & Tooltips
        ↓
Enable Interactions
        ↓
Build a Clear Dashboard
```

---

# 🔗 Official Microsoft Learn References

- [Power BI visualization types](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a)
- [Customize visualization titles, backgrounds, and legends](https://learn.microsoft.com/en-us/power-bi/create-reports/service-custom-visuals-format)
- [Power BI data labels](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-customize-title-background-and-legend)
- [Power BI report visual interactions](https://learn.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions)

---

## 👨‍💻 Project Type

**Power BI Data Visualization Practice Project**

### Visualizations Used

- 📊 Clustered Column Chart
- 📊 Clustered Bar Chart

### Analysis

**Sales by Category and Segment**

### Main Fields

```text
Category → Categorical field
Segment  → Categorical field / Legend
Sales    → Numerical measure
```

### Repository Structure

```text
PowerBI_Clustered_Column_Bar_Charts/
│
├── README.md
│
└── Images/
    ├── clustered-column-chart.png
    └── clustered-bar-chart.png
```
