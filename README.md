
# Mars Data Web Scraping and Analysis Project

## Introduction

This project demonstrates a multi-step approach to web scraping and data analysis, focusing on two key areas: scraping Mars-related news and analyzing Martian weather data. Splinter, BeautifulSoup, Pandas, and Matplotlib are leveraged to scrape, clean, analyze, and visualize data. This portfolio project serves as an example of skills relevant for a job application in data mining and web scraping.

## Tools and Libraries Used

- **Python**: Programming language for all aspects of the project.
- **Splinter**: Browser automation tool to interact with websites programmatically.
- **BeautifulSoup**: HTML parser used for web scraping.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib**: Data visualization.

## Project Workflow

### Web Scraping Mars-Related News

1. **Initialize the Web Browser**: Using Splinter, the Chrome browser is initialized to automate website interactions.

    ```python
    browser = Browser('chrome', executable_path=r"C:\path\to\chromedriver.exe")
    ```

2. **Navigate to Target Website**: Visit the Mars news site to scrape news titles and teaser text.

    ```python
    url = 'https://static.bc-edx.com/data/web/mars_news/index.html'
    browser.visit(url)
    ```

3. **HTML Parsing**: BeautifulSoup is used to parse the HTML content.

    ```python
    mars_soup = soup(html, 'html.parser')
    ```

4. **Data Extraction**: Iterate through the webpage to locate and extract news titles and teaser text into a list of dictionaries.

    ```python
    for article in mars_soup.find_all('div', class_='list_text'):
        # Extract and store data
    ```

### Web Scraping Mars Temperature Data

1. **Navigate to Another Target Website**: Visit a different Mars website to scrape temperature data.

    ```python
    url = 'https://static.bc-edx.com/data/web/mars_facts/temperature.html'
    browser.visit(url)
    ```

2. **HTML Parsing**: Parse the HTML content for temperature data.

    ```python
    temp_soup = soup(html, 'html.parser')
    ```

3. **Table Extraction**: Loop through the rows of the HTML table and extract the temperature data into a list.

    ```python
    for row in rows:
        # Extract and store data
    ```

### Data Cleaning and Transformation

1. **Load into DataFrame**: Load the scraped table data into a Pandas DataFrame.

    ```python
    mars_dataframe = pd.DataFrame(empty_list, columns = [...])
    ```

2. **Data Type Conversion**: Convert columns to appropriate data types for analysis.

    ```python
    mars_dataframe['column_name'] = mars_dataframe['column_name'].astype('new_type')
    ```

### Data Analysis and Visualization

1. **Statistical Analysis**: Using Pandas, answer questions like the number of Martian months, the number of days' worth of data, and average temperatures.

    ```python
    months_on_mars = mars_dataframe["month"].value_counts().sort_index()
    ```

2. **Data Visualization**: Use Matplotlib to create a bar graph showing the average temperature by month on Mars.

    ```python
    month_min_temp['min_temp'].plot(kind = 'bar')
    ```

## Conclusion

This project demonstrates a comprehensive set of skills in web scraping, data cleaning, data analysis, and data visualization. It highlights the ability to not only scrape web data but also to analyze and interpret it, making it an ideal portfolio piece for a job in data mining or web scraping.
