# Power BI – Pie Chart & Donut Chart Visualization

## 📊 Project Overview

This Power BI practice project demonstrates how to create and customize **Pie Chart** and **Donut Chart** visuals using a sales dataset.

The report compares **Sales by Segment**, using the following categories:

- Consumer
- Corporate
- Home Office

Both visuals represent a **part-to-whole relationship**, where each category shows its contribution to the total sales.

> **Example from this report:**  
> The Pie Chart and Donut Chart use `Segment` as the categorical field and `Sales` as the numerical measure.

<h2>📊 Power BI Dashboard</h2>

<p>
  The following image shows the Pie Chart and Donut Chart created in Power BI:
</p>

<img src="(![Power BI Pie & Donut Chart](https://github.com/Ganesh-Ganga/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/05.%20Creating%20a%20Column%20Chart/Images/image05.png)" 
     alt="Power BI Pie Chart and Donut Chart"
     width="900">

---images\image07.png

## 📁 Dataset Used

The report uses a sales dataset containing fields such as:

| Column | Data Type | Example / Purpose |
|---|---|---|
| Category | Categorical | Product category |
| City | Categorical | Customer city |
| Country | Categorical | Customer country |
| Customer ID | Identifier | Unique customer |
| Customer Name | Categorical | Customer name |
| Discount | Numerical | Discount value |
| Order Date | Date | Date of order |
| Order ID | Identifier | Unique order |
| Postal Code | Numerical / Categorical | Postal code |
| Product ID | Identifier | Product identifier |
| Product Name | Categorical | Product name |
| Profit | Numerical | Profit amount |
| Quantity | Numerical | Quantity sold |
| Region | Categorical | Sales region |
| Sales | Numerical | Sales amount |
| Segment | Categorical | Customer segment |
| Ship Date | Date | Shipping date |
| Ship Mode | Categorical | Shipping method |
| State | Categorical | State |
| Sub-Category | Categorical | Product sub-category |

---

# 1. 🥧 Pie Chart

## What is a Pie Chart?

A **Pie Chart** is used to display how individual categories contribute to a complete total.

Each slice represents one category, and the size of the slice represents that category's value relative to the total.

### Best use cases

A Pie Chart is suitable when:

- You want to show **parts of a whole**.
- The main comparison is based on **percentage/proportion**.
- You have a **small number of categories**.
- The categories are clearly distinguishable.
- You want users to quickly understand category contribution.

Microsoft recommends using pie and donut charts for part-to-whole relationships and keeping the number of categories relatively small for readability.

---

## What Type of Columns Should Be Used?

A Pie Chart normally needs:

### 1. Categorical Column

Use a **categorical column** for the categories/slices.

Examples:

- Segment
- Category
- Region
- Ship Mode
- Country
- Sub-Category

### 2. Numerical Column or Measure

Use a **numeric column/measure** for the values.

Examples:

- Sales
- Profit
- Quantity
- Discount

### Example

For this project:

```text
Legend  → Segment
Values  → Sales
```

This creates:

```text
Consumer
Corporate
Home Office
```

with each slice representing its corresponding sales contribution.

---

# 2. 🍩 Donut Chart

## What is a Donut Chart?

A **Donut Chart** is similar to a Pie Chart, but it has an empty center.

It is useful for showing part-to-whole relationships while also providing space in the center for a summary value.

For example:

```text
        Consumer
      ┌───────────┐
   ┌──┘           └──┐
   │      2.30M       │
   │                  │
   └──────────────────┘
       Corporate
```

In Power BI, a Donut Chart can display a **center value**, such as the total sales.

---

## What Type of Columns Should Be Used?

The same basic data structure used for a Pie Chart can be used for a Donut Chart.

### Categorical Column

Examples:

- Segment
- Category
- Region
- Ship Mode
- Country
- Sub-Category

### Numerical Column / Measure

Examples:

- Sales
- Profit
- Quantity
- Discount

### Example

```text
Legend  → Segment
Values  → Sales
```

The result shows the sales contribution of:

- Consumer
- Corporate
- Home Office

and the center can show the total sales.

---

# 3. 🆚 Pie Chart vs Donut Chart

| Feature | Pie Chart | Donut Chart |
|---|---|---|
| Shape | Complete circle | Ring |
| Part-to-whole analysis | ✅ | ✅ |
| Categorical data | ✅ | ✅ |
| Numerical measure | ✅ | ✅ |
| Percentage analysis | ✅ | ✅ |
| Center value | ❌ | ✅ |
| Total value displayed in center | ❌ | ✅ |
| Best for | Simple proportion analysis | Proportion + central KPI |
| Example | Sales by Segment | Sales by Segment + Total Sales |

---

# 4. 🛠️ How to Create a Pie Chart in Power BI

## Step 1 – Load the Dataset

1. Open **Power BI Desktop**.
2. Select **Home → Get Data**.
3. Choose the required source, such as:
   - Excel
   - CSV
   - SQL Server
   - Database
4. Load the dataset.

---

## Step 2 – Insert the Pie Chart

1. Go to the **Report** view.
2. Open the **Visualizations** pane.
3. Select the **Pie Chart** visual.
4. A blank Pie Chart will appear on the report canvas.

---

## Step 3 – Add the Category

From the Data pane:

1. Find `Segment`.
2. Drag `Segment` into the **Legend** field.

The legend will contain:

```text
Consumer
Corporate
Home Office
```

---

## Step 4 – Add the Numerical Value

1. Find `Sales`.
2. Drag `Sales` into the **Values** field.

Power BI will aggregate the sales values and create the slices.

The structure becomes:

```text
Legend
  ↓
Segment

Values
  ↓
Sales
```

---

# 5. 🍩 How to Create a Donut Chart

## Step 1

Select the **Donut Chart** visual from the Visualizations pane.

## Step 2

Drag:

```text
Segment → Legend
Sales   → Values
```

## Step 3

Select the Donut Chart and open:

```text
Format visual
```

## Step 4

Customize the visual according to your report requirements.

The Donut Chart can also display a center value representing the total of the charted values.

---

# 6. 🎨 Formatting the Pie and Donut Charts

Formatting makes the visualization easier to understand and more professional.

Select the visual and open:

```text
Format visual
```

Depending on the current Power BI Desktop interface, available formatting cards can vary slightly.

---

## A. Title

### Purpose

The title tells the viewer what the chart represents.

### Example

```text
Sales by Segment
```

### Steps

1. Select the chart.
2. Select **Format visual**.
3. Find **General / Title** or the visual's title formatting option.
4. Turn the title **On**.
5. Enter:

```text
Sales by Segment
```

6. Adjust:
   - Font
   - Font size
   - Text alignment
   - Color
   - Background, if required

---

# 7. 🏷️ Data Labels

Data labels display information directly around or on the slices.

Depending on the Power BI version, the label settings may appear under a card such as **Detail labels** or a similar visual-specific label section.

### Useful label information

You can display information such as:

- Category
- Data value
- Percentage of total

For example:

```text
Consumer
1.16M
50.56%
```

### Recommended approach

For a simple business dashboard, percentage labels are useful when the main objective is understanding contribution.

Avoid displaying too much information if the chart becomes crowded.

---

# 8. 📈 Showing Percentage Contribution

A Pie Chart naturally represents each category as a proportion of the total.

For example:

```text
Consumer      → 50.56%
Corporate     → 30.74%
Home Office   → 18.70%
```

The formula concept is:

```text
Percentage =
Category Sales / Total Sales × 100
```

Example:

```text
Consumer Percentage =
Consumer Sales / Total Sales × 100
```

### Important

In Power BI Desktop, use the visual's label/detail formatting options to display the percentage of the total where supported.

Do not manually type percentages into the chart.

---

# 9. 🔢 Formatting Values

Large values can be difficult to read.

Instead of:

```text
2,300,000
```

you can display:

```text
2.30M
```

Similarly:

```text
1,160,000
```

can be displayed as:

```text
1.16M
```

### Why use display units?

Display units such as:

- None
- Thousands (K)
- Millions (M)
- Billions (B)

make dashboards easier to read.

---

# 10. 🔤 Font Size

Font size can be adjusted for:

- Chart title
- Data labels
- Legend
- Center value
- Other visual text elements

### General recommendation

Use larger fonts for:

```text
Chart Title
```

and slightly smaller fonts for:

```text
Legend
Data Labels
```

The exact size depends on the report canvas and the amount of information shown.

---

# 11. 🗂️ Legend Formatting

The **Legend** identifies which color belongs to which category.

Example:

```text
● Consumer
● Corporate
● Home Office
```

### Legend customization can include

- Position
- Font size
- Text color
- Title
- Orientation, where supported
- Category colors

### Common legend positions

- Right
- Left
- Top
- Bottom

For the example report, the legend is positioned on the **right side** of the charts.

---

# 12. 🎨 Changing Slice Colors

To change the colors of Pie or Donut slices:

1. Select the visual.
2. Open **Format visual**.
3. Find the visual's **Colors / Slices / Data colors** section.
4. Select the color associated with each category.
5. Choose the required color.

Example:

```text
Consumer      → Blue
Corporate     → Dark Blue
Home Office   → Orange
```

### Best practice

Keep the same category colors across your report.

For example, if:

```text
Consumer = Blue
Corporate = Dark Blue
Home Office = Orange
```

then use the same mapping in other visuals whenever possible.

This makes dashboards easier to understand.

---

# 13. 🖌️ Conditional Formatting for Colors

For some Power BI visual scenarios, conditional formatting can be used to determine visual colors from a field or measure.

A typical workflow is:

```text
Select Visual
      ↓
Format visual
      ↓
Colors / Slices
      ↓
Conditional formatting (fx)
      ↓
Select Field value / Gradient
```

This is useful when category colors are stored in the data or when colors need to respond to values.

---

# 14. 🔘 Donut Center Value

One important difference between Pie and Donut Charts is the center value.

### Donut Chart

A Donut Chart can show:

```text
2.30M
```

in the center.

This can represent:

```text
Total Sales
```

### Steps

1. Select the Donut Chart.
2. Open **Format visual**.
3. Find **Center value**.
4. Turn it **On**.
5. Select the required measure.
6. Adjust:
   - Font size
   - Font
   - Display units
   - Number format
   - Label, if required

The center value can update when the report is filtered or interacted with.

---

# 15. 📐 Number Formatting

Before creating the chart, make sure numerical columns have appropriate formats.

For example:

### Sales

```text
Currency / Decimal / Whole Number
```

### Profit

```text
Currency / Decimal
```

### Quantity

```text
Whole Number
```

### Percentage

```text
Percentage
```

Power BI also supports custom format strings for controlling how numeric values are displayed.

---

# 16. 🖱️ Tooltips

Tooltips appear when the user moves the mouse over a chart segment.

A tooltip can provide additional information without overcrowding the visual.

For example:

```text
Segment: Consumer
Sales: $1.16M
Percentage: 50.56%
```

### Benefits

- Keeps the visual clean.
- Provides extra information on demand.
- Improves interactivity.

---

# 17. 🔍 Interactive Filtering

Power BI visuals are interactive.

For example, selecting the **Consumer** slice can affect other visuals on the same report page.

This allows users to explore the report dynamically.

Possible interactions include:

- Cross-filtering
- Cross-highlighting
- Selecting another category
- Clearing the selection

---

# 18. 🔎 Drill Down

Pie and Donut Charts can also be configured with hierarchical categorical fields.

Example:

```text
Category
   ↓
Sub-Category
   ↓
Product
```

This allows users to explore data at different levels.

Example:

```text
Category
    ↓
Furniture
    ↓
Chairs
    ↓
Individual Products
```

Use drill-down only when the hierarchy provides meaningful analysis.

---

# 19. 📊 Example from This Power BI Report

The screenshot contains two visuals.

### Visual 1 – Pie Chart

```text
Title:
Sales by Segment

Legend:
Segment

Values:
Sales
```

Categories:

```text
Consumer
Corporate
Home Office
```

The chart shows the relative contribution of each segment to total sales.

---

### Visual 2 – Donut Chart

```text
Title:
Sales by Segment

Legend:
Segment

Values:
Sales

Center Value:
Total Sales
```

The center of the Donut Chart shows the total sales amount.

The screenshot shows approximately:

```text
Total Sales = 2.30M
```

while the individual segments contribute approximately:

```text
Consumer      = 50.56%
Corporate     = 30.74%
Home Office   = 18.70%
```

---

# 20. 🧮 Basic Calculation Concept

If the total sales are:

```text
2.30M
```

and Consumer sales are:

```text
1.16M
```

then:

```text
Consumer %
=
1.16M / 2.30M × 100
≈ 50.56%
```

Similarly:

```text
Corporate %
≈ 30.74%

Home Office %
≈ 18.70%
```

The percentages should add up to approximately:

```text
100%
```

Small differences can occur because of rounding.

---

# 21. 📌 When NOT to Use a Pie or Donut Chart

Avoid Pie/Donut Charts when:

- There are too many categories.
- Categories have very similar values.
- Exact value comparison is important.
- The data represents a trend over time.
- The visual becomes difficult to read.

For many categories, consider using:

- Bar Chart
- Column Chart
- Treemap
- Table
- Matrix

For trends over time, consider:

- Line Chart
- Area Chart
- Column Chart

---

# 22. ✅ Best Practices

### Data

- Use a categorical field for the category/slice.
- Use a numerical measure for the value.
- Ensure values are meaningful and correctly aggregated.

### Design

- Keep the number of slices small.
- Use consistent category colors.
- Use readable font sizes.
- Avoid unnecessary 3D effects.
- Avoid excessive labels.
- Use a clear chart title.
- Format large numbers using K/M/B where appropriate.

### Labels

Use percentages when the purpose is contribution analysis.

Use values when exact amounts are important.

Use both only when the visual remains readable.

### Layout

Keep enough spacing between visuals.

Align charts consistently.

Use the same color mapping across the report.

---

# 23. 🚀 Suggested Power BI Workflow

A practical workflow for creating these visuals is:

```text
Load Dataset
     ↓
Check Data Types
     ↓
Clean / Transform Data
     ↓
Create Measures if Required
     ↓
Insert Pie Chart
     ↓
Add Category to Legend
     ↓
Add Measure to Values
     ↓
Format Title
     ↓
Format Legend
     ↓
Format Data Labels
     ↓
Format Colors
     ↓
Insert Donut Chart
     ↓
Add Category to Legend
     ↓
Add Measure to Values
     ↓
Enable Center Value
     ↓
Format Number Units
     ↓
Add Tooltips
     ↓
Test Interactions
     ↓
Align & Design Dashboard
```

---

# 24. 📚 Key Concepts Learned

This project demonstrates the following Power BI concepts:

- Data loading
- Data fields
- Categorical columns
- Numerical columns
- Measures
- Pie Charts
- Donut Charts
- Part-to-whole analysis
- Legends
- Data labels
- Percentage contribution
- Display units
- Number formatting
- Font formatting
- Color formatting
- Tooltips
- Cross-filtering
- Cross-highlighting
- Drill-down
- Center values
- Dashboard layout
- Visual formatting

---

# 25. 🎯 Conclusion

Pie and Donut Charts are useful Power BI visuals for understanding **how categories contribute to a total**.

In this project, the `Segment` column is used as the categorical field and `Sales` is used as the numerical measure.

The Pie Chart provides a straightforward view of sales contribution, while the Donut Chart additionally provides a central area where the total sales value can be displayed.

The main objective is not only to create the charts but also to understand how to:

```text
Choose the correct data
        ↓
Select the correct visual
        ↓
Configure fields
        ↓
Format the visual
        ↓
Display useful information
        ↓
Make the report interactive
```

---

## 🔗 Official Microsoft Learn References

- [Create and use pie and donut charts in Power BI](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-doughnut-charts)
- [Use custom format strings in Power BI Desktop](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-custom-format-strings)
- [Overview of visualizations in Power BI](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-a)

---

## 👨‍💻 Project Type

**Power BI Data Visualization Practice Project**

### Visualization Used

- 🥧 Pie Chart
- 🍩 Donut Chart

### Analysis

**Sales by Segment**

### Main Fields

```text
Category Field → Segment
Value Field    → Sales
```
