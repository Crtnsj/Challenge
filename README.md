# Disaster Prediction Challenge

This project analyzes historical data to predict different types of disasters in various city districts based on environmental and meteorological factors. Using machine learning techniques, we build a model that can classify disasters from weather and environmental data.

## Project Overview

The project consists of two main components:

1. **Data Preprocessing**: Cleaning, normalizing, and preparing raw disaster data for machine learning
2. **Predictive Modeling**: Building and training a gradient boosting classifier to predict disaster types

## Dataset

The dataset includes the following features:

- `temperature`: Ambient temperature
- `humidite`: Humidity level
- `force_moyenne_du_vecteur_de_vent`: Average wind vector force
- `force_du_vecteur_de_vent_max`: Maximum wind vector force
- `pluie_intensite_max`: Maximum rain intensity
- `date`: Date of the observation
- `quartier`: District ID
- `sismicite`: Seismic activity level
- `concentration_gaz`: Gas concentration
- `pluie_totale`: Total rainfall
- `catastrophe`: Target variable (disaster type)

## Project Structure

- `data_raw.csv`: Original, unprocessed dataset
- `data_clean.csv`: Cleaned and normalized dataset
- `data_for_model.csv`: Preprocessed dataset ready for modeling
- `main.ipynb`: Notebook containing data exploration, cleaning, and preprocessing steps
- `model.ipynb`: Notebook with machine learning model implementation
- `requirements.txt`: Python dependencies for the project
- `pyproject.toml`: Project configuration for package management

## Data Preprocessing

The preprocessing pipeline includes:

1. Cleaning and normalizing the raw data
2. Converting the district IDs to numerical values
3. Encoding categorical variables
4. Feature engineering based on date information

## Machine Learning Model

We use a Histogram-based Gradient Boosting Classifier with the following features:

- GridSearchCV for hyperparameter tuning
- Train/test split with stratification to handle class imbalance
- Feature preprocessing with scikit-learn's ColumnTransformer
- Performance evaluation using classification metrics

## Requirements

This project requires Python 3.8+ and the following packages:

- polars
- pandas
- scikit-learn
- matplotlib
- seaborn
- jupyter

You can install the required packages using:

```bash
pip install -r requirements.txt
```

## Usage

1. Run the `main.ipynb` notebook to process the raw data
2. Run the `model.ipynb` notebook to train and evaluate the prediction model

## License

This project is part of a data science challenge for YNOV.
