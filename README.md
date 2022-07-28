# AirBnB - Ratings Hosts and Superhosts
![photo of airbnb host Yoshiko][hosts]

Kaggle provides public datasets from Airbnb for [Boston](https://www.kaggle.com/datasets/airbnb/boston) and [Seattle](https://www.kaggle.com/datasets/airbnb/seattle) These datasets contain information about

* Listings, including full descriptions and average review score
* Reviews, including unique id for each reviewer and detailed comments
* Calendar, including listing id and the price and availability for that day

In this article we will take a closer look at the the listings data.

1. What influences average review scores?
1. Superhost and hosts: In what way are they different?
  * Which amneties are offered?
  * Are superhosts super-expensive?
3. What influences the superhost staus?

The datasets have a good quality, but of course some preparations were necessary to work with the data.

## What influences average review scores?
In addition to written reviews guests can rate their stay in different categories. More information about this can be found [here](https://www.airbnb.com/help/article/1257/star-ratings). To answer that question, a machine learnig model has been trained to compute the review score based on the features from the listings files. The most important features in the model and their influence on the model's result are depicted in the picture below. 

![Beeswarm plot of features affecting review scores](beeswarm-rating.png)

The most relevant features in the model were:
1. host_listings_count
1. host_is_superhost
1. host_response_rate
1. price 

High number of listings tend to decrease the review score. Hosts with a high response rate usually receive better review scores. Some cheap listings had a negative effect on the their review score. Of special interest for us is the second feature 'host_is_superhost'. According to AirBnB superhosts are:

> "Anyone who’s extremely welcoming and experienced at making guests feel like they belong, or anyone who can conjure up an extraordinary Airbnb Experience can become a Superhost.
> No need to apply—you simply earn Superhost status by **doing things like receiving positive reviews, being responsive, and avoiding cancellations** where possible."  

We will have a closer look at these superhosts in the following section.

## Superhosts and hosts: In what way are they different?
AirBnB states that one element of becoming a superhost are positive reviews. Positive reviews should lead to good review scores. 

![History plot of review scores](histplot-review-sccores.jpg)

[hosts]: hosts.jpg "airbnb host Yoshiko https://www.flickr.com/photos/tobin/14188971889 Attribution-ShareAlike 2.0 Generic (CC BY-SA 2.0)"




## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/schumadi/schumadi-schumadi.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/schumadi/schumadi-schumadi.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
