# Scraping Sneaker Deals: Building a Python eBay Web Scraper for Price Tracking and Other Details

![giant-sneaker-urban-environment](https://github.com/tasfiakatha/eBay-web-scraping/assets/120822849/df56842c-e464-44f5-a9ee-c58ece79f75f)

## Authors
[@tasfiakatha](https://github.com/tasfiakatha)

## Table of Contents
- [Business problem statement](https://github.com/tasfiakatha/eBay-web-scraping/edit/main/README.md#business-problem-statement)
- [Website link](https://github.com/tasfiakatha/eBay-web-scraping/edit/main/README.md#website-link)
- [Methods](https://github.com/tasfiakatha/eBay-web-scraping/edit/main/README.md#methods)
- [Quick look at the result](https://github.com/tasfiakatha/eBay-web-scraping/edit/main/README.md#quick-look-at-the-result)
- [Takeaways](https://github.com/tasfiakatha/eBay-web-scraping/edit/main/README.md#takeaways)
- [Blog post](https://github.com/tasfiakatha/eBay-web-scraping/edit/main/README.md#blog-post)
          
## Business problem statement
In the competitive landscape of the retail industry, staying ahead requires constant vigilance over market dynamics, especially pricing trends set by larger competitors. For small retailers like our client, manually tracking pricing information from giants like eBay for each product can be laborious and time-consuming. To address this challenge, I have developed a sophisticated web scraper tool tailored specifically for the needs of small retailers in the shoe industry.

The web scraper automates the collection of crucial product data, including pricing, demand metrics, reviews, and ratings, from major competitors' platforms. By running the scraper at regular intervals—daily or as desired—our client can effortlessly gather comprehensive insights into market trends without the need for manual intervention. The extracted data is organized and stored in a user-friendly CSV file, allowing our client to easily monitor pricing dynamics and adjust their own product prices accordingly.

This solution empowers small retailers to make informed pricing decisions swiftly and effectively, ensuring competitiveness in the ever-evolving market landscape. With the web scraper tool, our client can focus their time and resources on strategic initiatives to drive business growth, confident in their ability to navigate the competitive marketplace with precision and agility.

## Website link
[eBay shoes search results](https://www.ebay.com/sch/i.html?_from=R40&_nkw=shoes&_sacat=0&_odkw=nike&_osacat=0)

## Methods
I have built five key functions designed to extract specific information from the webpage using Beautiful Soup:

**1. get_title(soup):** This function locates and extracts the product title from the HTML content of the webpage. By identifying specific HTML tags and attributes, it accurately retrieves the title information.

**2. get_price(soup):** Similarly, this function employs Beautiful Soup to extract the product price from the HTML structure of the webpage. It navigates through the HTML elements, targeting the relevant tags and attributes to capture the price data effectively.

**3. get_availability(soup):** This function focuses on retrieving the availability or quantity sold of the product from the webpage. It utilizes Beautiful Soup to navigate the HTML hierarchy, pinpointing the necessary information regarding product availability.

**4. get_rating(soup):** Here, the function is dedicated to extracting the seller's rating from the eBay product page. It identifies and retrieves the HTML elements containing the seller's rating information accurately.

**5. get_review(soup):** Finally, this function targets the number of reviews for the seller present on eBay. 

In this project, I've detailed the process of scraping product information from a webpage. It all starts with setting up headers for the HTTP request and establishing a connection to the website using the Requests library. Once connected, I parsed the webpage's content into HTML format using BeautifulSoup, making data extraction structured and efficient. I located product links on the webpage using specific HTML tags and class attributes, storing them in an empty list called `links_list`. Moving forward, I collected information about each product listed on the webpage. I created a dictionary named `d` to store details like product title, price, availability, seller rating, and reviews. Iterating through each product link, I sent requests to the product page, leveraging BeautifulSoup to extract relevant information. To maintain data integrity, I handled missing or empty values in the 'title' column of the DataFrame. Finally, I converted the DataFrame into a CSV file named 'ebay_shoes.csv', ensuring easy access and further analysis of the scraped data.

## Quick look at the result
![image](https://github.com/tasfiakatha/eBay-web-scraping/assets/120822849/9dc34921-8173-41fc-8c3c-d56293398a7e)

## Takeaways
In a nutshell, this Python script simplifies the task of gathering important details from eBay listings. Using BeautifulSoup and requests, it quickly extracts information like product names, prices, availability, seller ratings, and reviews. It then organizes all this data neatly into a pandas DataFrame and saves it as a CSV file for easy review. Empowering small retailers with up-to-date automated information, this script facilitates everything from market research to competitive analysis, ensuring they remain agile and competitive in today’s dynamic marketplace.

## Blog post
You can find the tutorial blog post for this project [here](https://medium.com/@tasfiakatha04/scraping-sneaker-deals-building-a-python-ebay-web-scraper-for-price-tracking-and-other-details-47b95930ffa7)
