
# iPhone Data Analysis Mini Project

This project focuses on analyzing a dataset containing information about various Apple products, specifically iPhones. The analysis includes operations like loading data, examining product prices, and manipulating product names.

## Dataset

The dataset used in this project is `apple_products.csv`, which includes the following columns:
- Product Name
- Mrp (Maximum Retail Price)
- Star Rating

## Prerequisites

To run this project, you need to have Python installed along with the following packages:
- pandas

You can install the required packages using the following command:
```bash
pip install pandas
```

## Project Structure

The project consists of the following steps:

1. **Importing Necessary Libraries**:
    ```python
    import pandas as pd
    ```

2. **Loading the Dataset**:
    ```python
    df = pd.read_csv("Data/apple_products.csv")
    df.head()
    ```

3. **Basic Data Exploration**:
    - Count the number of entries in the dataset:
        ```python
        df.count()
        ```

    - Find the maximum and minimum prices:
        ```python
        df['Mrp'].max()
        df['Mrp'].min()
        ```

    - Display products with specific prices:
        ```python
        df[df['Mrp'] == 149900]
        df[df['Mrp'] == 39900]
        df[df['Mrp'] >= 100000]
        ```

4. **String Manipulations**:
    - Convert the product name to uppercase and lowercase:
        ```python
        list(df['Product Name'])[0].upper()
        list(df['Product Name'])[0].lower()
        ```

    - Extract and manipulate substrings from product names:
        ```python
        list(df['Product Name'])[51][6:15].upper().strip()
        ```

5. **Creating a New Column**:
    - Extract a part of the product name to create a new column `Model Name`:
        ```python
        df['Model Name'] = df['Product Name'].str[6:15]
        df.head()
        ```

6. **Sorting the Dataset**:
    - Sort the dataset by the star rating in descending order:
        ```python
        df.sort_values(by=['Star Rating'], ascending=False)
        ```

## Usage

To run the analysis, simply execute the notebook `iPhone Data Analysis Mini Project.ipynb` step by step. Each code cell contains comments and explanations to help you understand the process.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
