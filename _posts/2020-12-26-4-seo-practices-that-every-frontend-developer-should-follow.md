---
layout: post
title:  "Four SEO Practices every Frontend Developer should Follow"
author: arvind
categories: [SEO, tutorial]
tags: [SEO]
image: assets/images/seo-tips/seo-for-developers.png
# bannerimage: assets/images/seo-tips/seo.webp
description: "Four basic tips that every frontend developer should follow and put into practice"
featured: true
hidden: false
---


SEO is critical to any website. You might be using HTML and vanilla javascript or fancy frameworks like react and vue, but in order to make sure that people see it, it needs to show up on google search.

A recent study shows that more than 70% of the people prefer changing their search query rather than going to the second page of google. Therefore, we have to make sure that our website shows up on the first page of google.

In this article, I'll take you through five simple tips, which will greatly improve the SEO compatibility of your website.


## 1. Header Tag

The header tag `<head>..</head>` contains all the information about the html page. Some of the important tags important for SEO are listed below.

#### Meta Title and Meta Description
#### Canonical URL
#### Title
#### Viewport


Different people use different browsers, it maybe Firefox, Chrome, Safari or even Internet Explorer. We need to make sure that our style looks the same everywhere. This is where the CSS Reset comes in.

CSS Reset does exactly what it sounds like, it resets the style so that we have **a uniform and a consistent style** across all types of browsers and devices.

The code below shows what a CSS reset might look like. This is just a small subset. There are a lot of other components that require reset, for example tables, captions, textinput etc.

```css
/* CSS reset */
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,form,fieldset,input,textarea,p,blockquote,th,td { 
    margin:0;
    padding:0;
}
html,body {
    margin:0;
    padding:0;
}
ol,ul {
    list-style:none;
}
h1,h2,h3,h4,h5,h6 {
    font-size:100%;
    font-weight:normal;
}
```

We will be using <a href="https://necolas.github.io/normalize.css/" target="_blank" rel="nofollow">**Normalize CSS**</a>, which a really small and an amazing reset. You can checkout the code for Normalize <a href="https://github.com/necolas/normalize.css/blob/master/normalize.css" target="_blank" rel="nofollow">here</a>. It is well documented and you'll be able to clearly see what components are being reset to what values.

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

If you managed to read till this point, I hope this article gives some insight into what goes into planning a CSS framework. When you finish your planning, you should have an idea about the components that you will be including in your framework and have some clarity on different CSS architectures. 

In the next article, we will talk about some basic design guidlines after which we will start coding the framework in SASS.

## Further Links

This is the second article out of a series of article I am going to write. I hope this gave you more insight into how to plan out your framework.

This is still a work in progress. I will be finishing up these articles soon so that you can get started building your own framework.

<a href="javascript:void(0)">How to make your own CSS Framework - Designing</a> (Coming on 14th December)

<a href="javascript:void(0)">How to make your own CSS Framework - Coding/Documenting</a> (Coming on 16th December)