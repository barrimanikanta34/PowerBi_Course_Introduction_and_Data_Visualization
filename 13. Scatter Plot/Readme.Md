# 📊 Power BI Scatter Plot

![Power BI Scatter Plot](https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/13.%20Scatter%20Plot/Images/image3.png)

## 1. Introduction

A **Scatter Plot** in Power BI is used to display the relationship between **two numerical variables**. Each data point represents a record, category, customer, product, transaction, or another level of detail.

In this example, the chart is titled **"Sales V/S Profit"**:

- **X-axis:** Sales
- **Y-axis:** Profit
- **Each dot:** Represents an individual data point
- The chart helps observe how Sales and Profit are distributed and whether there is a visible relationship between them.

A scatter plot is especially useful when you want to examine:

- Relationship between two numerical variables
- Positive or negative association
- Clusters of observations
- Outliers
- High-value and low-value observations
- Distribution of data
- Possible patterns between two measures

---

# 2. When Should You Use a Scatter Plot?

A scatter plot is suitable when you have **two numerical/continuous variables** that you want to compare.

### Common examples

| X-axis | Y-axis | Purpose |
|---|---|---|
| Sales | Profit | Analyze sales-profit relationship |
| Quantity | Sales | Analyze quantity-sales relationship |
| Discount | Profit | Study discount-profit relationship |
| Advertising Cost | Revenue | Analyze marketing effectiveness |
| Hours Studied | Marks | Study learning relationship |
| Temperature | Sales | Analyze weather-sales relationship |
| Age | Income | Analyze demographic relationship |

### Example

For a business dataset:

```text
X-axis → Sales
Y-axis → Profit
```

Each dot represents an observation.

If Sales increases and Profit generally increases, the points may show an upward pattern.

If Sales increases while Profit generally decreases, the points may show a downward pattern.

---

# 3. What Type of Columns Are Suitable?

Scatter plots primarily require **numeric fields**.

## X-axis

Use a:

- Whole number
- Decimal number
- Currency
- Numeric measure
- Calculated numeric measure

Examples:

```text
Sales
Revenue
Quantity
Cost
Discount
Price
```

## Y-axis

Use another numerical field.

Examples:

```text
Profit
Revenue
Cost
Quantity
Margin
Score
```

### Recommended combination

```text
X-axis = Sales
Y-axis = Profit
```

This is the configuration used in the provided example.

---

# 4. What Columns Should NOT Normally Be Used as X/Y Values?

Categorical columns are generally not appropriate as the direct numerical X/Y values of a scatter plot.

Examples:

```text
Customer Name
City
Country
Category
Segment
Region
Ship Mode
Product Name
```

These fields are better used for **Details, Legend, Size, or filtering**, depending on the visual configuration.

For example:

```text
X-axis  → Sales
Y-axis  → Profit
Legend  → Segment
```

This allows the numerical relationship to be separated by customer segment.

---

# 5. Important Scatter Plot Fields in Power BI

Depending on the Power BI version and visual configuration, scatter plots can use several data roles.

## X-axis

Place the first numerical variable here.

Example:

```text
Sales
```

The horizontal axis represents Sales.

---

## Y-axis

Place the second numerical variable here.

Example:

```text
Profit
```

The vertical axis represents Profit.

---

## Details

The **Details** field determines the level at which individual points are created.

For example:

```text
Details → Customer ID
```

can create a point for each customer.

Other possible fields include:

```text
Product ID
Order ID
Customer Name
Product Name
City
```

Use a field that provides the level of detail you want to analyze.

### Important

If you use a highly aggregated field, Power BI may display fewer points.

If you use a unique identifier such as `Customer ID`, the visual can display many individual observations.

---

# 6. Legend

The **Legend** field divides the points into groups.

For example:

```text
Legend → Segment
```

Possible values might include:

```text
Consumer
Corporate
Home Office
```

This makes it possible to visually distinguish different groups.

### Suitable Legend columns

Categorical columns are usually suitable:

```text
Category
Segment
Region
Country
Ship Mode
Sub-Category
```

Use a legend when comparing groups is important.

---

# 7. Size

The **Size** field controls the relative size of the bubbles/points when bubble sizing is available in the scatter visual.

Example:

```text
X-axis → Sales
Y-axis → Profit
Size → Quantity
```

This can communicate a third numerical variable.

For example:

- X position = Sales
- Y position = Profit
- Bubble size = Quantity

This allows three numerical dimensions to be viewed in one visual.

---

# 8. Play Axis

The **Play Axis** can be used when you want to observe how the scatter plot changes over time.

A suitable field could be:

```text
Order Date
```

For example:

```text
X-axis → Sales
Y-axis → Profit
Play Axis → Order Date
```

The visual can then show changes across different time periods.

Use this only when time-based movement is meaningful for the analysis.

---

# 9. Example Using the Superstore Dataset

A suitable configuration is:

| Power BI Field | Column |
|---|---|
| X-axis | Sales |
| Y-axis | Profit |
| Details | Customer ID / Product ID |
| Legend | Segment |
| Size | Quantity |
| Play Axis | Order Date |

The exact fields you use depend on the question you want the dashboard to answer.

---

# 10. How to Create a Scatter Plot in Power BI

### Step 1 — Load the Dataset

Open Power BI Desktop.

Go to:

```text
Home → Get Data
```

Choose the appropriate data source.

Examples:

- Excel
- CSV
- SQL Server
- Web
- Text/CSV
- Other supported sources

---

### Step 2 — Select Scatter Chart

In the **Visualizations** pane:

1. Select the **Scatter chart** icon.
2. A blank scatter visual will appear on the report canvas.

---

### Step 3 — Add X-axis

Drag:

```text
Sales
```

to the **X-axis**.

---

### Step 4 — Add Y-axis

Drag:

```text
Profit
```

to the **Y-axis**.

---

### Step 5 — Add Details

If individual observations are required, add a field such as:

```text
Customer ID
```

to the appropriate detail field.

---

### Step 6 — Add Legend

To compare groups, add:

```text
Segment
```

to **Legend**.

---

### Step 7 — Add Size

If you want bubble size to represent another metric:

```text
Quantity
```

can be used.

---

### Step 8 — Check Aggregation

Power BI may automatically aggregate numerical fields.

For example:

```text
Sum of Sales
Sum of Profit
```

This may be appropriate for an aggregated analysis.

If you need individual observations, use an appropriate **Details** field to control the granularity.

---

# 11. Understanding the Scatter Plot

In the provided visual:

```text
X-axis = Sales
Y-axis = Profit
```

### X-axis

Moving from left to right represents increasing Sales.

### Y-axis

Moving upward represents increasing Profit.

### Each point

Each point represents an observation at a particular Sales and Profit combination.

### Point distribution

The distribution of points can help identify:

- Concentrated areas
- High-sales observations
- High-profit observations
- Negative-profit observations
- Potential outliers
- General relationship between Sales and Profit

---

# 12. Positive and Negative Relationships

A scatter plot can help visually inspect the relationship between variables.

## Positive relationship

If points generally move upward from left to right:

```text
Sales ↑
Profit ↑
```

This suggests that higher Sales values are generally associated with higher Profit values in the displayed data.

## Negative relationship

If points generally move downward from left to right:

```text
Sales ↑
Profit ↓
```

This suggests an inverse pattern in the displayed data.

## Weak relationship

If points are widely scattered without a clear direction, the relationship may be weak or difficult to identify visually.

> A visual pattern should not automatically be treated as proof of causation. Additional statistical analysis may be required.

---

# 13. Outliers

One of the major advantages of a scatter plot is identifying **outliers**.

An outlier is a point that is noticeably separated from the main concentration of observations.

For example, a point with:

```text
Very high Sales
Very low Profit
```

may deserve further investigation.

Possible reasons could include:

- Large discounts
- High costs
- Unusual transactions
- Data-entry problems
- Special orders
- Exceptional business conditions

Power BI allows you to select a point and interact with other visuals on the report.

---

# 14. Formatting the Scatter Plot

Select the scatter visual and open:

```text
Format visual
```

You can customize several properties.

---

## 14.1 Title

Go to:

```text
Format visual → General / Visual → Title
```

Use a meaningful title.

Example:

```text
Sales V/S Profit
```

Better titles can communicate the purpose of the visual clearly.

---

## 14.2 X-axis Formatting

Open:

```text
X-axis
```

You can configure:

- Title
- Font
- Font size
- Text color
- Display units
- Decimal places
- Start value
- End value
- Gridlines
- Label density

For Sales, appropriate display units may include:

```text
None
Thousands
Millions
```

depending on the data range.

---

## 14.3 Y-axis Formatting

Open:

```text
Y-axis
```

You can modify:

- Axis title
- Font size
- Display units
- Decimal places
- Start
- End
- Gridlines
- Label density

For Profit, select a display format that makes the values easy to understand.

---

# 15. Data Labels

Data labels can display values directly on the visual when supported by the selected scatter configuration.

They can help when the user needs to identify individual values.

However, if there are hundreds or thousands of points, displaying every label can make the visual difficult to read.

Use labels selectively.

---

# 16. Markers / Bubbles

The appearance of the points can be adjusted depending on the Power BI version and selected visual options.

You may be able to control:

- Marker size
- Transparency
- Bubble size
- Outline
- Data colors

When there are many points, smaller and partially transparent markers can make overlapping observations easier to interpret.

---

# 17. Data Colors

Go to the formatting options for the visual and configure **Data colors** when available.

If a Legend is used, Power BI can assign different colors to categories.

For example:

```text
Consumer
Corporate
Home Office
```

Each category can be visually distinguished.

Keep the color scheme consistent across your report.

---

# 18. Legend Formatting

When a Legend is enabled, you can modify:

- Position
- Font
- Font size
- Title
- Text properties

Common positions include:

```text
Top
Bottom
Left
Right
```

Choose a position that does not cover the main data points.

---

# 19. Gridlines

Gridlines help users estimate values from the axes.

You can configure:

```text
X-axis → Gridlines
Y-axis → Gridlines
```

Depending on the visual, you can adjust:

- Visibility
- Color
- Transparency
- Line width

Avoid excessive gridlines because they can make the chart visually crowded.

---

# 20. Tooltips

Tooltips appear when the user moves the mouse over a data point.

Useful tooltip fields include:

```text
Sales
Profit
Quantity
Customer Name
Product Name
Category
Segment
Region
```

Tooltips are especially useful for scatter plots because many points may be close together.

---

# 21. Filters

Filters can be used to focus the scatter plot on a particular subset of data.

Examples:

```text
Region = West
Segment = Consumer
Category = Technology
Year = 2017
```

Filters can be applied at different levels:

### Visual-level filter

Affects only the selected scatter plot.

### Page-level filter

Affects all visuals on the current page.

### Report-level filter

Can affect visuals throughout the report.

---

# 22. Slicers

A slicer provides an interactive filtering control for report users.

Useful slicer fields include:

```text
Region
Category
Segment
Year
Ship Mode
```

For example:

```text
Select Region → West
```

The scatter plot can then update to display the selected data.

---

# 23. Interactions with Other Visuals

Power BI visuals can interact with each other.

For example, selecting a segment in another visual may:

- Filter the scatter plot
- Highlight related points
- Change the displayed data

You can control these interactions using:

```text
Format → Edit interactions
```

This is useful when building interactive dashboards.

---

# 24. Zooming and Navigation

Scatter plots can contain many data points.

Depending on the visual configuration and Power BI version, users can use available zoom or axis controls to inspect a specific range.

Zooming is particularly useful when:

- Points overlap
- There are extreme values
- A small cluster needs investigation
- The dataset contains many observations

Use zoom-related controls only when they improve readability.

---

# 25. Analytics Options

The **Analytics** pane can provide additional analytical features depending on the visual and Power BI version.

Possible analytical features may include:

- Trend line
- X-axis constant line
- Y-axis constant line
- Average line
- Median line
- Other analytical/reference elements

### Example

A trend line can help communicate the general direction of the relationship between Sales and Profit.

These features should be used when they answer a meaningful analytical question rather than simply adding decoration.

---

# 26. Trend Line

A trend line can be useful when you want to examine the overall relationship between two numerical variables.

For example:

```text
Sales → Profit
```

A trend line can help users understand whether the overall relationship appears positive or negative.

Remember that a trend line represents a statistical relationship in the displayed data; it does not by itself establish causation.

---

# 27. Reference Lines

Reference lines can be used to identify important thresholds.

Examples:

```text
Average Sales
Average Profit
Target Profit
Minimum Sales
Maximum Sales
```

These can make the scatter plot easier to interpret when the business has defined targets or benchmarks.

---

# 28. Sorting

Scatter plots are primarily interpreted through point positions rather than category order.

However, sorting can still matter when another field, grouping, or supporting visual is involved.

When sorting options are available:

1. Select the visual.
2. Open the visual's **More options (...)** menu.
3. Choose the appropriate sorting field.
4. Select ascending or descending order.

---

# 29. Aggregation

Power BI automatically applies aggregation to numerical fields in many situations.

Common aggregations include:

```text
Sum
Average
Minimum
Maximum
Count
Distinct count
```

For example:

```text
Sum of Sales
Sum of Profit
```

may be used in the scatter plot.

Choose the aggregation based on the analytical question.

---

# 30. Measures vs Columns

Both columns and DAX measures can be used for numerical analysis.

### Column

Example:

```text
Sales
Profit
Quantity
```

### Measure

Example:

```DAX
Total Sales = SUM(Sheet1[Sales])
```

```DAX
Total Profit = SUM(Sheet1[Profit])
```

Measures are useful when you need controlled calculations that respond dynamically to filters.

---

# 31. Example DAX Measures

### Total Sales

```DAX
Total Sales =
SUM(Sheet1[Sales])
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
    SUM(Sheet1[Profit]),
    SUM(Sheet1[Sales]),
    0
)
```

These measures can be used in scatter plot analysis where appropriate.

---

# 32. Scatter Plot with Business Segments

A useful business configuration is:

```text
X-axis → Sales
Y-axis → Profit
Legend → Segment
Details → Customer ID
Size → Quantity
```

This can help compare the Sales-Profit relationship across:

```text
Consumer
Corporate
Home Office
```

---

# 33. Suitable Business Questions

A scatter plot can help answer questions such as:

1. Is higher Sales generally associated with higher Profit?
2. Which observations have high Sales but low Profit?
3. Are there unusual high-profit transactions?
4. Are there negative-profit observations?
5. How does the relationship differ between customer segments?
6. Are there visible clusters?
7. Are there potential outliers?
8. How does Quantity relate to Sales and Profit?

---

# 34. Common Mistakes to Avoid

### ❌ Using only categorical fields

A scatter plot requires meaningful numerical X and Y values.

### ❌ Using too many points without a useful level of detail

Thousands of overlapping points can make the visual difficult to interpret.

### ❌ Using unnecessary colors

Too many categories in the Legend can make the chart confusing.

### ❌ Adding too many labels

Labels can overlap when there are many observations.

### ❌ Ignoring outliers

Extreme values can strongly affect the visual interpretation.

### ❌ Using inappropriate aggregation

Always check whether Power BI is using:

```text
Sum
Average
Count
Distinct count
```

as intended.

### ❌ Over-formatting

Avoid excessive colors, borders, gridlines, and decorative elements.

---

# 35. Best Practices

✅ Use two meaningful numerical variables.

✅ Give the visual a clear title.

✅ Use a categorical Legend when group comparison is required.

✅ Use Details when individual observations are important.

✅ Use Size only when a third numerical dimension provides useful information.

✅ Use Tooltips to provide additional information without overcrowding the chart.

✅ Use filters and slicers for interactive analysis.

✅ Format large numbers using appropriate display units.

✅ Investigate unusual outliers.

✅ Keep the visual simple and readable.

---

# 36. Quick Reference

| Requirement | Recommended Field Type |
|---|---|
| X-axis | Numerical |
| Y-axis | Numerical |
| Details | Identifier / categorical |
| Legend | Categorical |
| Size | Numerical |
| Play Axis | Date/Time |
| Tooltip | Numerical or categorical |
| Filters | Categorical / date / numerical |

---

# 37. Example Configuration Used in This Project

The provided Power BI visual uses:

```text
Chart Type → Scatter Plot

Title → Sales V/S Profit

X-axis → Sales

Y-axis → Profit
```

The chart is designed to examine the relationship and distribution between **Sales** and **Profit**.

---

# 38. Final Checklist

Before considering a scatter plot complete, verify:

- [ ] Scatter chart selected
- [ ] Numerical field added to X-axis
- [ ] Numerical field added to Y-axis
- [ ] Appropriate aggregation selected
- [ ] Details configured when individual points are required
- [ ] Legend added only when group comparison is useful
- [ ] Size used only when a third numerical variable is meaningful
- [ ] Tooltip information configured
- [ ] X-axis formatted
- [ ] Y-axis formatted
- [ ] Title added
- [ ] Gridlines checked
- [ ] Data colors checked
- [ ] Filters tested
- [ ] Slicers tested if used
- [ ] Outliers reviewed
- [ ] Visual remains readable

---

## 📁 Project Structure

```text
Scatter-Plot/
│
├── README.md
└── scatter_plot.png
```

---

## 📌 Key Takeaway

A **Scatter Plot in Power BI** is mainly used to study the relationship between **two numerical variables**.

For the chart shown in this project:

```text
Sales → X-axis
Profit → Y-axis
```

The visual can be extended with categorical fields such as **Segment**, numerical fields such as **Quantity**, and additional information through **Tooltips, Filters, Slicers, and formatting options**.

It is particularly useful for identifying relationships, distributions, clusters, and potential outliers in business data.
