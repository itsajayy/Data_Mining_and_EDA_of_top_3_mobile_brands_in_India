# Web Scraping and Exploratory Data Analysis of Mobile Phones
### Project Overview
This data analysis project aims to provide insights into the mobile market in india between the top three companies in India. By analyzing various aspects of the mobile phones data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the phone market in india.

### Data Sources

Mobile Data - The primary dataset used for this analysis is the "top_3_brands.csv" file, containing detailed information about each company in India.

### Tools
  - Python - Web Scraping
  - Excel - Data Cleaning
  - SQL Server - Data Analysis
  - PowerBI - Creating reports

#### Web Scraping
#### Language used - Python
#### Libraries used - Beautiful Soup, Pandas, Openpyxl
 - Install Required Libraries:
Make sure you have the necessary libraries installed. You can install them using the following commands:
```python
  pip install beautifulsoup4
  pip install openpyxl
```
- Save HTML Content:
  Save the HTML content of the Amazon website by right-clicking on the webpage, selecting "Save As" (or using CTRL+S), and save the file in the same directory as your Python script. Add the file name to the open() function in your code:

```python
  with open("your_amazon_page.html", "r", encoding="utf-8") as file:
```
- Inspect HTML Structure:
  Inspect the HTML structure of the saved webpage to identify the relevant elements and their classes. Update the find_all method with the correct HTML tags and class names. For example:

```python
  product_divs = soup.find_all("div", class_="your-product-container-class")
```
- Update Data Extraction:
  Customize the code to extract the specific data you need from the webpage. Adjust the find methods based on the structure of the HTML. For instance:

```python
  product_name = div.find("span", class_="your-product-name-class")
  product_cost = div.find("span", class_="your-product-cost-class")
```
- Save to Excel:
  Provide the desired Excel file name in the excel_file variable. The code will create a new Excel file if it doesn't exist or append data to an existing one.

```python
excel_file = "your_data_file.xlsx"
```
- Run the Script:
  Execute the Python script in your terminal or IDE. Ensure that the script has the necessary permissions to read and write files in the directory.

```python 
  your_script.py
```
- Check Excel File:
  After running the script, check the specified Excel file for the scraped data. The script appends data to the existing file or creates a new one if needed.

```python
  print(f"Data has been appended to {excel_file}"
```


####  Data Cleaning/Preparation
#### Tools Used - Excel

In the initial data preparation phase, we performed the following tasks:

1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.
