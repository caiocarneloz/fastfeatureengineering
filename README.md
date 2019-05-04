# FastFeatureEngineering
Simple feature engineering using pandas for baseline purposes

## Getting Started
#### Dependencies
You need Python 3.5 or later to use FastFeatureEngineering. You can find it at python.org.

You aso need the pandas package, which is available from PyPI. If you have pip, just run:
```
pip install pandas
```
#### Installation
Clone this repo to your local machine using:
```
git clone https://github.com/caiocarneloz/FastFeatureEngineering.git
```

## Features
- Get list of columns by specific data type
- Do arithmetic operations with columns
- Get abs difference between columns
- Onehot encode columns
- Normalize columns

## Usage
The FastFeatureEngineering function takes as argument a dataframe containing the data and a dictionary containing the desired output. The outputs represents the dictionary keys while the column names represents the values. The possible outputs are represented by the following keys:

- sum (to get the sum of a set of columns)
- diff (to get the difference of a set of columns)
- quo (to get de quotient of a list of columns)
- prod (to get the product of a list of columns)
- abs_diff (to get the abs difference of a list of columns)
- onehot (to onehot encode a list of columns)
- norm (to normalize a list of columns)

#### Example
Creating the dictionary to get:
- A column with the difference between column_1 and column_2
- Columns with the sum of column_1 and column_2, and column_1, column_2 and column_3
- Columns representing the onehot encoding of column_4 and column_5
- Columns with column_6 and column_7 normalized
```
op_dict = {}
op_dict['diff'] = [['column_1', 'column2']]
op_dict['sum'] = [['column_1', 'column_2'], ['column_1', 'column2', 'column_3']]
op_dict['onehot'] = ['column_4', 'column_5']
op_dict['norm'] = ['column_6', 'column_7']
```
