# DataAnlysis
# Week 1 — Basics: objects, vectors, data frames, reading files

Short summary: Intro to R objects, subsetting, matrices/data.frames, reading messy CSVs, and computing weighted summary statistics.

What’s in the PDF:
- Q1: creating objects & vectors, logical indexing, `seq()`.
- Q2: matrices, data frames, lists, subsetting by condition.
- Q3: palmerpenguins exploration; cleaning a messy CSV; comparing `read.csv`, `read.table`, `readr::read_csv2`.
- Q4: grouped frequency table; weighted mean & variance calculations.

Keywords: vectors, matrix, data.frame, read.csv, read.table, dplyr (optional), plotting, weighted mean.

# Week 2 — Data Manipulation Using the Tidyverse

This week focuses on core tidyverse skills: reshaping data with pivot_longer / pivot_wider, joining datasets, filtering, selecting columns, grouping + summarising, and transforming variables. These skills are essential because almost every real analysis begins with getting the data into the right shape.

What’s in this folder
1️⃣ Week-2-Question-Sheet-solutions.pdf

Main weekly sheet covering:

Importing data (read.table, read_csv)

Why a dataset is not tidy

Reshaping using pivot_longer() and pivot_wider()

Grouped calculations (group_by, summarise)

Standard deviation by region + histogram plots

Creating tidy demographic data (suicides dataset)

Calculating suicide rates + summarising by gender and age


# Week-2-Question-Sheet-solutions

2️⃣ W2-practice-exercises-solutions.pdf

Additional exercises reinforcing tidyverse workflow:

Tidying penguins dataset using pivoting

Demonstrating why unique identifiers matter when reshaping

Using all join types: full_join, inner_join, semi_join, anti_join

Subsetting & arranging mtcars

Grouped summaries: mean, median, quantiles

Data transformations: sqrt, standardisation with mutate()


# W2-practice-exercises-solutions

3️⃣ additional-questions-solutions.pdf

Challenge questions using real datasets (TidyTuesday):

Working with volcano + eruptions datasets

Joining datasets to pull columns from each file

Filtering, arranging recent eruptions, VEI severity

Summaries by rock type, volcano type

Plant conservation dataset: grouping, rowwise sums, comparing extinction categories

Full pivoting, ranking, point-based scoring using tidyverse pipelines


additional-questions-solutions

Key Skills Learned This Week
🔹 Reshaping Data (tidyr)

pivot_longer() — make many columns into key–value pairs

pivot_wider() — spread measurement types back into columns

Handling multiple names in pivoting (names_to = c("gender","age") etc.)

🔹 Joining Data (dplyr)

full_join() — keep everything

inner_join() — keep matching rows only

semi_join() — filter based on matches

anti_join() — find what doesn’t match

🔹 Filtering, Selecting, Arranging

filter(mpg >= 20)

select(hp:vs)

arrange(desc(wt))

🔹 Grouped Calculations

Means, medians, quantiles, variances

Multi-group summaries (group_by(vs, am))

🔹 Transformations

mutate() new columns

Standardisation using group-specific values (e.g., by transmission type)

Square root transform for skewed data

# Week 3 — Introduction to Data Visualisation

This week introduces the fundamentals of data visualisation in R using both base R graphics and ggplot2. You learn how to choose appropriate plot types, customise them, interpret visual patterns, and present clear comparisons between groups, time periods, and variables.

1️⃣ Week-3-Question-Sheet-Solutions.pdf

This is the main sheet for Week 3. It includes:

Question 1 — Population & Deprivation Visualisations

Tidying a multi-year dataset using pivot_longer()

Boxplots comparing high vs low deprivation areas

Log-scaled boxplots to handle skewed distributions

Histograms comparing population distributions for 2001 vs 2013

Line plots of population trends over time

Grouped line plots comparing Upper vs Lower deprivation regions

(See pages 1–7 for these plot examples.) 

Week-3-Question-Sheet---Solutio…

Question 2 — Himalayan Expeditions (TidyTuesday data)

Seasonal variation in deaths and injuries using bar plots & line plots

Identifying which peaks have the most deaths (total vs average)

Scatter plot of team size vs highest point reached

Boxplots of oxygen use vs success
(See pages 7–13 & 17–22.)


Week-3-Question-Sheet---Solutio…

Question 3 — Suicides Dataset

Tidying with pivot_longer() & pivot_wider()

Calculating suicide rates per 100,000

Comparing rates between genders (histograms)

Boxplots for Gender × Age combinations

Faceted plots showing gender differences across age groups
(See pages 13–17.)


Week-3-Question-Sheet---Solutio…

Question 4 — Friends TV Show Dialogue Dataset

Determining the most positive season

Identifying which character spoke most overall

Tracking character dialogue changes across seasons
(See pages 17–22.)


Week-3-Question-Sheet---Solutio…

Question 5 — GP Prescribing Data

Multi-panel plots showing relationships between prescribing rate and demographics

Boxplots comparing prescribing across Health Boards (HBCode)

Annotating plots with labels + arrows
(See pages 23–28.)


Week-3-Question-Sheet---Solutio…

2️⃣ W3-practice-exercises-solutions.pdf

This PDF contains extra practice focused on common plot types.

Includes:
Bar Plots

Species counts

Species × Island counts

Max bill length by species
(Pages 1–3.)


W3-practice-exercises - solutio…

Histograms

Flipper length histogram

Histograms by species (multimodal distributions)
(Pages 3–5.)


W3-practice-exercises - solutio…

Boxplots

Single variable distributions

Boxplots by year

Species × Year comparisons
(Pages 5–7.)


W3-practice-exercises - solutio…

Scatter Plots

Bill length vs bill depth

Colouring points by species
(Pages 8–9.)


W3-practice-exercises - solutio…

Plot Customisation

Titles, axis labels, legends

Improving readability

Custom colour palettes
(Pages 9–11.)


W3-practice-exercises - solutio…

Key Skills Learned This Week
📌 Choosing the right plot

Boxplots for comparing distributions

Histograms for shape & spread

Scatter plots for relationships

Line charts for trends over time

Bar charts for counts & group comparisons

📌 Using ggplot2 effectively

geom_point(), geom_line(), geom_col(), geom_histogram(), geom_boxplot()

Adding aesthetics: colour, fill, group, alpha

Facetting (facet_wrap) to compare subgroups

Log scaling (scale_y_log10())

📌 Plot interpretation

Understanding skew, multimodality, outliers, and group differences

Recognising when transformations are appropriate

Comparing trends between subgroups (gender, deprivation, season, species)

