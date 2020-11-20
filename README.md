
# CZ4032 Project - Topic Modelling via Latent Dirichlet Allocation (LDA)

This project seeks to derive a score profile for restaurants across certain aspects in hopes to provide some insight as to how each restaurant can improve their business. The aspects are derived via topic modelling using LDA and we're using business reviews from the Yelp dataset to train our LDA model with.

As there is a large amount of reviews from the dataset, we are only zooming in to reviews for restaurants located in Las Vegas for computational efficiency since this subset contributes to the greatest proportion of points in the dataset.

### Requirements

The yelp dataset can be obtained from [here](https://www.yelp.com/dataset), and experiments were conducted primarily on [Google Colab](https://colab.research.google.com/) as well. We only require two of the datasets from Yelp, namely `business.json` and `review.json`.

### Set up

We have only 3 files which focus on different actions:

- `yelp_business_filtering.ipynb`: Handles the filtering of businesses to extract restaurants within Las Vegas based on the properties `city` and `categories`

- `yelp_review_filtering.ipynb`: Handles the filtering of reviews to extract all reviews related to restaurants in Las Vegas based on `business_id`.

- `yelp_lda_model.ipynb`: Handles the preprocessing and actual training of the LDA model based on the filtered reviews, as well some analysis on the results.

### Running the program

- `yelp_business_filtering.ipynb`: This notebook was written and executed on a local machine. Ensure that `business.json` is located in the same directory as this script, and rename the file to `yelp_academic_dataset_business.json`

- `yelp_review_filtering.ipynb`: This notebook was written and executed on a local machine. Ensure that `review.json` is located in the same directory as this script, convert it to CSV and rename the file to `review_tester.csv`

- `yelp_lda_model.ipynb`: This notebook was written and executed on Google Colab, which uses Google Drive as the primary storage location. Ensure that this script, along with the filtered reviews dataset (`yelp_review.csv`) are located on a folder `CZ4032 (Local)` in the root of your Google Drive.