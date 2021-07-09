# HTML IMAGES
![Images](img/htmlimages.png)
## Inserting Images into Web Pages
Images enhance visual appearance of the web pages by making them more interesting and colorful.


The `<img>` tag is used to insert images in the HTML documents. It is an empty element and contains attributes only. The syntax of the `<img>` tag can be given with:

`<img src="url" alt="some_text">`

**The following example inserts three images on the web page:**

1- `<img src="kites.jpg" alt="Flying Kites">`
2- `<img src="sky.jpg" alt="Cloudy Sky">`
3- `<img src="balloons.jpg" alt="Balloons">`

Each image must carry at least two attributes: the `src` attribute, and an `alt` attribute.

The `src` attribute tells the browser where to find the image. Its value is the URL of the image file.

Whereas, the `alt` attribute provides an alternative text for the image, if it is unavailable or cannot be displayed for some reason. Its value should be a meaningful substitute for the image.

## Setting the Width and Height of an Image
The `width` and `height` attributes are used to specify the width and height of an image.

The values of these attributes are interpreted in pixels by default.

**Example**
1- `<img src="kites.jpg" alt="Flying Kites" width="300" height="300">`
2- `<img src="sky.jpg" alt="Cloudy Sky" width="250" height="150">`
3- `<img src="balloons.jpg" alt="Balloons" width="200" height="200">`


You can also use the style attribute to specify width and height for the images. It prevents style sheets from changing the image size accidently, since inline style has the highest priority.
**Example**
1- `<img src="kites.jpg" alt="Flying Kites" style="width: 300px; height: 300px;">`
2- `<img src="sky.jpg" alt="Cloudy Sky" style="width: 250px; height: 150px;">`
3- `<img src="balloons.jpg" alt="Balloons" style="width: 200px; height: 200px;">`


## Using the HTML5 Picture Element
Sometimes, scaling an image up or down to fit different devices (or screen sizes) doesn't work as expected. Also, reducing the image dimension using the `width` and `height` attribute or property doesn't reduce the original file size. To address these problems HTML5 has introduced the `<picture>` tag that allows you to define multiple versions of an image to target different types of devices.

The `<picture>` element contains zero or more `<source>` elements, each referring to different image source, and one `<img>` element at the end. Also each `<source>` element has the media attribute which specifies a media condition (similar to the media query) that is used by the browser to determine when a particular source should be used. Let's try out an example:

`<picture>`
  `  <source media="(min-width: 1000px)" srcset="logo-large.png">`
   ` <source media="(max-width: 500px)" srcset="logo-small.png">`
   ` <img src="logo-default.png" alt="My logo">`
`</picture>`



# Practical information


![seo](img/seo.jpeg)
## What Is SEO? A Beginner’s Guide to Search Engine Optimization
This article aims to give an overview of what SEO is, why it is important, how Google functions, and a guide to what you can do. This article is not a definitive guide to every aspect and subtlety of SEO — search engine optimization. This is a vast subject that cannot be fully covered in a single article.

**Definition of SEO**
SEO is the art and science of persuading search engines such as Google, Bing, and Yahoo, to recommend your content to their users as the best solution to their problem. 

**If you want search engines to offer your content in results, you need to do three things:**
- Ensure these search engines understand who you are and what you offer.

- Convince them that you are the most credible option for their users.

- Make your content deliverable.


## What Is SEO
This article aims to give an overview of what SEO is, why it is important, how Google functions, and a guide to what you can do. This article is not a definitive guide to every aspect and subtlety of SEO — search engine optimization. This is a vast subject that cannot be fully covered in a single article.

## Definition of SEO
SEO is the art and science of persuading search engines such as Google, Bing, and Yahoo, to recommend your content to their users as the best solution to their problem. 

If you want search engines to offer your content in results, you need to do three things:

Ensure these search engines understand who you are and what you offer.

Convince them that you are the most credible option for their users.

Make your content deliverable.

How high in the rankings and how often you appear is merit-based; these engines will show the results they consider to be the best fit for their users.

 
## Why is SEO important? 
Search Engine Optimization brings you the most precious traffic (also known as organic traffic), which is "free" — when a search engine shows your content to its users in the organic part of a SERP (Search Engine Results Page), you do not pay for the ranking. When the user clicks on the result and visits your site, you do not pay Google for a visit. And that briefly describes what is SEO used for.

On that same SERP, there are often paid results; they are identifiable by the ‘Ad’ icon to the left. When a user clicks on a paid result and visits the site, the advertiser pays the search engine for that visit.
![seo](https://static.semrush.com/blog/uploads/media/44/2d/442dfbdcfc1ae10fcda29e24f50978c9/serp.webp)

## How Search Engines Work 
The fundamental aim of search engines is to satisfy its users. They want to provide the best results when a user searches for something. When someone uses a search engine, such as Google, Bing, or Yahoo, they are looking for the solution to a problem or the answer to a question. These engines want to provide the most helpful, relevant, and credible answer or solution.


## Keywords
In SEO, we often refer to ‘keywords’ — this is slightly misleading. ‘Search queries’ is a much better term. We are not looking at individual words; we are looking at combinations of words that express a problem or a question.


# Using analytics to understand visitors
![analytics](https://www.klipfolio.com/sites/default/files/blog/banner-ga-data-with-klipfolio.png)
### What is web analytics?
Web analytics is the process of analyzing the behavior of visitors to a website. This involves tracking, reviewing and reporting data to measure web activity, including the use of a website and its components, such as webpages, images and videos.

Data collected through web analytics may include traffic sources, referring sites, page views, paths taken and conversion rates. The compiled data often forms a part of customer relationship management analytics (CRM analytics) to facilitate and streamline better business decisions.


Web analytics enables a business to retain customers, attract more visitors and increase the dollar volume each customer spends.

Analytics can help in the following ways:

- Determine the likelihood that a given customer will repurchase a product after purchasing it in the past.

- Personalize the site to customers who visit it repeatedly.

- Monitor the amount of money individual customers or specific groups of customers spend.

- Observe the geographic regions from which the most and the least customers visit the site and purchase specific products.

- Predict which products customers are most and least likely to buy in the future.

The objective of web analytics is to serve as a business metric for promoting specific products to the customers who are most likely to buy them and to determine which products a specific customer is most likely to purchase. This can help improve the ratio of revenue to marketing costs.

In addition to these features, web analytics may track the clickthrough and drilldown behavior of customers within a website, determine the sites from which customers most often arrive, and communicate with browsers to track and analyze online behavior. The results of web analytics are provided in the form of tables, charts and graphs.

### Web analytics process
The web analytics process involves the following steps:

1- **Setting goals.** The first step in the web analytics process is for businesses to determine goals and the end results they are trying to achieve. These goals can include increased sales, customer satisfaction and brand awareness. Business goals can be both quantitative and qualitative.

2- **Collecting data.** The second step in web analytics is the collection and storage of data. Businesses can collect data directly from a website or web analytics tool, such as Google Analytics. The data mainly comes from Hypertext Transfer Protocol requests -- including data at the network and application levels -- and can be combined with external data to interpret web usage. For example, a user's Internet Protocol address is typically associated with many factors, including geographic location and clickthrough rates.

3- **Processing data.** The next stage of the web analytics funnel involves businesses processing the collected data into actionable information.

4- **Identifying key performance indicators (KPIs).** In web analytics, a KPI is a quantifiable measure to monitor and analyze user behavior on a website. Examples include bounce rates, unique users, user sessions and on-site search queries.


5- **Developing a strategy.** This stage involves implementing insights to formulate strategies that align with an organization's goals. For example, search queries conducted on-site can help an organization develop a content strategy based on what users are searching for on its website.

6- **Experimenting and testing.** Businesses need to experiment with different strategies in order to find the one that yields the best results. For example, A/B testing is a simple strategy to help learn how an audience responds to different content. The process involves creating two or more versions of content and then displaying it to different audience segments to reveal which version of the content performs better.
