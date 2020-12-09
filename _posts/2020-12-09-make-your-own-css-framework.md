---
layout: post
title:  "How to Make your own CSS Framework - Part 1"
author: arvind
categories: [CSS, tutorial]
tags: [CSS]
image: assets/images/makecss/css.webp
bannerimage: assets/images/makecss/css.webp
description: "This article is a comprehensive guide on how one can go about making their own CSS framework"
featured: true
hidden: false
---


This article is the first part of a comprehensive guide on how to build your own CSS framework, starting from planning, designing all the way to coding. These are the things that I learnt while I built my own CSS Framework <a href="https://sleek.arvindrs.com/" target="_blank">Sleek</a>, which is completely useless.




## Introduction

CSS Framework is a must have tool for building a web application, especially if you are not a designer like me. In fact, I always start developing a new project by first choosing a JS and a CSS framework. There are a lot of good options out there, just to list a few:

* <a href="https://getbootstrap.com/" target="_blank" rel="nofollow">Bootstrap</a>
* <a href="https://www.bulma.io" target="_blank" rel="nofollow">Bulma</a>
* <a href="https://tailwindcss.com/" target="_blank" rel="nofollow">Tailwind</a>
* <a href="https://semantic-ui.com/" target="_blank" rel="nofollow">Semantic UI</a>

And there is my CSS framework too!

* <a href="https://sleek.arvindrs.com/" target="_blank">Sleek</a>

Unfortunately, it was really bad and no one used it, not even me. But I'm here to make sure you don't make the same mistakes that I did. In this article I'll talk about how I went about building one and how you can build yours too. We will see how to plan, design, and code your CSS Framework in detail. It will be a long and arduous journey, so buckle up!

Now, before you start spending hours on building one, I have a question for you:

### Why do you want to build a CSS Framework?

Personally, I built it because I wanted to learn how to build one. If you are here for that, good for you. It'll be a really great learning experience. 

Another reason might be that you have a design system of your own, some buttons and components that you designed and you want a small CSS framework so that you can easily use it easily for your other projects. That is also a really good motive.


But if you are here hoping to build a CSS framework that you want thousands of people to use, then I want you to ask yourself: **What unique feature does my CSS Framework offer**. Is it worth spending your precious time to build one? What is it that you are offerring that the dozens of frameworks out there don't already have? Maybe it's a new design, maybe it's a bunch of really good components, maybe it's a new way to write CSS. Unless your CSS framework is really good, it won't attract the attention of developers and it will end up going to the CSS Framework graveyard, next to mine. 


Now, for those of you who are still willing to make a framework, let's move on to the juicy stuff. 

## How to build a CSS Framework

The process of building a CSS Framework can be essentially summed up into these four broad category:


### Planning

A lot of planning is involved in the building of a CSS framework. We will be looking at these things in detail in another article. Just to get you started, these are some questions that you might wanna think about:

* **What type of framework do you want to build?** A simple, minimalistic one like <a href="https://purecss.io/" rel="nofollow" target="_blank"> PureCSS</a> or a full fledged powerhouse like <a href="https://getbootstrap.com/" target="_blank" rel="nofollow">Bootstrap</a>.

* **What components will your framework be offering?** Based on the answer to the previous question, you can either make a framework with just a couple different buttons and texts or complicated ones like navbar, accordions, dropdowns etc which might even require JS.

* **What architecture do you want to follow?** There are several architectures such as **SMACSS** (Scalable Modular Architecture for CSS) or **OOCSS** (Object Oriented CSS) or **Atomic CSS**. Tailwind uses atomic architecture whereas Bulma uses SMACSS. This is something that you need to decide upon before building your framework.




### Designing

Now this is the core part of the process. **You need to design your components!** You have to make buttons, specify the padding, margins, width, fonts, colors and so much more! This is the place where you can show your creativity! The main topics to tackle in the designing phase are:

* Designing Components
* Color Palette
* Typography

We won't be going in-depth since I'm not exactly a designer and I am not qualified to talk about these. But I'll mention the important things you need to lookout for while designing.


### Coding

This is the where we get hands on and start to implement the designs. This will be a long, boring and repititive task.

We will mainly have a look at:

* How to setup a node environment for your framework
* Setup SASS and facilitate the process of building css and css.min.
* Writing your framework
* Building a complete pipeline starting from compiling to hosting your project online.

### Documenting

This is something that I completely forgot about when I was building my framework Sleek. <a href="https://sleek.arvindrs.com/documentation" target="_blank">Sleek's documentation</a> is still incomplete because too many things got piled up and I never got time to finish. 

Documentation is just as important as anything else in this process. **No documentation means no on can use your framework!**. Whoever wants to use your framework will use the documentation for reference. So if the documentation isn't good, however good your framework might be, no one will use it. **Therefore, this has to go hand in hand with the coding process**.

Now, there are a few automatic document generators out there. But remember, you are building a CSS framework here. So your documentation website should use your CSS framework and not generate it manually. Therefore, automatic generators are a no go. You will have to do it on your own. If you do know a better method, comment it below or send it to me. I'll be more than happy to put it up here.



## Further Links

This is the first article out of a series of article I am going to write. I hope this gave you some food for thought and got you motivated for building your own CSS Framework! 

This is still a work in progress. I will be finishing up these articles soon so that you can get started building your own framework.

<a href="javascript:void(0)">How to make your own CSS Framework - Planning</a> (Coming on 11th December)

<a href="javascript:void(0)">How to make your own CSS Framework - Designing</a> (Coming on 13th December)

<a href="javascript:void(0)">How to make your own CSS Framework - Coding/Documenting</a> (Coming on 15th December)


In the meantime, you can go ahead and look at other resources or find out more about things I've mentioned in this article like SMACSS and OOCSS.