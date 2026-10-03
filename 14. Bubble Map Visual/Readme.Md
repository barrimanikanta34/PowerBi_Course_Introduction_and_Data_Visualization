# Power BI Map Chart – Sales by City

![Sales by City Map](https://github.com/barrimanikanta34/PowerBi_Course_Introduction_and_Data_Visualization/blob/main/14.%20Bubble%20Map%20Visual/images/image3.png)

## 📌 Overview

This section demonstrates how to create and format a **Map Chart in Microsoft Power BI** to visualize a measure geographically.

The example shown above is a **bubble map** titled **Sales by City**. It uses:

- **City** → geographic location
- **Sales** → numeric measure represented by the bubbles
- **Map background** → geographic context for the locations

The bubbles help users understand where sales activity is concentrated geographically.

---

## 🎯 What Is a Map Chart?

A Map Chart displays data according to geographic information such as:

- Country
- State / Province
- City
- Postal Code
- Address
- Latitude
- Longitude
- Region

A numeric measure such as Sales, Profit, Revenue, Quantity, Orders, or Population can then be analyzed for each location.

A map is most useful when **location is an important part of the analysis**.

---

# 📊 What Kind of Data Is Suitable?

A map generally needs two important types of information:

### 1. Geographic / Categorical Data

These fields tell Power BI **where** something is located.

Examples:

- City
- State
- Country
- Province
- Region
- Postal Code
- Address

### 2. Numerical Data

These fields represent the value associated with the location.

Examples:

- Sales
- Revenue
- Profit
- Quantity
- Number of Orders
- Customer Count
- Population
- Cost

### Example

| City | Sales |
|---|---:|
| New York | 250000 |
| Chicago | 180000 |
| Seattle | 125000 |
| Boston | 95000 |

The map can represent higher Sales using larger bubbles.

---

# 🧩 Suitable Data Types

| Field | Typical Data Type | Purpose |
|---|---|---|
| City | Text / Geographic | Location |
| State | Text / Geographic | Location context |
| Country | Text / Geographic | Location context |
| Postal Code | Text/Number / Geographic | Location |
| Latitude | Decimal Number | Exact position |
| Longitude | Decimal Number | Exact position |
| Sales | Decimal/Currency | Bubble/value measure |
| Profit | Decimal/Currency | Bubble/value measure |
| Quantity | Whole Number | Bubble/value measure |
| Order ID | Text | Can be counted/distinct-counted |

---

# 🗺️ Geographic Categories in Power BI

Power BI can assign geographic categories to columns.

Common categories include:

```text
Country       → Country/Region
State         → State or Province
City          → City
Postal Code   → Postal Code
Latitude      → Latitude
Longitude     → Longitude
```

To assign a category:

**Select column → Column tools → Data category**

Correct geographic categorization helps Power BI interpret the location correctly.

---

# 🛠️ How to Create the Map Chart

## Step 1 – Load the Dataset

Go to:

**Home → Get Data**

You can import data from sources such as:

- Excel
- CSV
- SQL Server
- MySQL
- PostgreSQL
- Web
- Other supported sources

---

## Step 2 – Check the Geographic Field

In the **Data** pane, locate the location field.

For this example:

```text
City
```

Select the column and verify its **Data category** is appropriate.

---

## Step 3 – Insert a Map Visual

From the **Visualizations** pane, select the required map visual available in your Power BI version.

Depending on the version and enabled visuals, you may see map options such as:

- Map
- Azure Maps
- Filled Map
- Other map visuals

The screenshot represents a **bubble-style map**.

---

## Step 4 – Add the Location

Drag:

```text
City
```

into the map's location field.

Power BI will attempt to place the cities on the map.

---

## Step 5 – Add the Numeric Measure

Add:

```text
Sales
```

to the appropriate numeric/value field of the map.

The Sales value can control the size of the bubbles.

Conceptually:

```text
City + Sales
     ↓
Bubble Map
```

---

# 🔵 Understanding Bubble Size

Bubble size communicates the magnitude of a numeric measure.

For example:

```text
Higher Sales → Larger bubble
Lower Sales  → Smaller bubble
```

Example:

```text
City A → ₹500,000 → Large bubble
City B → ₹250,000 → Medium bubble
City C → ₹50,000  → Small bubble
```

This makes geographic differences easier to identify visually.

---

# 📐 Aggregation

Power BI may automatically aggregate numeric fields when they are added to a visual.

Common aggregations include:

- Sum
- Average
- Minimum
- Maximum
- Count
- Distinct count

For Sales analysis, a common choice is:

```text
Sales → Sum
```

This calculates total Sales for each geographic location.

---

# 🗺️ Map Settings

Open **Format visual** after selecting the map.

Depending on the map visual, **Map settings** can control options such as:

- Map style
- Zoom behavior
- Map controls
- Auto zoom
- Geographic display
- Map position

Use these settings to make the map easier to navigate and understand.

---

# 🔵 Bubbles

The **Bubbles** section controls the appearance of location markers.

Depending on the visual and Power BI version, you may be able to adjust:

- Bubble size
- Transparency
- Color
- Minimum/maximum size
- Marker appearance

Avoid making bubbles so large that nearby locations become difficult to distinguish.

---

# 🏷️ Category Labels

Category labels can display geographic names directly on the map.

Examples:

```text
New York
Chicago
Seattle
Boston
```

Labels are useful when the number of locations is small.

For hundreds of locations, showing every label can make the map crowded. In that situation, use tooltips, filters, or aggregation instead.

---

# 🎨 Legend

A legend becomes useful when another categorical field is used to divide locations into groups.

Examples:

- Segment
- Region
- Category
- Product Type
- Customer Type

For example:

```text
Consumer
Corporate
Home Office
```

In the screenshot, the legend is **Off**, because the main analysis is based on City and Sales.

---

# 🔥 Heat Map

A heat map can be useful when many geographic points overlap.

It helps show areas with greater concentration rather than requiring users to inspect every individual bubble.

Use a heat map when:

- There are many locations
- Bubbles overlap heavily
- Geographic concentration is more important than individual locations
- You want to identify high-density areas

---

# 🔍 Zoom Controls

Map visuals normally provide navigation controls such as:

- Zoom In
- Zoom Out
- Pan

The screenshot shows **+** and **−** controls.

### Zoom In

Use it to inspect a smaller geographic area.

### Zoom Out

Use it to see a larger geographic region.

Zooming is especially useful when many locations are close together.

---

# 🖱️ Tooltips

Hover over a bubble to display additional information.

Useful tooltip fields include:

```text
City
Sales
Profit
Quantity
Orders
Customer Count
```

Tooltips allow you to provide additional details without filling the map with labels.

---

# 🎛️ Filters

Filters can restrict which locations appear on the map.

Examples:

```text
Country = United States
Segment = Consumer
Category = Technology
Year = 2025
```

Filters are useful when the dataset contains many locations.

---

# 🎚️ Slicers

Slicers allow report users to interactively filter the map.

Useful slicers include:

- Year
- Country
- Region
- Segment
- Category
- Ship Mode
- Product Category

Example:

```text
Year
[2025 ▼]
```

The map updates based on the selected value.

---

# 📈 Useful Measures for Map Charts

## Total Sales

```DAX
Total Sales = SUM(Sales[Sales])
```

## Total Profit

```DAX
Total Profit = SUM(Sales[Profit])
```

## Total Quantity

```DAX
Total Quantity = SUM(Sales[Quantity])
```

## Number of Orders

```DAX
Total Orders = DISTINCTCOUNT(Sales[Order ID])
```

## Customer Count

```DAX
Customer Count = DISTINCTCOUNT(Sales[Customer ID])
```

These measures can be analyzed geographically.

---

# 📍 Using Latitude and Longitude

If the dataset contains exact coordinates, latitude and longitude can provide more precise geographic positioning.

Example:

| City | Latitude | Longitude |
|---|---:|---:|
| Delhi | 28.6139 | 77.2090 |
| Mumbai | 19.0760 | 72.8777 |
| Chennai | 13.0827 | 80.2707 |

Use:

```text
Latitude  → Latitude
Longitude → Longitude
```

This is particularly useful when city names are ambiguous or when the dataset represents exact locations.

---

# 🧭 Why Latitude and Longitude Can Be Useful

City names can sometimes be ambiguous.

For example, the same city name can exist in different states or countries.

Adding:

```text
Country + State + City
```

can provide more context.

For highly precise location analysis, use:

```text
Latitude + Longitude
```

when those fields are available and accurate.

---

# 🏢 Business Use Cases

## Sales Analysis

```text
Sales by City
Sales by State
Sales by Country
```

Useful for understanding geographic sales distribution.

## Profit Analysis

```text
Profit by City
Profit by Region
Profit by State
```

Useful for geographic profitability analysis.

## Customer Analysis

```text
Customers by City
Customer Count by Region
```

Useful for understanding customer concentration.

## Logistics

```text
Orders by Delivery City
Shipments by Region
Delivery Volume by State
```

Useful for logistics and distribution analysis.

## Marketing

```text
Leads by City
Campaign Responses by Region
Customers by Country
```

Useful for geographic marketing analysis.

## Retail

```text
Store Sales by Location
Store Profit by City
Orders by Store Region
```

Useful for comparing store performance geographically.

---

# 📋 Example Dataset

A dataset suitable for a map could look like this:

| City | State | Country | Sales | Profit | Quantity |
|---|---|---|---:|---:|---:|
| New York | New York | USA | 250000 | 45000 | 1200 |
| Chicago | Illinois | USA | 180000 | 32000 | 850 |
| Seattle | Washington | USA | 125000 | 22000 | 600 |
| Boston | Massachusetts | USA | 95000 | 18000 | 450 |

Possible configuration:

```text
Location → City
Value/Size → Sales
Tooltip → Profit, Quantity
```

---

# ⚠️ Common Problems and Solutions

## City is not recognized

**Possible cause:** Power BI cannot determine the geographic location.

**Solution:** Set the correct Data Category, for example:

```text
City → City
```

Also provide State and Country where appropriate.

## Wrong location appears

**Possible cause:** The location name is ambiguous.

**Solution:** Add:

```text
Country
State
City
```

or use:

```text
Latitude
Longitude
```

## Too many bubbles

**Solutions:**

- Apply filters
- Use slicers
- Aggregate by State/Region/Country
- Use a heat map where appropriate
- Focus on a smaller geographic area

## Map is difficult to read

**Solutions:**

- Adjust bubble size
- Adjust transparency
- Use appropriate zoom
- Reduce unnecessary labels
- Apply filters
- Put extra information in tooltips

---

# 🎯 Best Practices

1. Use a meaningful geographic field.
2. Set the correct Data Category for geographic columns.
3. Use a numerical measure such as Sales, Profit, Quantity, or Orders.
4. Add Country/State information when city names can be ambiguous.
5. Use latitude and longitude when precise coordinates are available.
6. Avoid showing too many labels on a crowded map.
7. Use tooltips for additional information.
8. Use filters and slicers for interactive analysis.
9. Choose bubble sizes that are easy to compare.
10. Use a heat map when points overlap heavily.
11. Keep the map focused on a clear analytical question.
12. Do not use a map simply because geographic data exists; use it when geography adds analytical value.

---

# ❌ When NOT to Use a Map Chart

A map is not always the best visual.

Avoid using a map when:

- Location is irrelevant to the question.
- You only need to compare categories.
- Exact numerical comparison is more important than geographic distribution.
- A bar or column chart would communicate the comparison more clearly.

For example, comparing:

```text
Technology vs Furniture vs Office Supplies
```

is generally better represented using a bar or column chart than a map.

---

# 🆚 Map vs Other Power BI Charts

| Requirement | Suitable Visual |
|---|---|
| Sales by City | Map |
| Sales by Country | Map |
| Profit by Region | Map |
| Compare Product Categories | Bar / Column Chart |
| Sales over Time | Line Chart |
| Part-to-whole relationship | Pie / Donut Chart |
| Relationship between two numeric variables | Scatter Plot |
| Trend + comparison | Combo Chart |
| Geographic concentration | Map / Heat Map |

---

# 📚 Quick Reference

| Component | Example |
|---|---|
| Visual | Map |
| Location | City |
| Numeric measure | Sales |
| Bubble size | Sales |
| Tooltip | Profit, Quantity |
| Legend | Segment / Region |
| Geographic category | City |
| Precision fields | Latitude, Longitude |
| Filters | Country, Region, Year |
| Slicers | Year, Category, Segment |
| Navigation | Zoom In / Zoom Out |
| Alternative for many points | Heat Map |

---

# 🚀 Final Summary

The **Sales by City** map demonstrates how Power BI can combine geographic and numerical data to create an interactive geographic visualization.

The core concept is:

```text
Geographic Field + Numeric Measure
            ↓
        Map Chart
            ↓
 Geographic Distribution
```

For this example:

```text
City + Sales
      ↓
Sales by City Map
```

The same approach can be extended to:

```text
State + Sales
Country + Revenue
City + Profit
Region + Quantity
Store Location + Orders
```

A good map should help answer questions such as:

- Where are sales concentrated?
- Which cities have higher sales?
- Which regions generate more profit?
- Where are customers located?
- Where are orders concentrated?
- Which geographic areas require further investigation?

The key principle is to use a map when **geographic location contributes meaningful analytical information**.
