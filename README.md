# Car Dealer Data Scraping and Analysis

![Car Dealer Data Scraping and Analysis](https://img.shields.io/badge/Python-3.6%20%7C%203.7%20%7C%203.8%20%7C%203.9%20%7C%203.10-blue)

This Python script is designed to scrape car dealership information from the [Cars.com](https://www.cars.com/) website, specifically focusing on Mercedes-Benz vehicles. It extracts data such as car name, mileage, dealer name, rating, rating count, and price. After extracting the data, it performs data cleaning and provides visualizations for analysis.

## Prerequisites

Before running this script, make sure you have the following libraries installed:

- BeautifulSoup (bs4)

- requests

- os

- pandas

- numpy

- matplotlib

- seaborn

You can install these libraries using `pip`:

```bash
pip install beautifulsoup4 requests pandas numpy matplotlib seaborn
```

## How to Use

1. Clone or download this repository to your local machine.

2. Open the Python script in your preferred code editor or Python environment.

3. Run the script. It will scrape data from the specified website, clean the data, and generate visualizations.

## Code Explanation

### Web Scraping

- The script starts by importing the necessary libraries and defining the target website URL.

- It sends an HTTP GET request to the website using the `requests` library and checks the response status code.

- The HTML content is parsed using `BeautifulSoup` to make it easier to extract data.

- The script finds all vehicle cards on the page and counts the number of results.

- It initializes lists to store data for car name, mileage, dealer name, rating, rating count, and price.

- Data is extracted from each vehicle card using try-except blocks to handle missing or erroneous data.

### Data Cleaning

- The script creates a DataFrame from the extracted data using the pandas library.

- It performs data cleaning by:

    - Extracting numeric values from the 'Rating Count' column.
    - Removing currency symbols and commas from the 'Price' column and converting it to a numeric format.

## Visualizations and Analysis

The script provides several visualizations for data analysis:

- **Average Price by Dealer**: A bar plot showing the average price by dealer.

- **Correlation between Mileage and Price**: The correlation coefficient between mileage and price is calculated and displayed.

- **Price Distribution**: A histogram showing the distribution of prices.

- **Number of Ratings vs. Rating**: A scatter plot of the number of ratings against the rating.

- **Top Car Models by Frequency**: A bar plot showing the top car models by frequency.

- **Price Distribution by Car Model**: A box plot showing the price distribution for different car models.

- **Price vs. Dealer**: A scatter plot showing the relationship between price and the dealer.

- **Average Mileage by Car Model**: A bar plot showing the average mileage by car model.

## Data Export

The script creates a 'data' directory if it doesn't exist and saves the DataFrame to an Excel file named 'car_data.xlsx' in that directory.