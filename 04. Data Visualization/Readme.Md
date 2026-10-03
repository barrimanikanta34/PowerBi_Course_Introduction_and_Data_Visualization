# Creating and Formatting a Stacked Bar Chart in Power BI

## Overview

A Stacked Bar Chart is a useful visualization in Power BI for comparing values across different categories while also showing the contribution of sub-categories.

In this tutorial, we will learn how to:

- Import data into Power BI Desktop
- Create a Stacked Bar Chart
- Add fields to the chart
- Open and use the Format visual pane
- Change data colors
- Format the X-axis
- Format the Y-axis
- Add and format data labels
- Format the legend
- Add and format the chart title
- Change the chart background
- Add and format a border
- Configure gridlines
- Review and improve the overall appearance of the chart

---

# 1. Prerequisites

Before creating the chart, make sure that:

1. Power BI Desktop is installed on your computer.
2. You have a dataset available in a supported format such as Excel or CSV.
3. The dataset contains at least one categorical column and one numerical column.

---

# 2. Inserting Data into Power BI

Before creating a chart, the required dataset must first be imported into Power BI Desktop.

## Step 1: Open Power BI Desktop

1. Open **Power BI Desktop**.
2. Wait for the Power BI Desktop home screen to load.

## Step 2: Select Get Data

1. Go to the **Home** tab.
2. Click **Get data**.
3. Select the required data source.

For example:

- Excel workbook
- Text/CSV
- SQL Server
- Other supported sources

## Step 3: Select the Dataset

1. Browse to the location of your dataset.
2. Select the required file.
3. Select the required sheet or table.
4. Click **Load**.

## Step 4: Verify the Data

After loading the data:

1. Look at the **Data** pane.
2. Locate the imported table.
3. Check whether the required columns are available.
4. Verify that the numerical columns contain the correct data.

### Screenshot 1 – Inserting Data

![Importing Data into Power BI](Images\image.png)

---

# 3. Creating a Stacked Bar Chart

After importing the data, the next step is to create the Stacked Bar Chart.

## Step 1: Select the Stacked Bar Chart

1. Go to the **Visualizations** pane.
2. Locate the **Stacked Bar Chart** visual.
3. Click the Stacked Bar Chart icon.

A blank chart will appear on the report canvas.

## Step 2: Add Fields to the Chart

Select the required fields from the Data pane and place them into the appropriate areas of the visual.

A typical configuration can be:

```text
Y-axis / Category  → Category
X-axis / Values    → Sales
Legend             → Region
```

The exact field names depend on the dataset being used.

## Step 3: Understand the Chart

- **Category:** Determines the items displayed along the vertical axis.
- **Values:** Determines the length of the bars.
- **Legend:** Divides each bar into different colored sections.

### Screenshot 2 – Stacked Bar Chart

![Importing Data into Power BI](Images\image02.png)

---

# 4. Opening the Format Visual Pane

After creating the chart, we can customize its appearance.

## Steps

1. Select the Stacked Bar Chart.
2. Go to the **Visualizations** pane.
3. Select **Format visual**.
4. The formatting options will appear.

Common formatting sections include:

- Visual
- X-axis
- Y-axis
- Legend
- Data labels
- Title
- Background
- Border
- Gridlines
- Other visual-specific settings

### Screenshot 3 – Format Visual Pane

![Power BI Format Visual Pane](Images\image03.png)

---

# 5. Changing the Data Colors

Data colors determine the colors used for the different sections of the Stacked Bar Chart.

## Steps

1. Select the Stacked Bar Chart.
2. Open **Format visual**.
3. Find **Data colors**.
4. Select the required data series.
5. Click the color option.
6. Choose the required color.

### Simple Process

```text
Select Chart
     ↓
Format visual
     ↓
Data colors
     ↓
Select Data Series
     ↓
Choose Color
```

---

# 6. Formatting the X-axis

In a horizontal Stacked Bar Chart, the X-axis generally represents the numerical values.

## Steps

1. Select the Stacked Bar Chart.
2. Open **Format visual**.
3. Select **X-axis**.
4. Review the available formatting options.
5. Change the required settings.

Possible options include:

- Axis title
- Title text
- Text size
- Text color
- Display units
- Decimal places
- Gridlines
- Range settings

## Changing X-axis Text Color

1. Go to **Format visual**.
2. Select **X-axis**.
3. Locate the text or value formatting option.
4. Select the required color.
5. Check the result on the chart.

## Changing X-axis Text Size

1. Open **Format visual**.
2. Select **X-axis**.
3. Locate the text-size option.
4. Increase or decrease the size.
5. Check whether the labels are easy to read.

---

# 7. Formatting the Y-axis

The Y-axis generally displays the categories of a horizontal Stacked Bar Chart.

## Steps

1. Select the chart.
2. Open **Format visual**.
3. Select **Y-axis**.
4. Review the available options.
5. Change the required settings.

Possible options include:

- Text color
- Text size
- Axis title
- Title text
- Category display settings

## Changing Y-axis Text Color

1. Select the chart.
2. Open **Format visual**.
3. Select **Y-axis**.
4. Locate the text formatting option.
5. Select the required color.
6. Check the chart.

## Changing Y-axis Text Size

1. Open **Format visual**.
2. Select **Y-axis**.
3. Find the text-size option.
4. Select the required size.
5. Check the chart for readability.

---

# 8. Adding a Chart Title

A chart title helps users immediately understand what the visualization represents.

## Steps

1. Select the Stacked Bar Chart.
2. Open **Format visual**.
3. Find **Title**.
4. Turn the title **On**.
5. Enter the required title.

Example:

```text
Sales by Category and Region
```

## Formatting the Chart Title

### Change Title Text

1. Open **Format visual**.
2. Select **Title**.
3. Find the title text option.
4. Enter the required title.

### Change Title Size

1. Select **Title**.
2. Find the text-size option.
3. Increase or decrease the size.

### Change Title Color

1. Select **Title**.
2. Locate the color option.
3. Select the required color.

### Change Title Alignment

1. Open **Title**.
2. Find the alignment option.
3. Select the required alignment.

Common options may include:

- Left
- Center
- Right

---

# 9. Adding Data Labels

Data labels display numerical values directly on the chart.

## Steps

1. Select the Stacked Bar Chart.
2. Open **Format visual**.
3. Select **Data labels**.
4. Turn **Data labels** On.

The numerical values will now appear on the bars.

## Formatting Data Labels

Depending on the visual and Power BI version, you may be able to modify:

- Text size
- Text color
- Display units
- Decimal places
- Position
- Value display

### Steps

1. Open **Format visual**.
2. Select **Data labels**.
3. Change the required setting.
4. Check the chart.
5. Adjust the settings until the values are clearly readable.

---

# 10. Formatting the Legend

The Legend identifies the different sections of the stacked bars.

## Steps

1. Select the chart.
2. Open **Format visual**.
3. Select **Legend**.
4. Turn the Legend On or Off as required.

## Changing Legend Position

1. Open **Format visual**.
2. Select **Legend**.
3. Find the **Position** option.
4. Select the required position.

Possible positions may include:

- Top
- Bottom
- Left
- Right

## Formatting Legend Text

1. Open **Format visual**.
2. Select **Legend**.
3. Locate the text-size option.
4. Change the text size.
5. Locate the text-color option if available.
6. Select the required color.

---

# 11. Changing the Chart Background

A background can help separate the visualization from the report canvas.

## Steps

1. Select the Stacked Bar Chart.
2. Open **Format visual**.
3. Find **Background**.
4. Turn the background **On**.
5. Select the required color.
6. Adjust transparency if available.

### Simple Process

```text
Select Chart
     ↓
Format visual
     ↓
Background
     ↓
On
     ↓
Select Color
     ↓
Adjust Transparency
```

---

# 12. Adding a Border

A border can help separate the chart from other elements on the report page.

## Steps

1. Select the chart.
2. Open **Format visual**.
3. Find **Border**.
4. Turn the border **On**.
5. Configure the available options.

Depending on the Power BI version, you may be able to adjust:

- Border color
- Border width
- Rounded corners
- Transparency

---

# 13. Formatting Gridlines

Gridlines can help users understand the numerical scale of the chart.

## Steps

1. Select the chart.
2. Open **Format visual**.
3. Select the appropriate axis.
4. Find **Gridlines**.
5. Turn gridlines On or Off.
6. Adjust the available formatting options.

Gridlines should be used carefully because too many visual elements can make a chart difficult to read.

---

# 14. Formatting the Visual

The visual-level formatting section controls settings specific to the selected chart.

Depending on the selected visual and Power BI version, visual-specific options may include:

- Bar settings
- Spacing
- Inner padding
- Shapes
- Visual-specific properties
- Other chart settings

## Steps

1. Select the Stacked Bar Chart.
2. Open **Format visual**.
3. Open the relevant visual formatting section.
4. Identify the required setting.
5. Change the setting.
6. Observe the result on the report canvas.

Make changes one at a time so that you can clearly understand the effect of each setting.

---

# 15. Formatting the Entire Chart

After making individual formatting changes, review the complete chart.

## Chart Title

Check:

- Is the title meaningful?
- Is the title readable?
- Is the alignment appropriate?

## X-axis

Check:

- Are the values visible?
- Is the text readable?
- Are the display units appropriate?

## Y-axis

Check:

- Are the category names visible?
- Is the text size appropriate?
- Are the categories easy to understand?

## Data Colors

Check:

- Are the different series easy to distinguish?
- Are the colors consistent?
- Do the colors provide enough contrast?

## Data Labels

Check:

- Are the values readable?
- Are there too many labels?
- Do the labels make the chart easier to understand?

## Legend

Check:

- Is the legend necessary?
- Is it positioned appropriately?
- Are the legend labels readable?

## Background

Check:

- Does the background provide sufficient contrast?
- Does it make the chart easier to read?

## Border

Check:

- Does the border separate the chart clearly?
- Is the border too strong or distracting?

## Gridlines

Check:

- Do gridlines improve readability?
- Are unnecessary gridlines removed?

---

# 16. Recommended Formatting Workflow

Use the following order when formatting the chart:

```text
Select Chart
      ↓
Open Format visual
      ↓
Set Data Colors
      ↓
Format X-axis
      ↓
Format Y-axis
      ↓
Format Data Labels
      ↓
Format Legend
      ↓
Add Chart Title
      ↓
Format Background
      ↓
Format Border
      ↓
Configure Gridlines
      ↓
Review Overall Appearance
```

---

# 17. Professional Formatting Guidelines

1. Use meaningful titles that clearly describe the chart.
2. Use consistent colors throughout the report.
3. Avoid using too many colors.
4. Keep axis labels, titles, legends, and data labels readable.
5. Avoid unnecessary formatting.
6. Maintain proper spacing.
7. Keep the visualization simple and focused on communicating information.

---

# 18. Complete Process

```text
Import Data
     ↓
Verify Dataset
     ↓
Select Stacked Bar Chart
     ↓
Add Category Field
     ↓
Add Numerical Field
     ↓
Add Legend Field
     ↓
Open Format visual
     ↓
Change Data Colors
     ↓
Format X-axis
     ↓
Format Y-axis
     ↓
Add Data Labels
     ↓
Format Legend
     ↓
Add Chart Title
     ↓
Format Background
     ↓
Add Border
     ↓
Configure Gridlines
     ↓
Review Chart
     ↓
Save Power BI Report
```

---

# 19. Final Result

After completing these steps, the Stacked Bar Chart should provide a clear visual comparison of categories and their corresponding sub-categories.

The final visualization should have:

- A meaningful title
- Clearly visible category names
- Appropriate data colors
- Readable numerical values
- A properly positioned legend
- Suitable background
- Appropriate border
- Useful gridlines
- Proper spacing
- A clean and professional appearance

---

# 20. Important Points to Remember

1. Always select the visual before changing its formatting.
2. Use **Format visual** to access the formatting options.
3. Change one formatting option at a time.
4. Use appropriate colors to distinguish different data series.
5. Keep axis labels readable.
6. Use data labels when exact values are useful.
7. Give the chart a meaningful title.
8. Position the legend appropriately.
9. Avoid excessive colors and unnecessary formatting.
10. Maintain consistency between different visualizations in the same report.
11. Always check the final chart from the user's perspective.
12. Formatting should improve understanding rather than only improve appearance.

---

# Conclusion

A Stacked Bar Chart is useful for comparing categories while also showing how different sub-categories contribute to each category.

Power BI provides several formatting options that allow users to customize the appearance of the visualization.

The recommended approach is:

```text
Create the Chart
      ↓
Add the Required Data
      ↓
Open Format visual
      ↓
Format Each Element Step by Step
      ↓
Review the Visualization
      ↓
Finalize the Report
```

By following these steps, users can create a clear, readable, and professional Stacked Bar Chart in Power BI.

---

## Images Used in This Tutorial

| Image | Description |
|-------|-------------|
| `01-inserting-data.png` | Importing and inserting data into Power BI |
| `02-stacked-bar-chart.png` | Creating the Stacked Bar Chart |
| `03-format-pane.png` | Opening and using the Format visual pane |

---

## Folder Structure

```text
04-Stacked-Bar-Chart/
│
├── README.md
│
└── images/
    ├── 01-inserting-data.png
    ├── 02-stacked-bar-chart.png
    └── 03-format-pane.png
```
