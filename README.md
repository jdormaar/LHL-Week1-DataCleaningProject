# Final-Project-Transforming-and-Analyzing-Data-with-SQL

## Project / Goals

To apply what we learned during the first week of the Lighthouse Labs bootcamp, among which included:

1. Inspecting and importing CSV formatted dataset into a Postgres database
1. Applying data cleaning techniques and analysis
1. Perform quality assurance on the dataset

## Process

Steps followed:

1. Data was inspected for obvious errors and inconsistencies such as data type mismatch, and abrupt changes in formatting.
1. Data familiarization to better understand the dataset, such as expected vs unexpected data results, and the meaning of data columns and values.
1. Removing inconsistencies, such as duplicate or irrelevant data.
1. Handling missing data
1. Data verification and quality assurance was performed by running queries to assess the relevance and validity of the data.
1. Documentation of tracked changes with self-documenting code and formatting with concise commenting and relevant rationales

## Results

Without the objective benefit of statistical analysis applied to the dataset, a few subjective observations could be made at best until further cleaning, analysis, and quality assurance processing can take place:

- Google Nest purchases in Mountain View are quite high which appears to be correlated with the location of Google Headquarters. One could theorize that employees might be required to purchase units for QA assurance and testing purposes, or the population of Mount View quite enjoy a constant temperature.
- Youtube is a more successful shopping platform than I was previously aware of.
- US appears to really enjoy Mens T-shirts.

## Challenges 

Time was absolutely the most precious resource throughout this project, which is appropriate since I am learning and I initially approached the process without drawing constraints or boundaries. Particularly when dealing with the larger database tables I found myself having to fight against paralysis regarding how and when to get started. I spent a lot of time trying to acclimate and find clear logical steps and structure to the process of data cleaning and it's documentation in an attempt to constrain and organize my thoughts. Eventually my process evolved into maintaining a living document capable of safekeeping the queries I generated, and their associated inquiry details within a readable logical context. A significant improvement in my time management could have been achieved had I adopted this documentation technique earlier on in the process. Technical difficulties were also an issue, specifically regarding the permissions for PgAdmin to access the CSV files while importing. I found this particularly difficult because I'm still learning to use a Mac, and I'm new to data science software management. Additional setbacks from a lack of understanding of how to protect myself from accidental data losses during cleaning. On two specific occurrences of this mistakes I was required to re-create the table data and re-apply the cleaning techniques, which resulted in significant time loss, but did read up on ways to mitigate data loss using a transaction. The final issue that cost a lot of time was not being able to push changes to GitHub due to a `Push failed on refs/heads/main: pre-receive hook declined error`.  The error was not descriptive, but after a couple hours of reading and trying to fix this issue I came across a single post in StackOverflow indicating that GitHub does not accept files over 100MB, and the `analytics.md` file is ~500MB, which was committed in order ot keep the raw data together with the project for my own reference.

## Future Goals

1. Complete a more thorough cleaning of the data. For example, the `all_sessions` table is oversized and contains data that could be pulled out into new or existing tables, and further constraints applied to facilitate the entity relationships. For example the `all_sessions` transaction related column data could be moved into a new `transactions` table, and the product related column data moved into the existing `products` table. This would significantly improve the accessibility of the data contained within the database.
1. Cross analysis of existing column data to create appropriate entity relationships to improve understanding of the dataset and help with further analysis.
1. Explore alternative planning methods regarding the approach to the data cleaning process, such as project mapping using sticky notes posted on the wall to provide a large visual representation of entities, relationships, and data related issues.