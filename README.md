# Scraping Sneaker Deals: Building a Python eBay Web Scraper for Price Tracking and Other Details

![giant-sneaker-urban-environment](https://github.com/tasfiakatha/eBay-web-scraping/assets/120822849/df56842c-e464-44f5-a9ee-c58ece79f75f)

## Business problem statement
In the competitive landscape of the retail industry, staying ahead requires constant vigilance over market dynamics, especially pricing trends set by larger competitors. For small retailers like our client, manually tracking pricing information from giants like eBay for each product can be laborious and time-consuming. To address this challenge, I have developed a sophisticated web scraper tool tailored specifically for the needs of small retailers in the shoe industry.

The web scraper automates the collection of crucial product data, including pricing, demand metrics, reviews, and ratings, from major competitors' platforms. By running the scraper at regular intervals—daily or as desired—our client can effortlessly gather comprehensive insights into market trends without the need for manual intervention. The extracted data is organized and stored in a user-friendly CSV file, allowing our client to easily monitor pricing dynamics and adjust their own product prices accordingly.

This solution empowers small retailers to make informed pricing decisions swiftly and effectively, ensuring competitiveness in the ever-evolving market landscape. With the web scraper tool, our client can focus their time and resources on strategic initiatives to drive business growth, confident in their ability to navigate the competitive marketplace with precision and agility.

## Website link
https://www.ebay.com/sch/i.html?_from=R40&_nkw=shoes&_sacat=0&_odkw=nike&_osacat=0

## Methods
I have built five key functions designed to extract specific information from the webpage using Beautiful Soup:

**1. get_title(soup):** This function locates and extracts the product title from the HTML content of the webpage. By identifying specific HTML tags and attributes, it accurately retrieves the title information.

**2. get_price(soup):** Similarly, this function employs Beautiful Soup to extract the product price from the HTML structure of the webpage. It navigates through the HTML elements, targeting the relevant tags and attributes to capture the price data effectively.

**3. get_availability(soup):** This function focuses on retrieving the availability or quantity sold of the product from the webpage. It utilizes Beautiful Soup to navigate the HTML hierarchy, pinpointing the necessary information regarding product availability.

**4. get_rating(soup):** Here, the function is dedicated to extracting the seller's rating from the eBay product page. It identifies and retrieves the HTML elements containing the seller's rating information accurately.

**5. get_review(soup):** Finally, this function targets the number of reviews for the seller present on eBay. 
