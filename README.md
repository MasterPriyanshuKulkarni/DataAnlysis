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

Week 3 — Introduction to Data Visualisation

This week introduces the foundations of data visualisation in R, using both base R and ggplot2.
You learn how to choose the right plot, tidy data before plotting, compare distributions, analyse trends, and communicate patterns clearly.

📂 What’s in this folder
# 1️⃣ Week-3-Question-Sheet-Solutions.pdf

Main worksheet for Week 3. It contains the core visualisation problems for the week.

Question 1 — Visualising Population & Deprivation (Pages 1–7)

Covers:

Reading & tidying data using pivot_longer()

Boxplots comparing populations across deprivation groups
(See examples on pages 1–3) 

Week-3-Question-Sheet---Solutio…

Log-transformed boxplots (scale_y_log10()) to handle skew

Histograms comparing 2001 vs 2013 population distributions
(Page 3–4) 

Week-3-Question-Sheet---Solutio…

Overall population trends using line charts
(Pages 4–5)

Grouped time trends for Lower vs Upper deprivation
(Pages 6–7)

Question 2 — Himalayan Expedition Data (Pages 7–13)

Data from TidyTuesday: deaths, injuries, peaks climbed.

Includes:

Seasonal variation in deaths & injuries (bar charts and line graphs)
(Pages 7–9) 

Week-3-Question-Sheet---Solutio…

Identifying peaks with most deaths (total and per expedition)
Annotated plots with arrows (Pages 9–11)

Scatterplots: team size vs highest point reached (Pages 11–12)

Whether oxygen use indicates "good" or "bad" expeditions (Page 12)

Question 3 — Suicide Rate Visualisation (Pages 13–17)

Tasks include:

Tidying gender × age data using pivoting

Calculating suicide rates per 100,000

Histograms comparing male vs female suicide rates (Pages 13–14)

Boxplots of Gender × Age groups (Pages 14–15)

Faceted boxplots comparing gender differences across each age group
(Pages 15–17)


Week-3-Question-Sheet---Solutio…

Question 4 — Friends Dialogue Dataset (Pages 17–22)

Using season, speaker, and emotion data.

You visualise:

Which season had the most positive emotions (Page 17–18)

Which character spoke the most overall (Pages 18–19)

How speaking frequency changed across seasons and episodes
Using line plots with season breaks (Pages 20–22)


Week-3-Question-Sheet---Solutio…

Question 5 — GP Prescribing Data (Pages 23–28)

You explore relationships between prescribing rates and demographics.

Plots include:

Multi-panel comparisons (dispensing, age distribution, list size, area type)
(Pages 23–25)

Differences in prescribing rate across Health Boards (HBCode)
(Pages 25–28)

Adding annotations + curved arrows in ggplot


Week-3-Question-Sheet---Solutio…

# 2️⃣ W3-practice-exercises-solutions.pdf

These are your skill drills for Week 3 — fast reference during the exam.

Exercise 1 — Bar Plots (Pages 1–3)

Species counts for penguins

Species × Island counts

Max bill length by species


W3-practice-exercises - solutio…

Exercise 2 — Histograms (Pages 3–5)

Basic flipper length histogram

Multimodal distributions by species

Overlaid histograms using alpha transparency


W3-practice-exercises - solutio…

Exercise 3 — Boxplots (Pages 5–8)

Body mass distribution

Body mass by year (group=year)

Species × year boxplots


W3-practice-exercises - solutio…

Exercise 4 — Scatter Plots (Pages 8–9)

Bill length vs bill depth

Colouring points by species

Base R vs ggplot syntax


W3-practice-exercises - solutio…

Exercise 5 — Customisation (Pages 9–11)

Adding titles, axis labels, legends

Improving colour choices

Better x-axis labelling for grouped boxplots
