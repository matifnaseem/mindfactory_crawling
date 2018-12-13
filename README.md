# Mindfactory.de Crawler
This repository contains a crawler for [Mindfactory](https://www.mindfactory.de), a German ecommerce shop (for computer hardware). The crawler extracts the data contained on every single product page and stores the scraped products in a SQLite database consisting of two tables.  

Each product has the following properties:  
* ID (SQLite identifier)
* URL
* Product name
* Brand name
* EAN
* SKU
* Items sold (Count)
* People watching (Count)
* RMA quote (in percent)
* Price  

Additionally, for every product all reviews are collected and stored in a separate SQLite table. A entry in this table has the following properties:
* Product ID (Reference to the corresponding ID in the product table)
* Stars (Rating, from 0 to 5)
* Text
* Author
* Date
* Verified (actually bought the product at Mindfactory)

# Prerequisites  
* Python3
* scrapy
* SQLite3

# Run the scraper  
    scrapy crawl mindfactory_products
