# Data

This project uses the **Netflix Movies and TV Shows Dataset** from Kaggle.

## Source

- **Dataset:** Netflix Movies and TV Shows Dataset
- **Author:** Muhammad Tahir
- **Platform:** Kaggle
- **Source:** https://www.kaggle.com/datasets/muhammadtahir194/netflix-movies-and-tv-shows-dataset/code?datasetId=6874934

## Dataset Overview

The analysis uses a dataset containing **8,807 Netflix titles** and **12 original columns**, covering Movies and TV Shows added between **2008 and 2021**.

Key fields used in this analysis include:

- `type`
- `title`
- `country`
- `date_added`
- `release_year`
- `rating`
- `duration`
- `listed_in`

The `listed_in` field contains multiple genre labels per title. For genre-level analysis, these labels were split into separate rows.

After transformation, the genre-level dataset contained **19,323 genre appearances across 42 unique genres**.

Because one title can belong to multiple genres, genre counts in this project represent **genre appearances rather than unique title counts**.

## Reproducing the Analysis

The original dataset is not included directly in this repository.

To reproduce the analysis:

1. Download the dataset from the Kaggle link above.
2. Save the file as `netflix_titles.csv`.
3. Place it inside this `data/` directory.
4. Run `notebooks/netflix_analysis.ipynb`.

## Scope and Limitations

This dataset describes Netflix catalog metadata rather than audience behavior.

It does not contain:

- viewership data
- subscriber data
- revenue data
- engagement metrics

The catalog ends in **2021**, so this project should be interpreted as a historical analysis of Netflix's content library rather than a description of its current catalog.
