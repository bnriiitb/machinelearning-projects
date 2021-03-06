## Capstone Proposal
## Machine Learning Engineer Nanodegree


## Media Product Classification 
### Nagaraju Budigam
###                                              November 28th, 2017


## Project Overview

Note: This is the original problem that I am developing at production level. Due to company compliance policies original datasets are not exposed, however the provided datasets are resembling the original datasets.

Indix is a Product Intelligence company based in Seattle, that currently offers a cloud-based product information platform. It is also building a broad and deep product catalogue to enable mobile and desktop apps and websites to become product-aware. Indix provides access to APIs that enable developers to build product-aware applications. 
As mentioned above, Indix hosts the world’s largest collection of programmatically accessible structured product information in the cloud. The products in our database belong to 25 verticals and that translates approximately to 6000 sub-categories. Every product that we carry in our database gets stamped with information about the “category” it belongs to. 
Indix's services are centred on proprietary algorithms that structure crawled product data and a data-as-a-service business model.
The database offers coverage for most consumer retail product categories. The database also includes many industrial and business-to-business products. Indix provides brands and retailers with access to data such as specifications, facets, availability, assortment, promotions, and real-time pricing information. In comparison to offerings from Google, which are influenced by Google's utilization of relevance algorithms, or Amazon, which is limited to only the products in its own catalogue, Indix's infinite product catalogue helps all client-facing digital media and environments become more product-aware.



## Problem Statement

As Indix has the tons of data collected programmatically from web, it has become a challenging task to classifying a product into a particular category, which is very important to serve various use cases – like, helping search, performing product matching, providing category specific insights, and so on. 
From the project overview and project statement it is clear that, the problem of stamping every product in our catalogue into a category is a Classification problem in Machine Learning. We have a handful of techniques and methods in Machine Learning to tackle this kind of real world problems.
To be more specific, here the stamping every product in our catalogue is a Multi Class Classification problem.



## Data Description

The training dataset contains storeid, url, additionalAttributes, breadcrumbs and label features.


1. storeId - a unique number for identifying a website
2. additionalAttributes - Product attribute related to a particular product. These are key, value pairs that can be found in tabular format as product information for most products in e-commerce websites.

An example of additionalAttributes
{"ASIN": " B000JJRY9M",
"Amazon Bestsellers Rank": " in DVD & Blu-ray (See Top 100 in DVD & Blu-ray)",
"Average Customer Review": " Be the first to review this item",
"Classification": " Exempt",
"DVD Release Date": " 26 Feb. 2007",
"Format": " AC-3, Colour, Dolby, DVD-Video, PAL",
"Language": " English",
"Number of discs": " 1",
"Region": " Region 2 (This DVD may not be viewable outside Europe. Read more about
DVD formats.)",
"Run Time": " 287 minutes",
"Studio": " Hip-O Records"}

3. breadcrumbs- breadcrumb captured at the page. Breadcrumbs typically appear horizontally across the top of a Web page, often below title bars or headers.

An example of breadcrumb
subjects > travel > world regions > europe > european nations > france

4. label- The class to which a product belongs. Values belong to the finite set (‘books’,’music’,‘videos’,’rest’)

It is possible that for some products only one among (2) or (3) might be available. 

The problem statement is to classify the products into any one of the buckets

(i) Books
(ii) Music
(iii) Videos
(iv) Rest - A default class for products which doesn’t belong to (i),(ii) or (iii) category.



### Install

To run this code, it requires **Python 3.6** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. Make sure that you select the Python 3.x installer and not the Python 2.7 installer.

### Code

`media_product_classification.ipynb` notebook file contains the full implementation of the coding challenge.

### Run

In a terminal or command window, navigate to the top-level project directory `capstone/` (that contains this README) and run one of the following commands:

```bash
ipython notebook media_product_classification.ipynb
```  
or
```bash
jupyter notebook media_product_classification.ipynb
```

This will open the Jupyter Notebook software and project file in your browser.

### Data

**Features**
1. `storeId`: store id
2. `url`: product page url
3. `additionalAttributes`: additional attrvutes describing the product
4. `breadcrumbs`: bread crumb navigation data
5. `label`: label

**Target Variable**
4. `label`: category of the product
