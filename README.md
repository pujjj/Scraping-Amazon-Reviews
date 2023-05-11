# Scraping Amazon Reviews

In this repository I have built an Amazon scraper for reviews of macbook air using a python framework called scrapy. 

I have extracted the following features:
    
1. Reviewer’s name
2. Star rating
3. Title of the review
4. Reviews

Product chosen to scrape: Macbook Air

Product Link: https://www.amazon.in//dp/B08N5W4NNB

Product ASIN number: B08N5W4NNB

## Using the Amazon Spider
Make sure Scrapy is installed:
```bash
pip3 install scrapy
```
To create the project: 
```bash
scrapy startproject amazon
```
To create a spider:

Now we need a spider to crawl through the amazon page. So we instruct scrapy to build one for us using the genspider.

```bash
scrapy genspider reviews https://www.amazon.in/product-reviews/B08N5W4NNB 
```

This gives an empty spider python file - reviews.py

## Getting request headers of the product
We inspect the page to get the request headers of the product and at it to settings.py
![reqheaders](https://github.com/pujjj/Scraping-Amazon-Reviews/assets/97466150/1efa1bd2-6ed0-4cb4-a2a5-13824f1a59b2)
To convert the headers to a dictionary , first install scraper helper:
```bash
pip install scraper-helper
```

## Getting the css selectors of all the reviews
For this purpose we can use a chrome extension - SelectorGadget which is a CSS Selector generation.

With this we get the css selector of all reviews: 
```bash
[data-hook = "review"]
```
![cssselectors](https://github.com/pujjj/Scraping-Amazon-Reviews/assets/97466150/5e566371-af3a-476a-b254-f9517651f778)

## Running the spider 
To convert the scraped reviews to csv format:
```bash
scrapy crawl reviews -O reviews.csv
```
To convert reviews to json format:
```bash
scrapy crawl reviews -O reviews.json
```
