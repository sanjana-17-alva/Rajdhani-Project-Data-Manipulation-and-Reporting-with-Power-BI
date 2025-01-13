# Rajdhani Project - Data Manipulation and Reporting with Power BI

## Project Overview

The **Rajdhani Project** aims to build a consolidated and interactive Power BI report for Rajdhani, a global restaurant aggregation and meal delivery service. Rajdhani operates in several countries and provides detailed information about various eateries and consumer reviews. The goal of this project is to allow Rajdhani's owners to quickly assess their business performance, identify hidden irregularities in their data, and make informed decisions.

This Power BI report will help stakeholders analyze the business performance on a global scale, with the ability to drill down to granular levels and extract key insights about the restaurants and their operations across different regions.

## Objectives

The main objectives of this project are to enable Rajdhani to:

1. **Derive data** on the total number of restaurants worldwide, categorized by continents, countries, and cities.
2. **View data** globally with the capability to drill down to more detailed levels.
3. **Analyze restaurant ratings** to find the restaurants with the highest average customer ratings.
4. **Identify the restaurants** with the lowest average costs.
5. **Filter and view information** based on:
   - Geographical dimensions (continent, country, city)
   - Services offered (online ordering, reservation services)
   - Average rating slabs (using color coding)
6. **Identify the restaurants with the most cuisines** served.
7. **Design a multi-page report** that suits Rajdhani’s theme with easy navigation across sections.
8. **Ensure accessibility** for Rajdhani users via both web browsers and mobile devices.

## Aim of the Project

The aim is to construct an interactive Power BI report that consolidates data from multiple Excel files and provides actionable insights to Rajdhani’s management team for performance assessment.

## Steps to Complete the Project

### 1. **Data Import and Transformation**
   - Import data from the available Excel files containing restaurant details.
   - **Data Transformation:**
     - Correct city names (e.g., “Sí£o Paulo” should be corrected to “São Paulo”).
     - Ensure clarity in city names (e.g., “Cedar Rapids/Iowa City” corrected to “Cedar Rapids”).
     - Remove unnecessary columns.
     - Create two columns: Restaurant Name and Restaurant Address.
     - Create a separate table for cuisines served by each restaurant (split by rows if a restaurant serves multiple cuisines).
   - **Country-Code Table:**
     - Ensure only unique, non-blank values are included in the Country-Code dimension table.

### 2. **Data Model Optimization**
   - Rename the KPI table as a fact table.
   - Apply trimming operations where required to ensure data cleanliness.
   - Optimize the data model for faster loading and performance.

### 3. **DAX Implementation**
   - **Rating Colour Column:** Create a DAX formula to categorize restaurants based on their aggregate ratings, with corresponding colors:
     - `0`: Not Rated
     - `<= 2.9`: Red
     - `<= 3.4`: Orange
     - `<= 3.9`: Yellow
     - `<= 4.4`: Green
     - `> 4.4`: Dark Green
   - **Measures:** Create the following measures for analytics:
     - **Restaurant Count**: Total number of restaurants.
     - **Total Restaurant**: Total restaurants across regions.
     - **Average Cost**: Average cost of meals.
     - **Average Rating**: Average rating across all restaurants.
     - **Unique Cuisine Count**: Count of unique cuisines served.
   - **Continent Column in Country Code Table:** Use a SWITCH measure to create the continent column, with the following mappings:
     - 189: "Africa"
     - 215: "Europe"
     - 37: "NAM" (North America)
     - 30: "SAM" (South America)
     - 14, 148: "Oceania"
     - 150: "Asia"

## Report View

### 1. **Formatting and Visual Design**
   - Use the **format painter** to apply consistent formatting across visuals.
   - **Enable visuals** that are disabled by default.
   - **Apply Filters** where necessary to enhance user interactivity and customization.
   - **Restaurant Logos:** Embed restaurant logos in the report with clickable URLs linking to their respective websites (e.g., [Restaurant URL](https://shorturl.at/cnyzA)).

### 2. **Multi-Page Report Navigation**
   - Design the report with multiple pages for different analytical perspectives.
   - Ensure easy navigation between sections to enhance the user experience.

### 3. **Mobile and Web Compatibility**
   - Ensure that the report is optimized for both desktop (web browser) and mobile device views.

## Conclusion

The Rajdhani Power BI report will allow the management team to gain comprehensive insights into restaurant performance worldwide. With the ability to filter by geographical dimensions, service type, rating, and cuisine, stakeholders can make informed decisions that improve business operations and customer satisfaction. This project consolidates data into an accessible, easy-to-navigate report designed for fast, interactive decision-making across multiple devices.
