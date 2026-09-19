# Netflix Content Strategy Analysis

Exploratory analysis of Netflix's catalog evolution, content mix, and genre distribution using Python.

## Overview

This project analyzes how Netflix's content catalog evolved between 2008 and 2021 using a public dataset of 8,807 Movies and TV Shows.

The analysis focuses on three questions:

- How is Netflix's catalog distributed between Movies and TV Shows?
- How did the number of titles added to Netflix change over time?
- Which genre categories appear most frequently in the catalog?

I used exploratory data analysis to understand the structure of Netflix's catalog before the team moved into deeper genre and content-strategy analysis.

## Tech Stack

- Python
- pandas
- Matplotlib
- Jupyter Notebook

## Project Context

This repository contains my EDA contribution from a five-person course project on Netflix content strategy, reorganized here as a standalone portfolio project.

My contribution focused on:

- dataset overview and exploratory analysis
- data preparation for descriptive analysis
- Movie vs. TV Show distribution
- catalog growth over time
- genre frequency analysis
- data visualization and interpretation

## Key Findings

### 1. Movies make up the majority of the catalog

The dataset contains **6,131 Movies** and **2,676 TV Shows**, so Movies make up about 70% of the titles in the dataset.

![Movies vs. TV Shows](images/movie_vs_tv_show.png)

### 2. Catalog expansion accelerated after 2015

Title additions increased sharply after 2015 and peaked in **2019**, when 2,016 titles were added.

![Titles Added by Year](images/titles_added_by_year.png)

### 3. International content and drama-related genres are highly represented

After splitting multi-label genre entries into individual genre appearances, the most frequent categories were:

- **International Movies:** 2,752 appearances
- **Dramas:** 2,427 appearances
- **Comedies:** 1,674 appearances

Because a single title can belong to multiple genres, these values represent **genre appearances rather than unique title counts**.

![Top 10 Genres](images/top_10_genres.png)

## Methodology

My analysis included the following steps:

1. **Inspect the dataset**
   - Reviewed dataset dimensions, column types, and missing values.

2. **Prepare the data**
   - Removed duplicate records.
   - Converted `date_added` to datetime format.
   - Created a `year_added` variable for time-based analysis.
   - Replaced missing values in selected categorical fields with `Unknown`.

3. **Transform genre data**
   - Split the multi-label `listed_in` field into individual genres.
   - Exploded the genre lists into separate rows for genre-level analysis.

4. **Analyze catalog composition**
   - Compared Movies and TV Shows.
   - Examined the number of titles added by year.
   - Identified the most frequently appearing genre categories.

5. **Visualize and interpret findings**
   - Used Matplotlib to create charts highlighting the main catalog patterns.

## Repository Structure

```text
netflix-content-strategy-analysis/
├── data/
│   └── README.md
├── images/
│   ├── movie_vs_tv_show.png
│   ├── titles_added_by_year.png
│   └── top_10_genres.png
├── notebooks/
│   └── netflix_analysis.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```

- `data/` contains dataset documentation and reproduction instructions.
- `images/` contains visualizations used in this README.
- `notebooks/` contains the exploratory analysis notebook.

## How to Run

1. Clone this repository:

```bash
git clone https://github.com/simingdu/netflix-content-strategy-analysis.git
cd netflix-content-strategy-analysis
```

2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

3. Download the Netflix Movies and TV Shows dataset from the Kaggle source documented in `data/README.md`.

4. Save the dataset as:

```text
data/netflix_titles.csv
```

5. Launch Jupyter Notebook:

```bash
jupyter notebook
```

6. Open:

```text
notebooks/netflix_analysis.ipynb
```

## Limitations

This analysis focuses on Netflix catalog metadata rather than user behavior or financial performance.

Key limitations include:

- The dataset only covers catalog additions through **2021**.
- It does not contain viewership, subscriber, revenue, or engagement data.
- Some fields contain missing values.
- Genre labels are multi-label, so genre frequencies represent appearances rather than unique titles.
- The analysis is primarily descriptive and does not establish causal relationships between observed catalog patterns and Netflix's business strategy.
