# Power BI – Stacked Area Chart

## 📊 Project Overview

This Power BI visualization demonstrates a **Stacked Area Chart** for analyzing **Sales by Ship Mode and Segment**.

The visual combines:

- **Ship Mode** as the X-axis
- **Sales** as the Y-axis
- **Segment** as the Legend
- Multiple colored areas to show the contribution of each customer segment
- Data labels to display sales values
- Interactive filtering and highlighting
- Formatting options such as title, axes, legend, colors, labels, gridlines, and zoom/slider controls

This README explains how to create the visual and how to configure the major Power BI options associated with it.

---

# 🖼️ Visualization Used

<p align="center">
  <img src="images\image06.png"
       alt="Power BI Stacked Area Chart - Sales by Ship Mode and Segment"
       width="1000">
</p>

---

# 1. 🌊 What Is a Stacked Area Chart?

A **Stacked Area Chart** displays multiple data series as filled areas stacked on top of one another.

It is useful when you want to understand:

- Overall magnitude
- Contribution of different categories
- Changes across an ordered dimension
- Composition of a total
- Relationship between multiple series

In this example, Sales are divided among three customer segments:

```text
Consumer
Corporate
Home Office
```

The chart shows how each segment contributes to total Sales for each Ship Mode.

---

# 2. 📌 Chart Configuration

The visual shown in the screenshot uses the following configuration:

```text
Visual Type → Stacked Area Chart

X-axis      → Ship Mode

Y-axis      → Sum of Sales

Legend      → Segment
```

In Power BI:

```text
X-axis
    Ship Mode

Y-axis
    Sum of Sales

Legend
    Segment
```

---

# 3. 📋 Fields Used

| Power BI Field | Data Type | Role in Chart |
|---|---|---|
| Ship Mode | Categorical | X-axis |
| Sales | Numerical | Y-axis |
| Segment | Categorical | Legend |

### Ship Mode

The chart contains:

```text
Standard Class
Second Class
First Class
Same Day
```

### Segment

The chart contains:

```text
Consumer
Corporate
Home Office
```

### Sales

Sales is a numerical field and is aggregated as:

```text
Sum of Sales
```

---

# 4. 📊 Understanding the Chart

The stacked areas represent different customer segments.

For example:

```text
Standard Class
├── Consumer
├── Corporate
└── Home Office
```

The total height of the stacked area represents the combined Sales.

Conceptually:

```text
Total Sales
┌──────────────────────┐
│ Consumer              │
├──────────────────────┤
│ Corporate             │
├──────────────────────┤
│ Home Office           │
└──────────────────────┘
```

Therefore, the chart can answer questions such as:

- Which Ship Mode has the highest total Sales?
- How much does each Segment contribute?
- Which Segment contributes the largest amount?
- How does the composition change between Ship Modes?

---

# 5. 🛠️ How to Create the Stacked Area Chart

## Step 1 – Load the Dataset

Open:

```text
Power BI Desktop
```

Then:

```text
Home → Get Data
```

Select the required data source and load the dataset.

---

## Step 2 – Open Report View

Select:

```text
Report View
```

from the left navigation.

---

## Step 3 – Select Stacked Area Chart

From the **Visualizations** pane, select the **Stacked Area Chart** visual.

A blank visual will appear.

---

## Step 4 – Add Ship Mode

Drag:

```text
Ship Mode
```

into:

```text
X-axis
```

---

## Step 5 – Add Sales

Drag:

```text
Sales
```

into:

```text
Y-axis
```

Power BI will normally create:

```text
Sum of Sales
```

---

## Step 6 – Add Segment

Drag:

```text
Segment
```

into:

```text
Legend
```

This creates separate stacked areas for:

```text
Consumer
Corporate
Home Office
```

---

# 6. 🧮 Aggregation – Sum of Sales

Because Sales is numerical, Power BI automatically aggregates it.

The screenshot shows:

```text
Sum of Sales
```

Other aggregation options can include:

```text
Sum
Average
Minimum
Maximum
Count
Distinct Count
```

For this analysis, **Sum of Sales** is appropriate because the objective is to compare total Sales.

---

# 7. 🏷️ Data Labels

Data labels show numerical values directly on the visual.

Examples visible in the screenshot include values such as:

```text
0.71M
0.41M
0.24M
0.23M
0.15M
0.08M
```

Depending on the selected series and formatting settings, Power BI can display labels for the stacked portions.

### To configure Data Labels

1. Select the chart.
2. Open **Format visual**.
3. Find the data labels/detail labels section.
4. Turn labels **On**.
5. Configure:
   - Font size
   - Display units
   - Decimal places
   - Position
   - Color
   - Series options where available

---

# 8. 🔢 Display Units

Large numbers can be displayed using compact units.

Examples:

```text
710,000 → 0.71M
410,000 → 0.41M
240,000 → 0.24M
```

Common display units include:

```text
None
Thousands
Millions
Billions
```

For this visualization, **Millions (M)** makes the labels easier to read.

---

# 9. 📚 Legend

The **Legend** identifies each stacked series.

In this chart:

```text
Legend → Segment
```

The legend contains:

```text
Consumer
Corporate
Home Office
```

The colors correspond to the segments shown in the stacked areas.

---

## Why Is the Legend Important?

Without the legend, users may not know which color represents which Segment.

The legend allows users to understand:

```text
Color → Segment
```

For example:

```text
Blue → Consumer
Dark Blue → Corporate
Orange → Home Office
```

The exact colors may vary depending on the Power BI theme.

---

# 10. 🎨 Formatting the Legend

Select:

```text
Format visual
```

Then locate the legend formatting options.

Depending on the Power BI version, you can configure:

- Legend On/Off
- Position
- Orientation
- Font size
- Text color
- Title
- Marker size
- Spacing

Possible positions include:

```text
Top
Bottom
Left
Right
```

### Best Practice

Place the legend where it does not overlap with:

- Data labels
- Axis labels
- Chart title
- Important data

---

# 11. 🏷️ Chart Title

The title in the screenshot is:

```text
Sum of Sales by Ship Mode and Segment
```

A more concise business-friendly title could be:

```text
Sales by Ship Mode and Segment
```

### To change the title

1. Select the chart.
2. Open **Format visual**.
3. Open the **Title** section.
4. Turn Title **On**.
5. Enter the desired title.
6. Configure:
   - Font
   - Font size
   - Alignment
   - Text color
   - Background

---

# 12. 📏 X-axis

The X-axis contains:

```text
Ship Mode
```

The categories are:

```text
Standard Class
Second Class
First Class
Same Day
```

The X-axis is categorical in this example.

### Formatting options may include:

- Title
- Font
- Font size
- Text color
- Label density
- Concatenation
- Axis type where supported

---

# 13. 📐 Y-axis

The Y-axis represents:

```text
Sum of Sales
```

The axis values in the screenshot are displayed using millions:

```text
0.0M
0.2M
0.4M
0.6M
0.8M
1.0M
1.2M
1.4M
```

### Formatting options include:

- Axis title
- Font size
- Display units
- Decimal places
- Minimum
- Maximum
- Gridlines
- Scale

---

# 14. 🔍 Zoom Slider / Zoom Controls

Power BI visuals can provide zoom and navigation controls when the visual supports them and the relevant axis/settings are enabled.

A zoom slider allows the user to focus on a selected portion of the axis rather than viewing the complete range at once.

Conceptually:

```text
Full Range
|-------------------------------------------|

Zoomed Range
        |----------------|
```

This is particularly useful when there are:

- Many categories
- Long date ranges
- Dense axis labels
- Large datasets
- Detailed time-series data

---

## How to Check Zoom Slider Settings

1. Select the visual.
2. Open **Format visual**.
3. Open the relevant **X-axis** or **Zoom slider** formatting section.
4. If available, turn **Zoom slider** On.
5. Adjust the slider directly on the visual.

The exact location and availability of the zoom-slider option can vary depending on the visual type and current Power BI Desktop version.

---

# 15. 🎯 Why Use a Zoom Slider?

A zoom slider can help users:

- Focus on a specific range
- Inspect dense data
- Navigate long axes
- Reduce visual clutter
- Explore details interactively

For a chart with only four Ship Mode categories, a zoom slider is generally less important.

For a chart such as:

```text
January 2020 → December 2026
```

a zoom slider can be much more useful.

---

# 16. 🧭 X-axis Zoom vs Time-Series Analysis

This chart uses:

```text
Ship Mode
```

which is categorical.

For a genuine trend visualization, a date field such as:

```text
Order Date
```

would be more appropriate.

Example:

```text
Order Date → X-axis
Sales      → Y-axis
Segment    → Legend
```

This could show Sales trends over time for each Segment.

---

# 17. 🖱️ Tooltips

Tooltips appear when the user hovers over a data point.

A tooltip can provide additional information without adding more labels to the chart.

For example:

```text
Ship Mode: Standard Class
Segment: Consumer
Sales: 0.71M
```

### To configure tooltips

1. Select the visual.
2. Open the visual field configuration.
3. Locate **Tooltips** if available.
4. Add additional fields if required.
5. Format the tooltip where supported.

---

# 18. 🎨 Colors

Colors distinguish the different Segment series.

For example:

```text
Consumer
Corporate
Home Office
```

Each series receives a different color.

### To change colors

1. Select the visual.
2. Open **Format visual**.
3. Locate the series/color formatting section.
4. Select the required series.
5. Choose the desired color.

---

# 19. 🎨 Color Best Practices

Use colors consistently throughout the report.

For example, if:

```text
Consumer = Blue
Corporate = Dark Blue
Home Office = Orange
```

keep those assignments consistent across other visuals.

Avoid:

- Too many colors
- Very similar colors
- Low-contrast colors
- Random colors between visuals

---

# 20. 📏 Gridlines

Gridlines help users estimate values.

For example:

```text
1.4M ─────────────────
1.2M ─────────────────
1.0M ─────────────────
0.8M ─────────────────
0.6M ─────────────────
0.4M ─────────────────
0.2M ─────────────────
0.0M ─────────────────
```

Gridlines should support the visual without dominating it.

---

# 21. 🔤 Font Size

Font size can be adjusted for:

- Chart title
- X-axis
- Y-axis
- Legend
- Data labels
- Tooltip text

Use consistent typography across the report.

---

# 22. ↕️ Sorting

Power BI allows visuals to be sorted.

Use the visual's **More options (...)** menu to access sorting options.

Possible sorting:

```text
Sort by Ship Mode
Sort by Sum of Sales
Ascending
Descending
```

For this visual, sorting by Sales can help identify the highest-value categories.

However, if the category order has business meaning, preserve that meaningful order.

---

# 23. 🔄 Visual Interactions

Power BI reports are interactive.

Selecting a segment or category can affect other visuals on the same report page.

Possible interaction types include:

```text
Filter
Highlight
No impact
```

For example:

```text
Click Consumer
      ↓
Other visuals may filter/highlight
Consumer-related data
```

---

# 24. 🔎 Drill-Down

Drill-down allows users to move from a higher-level category to a lower-level category when a hierarchy is configured.

Example:

```text
Region
   ↓
State
   ↓
City
```

For dates:

```text
Year
   ↓
Quarter
   ↓
Month
   ↓
Day
```

Drill-down is useful when the report contains hierarchical information.

---

# 25. 🎚️ Slicers

A **Slicer** is an interactive filtering control.

For example, you could add:

```text
Region
Category
Segment
Ship Mode
Order Date
```

Users can select values and filter the report.

Example:

```text
Segment Slicer

☑ Consumer
☐ Corporate
☐ Home Office
```

The chart can then update based on the selected filter.

---

# 26. 🔘 Single Select / Multi Select

Slicers can support different selection behaviors.

### Single Select

Allows one value:

```text
Consumer
```

### Multi Select

Allows multiple values:

```text
Consumer
Corporate
```

Use the appropriate option depending on the analysis requirement.

---

# 27. 🧹 Filters Pane

Power BI provides filtering at different levels.

Common levels include:

```text
Visual-level filter
Page-level filter
Report-level filter
```

### Visual-level filter

Affects only the selected visual.

### Page-level filter

Affects visuals on the current report page.

### Report-level filter

Can affect the entire report.

---

# 28. 🧩 Small Multiples

The screenshot's Visualizations pane also shows:

```text
Small multiples
```

Small multiples can split one visual into several smaller visuals based on a categorical field.

For example:

```text
Sales by Ship Mode
```

could be divided by:

```text
Region
```

producing separate visual panels for each Region.

This is useful for comparing the same measure across multiple groups.

---

# 29. 🪄 Conditional Formatting

Where supported, Power BI allows formatting based on data values.

For example:

```text
High Sales → one visual treatment
Low Sales  → another visual treatment
```

Conditional formatting is useful when the color itself communicates information.

---

# 30. 🧮 Measures vs Columns

Power BI distinguishes between:

### Columns

Values stored in the dataset.

Examples:

```text
Sales
Profit
Quantity
Segment
Ship Mode
```

### Measures

Calculated values created using DAX.

Example:

```DAX
Total Sales = SUM(Sheet1[Sales])
```

Using measures can provide more control over calculations and report logic.

---

# 31. 🧠 Example DAX Measure

Instead of relying only on automatic aggregation, you can create:

```DAX
Total Sales = SUM(Sheet1[Sales])
```

Then use:

```text
Total Sales → Y-axis
```

This makes the measure explicit and reusable across multiple visuals.

---

# 32. 📊 Percentage of Total

Power BI can also be used to analyze each Segment's contribution to total Sales.

Conceptually:

```text
Segment Sales
────────────── × 100
Total Sales
```

For example, a DAX measure could be created for percentage analysis.

```DAX
Sales % =
DIVIDE(
    [Total Sales],
    CALCULATE(
        [Total Sales],
        ALL(Sheet1[Segment])
    )
)
```

The exact formula should be adapted to the model and filter context being used.

---

# 33. 🧮 Why Percentage Analysis Is Useful

Instead of only asking:

```text
How much Sales?
```

you can ask:

```text
What percentage of total Sales
comes from each Segment?
```

This is useful for contribution analysis.

---

# 34. 📌 Visual Header

Power BI visuals can provide header controls such as:

- Filter
- Focus mode
- More options
- Additional interaction controls depending on the visual

In the screenshot, the visual header contains icons near the top-right of the visual.

---

# 35. 🔍 Focus Mode

Focus mode expands a visual so that it can be inspected more closely.

This is useful when:

- The report contains many visuals
- The visual is small
- Detailed inspection is required

The user can return to the normal report view afterward.

---

# 36. ⋯ More Options

The **More options (...)** menu can provide actions such as:

- Sorting
- Exporting data
- Show as a table
- Spotlight
- Other visual-specific options

The exact available commands can vary by visual and Power BI version.

---

# 37. 📤 Export Data

Power BI can provide export options for visual data, depending on report permissions and settings.

This can allow users to analyze the underlying summarized data outside the visual.

Always consider whether exported data should contain only summarized values or whether detailed data is appropriate for the report's purpose.

---

# 38. 📱 Responsive Report Design

When designing Power BI reports:

- Keep visuals aligned.
- Avoid excessive empty space.
- Use readable fonts.
- Avoid overlapping labels.
- Keep consistent colors.
- Make important KPIs easy to find.
- Consider how the report will appear on different screen sizes.

---

# 39. 🖥️ Dashboard Layout

A professional report page can follow a structure such as:

```text
┌───────────────────────────────────────────┐
│              REPORT TITLE                │
├───────────────┬───────────────────────────┤
│    SLICERS    │       KPI CARDS           │
├───────────────┴───────────────────────────┤
│                                           │
│          MAIN AREA CHART                  │
│                                           │
├───────────────────────┬───────────────────┤
│ Supporting Visual 1   │ Supporting 2      │
└───────────────────────┴───────────────────┘
```

---

# 40. ⚠️ Important Note About This Visual

The screenshot uses:

```text
Ship Mode
```

on the X-axis.

Ship Mode is a categorical field:

```text
Standard Class
Second Class
First Class
Same Day
```

Therefore, this chart is useful for comparing Sales composition across Ship Modes.

For a true continuous trend, consider:

```text
Order Date → X-axis
Sales → Y-axis
Segment → Legend
```

This would create a time-based Sales trend for each Segment.

---

# 41. 🆚 Stacked Area Chart vs Other Charts

| Chart | Best Use |
|---|---|
| Stacked Area | Composition + magnitude across ordered categories |
| Line Chart | Trend/change |
| Area Chart | Trend + magnitude |
| Stacked Column | Category composition |
| Clustered Column | Side-by-side comparison |
| Bar Chart | Category comparison |
| Pie Chart | Part-to-whole with few categories |
| Donut Chart | Part-to-whole with few categories |

---

# 42. ❌ When Not to Use a Stacked Area Chart

Avoid it when:

- There are too many series.
- Categories are not meaningfully ordered.
- Exact individual values are the main requirement.
- Areas overlap and become difficult to read.
- The chart contains too many categories.
- A simple bar or column chart would communicate the comparison more clearly.

---

# 43. 🎯 Best Practices

### Data

- Use a meaningful X-axis.
- Use a numerical measure on the Y-axis.
- Use a categorical field for the Legend.
- Verify aggregation.

### Design

- Use a clear title.
- Keep the legend visible when multiple series exist.
- Use consistent colors.
- Use readable labels.
- Avoid excessive data labels.
- Use appropriate display units.
- Keep gridlines subtle.

### Interactivity

- Use slicers for filtering.
- Configure visual interactions.
- Use tooltips for additional information.
- Use drill-down when a hierarchy exists.
- Use zoom controls when the axis contains many values.

---

# 44. 🚀 Recommended Power BI Workflow

```text
Load Dataset
      ↓
Check Data Types
      ↓
Transform/Clean Data
      ↓
Create Measures if Required
      ↓
Select Stacked Area Chart
      ↓
Add Ship Mode to X-axis
      ↓
Add Sales to Y-axis
      ↓
Add Segment to Legend
      ↓
Check Sum of Sales
      ↓
Configure Data Labels
      ↓
Configure Display Units
      ↓
Format Title
      ↓
Format X-axis
      ↓
Format Y-axis
      ↓
Format Legend
      ↓
Configure Colors
      ↓
Configure Gridlines
      ↓
Configure Tooltips
      ↓
Configure Zoom/Navigation if Useful
      ↓
Add Slicers if Required
      ↓
Check Sorting
      ↓
Test Interactions
      ↓
Review Report
```

---

# 45. 🧠 Key Power BI Concepts Learned

This visualization demonstrates:

- Stacked Area Charts
- Categorical fields
- Numerical fields
- Measures
- Aggregations
- X-axis
- Y-axis
- Legend
- Data labels
- Display units
- Font formatting
- Color formatting
- Gridlines
- Tooltips
- Sorting
- Zoom controls
- Visual interactions
- Drill-down
- Slicers
- Filters
- Small multiples
- Conditional formatting
- DAX measures
- Percentage calculations
- Dashboard design

---

# 46. 📌 Quick Reference

```text
Chart Type:
Stacked Area Chart

X-axis:
Ship Mode

Y-axis:
Sum of Sales

Legend:
Segment

Measure:
Sales

Aggregation:
Sum
```

---

# 47. 🎓 Learning Outcome

After completing this visualization, you should be able to:

1. Identify categorical and numerical fields.
2. Select an appropriate Power BI visual.
3. Build a Stacked Area Chart.
4. Configure X-axis and Y-axis.
5. Add a categorical Legend.
6. Understand aggregation.
7. Configure data labels.
8. Format display units.
9. Change title and font settings.
10. Format colors.
11. Configure gridlines.
12. Configure tooltips.
13. Understand sorting.
14. Use slicers and filters.
15. Understand visual interactions.
16. Understand zoom/navigation controls.
17. Use drill-down.
18. Use small multiples.
19. Create DAX measures.
20. Design a professional Power BI report.

---

# 48. 🏁 Conclusion

The **Stacked Area Chart** is useful for understanding both **total Sales** and the **contribution of individual Segments** across Ship Modes.

The configuration used in this project is:

```text
Ship Mode
    ↓
X-axis

Sales
    ↓
Y-axis
    ↓
Sum of Sales

Segment
    ↓
Legend
```

The chart can be enhanced using:

```text
Data Labels
Legend
Tooltips
Colors
Gridlines
Zoom Controls
Slicers
Filters
Drill-down
Small Multiples
DAX Measures
```

The most important principle is to choose a visual based on the question being answered. A Stacked Area Chart is particularly useful when both **overall magnitude** and **category contribution** need to be communicated.

---

# 🔗 Microsoft Power BI References

- [Power BI visualization types](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a)
- [Customize Power BI visualizations](https://learn.microsoft.com/en-us/power-bi/create-reports/service-custom-visuals-format)
- [Visual interactions in Power BI](https://learn.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions)
- [Power BI slicers](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers)
- [Power BI filters](https://learn.microsoft.com/en-us/power-bi/create-reports/power-bi-report-add-filter)
- [Power BI drill mode](https://learn.microsoft.com/en-us/power-bi/consumer/end-user-drill)
- [DAX in Power BI](https://learn.microsoft.com/en-us/dax/)

---

## 👨‍💻 Project Information

**Project Type:** Power BI Data Visualization Practice

**Visualization:** Stacked Area Chart

**Analysis:** Sales by Ship Mode and Segment

**Fields Used:**

```text
Ship Mode → X-axis
Sales     → Y-axis
Segment   → Legend
```

### Repository Structure

```text
PowerBI_Stacked_Area_Chart/
│
├── README.md
│
└── Images/
    └── stacked-area-chart.png
```
