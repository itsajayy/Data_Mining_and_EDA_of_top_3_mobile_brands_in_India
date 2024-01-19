# Delving into Amazon's Best-Selling MObile brands in India through Webscraping and Data Exploration

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

- Save HTML Content:
  - Save the Amazon webpage by right-clicking and selecting "Save As" into the same directory as your script.
  - Update the file name in the 'open()' function in your Python script.

- Inspect HTML Structure:
  - Examine the HTML structure of the saved webpage to identify relevant elements and classes.
  - Adjust the 'find_all' and 'find' methods in your script based on the HTML structure.

- Run the Script:
  - Execute the Python script in your terminal or IDE using python your_script.py.
  - Ensure the script has permissions to read and write files in the directory.

- Check Excel File:
  - After running the script, verify the specified Excel file for the scraped data.
  - The script appends data to an existing file or creates a new one if needed

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
  
  ## EDA Conclusion
 ### Conclusion
 - From the visuals below we can see the most sold smartphoe, the most rated smartphone, the most expensive smartphone as we the cheapest smartphone available on amazon from the top three brands on amazon.
   -    From Apple:
         ![min max apple cost in dataset](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/0cef367c-707d-4ec1-bd49-d17001f608ad)

   - From Samsung:
         ![min max samsung cost in dataset](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/777f683f-d9f1-483b-a72c-2952b7a32dc6)
     
   - From Oppo:
        ![min max oppo cost in dataset](https://github.com/itsajayy/Web_Scraping-and-EDA/assets/135236892/42641bb3-461c-48f1-afbf-21d6de55c418)

  - We can also see the spectrum of ratings given to each brand.
        

- **What are the specification that affecting phone prices**
 from our analysis using the correlation method and seaborn heatmap, the major specification that affecting the price range are 
       
   1. **RAM Size** the more expensive phone **(higher price range)** has a higher RAM size. From our analysis we found out that the higher the price range the higher the minimum ram size for phones.
        
   2. **Storage** the more expensive phone **(higher price range)** has a higher storage size. From our analysis we found out that the higher the price range the higher the minimum Storage capacity for phones. 
   
- **Color of the phone and Phone Price Range** 
In general the color of the phone doesn't really much effect on the price range.

- **The Best Selling Smartphones from the top three brands**

## Recommendation 

**Ram Size**

The main factor that's affecting phone price range is **RAM SIZE** so if a phone so if a smartphone company would like to create a phone in a specific price range, the **RAM Size** is one of the specification that needs to be watched carefully, since it's a feature that affecting the price range of a phone from this dataset

**Storage**

The second factor is **Storage** the more expensive the smartphone the higher the storage sizes it should have, since higher RAM needs more power from the battery, a smartphone company should adjust their storage and ram accordingly since they both are correlated.

**Reviews and Ratings**

The third factor is **Reviews and Ratings**. When purchasing a smartphone, we usually consider the quantity of reviews and ratings the device has received. Depending on how highly rated and how many reviews it has received, a smartphone's likelihood of being purchased What are the benefits and drawbacks of that smartphone, as well as how does it operate?

</details>
