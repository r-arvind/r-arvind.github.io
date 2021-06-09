---
layout: post
title:  "Four SEO Practices every Frontend Developer should Follow"
author: arvind
categories: [SEO, tutorial]
tags: [SEO]
image: assets/images/seo-tips/seo.png
bannerimage: assets/images/seo-tips/seo.webp
description: "Four basic tips that every frontend developer should follow and put into practice to improve SEO of your website"
featured: true
hidden: false
---


SEO is critical to any website. You might be using HTML and vanilla javascript or fancy frameworks like react and vue, but in order to make sure that people see it, it needs to show up on google search.

A recent study shows that more than 70% of the people prefer changing their search query rather than going to the second page of google. Therefore, we have to make sure that our website shows up on the first page of google.

In this article, I'll take you through five simple tips, which will greatly improve the SEO compatibility of your website.


## 1. Header Tag

The header tag `<head></head>` contains all the information about the html page. Some of the important tags important for SEO are listed below.

```html
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<title>Home | Arvind Ram Sankar</title>
<meta name="description" content="Description of your website">
<link rel="canonical" href="https://www.example.com/">
</head>
```

#### Title

The title tag `<title></title>` is nothing but the title of your website. It is displayed on the browser tab. The title should be relevant to your website and include all the necessary keywords.

<figure class="image">
<img src="{{site.imageurl}}/seo-tips/title.png" alt="An example of Title tag for SEO" />
 <figcaption>Example of Title Tag</figcaption>
</figure>

For example, if your website is for a specific brand, make sure your title always has the brand name. The home page should be <b>"Home \| Brand"</b>, the about page should be <b>"About Us \| Brand"</b> and so on.

#### Meta Description

Meta description is another extremely important tag. Whenever you search for something in google, the small description that you see below each link is the Meta description of the website. This is what the users read before clicking on the link.

<figure class="image">
<img src="{{site.imageurl}}/seo-tips/meta.png" alt="An example of Title tag for SEO" />
 <figcaption>Example of Meta Description</figcaption>
</figure>

Always keep the meta description between 90-160 characters long. Google only shows the first 160 characters of your description and cuts out the rest.

A good meta description should have all the relevant keywords that will make the users click on the link as soon as they read it.


#### Canonical URL

Let's take a simple example to understand this tag. Let's say you write an amazing blog post. You post it on your website. Then you post on Medium, Blogger and some of the other blogging platforms. Now, there are multiple copies of the same content existing on different websites.

You don't want the google bot to think that one website has copied from the other or vice versa. And you also don't want the same content to compete against each other for top ranking on search results page.  Therefore, if you put the `<link rel="canonical" href="https://example.com">`, the google search engine will know that they are the same content existing in two different places. The `href` provided in the tag is considered to be the master copy. And you need to put the canonical tag in all the other websites where you've duplicated the content.


## 2. Image Alt Attribute

Always add alt tags to your images. Image alt tags are extremely important. It looks something like this:

```html
    <img src="someimage.jpg" alt="Image of a flower"> </img>
```
The google bots which crawl your websites cannot see what the image is about. Instead, they use the alt tag to understand what the image is about. Therefore, it is important that you put these alt tags to all the images on your website.

## 3. `rel` Attribute for Links

<i>SEO is all about links.</i> In order to have a higher SEO ranking, you need to gain links from various websites. Adding links to your website provides helps improve SEO of the linked website.

```html
<a href="https://google.com" rel="nofollow noopener"> Link </a>
```

`rel="nofollow"` is essentially like a SEO blocker. If you see a website that has links to your website but has the `rel="nofollow"` attribute, that means it doesn't contribute to your SEO. Similarly putting it on your website won't pass on SEO juice to the linked website. 

Make sure to use this cleverly and always keep this in mind when you are looking for backlinks to your website.

## 4. Sitemaps and Robots.txt

Sitemaps, just like its name suggests is a map to your site. It is usually located at `/sitemap.xml`. For example, the sitemap for my website is located at <a href="https://www.arvindrs.com/sitemap.xml" target="_blank"> arvindrs.com/sitemap.xml </a>. It contains a list of all the URLs located in my website. 
Since my website is built using Jekyll, I use the <a href="https://github.com/jekyll/jekyll-sitemap" target="_blank">jekyll-sitemap</a> plugin to automatically generate these sitemaps.

Google and other search engines use web crawlers to index and rank your website. <b>Robots.txt</b> is a file which contains guidelines on how these crawlers should index your website. You can mention which URLs to crawl and which shouldn't be crawled. You can checkout my Robots.txt file at <a href="https://arvindrs.com/robots.txt" target="_blank">arvindrs.com/robots.txt</a>. It doesn't really have anything because I don't have any restrictions for crawling.

Now, although both of these files don't affect SEO directly, these are really helpful for web crawlers when they index your website. It is always a good practice to add both the files to your website.


## Conclusion

In this article, we saw four basic ways to perform search engine optimization as a front-end engineer. We should always follow these good practices to make sure that our content has a good ranking.

But remember, <b>these four points are barely the tip of the iceberg</b>. There are so many things that you need to take care of when performing search engine optimization. There are social media tags, open graph tags, h1 tags and so much more. So, keep exploring!
