# Fake and Real News Dataset Analysis

This repository contains a Jupyter Notebook (`main.ipynb`) that downloads and explores the [Fake and Real News dataset](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset) from Kaggle. The notebook demonstrates how to install dependencies, download the dataset using `kagglehub`, load the data with pandas, and perform basic exploratory data analysis.

## Overview

The notebook performs the following tasks:
- **Install Required Packages:** Uses `pip` to install necessary libraries such as `torchmetrics`, `datasets`, `transformers`, and `kagglehub`.
- **Download the Dataset:** Leverages `kagglehub.dataset_download` to download the latest version of the dataset.
- **Data Loading:** Reads the `Fake.csv` and `True.csv` files into pandas DataFrames.
- **Exploratory Analysis:** Prints out samples, displays DataFrame information, and summarizes the dataset using pandas functions like `head()`, `describe()`, and `info()`.

## Prerequisites

- **Python 3.x**
- **Jupyter Notebook Environment:** This notebook can be run locally or on platforms like Google Colab.
- **Internet Connection:** Required for downloading the dataset from Kaggle via `kagglehub`.

## Installation

The notebook automatically installs the required dependencies. However, if you prefer to install them manually, run the following command in your terminal or notebook cell:

```bash
pip install torchmetrics datasets transformers kagglehub
```

## Running the Notebook

1. **Open the Notebook:** Launch Jupyter Notebook or open the file in Google Colab.
2. **Run the Cells:** Execute the notebook cells in order. The notebook will:
   - Install necessary packages.
   - Download the dataset from Kaggle.
   - Load the dataset into pandas DataFrames.
   - Display initial exploration of the data.
3. **Explore and Extend:** Use the provided analysis as a starting point for further exploration or to build machine learning models.

## Dataset Description

The [Fake and Real News dataset](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset) is composed of two CSV files:

- **Fake.csv:** Contains fake news articles.
- **True.csv:** Contains real news articles.

Each file includes the following columns:
- **title:** The title of the news article.
- **text:** The full text of the article.
- **subject:** The category or subject of the article.
- **date:** The publication date of the article.

The notebook uses this dataset to perform a preliminary analysis and can be expanded for tasks like text classification, sentiment analysis, or other forms of data mining.

## License

*Include your license information here if applicable.*

## Acknowledgments

- Thanks to [Kaggle](https://www.kaggle.com/) and the dataset creator, Clément Bisaillon, for providing the Fake and Real News dataset.
- Thanks to the developers of `kagglehub` for streamlining the dataset download process.
