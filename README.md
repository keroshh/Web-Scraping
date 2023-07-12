# Web Scraping Laptop Data from Vatan Computer

This Python script scrapes laptop data from the Vatan Computer website using web scraping techniques. It retrieves information such as the product price, brand, screen size, disk size, RAM size, processor generation, processor type, and operating system. The scraped data is then stored in an Excel file for further analysis.

## How it Works

The program follows these steps:

1.  Imports the necessary libraries: `BeautifulSoup` for web scraping, `lxml` for HTML parsing, `requests` for making HTTP requests, and `pandas` for data manipulation.
    
2.  Initializes an empty list called `data` to store the scraped data.
    
3.  Initializes variables `a` and `site` for iteration and site identification, respectively.
    
4.  Enters a loop that runs until `a` reaches the value of 20. This loop scrapes data from multiple pages.
    
5.  Sets the `headers` dictionary with a user-agent string to mimic a web browser.
    
6.  Makes a GET request to the Vatan Computer website URL using `requests.get()`.
    
7.  Parses the response content using `BeautifulSoup` with the `lxml` parser.
    
8.  Navigates through the HTML structure to locate the elements containing the desired product details.
    
9.  Iterates over the product elements found on the page and extracts the product link.
    
10.  Makes another GET request to the product link and parses the content using `BeautifulSoup`.
    
11.  Extracts the product price and brand from the parsed content.
    
12.  Locates a table element containing the detailed specifications of the product and extracts the relevant information.
    
13.  Appends the extracted data as a list to the `data` list.
    
14.  After the loop completes, creates a `DataFrame` from the `data` list using `pandas`.
    
15.  Specifies the column names for the `DataFrame`.
    
16.  Saves the scraped data as an Excel file named "vatan.xlsx" using the `to_excel()` function.
    

## Getting Started

To run the program and scrape laptop data from the Vatan Computer website, follow these steps:

1.  Install Python (version 3.6 or later) on your machine.
    
2.  Clone this repository or create a new Python file and copy the provided code into the file.
    
3.  Open a terminal or command prompt and navigate to the directory where the Python file is located.
    
4.  Install the required libraries by running the following command:
    
   
    
    `pip install beautifulsoup4 lxml pandas requests` 
    
5.  Run the program using the following command:
    

    
    `python your_file_name.py` 
    
    Replace `your_file_name` with the actual name of your Python file.
    
6.  The program will start scraping the laptop data from the Vatan Computer website and save it as an Excel file named "vatan.xlsx" in the same directory.
    

## Requirements

-   Python 3.6 or later
-   beautifulsoup4
-   lxml
-   pandas
-   requests

## License

This project is licensed under the MIT License. See the [LICENSE](https://chat.openai.com/LICENSE) file for details.
