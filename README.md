# Delving into Amazon's Best-Selling Mobile brands in India through Webscraping and Data Exploration

### Project Overview
This data research study attempts to provide insights into the mobile market in India by comparing the top three players. We hope to discover patterns, generate data-driven recommendations, and acquire a better understanding of the phone market in India by evaluating various elements of mobile phone data.

### Data Sources

Mobile Data - The primary dataset used for this analysis is the "processed_data.csv" file, containing detailed information about each company in India.

### Tools Used
  - Python - Web Scraping
  - Excel - Data Cleaning
  - PowerBI - Creating reports

<details>
  <summary><h2> Web Scraping </h2></summary>
  
#### Language used - Python
#### Libraries used - Beautiful Soup, Pandas, Openpyxl

- Install Required Libraries:
  - Make sure you have the necessary libraries installed. You can install them using the following commands:
``` python
pip install beautifulsoup4
pip install openpyxl
```
- Save HTML Content:
  - Save the HTML content of the Amazon website by right-clicking on the webpage, selecting "Save As" (or using CTRL+S), and save the file in the same directory as your Python script.
  - Add the file name to the open() function in your code:

``` python
with open("your_amazon_page.html", "r", encoding="utf-8") as file:
```
- Inspect HTML Structure:
  - Inspect the HTML structure of the saved webpage to identify the relevant elements and their classes.
  - Update the find_all method with the correct HTML tags and class names. For example:

``` python
product_divs = soup.find_all("div", class_="your-product-container-class")
```
-Update Data Extraction:
  - Customize the code to extract the specific data you need from the webpage.
  - Adjust the find methods based on the structure of the HTML. For instance:

``` python
product_name = div.find("span", class_="your-product-name-class")
product_cost = div.find("span", class_="your-product-cost-class")
```
- Save to Excel:
  - Provide the desired Excel file name in the excel_file variable.
  - The code will create a new Excel file if it doesn't exist or append data to an existing one.

``` python
excel_file = "your_data_file.xlsx"
```
- Run the Script:
  - Execute the Python script in your terminal or IDE.
  - Ensure that the script has the necessary permissions to read and write files in the directory.

``` python
python your_script.py
```
- Check Excel File:
  - After running the script, check the specified Excel file for the scraped data.
  - The script appends data to the existing file or creates a new one if needed.

``` python
print(f"Data has been appended to {excel_file}")
```
</details>

<details>
    <summary><h2> Data Cleaning and Preparation </h2></summary>

  #### Tools Used - Excel

- The web scraped data is saved on a local excel sheet and is further inspected to clean the data, which is presented as follows:
   ![preprocessed_data](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/32438e20-ab6c-4fab-81f9-524d7929aa12)
  
- In the initial data preparation phase, we performed the following tasks:

  1. Data loading and inspection.
  2. Handling missing values.
  3. Data cleaning and formatting.

  ![processed_data](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/1f74106c-724a-4f3b-901e-e8d4b0229e83)
The above is the processed and cleaned data.
</details>

<details>
    <summary><h2> Exploratory Data Analysis </h2></summary>

  #### Tool Used - Power Bi Analytics
#### Goals of the project - 
EDA involved exploring the sales data to answer key questions, such as:
- What is the distribution of phone prices?
- Which phone company has the highest and lowest average cost of models?
- Which phone company has the highest and lowest average cost of models?
- Is there a correlation between reviews and ratings?
- How does the average rating vary among different phone companies?
- What is the distribution of phone models across different RAM and storage sizes?

#### Tool Used - Python
#### Libraries Used - Numpy,Pandas,seaborn
- Explored essential metrics such as storage capacity, reviews, ratings, RAM, cost, brand, and product details for a comprehensive understanding.
- By looking below we can see the correlation between all the factors taken into consideration for this analysis:
    ![correlation between all columns](https://github.com/itsajayy/Web_Scraping-and-Data_analysis/assets/135236892/c6e6060c-c4cd-4f9f-a6bf-de30affc208b)

- Statistical Insights:
  - Utilized numpy for statistical analysis, computing measures like mean, median, and standard deviation for each key metric.
  -Extracted valuable insights into the distribution and central tendencies of the data.
- Visualization:
  - Leveraged matplotlib to create insightful visualizations, including histograms, scatter plots, and bar charts, providing a clear representation of the data trends.
 
</details>

<details>
    <summary><h2> Visualization </h2></summary>

  ### Visualization
#### Tool used - Power Bi
- Created compelling visualizations using Power BI to illustrate trends and patterns in the mobile data.
- Utilized Power BI's interactive features for dynamic exploration of the dataset.
- Conducted a comparative analysis across the top 3 mobile brands, presenting visual insights into their strengths and weaknesses in terms of storage, reviews, ratings, RAM, and cost.
- Derived actionable recommendations based on the visualized findings, providing valuable insights for consumers, manufacturers, and industry analysts.

</details>

<details>
    <summary><h2> Exploratory Data Analysis (Summary)</h2></summary>
  
  ## Conclusion
 ### Results
 - From the visuals below we can see the most sold smartphoe, the most rated smartphone, the price range of all the smartphones provided by them, the most expensive smartphone as we the cheapest smartphone available on amazon from the top three brands on amazon.
   -    From Apple:
         ![min max apple cost in dataset](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/0cef367c-707d-4ec1-bd49-d17001f608ad)
        - Most Reviewed Smartphone : Apple iPhone 13
        - Most Expensive Smartphone: Apple iPhone 15 Pro Max 
        - Least Expensive Smartphone: Apple iPhone 13
        - Number of Colors offered: 87

   - From Samsung:
         ![min max samsung cost in dataset](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/777f683f-d9f1-483b-a72c-2952b7a32dc6)
        - Most Reviewed Smartphone : Samsung Galaxy M21
        - Most Expensive Smartphone: Samsung Galaxy Z Fold 5
        - Least Expensive Smartphone: Samsung Guru 1215
        - Number of Colors offered: 397
     
   - From Oppo:
        ![min max oppo cost in dataset](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/42641bb3-461c-48f1-afbf-21d6de55c418)
        - Most Reviewed Smartphone : Oppo F17
        - Most Expensive Smartphone:  Oppo Find N2 Flip
        - Least Expensive Smartphone: Oppo A11K
        - Number of Colors offered: 182

  - The spectrum of ratings given to each brand is shown below: 
        ![count of rating and brand](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/c7bcf245-eb71-46da-afee-9c00d7692233)
     - From the above graph we can see that the Apple has it's ratings starting from 3 on a scale of 5 while oppo has a few 2 and 1 star ratings compared to samsung.
   
  - The Average Rating and total number of ratings given to each brand is seen:
        ![count and average product ratings](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/296ddade-bcd8-4af9-8c69-ef67c7307d14)
      - A large chunk of products are rated 4 stars the average rating of iphones are much higher than that of Oppo and samsung. A conclusion can be drawn that Apple is highly rated and a more premium smartphone comapred to Oppo and Samsung.
  
  - The same is found out to the three companies with the amount of reviews mentioned:
        ![count and average product review](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/8e83e086-357d-4bd6-bc22-0b50d98f23d9)
    - Samsung is the most Reviewed smartphone brand with average reviews of each products of 2,400 while apple is the least reviewed with average reviews of each products of 5,200. A conclusion can be drawn that Samsung is frequently bought even more than Apple and Oppo products but people who buy apple products tend to review more comapared to other comapnies.
   
- We can also see the count of Refurbished and New products offered by all these three products:
       ![count of refurbished vs new](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/928a30a5-01f0-47cd-a454-d835fb8fbbc5)
     - Samsung has equal number of refurbished and new products while as apple only offers new products.
  
      
        
- **What are the specification that affecting phone prices**
 from our analysis using the correlation method, the major specification that affecting the price range are
       
   1. **RAM Size** the more expensive phone **(higher price range)** has a higher RAM size. From our analysis we found out that the higher the price range the higher the minimum ram size for phones.
       ![Count of ram vs price range](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/0ecc0e09-650e-46a4-8118-c94b51388c13)
  
   3. **Storage** the more expensive phone **(higher price range)** has a higher storage size. From our analysis we found out that the higher the price range the higher the minimum Storage capacity for phones.
        ![storage vs price range](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/92b01125-31f4-435d-878c-bceea7d68abd)

- **Color of the phone and Phone Price Range** 
- In general the color of the phone doesn't really much effect on the price range.
- But with a large variety of colors offered by Samsung there are more options for the buyers to customize the phone to their liking which might increase the number of sales.
- Larger variety of phone colors include a larger catalogue of phone which can be seen from the products available on Samsung was 397 while as apple was the least at 89.

## Recommendation 

**Ram Size**

The main factor that's affecting phone price range is **RAM SIZE** so if a phone so if a smartphone company would like to create a phone in a specific price range, the **RAM Size** is one of the specification that needs to be watched carefully, since it's a feature that affecting the price range of a phone from this dataset.

**Storage**

The second factor is **Storage** the more expensive the smartphone the higher the storage sizes it should have, since higher RAM needs more power from the battery, a smartphone company should adjust their storage and ram accordingly since they both are correlated.

**Reviews and Ratings**

The third factor is **Reviews and Ratings**. When purchasing a smartphone, we usually consider the quantity of reviews and ratings the device has received. Depending on how highly rated and how many reviews it has received, a smartphone's likelihood of being purchased What are the benefits and drawbacks of that smartphone, as well as how does it operate?

### Further Scope

1. By taking more factors such as screen size, battery capcity, camera offered we can dive deep into what factors are very crucial when it comes to buy a smart phone.
2. Build a Machine Learning model which can select a phone for you based on your speicifications.
3. Build a sentiment analysis model with the reivews and ratings using machine learning.  

</details>
