# Crowdfunding Extract, Transform, and Load (ETL)

## Table of Contents
1. [Overview](#overview)
2. [Project Details](#project-details)
   - [Background](#background)
   - [Goals](#goals)
   - [Methodology](#methodology)
3. [Conclusions](#conclusions)
4. [Future Work](#future-work)
5. [Collaborators](#collaborators)

## Overview

This project focuses on the extraction, transformation, and loading (ETL) of a crowdfunding dataset into a PostgreSQL relational database. The dataset includes rich information on donors, blurbs, goals, pledged amounts, campaign outcomes (success or failure), categories, subcategories, currencies, launch dates, and deadlines. The primary goal is to clean and organize the data into separate, meaningful tables to improve its integrity, accessibility, and future usability for analysis and visualization. Storing this data in a relational database minimizes redundancy and simplifies future modifications.

## Project Details

### Background

The motivation behind this project is to explore the relationships and patterns between various crowdfunding variables. By organizing and storing the data efficiently, this project lays the foundation for future analysis that could provide insights and business advice to enhance the success of crowdfunding campaigns.

### Goals

- Create DataFrames for Categories, Subcategories, Campaigns, and Contacts.
- Develop a relational database for the crowdfunding dataset.
- Future goal: Perform analysis and visualization based on the cleaned data.

### Methodology

- **Data Collection:** The original dataset was extracted from a CSV file using Python's Pandas library.

- **Data Cleaning:** Initially, the 'Category' and 'Subcategory' were in a single column. These were split into two separate columns and then into distinct DataFrames. Columns were renamed for clarity (e.g., 'blurb' was changed to 'description'). Data types were checked, and some columns were converted from object types to floats as needed. Unnecessary columns were dropped. The 'Contacts' DataFrame was created by separating the 'name' column into 'First Name' and 'Last Name' columns.

- **Data Storage:** An Entity-Relationship Diagram (ERD) was sketched to design the database schema. Using PostgreSQL, a relational database was created, and the cleaned CSV files were imported into the respective tables: Categories, Subcategories, Campaigns, and Contacts.

#### Figure 1: Original Crowdfunding Data
![Figure 1](https://github.com/shahdhwani4/Crowdfunding_ETL/blob/jenny_branch/images/fig1.png)
*A portion of the original DataFrame extracted before cleaning.*

#### Figure 2: Entity-Relationship Diagram (ERD)
![Figure 2](https://github.com/shahdhwani4/Crowdfunding_ETL/blob/jenny_branch/images/fig2.png)
*The entity-relationship diagram illustrating the database schema.*

#### Figure 3: Contacts Table
![Figure 3](https://github.com/shahdhwani4/Crowdfunding_ETL/blob/jenny_branch/images/fig3.png)
*A portion of the 'Contacts' table in the crowdfunding database.*

#### Figure 4: Category Table
![Figure 4](https://github.com/shahdhwani4/Crowdfunding_ETL/blob/jenny_branch/images/fig4.png)
*A portion of the 'Category' table in the crowdfunding database.*

#### Figure 5: Subcategory Table
![Figure 5](https://github.com/shahdhwani4/Crowdfunding_ETL/blob/jenny_branch/images/fig5.png)
*A portion of the 'Subcategory' table in the crowdfunding database.*

#### Figure 6: Campaign Table
![Figure 6](https://github.com/shahdhwani4/Crowdfunding_ETL/blob/jenny_branch/images/fig6.png)
*A portion of the 'Campaign' table in the crowdfunding database.*

## Conclusions

This project successfully extracted, cleaned, and organized a complex crowdfunding dataset into a relational database. By structuring the data into separate tables, the project has significantly improved data integrity and accessibility, laying a strong foundation for future analysis and visualization efforts.

## Future Work

This project serves as the initial phase of a broader endeavor aimed at analyzing and visualizing the relationships between the variables within the crowdfunding dataset. Future work will focus on detailed analysis and the creation of visualizations that can offer actionable insights for improving the success rates of crowdfunding campaigns.

## Collaborators

- **Dhwani Shah:** Data extraction, cleaning, database design, and README documentation.
- **Jennifer Jaurequi:** Data extraction, cleaning, database design, and README documentation.

*Note: This project was a collaborative effort, with both partners contributing equally to all aspects.*
