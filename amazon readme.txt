Web Scraping Project: Amazon Products & Job Listings
Overview
This project demonstrates two separate web scraping tasks:

Amazon Product Scraping: Scraping product data from Amazon search result pages using Selenium and BeautifulSoup. The script extracts details such as product name, price, rating, and reviews from multiple pages.
Apify Job Listings Scraping: Using the Apify API to scrape job listings for a specific position (e.g., "Web Developer") in a given location (e.g., "San Francisco"). The data is stored in a structured JSON format and can be converted into a CSV for analysis.
Technologies Used
Python 3.x
Selenium: For automating web browser interaction to scrape data from dynamic pages.
BeautifulSoup: For parsing HTML and extracting data from Amazon's static page source.
Apify API: For accessing job listings through a prebuilt Apify actor.
Pandas: For data manipulation and exporting scraped data to CSV.
Random and Time: For adding delays between requests to avoid being blocked or flagged as a bot.
Amazon Product Scraping
The Amazon Scraping script uses Selenium and BeautifulSoup to extract product details from Amazon search results. The data includes the product's name, price, rating, and reviews.

Steps to Scrape Amazon Product Data
Set Up Selenium: Selenium automates browsing. The script runs in headless mode to avoid opening a visible browser window.
Extract Product Data: The script extracts product details from each page using BeautifulSoup.
Random Delays: Randomized delays between page loads mimic human browsing and reduce the chance of being blocked.
Save Data: The extracted data is saved in a CSV file named amazon_products.csv.
How to Run:
Install the necessary libraries:

bash
Copy
pip install selenium webdriver-manager beautifulsoup4 pandas
Run the script:

bash
Copy
python amazon_scraper.py
The results will be saved as amazon_products.csv in the same directory.

Apify Job Listings Scraping
The Apify Scraping script utilizes the Apify API to fetch job listings for specific roles (e.g., "Web Developer") in a given location (e.g., "San Francisco").

Steps for Apify Job Scraping
Initialize Apify Client: The script uses the Apify API client to call a predefined actor (in this case, hMvNSpz3JnHgl5jkh) to scrape job listings.
Actor Input: The input includes job position, location, and country.
Data Extraction: After the scraping is complete, the script collects the data from the dataset and saves it as a JSON file.
Save Results: The job listings are saved as scraped_data.json and can be optionally converted to a Pandas DataFrame and exported as a CSV file.
How to Run:
Install the necessary libraries:

bash
Copy
pip install apify-client pandas
Replace "apify_api_VcZrdN96kkUnvKBTGI8oiuovfwFu2K3XDMiX" with your Apify API token.

Run the script:

bash
Copy
python apify_job_scraper.py
The scraped data will be saved as scraped_data.json and can also be exported as a CSV.

File Structure
plaintext
Copy
.
├── amazon_scraper.py  # Script for scraping Amazon product data
├── apify_job_scraper.py  # Script for scraping job listings using Apify API
├── amazon_products.csv  # CSV file with scraped Amazon product data
└── scraped_data.json  # JSON file with scraped job listing data
Contributing
Feel free to fork the project, open issues, and submit pull requests to enhance or extend the project.

License
This project is licensed under the MIT License – see the LICENSE file for details.

Contact
For any inquiries or suggestions, please feel free to reach out to the project creator.