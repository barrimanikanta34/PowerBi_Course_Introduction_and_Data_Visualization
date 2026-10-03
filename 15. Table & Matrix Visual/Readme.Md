# Power BI Table & Matrix Visuals

This section explains how to create and customize **Table** and **Matrix** visuals in Microsoft Power BI.

- **Table** → Displays data in a simple row-and-column format.
- **Matrix** → Displays data in a cross-tabular format with rows, columns, hierarchies, subtotals, and grand totals.

---

# 📊 1. Table Visual

A Power BI **Table** visual is used to display detailed records in a simple tabular format.

It is useful when you want to show multiple fields for individual records or categories without creating a hierarchical structure.

## Example

The following table displays:

- Country
- Region
- City
- Profit
- Sales

![Power BI Table Visual](https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/15.%20Table%20%26%20Matrix%20Visual/images/image09.png)

---

## 1.1 When Should We Use a Table?

A Table visual is suitable when:

- You need to display detailed records.
- You want to compare multiple numerical values.
- Users need to read exact values.
- You want a simple list-like structure.
- You do not require row/column hierarchies.

### Common Examples

- Customer details
- Product details
- Sales transactions
- Employee information
- Order details
- Sales and profit by city
- Inventory information
- Financial transaction details

---

## 1.2 Suitable Data Types for a Table

| Data Type | Example | Suitable? |
|---|---|---|
| Text | City, Product Name | ✅ |
| Category | Segment, Category | ✅ |
| Geographic | Country, State, City | ✅ |
| Date | Order Date | ✅ |
| Numeric | Sales, Profit | ✅ |
| Decimal | Discount, Profit Margin | ✅ |
| Whole Number | Quantity | ✅ |
| Measures | Total Sales, Total Profit | ✅ |

A table can contain a combination of **categorical and numerical columns**.

---

## 1.3 Example Dataset

| Country | Region | City | Sales | Profit |
|---|---|---|---:|---:|
| United States | Central | Aberdeen | 25.50 | 6.63 |
| United States | Central | Abilene | 1.39 | -3.76 |
| United States | Central | Allen | 290.21 | -39.88 |
| United States | Central | Amarillo | 3773.06 | -387.97 |
| United States | Central | Ann Arbor | 889.27 | 228.92 |

This type of data is suitable for a Table visual.

---

## 1.4 How to Create a Table Visual

### Step 1: Load the Dataset

Open Power BI Desktop.

Go to:

**Home → Get Data**

Select the required data source.

### Step 2: Insert a Table

From the **Visualizations** pane:

1. Select the **Table** visual.
2. A blank table will appear on the report canvas.

### Step 3: Add Fields

Drag the required columns into the table.

For example:

```text
Country
Region
City
Profit
Sales
```

The table will display the selected fields row by row.

---

## 1.5 Aggregation in a Table

Numeric columns can be aggregated using:

- Sum
- Average
- Minimum
- Maximum
- Count
- Distinct Count

For example:

```text
Sales    → Sum
Profit   → Sum
Quantity → Sum
Discount → Average
```

The aggregation can be changed from the field dropdown in the visual.

---

## 1.6 Sorting

You can sort table data by:

- Country
- Region
- City
- Sales
- Profit
- Quantity

For example, to sort Sales from highest to lowest:

1. Select the Table.
2. Select the **Sales** column.
3. Choose descending sort.

---

## 1.7 Formatting a Table

Select the table and open:

**Format visual**

You can customize:

### Values

Change:

- Font size
- Font family
- Text color
- Background
- Alignment
- Decimal places

### Column Headers

You can change:

- Header font size
- Header color
- Header background
- Header alignment

### Grid

You can control:

- Grid lines
- Row padding
- Outline
- Horizontal lines
- Vertical lines

---

## 1.8 Conditional Formatting

Conditional formatting can make important values easier to identify.

You can apply:

- Background color
- Font color
- Data bars
- Icons
- Color scales

For example, Profit can be formatted so that positive and negative values are visually different.

---

## 1.9 Totals in a Table

A Table can display totals for numeric columns.

For example:

```text
Total Profit = 2,86,397.02
Total Sales  = 22,97,200.86
```

Totals are useful when the table contains aggregated numerical information.

---

## 1.10 Filters in a Table

You can filter the table using:

- Country
- Region
- City
- Category
- Segment
- Sales
- Profit
- Date

Filters can be applied using:

- Visual-level filters
- Page-level filters
- Report-level filters
- Slicers

---

## 1.11 Table Use Cases

Table visuals are commonly used for:

- Sales reports
- Customer reports
- Product reports
- Order reports
- Financial reports
- Employee reports
- Inventory reports
- Transaction reports
- Detailed business reports

---

# 📊 2. Matrix Visual

A Power BI **Matrix** visual is similar to a table, but it provides additional functionality such as:

- Row hierarchies
- Column hierarchies
- Subtotals
- Grand totals
- Expand/collapse
- Drill-down
- Cross-tab analysis

The Matrix is especially useful when you need to compare values across multiple categories.

## Example

The following Matrix compares:

- Country
- City
- Region
- Sales
- Profit

across different regions.

![Power BI Matrix Visual](https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/15.%20Table%20%26%20Matrix%20Visual/images/image10.png)

---

## 2.1 When Should We Use a Matrix?

Use a Matrix when you need:

- Hierarchical data
- Cross-tabular analysis
- Row grouping
- Column grouping
- Subtotals
- Grand totals
- Expand/collapse functionality
- Drill-down analysis
- Comparison across categories

---

## 2.2 Suitable Data Types for a Matrix

### Rows

Categorical or hierarchical fields:

```text
Country
Region
City
Category
Sub-Category
Product
```

### Columns

Categorical fields:

```text
Region
Segment
Category
Year
Quarter
Month
```

### Values

Numerical columns or measures:

```text
Sales
Profit
Quantity
Discount
Total Sales
Total Profit
```

---

## 2.3 Basic Matrix Structure

A Matrix contains three important areas:

```text
Rows
Columns
Values
```

For example:

```text
Rows:
Country
City

Columns:
Region

Values:
Sales
Profit
```

This creates a cross-tabular report.

---

## 2.4 How to Create a Matrix

### Step 1: Select Matrix

From the Visualizations pane:

**Select → Matrix**

### Step 2: Add Row Fields

Drag:

```text
Country
City
```

into:

```text
Rows
```

This creates a hierarchy:

```text
Country
   ↓
City
```

### Step 3: Add Column Fields

Drag:

```text
Region
```

into:

```text
Columns
```

### Step 4: Add Numerical Values

Drag:

```text
Sales
Profit
```

into:

```text
Values
```

The Matrix will now display Sales and Profit for each region and city.

---

## 2.5 Matrix Hierarchy

One of the biggest advantages of a Matrix is hierarchical data.

For example:

```text
Country
   └── Region
        └── City
             └── Customer
```

This allows users to move between different levels of detail.

---

## 2.6 Expand and Collapse

Matrix visuals allow users to expand and collapse hierarchical data.

For example:

```text
United States
   Central
      Chicago
      Austin
      Dallas
```

The user can expand or collapse the hierarchy to control how much information is displayed.

---

## 2.7 Drill Down

Drill-down allows users to move from a higher level to a lower level.

Example:

```text
Country
   ↓
Region
   ↓
City
```

For example:

```text
United States
      ↓
Central
      ↓
Chicago
```

This is useful when analyzing data from a general level to a detailed level.

---

## 2.8 Drill Up

Drill-up moves the analysis back to a higher level.

Example:

```text
City
 ↓
Region
 ↓
Country
```

If you are currently viewing cities, you can move back to the region or country level.

---

## 2.9 Subtotals

Matrix visuals can automatically calculate subtotals.

For example:

```text
Central
    Chicago        48,539.54
    Austin          6,057.98
    Dallas          9,xxx.xx
--------------------------------
Central Total      XX,XXX.XX
```

Subtotals make hierarchical reports easier to analyze.

---

## 2.10 Grand Total

A Matrix can display a Grand Total.

Example:

```text
Central       5,01,239.89
East          6,78,781.24
South         3,91,721.91
West          7,25,457.82
--------------------------------
Grand Total  22,97,200.86
```

Grand totals provide an overall summary of the selected data.

---

## 2.11 Conditional Formatting in a Matrix

Conditional formatting is very useful in Matrix visuals.

You can apply:

### Background Color

Highlight high and low values.

### Font Color

Change the color based on values.

### Data Bars

Display a horizontal bar representing the numerical value.

### Icons

Use icons to identify:

- High values
- Low values
- Positive values
- Negative values

---

## 2.12 Matrix Formatting

Select the Matrix and open:

**Format visual**

You can customize:

### Row Headers

Change:

- Font size
- Font color
- Background
- Alignment

### Column Headers

Change:

- Font size
- Font color
- Background
- Alignment

### Values

Change:

- Font size
- Font color
- Decimal places
- Alignment

### Grid

Control:

- Horizontal grid lines
- Vertical grid lines
- Outline
- Row padding

---

## 2.13 Column Width

Matrix columns can be resized to improve readability.

If a column contains long text such as:

```text
Customer Name
Product Name
City
```

increase the column width so that the information is clearly visible.

---

## 2.14 Word Wrap

Word wrap can be useful for long headers or text values.

For example:

```text
Total Sales
by Region
```

instead of forcing the complete text into a single line.

---

## 2.15 Sorting a Matrix

A Matrix can be sorted by:

- Country
- Region
- City
- Sales
- Profit
- Quantity

For example:

```text
Sort Sales → Descending
```

This can help organize the displayed records according to numerical values.

---

## 2.16 Filters and Slicers

Matrix visuals work well with slicers.

Example slicers:

```text
Year
Country
Region
Category
Segment
```

A user can select:

```text
Country = United States
```

and the Matrix will update based on the selection.

---

## 2.17 Tooltips

Tooltips display additional information when the user moves the mouse over a value.

For example:

```text
Sales: 5,847.77
Profit: 4,169.70
Region: Central
City: Arlington
```

Tooltips provide additional context without adding more columns to the Matrix.

---

# 3. Table vs Matrix

| Feature | Table | Matrix |
|---|---|---|
| Simple rows and columns | ✅ | ✅ |
| Detailed records | ✅ | ✅ |
| Row hierarchy | Limited | ✅ |
| Column hierarchy | ❌ | ✅ |
| Expand/Collapse | ❌ | ✅ |
| Drill Down | Limited | ✅ |
| Subtotals | Limited | ✅ |
| Grand Total | ✅ | ✅ |
| Cross-tab analysis | ❌ | ✅ |
| Conditional formatting | ✅ | ✅ |
| Data bars | ✅ | ✅ |
| Icons | ✅ | ✅ |
| Best for transaction details | ✅ | Sometimes |
| Best for hierarchical analysis | ❌ | ✅ |

---

# 4. Recommended Columns

For a sales dataset, the following columns are useful.

### Dimension / Categorical Columns

```text
Country
Region
State
City
Category
Sub-Category
Segment
Ship Mode
Product Name
Customer Name
```

### Numerical Columns

```text
Sales
Profit
Quantity
Discount
```

### Date Columns

```text
Order Date
Ship Date
```

---

# 5. Useful Power BI Features

Both Table and Matrix visuals can be combined with:

- Filters
- Slicers
- Tooltips
- Conditional formatting
- Sorting
- DAX measures
- Hierarchies
- Drill-down
- Expand/Collapse

---

# 6. Example DAX Measures

## Total Sales

```DAX
Total Sales =
SUM(Sheet1[Sales])
```

## Total Profit

```DAX
Total Profit =
SUM(Sheet1[Profit])
```

## Total Quantity

```DAX
Total Quantity =
SUM(Sheet1[Quantity])
```

## Average Sales

```DAX
Average Sales =
AVERAGE(Sheet1[Sales])
```

## Profit Margin

```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)
```

These measures can be added to both Table and Matrix visuals.

---

# 7. Business Applications

## Table Visual

Tables are commonly used for:

- Sales transaction reports
- Customer lists
- Product lists
- Order details
- Employee information
- Inventory reports
- Financial transactions
- Detailed operational reports

## Matrix Visual

Matrices are commonly used for:

- Sales by region
- Profit by category
- Revenue by year and region
- Sales by country and city
- Financial statements
- Budget vs actual analysis
- Department-wise performance
- Category and sub-category analysis
- Multi-level business reports

---

# 8. Best Practices

## For Tables

- Avoid adding too many unnecessary columns.
- Use meaningful column names.
- Format numerical values properly.
- Use appropriate decimal places.
- Apply conditional formatting when useful.
- Sort important numerical columns appropriately.
- Use filters for large datasets.

## For Matrices

- Use logical hierarchies.
- Keep the hierarchy easy to understand.
- Use subtotals when they provide useful information.
- Use conditional formatting for important metrics.
- Avoid excessive numbers of columns.
- Use expand/collapse for large hierarchies.
- Use slicers to make the report interactive.

---

# 9. Common Mistakes

### Mistake 1: Adding Too Many Columns

A Table containing too many columns can become difficult to read.

**Solution:** Keep only the fields required for analysis.

### Mistake 2: Using Text as Numerical Data

For example:

```text
Sales = "1000"
```

instead of a numeric value.

This can prevent correct aggregation.

**Solution:** Set Sales as a numeric data type.

### Mistake 3: Incorrect Aggregation

For example, using:

```text
Average Sales
```

when the analysis requires:

```text
Total Sales
```

Always select the aggregation appropriate for the business question.

### Mistake 4: Poor Hierarchy

A Matrix hierarchy should generally follow a logical structure.

For example:

```text
Country
   ↓
Region
      ↓
City
```

---

# 10. Quick Reference

| Requirement | Recommended Visual |
|---|---|
| Show detailed records | Table |
| Show simple rows and columns | Table |
| Compare multiple metrics | Table / Matrix |
| Show hierarchy | Matrix |
| Show row hierarchy | Matrix |
| Show column hierarchy | Matrix |
| Expand and collapse data | Matrix |
| Drill down through levels | Matrix |
| Display subtotals | Matrix |
| Cross-tab analysis | Matrix |
| Customer transaction details | Table |
| Regional performance hierarchy | Matrix |
| Sales by Country → Region → City | Matrix |

---

# 11. Summary

## Table

A **Table visual** is best when the goal is to display detailed information in a straightforward row-and-column structure.

It is especially useful for:

- Transaction data
- Customer information
- Product details
- Order details
- Sales and profit records

## Matrix

A **Matrix visual** is best when the goal is to analyze hierarchical and cross-tabulated information.

It is especially useful for:

- Country → Region → City
- Category → Sub-Category
- Year → Quarter → Month
- Sales and Profit comparisons
- Subtotals and Grand Totals
- Drill-down analysis

Both visuals become more powerful when combined with:

- Filters
- Slicers
- Tooltips
- Conditional formatting
- Sorting
- DAX measures
- Hierarchies
- Drill-down
- Expand/Collapse

---

# 📁 Project Structure

Recommended folder structure:

```text
PowerBI-Table-Matrix/
│
├── README.md
│
└── Images/
    ├── table_visual.png
    └── matrix_visual.png
```

---

# 🖼️ Visuals Used in This Project

### Table Visual

![Power BI Table Visual](images\image09.png)

### Matrix Visual

![Power BI Matrix Visual](images\image10.png)

---

# 🛠️ Tools Used

- Microsoft Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Power BI Table Visual
- Power BI Matrix Visual

---

