# House-Price-Prediction
# London House Price Predictor

A Python machine learning project that estimates London residential property prices using historical housing data.  
The program processes a London house price dataset, trains a Random Forest regression model, and allows a user to enter property details through a simple console interface to receive a predicted price.

## Overview

This project was built to explore how Python can be used to solve a realistic data-driven problem by combining:

- Data cleaning and preprocessing
- Feature engineering
- Machine learning model training
- User input handling through an interactive console interface
- Software design and validation through diagrams and structured test cases

The model uses property information such as:

- Outcode
- Property type
- Number of bedrooms
- Number of bathrooms
- Floor area
- Number of living rooms
- Historical sale price
- Historical sale year
- Build type

## Features

- Loads and processes a London house price dataset
- Trains a Random Forest regression model
- Accepts user-entered property details
- Predicts a current estimated house price
- Applies build-type adjustments such as:
  - normal
  - new_build
  - luxury
- Handles incomplete or invalid user input with fallback/default behaviour

## Technologies Used

- **Python**
- **pandas** for data loading and preprocessing
- **NumPy** for numerical handling
- **scikit-learn** for training the Random Forest regression model

## How It Works

1. The dataset is loaded from CSV.
2. Relevant columns are selected and cleaned.
3. Categorical values such as outcode and property type are encoded.
4. Numerical features are prepared and missing values are handled.
5. A Random Forest regression model is trained on the processed data.
6. The user enters details of a property through the console.
7. The program converts the user input into the same feature format used during training.
8. The trained model predicts a base price.
9. A build-type premium is applied where appropriate.
10. The final estimated price is displayed.

## Project Structure

```text
.
├── README.md
├── requirements.txt
├── data/
│   └── london_house_prices.csv
├── notebooks/
│   └── house_price_prediction.ipynb
├── src/
│   └── house_price_predictor.py
└── tests/
    └── test_cases.md
```

> Update the file names above so they match your actual repository structure.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. Create and activate a virtual environment (optional but recommended):

```bash
python -m venv venv
```

### On Windows

```bash
venv\Scripts\activate
```

### On macOS / Linux

```bash
source venv/bin/activate
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

## Usage

Run the main Python script:

```bash
python src/house_price_predictor.py
```

The program will then prompt you to enter property details such as:

- outcode
- property type
- bedrooms
- bathrooms
- floor area
- living rooms
- previous sale price
- previous sale year
- build type

It will then output an estimated current property price.

## Example

```text
Enter outcode: E15
Enter property type: Flat
Enter bedrooms: 2
Enter bathrooms: 1
Enter floor area: 60
Enter living rooms: 1
Enter previous sale price: 250000
Enter previous sale year: 2015
Enter build type: normal

Estimated property price: £xxx,xxx.xx
```

## Validation and Testing

This project also includes a structured software design and validation process. Testing was designed around three areas:

- Feature construction validation
- Prediction and premium logic validation
- Console user interface validation

Test cases include:

- Expected / nominal operation
- Edge cases and failure states
- Malicious / hostile user input

## Limitations

- The model depends on the quality and age of the dataset used for training.
- Premiums for categories such as `new_build` and `luxury` are manually defined rather than directly learned from labelled data.
- The console interface is simple and intended as a prototype rather than a polished end-user application.

## Future Improvements

- Retrain using more recent housing data
- Add richer features and improved feature engineering
- Improve the console interface and user feedback
- Convert manual validation tables into automated unit tests
- Compare predictions against live property listing data

## Author

**Omar Hassaballa**  
GitHub username: **oh666**

## License

Add a license here if you intend to make the repository open source, for example MIT.
