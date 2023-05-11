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
We inspect the page to get the request headers of the product 
![reqheaders](https://github.com/pujjj/Scraping-Amazon-Reviews/assets/97466150/1efa1bd2-6ed0-4cb4-a2a5-13824f1a59b2)
To convert the headers to a dictionary , first install scraper helper:
```bash
pip install scraper-helper
```

