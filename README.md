# Shoeshop Return Prediction Model

This repository contains the machine learning model for predicting whether an item sold by a shoeshop will be returned. The model is built using a dataset of transactions stored in `transactions.parquet`.

## Dataset

The dataset `transactions.parquet` includes various features extracted from the transaction records of a shoeshop. It is structured in a way that each row represents a unique transaction, and each column represents a feature that could be related to the likelihood of an item being returned.

## Model

The model is trained to predict if an item is likely to be returned using historical transaction data. It takes into account various attributes of the purchase and the item itself.

## Getting Started

To use the model, you will need to have Python installed along with the necessary libraries listed in `requirements.txt`.

### Prerequisites

Ensure that you have the following prerequisites installed:

- Python 3.6 or later
- Pandas
- Scikit-learn
- PyCaret

### Installation

1. Clone the repository:

```bash
git clone https://github.com/audeha/shoeshop.git
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```
### Usage
To make predictions using the model:

Load your transactions.parquet file into a Pandas DataFrame.
Preprocess the data using the provided preprocessing script.
Load the trained model.
Call the predict method on the processed data.

### Contributing

Contributions to improve the prediction model or to extend the functionality are welcome. Please feel free to fork the repository and submit a pull request with your changes.

### License

This project is licensed under the MIT License.

### Acknowledgments

Thanks to the contributors who have helped in building and optimizing the model.
Special thanks to the data science community for the continuous exchange of knowledge.
Blabla, who reads this?
