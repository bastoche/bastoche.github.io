---
layout: post
title:  "Lean in Japan"
date:   2017-11-05 14:32:33
categories: lean
comments: true
---

I have spent a week touring the Nagoya area to visit companies applying the toyota production system. They varied in size and industry, but had the following common traits:
- they are not doing this for fun or because some consultant told them so, but to survive
- they are passionate about their products, from steel coils to second hand books

In this post, I will share what I saw over there on the shop floor, and what a software engineering team might learn from it. Here's the gist of it:
> Most of the work being performed by a software engineering team is hidden, use visual management to make it visible

> The role of the team leader is to support operators in their day-to-day job, which means he should be both knowledgeable and available

> Not knowing how to perform a task is not an interesting challenge to solve for the operator, it is an issue for the management team

# Visualize what has to be done, and what is going on

When you visit the shop floor, even though you don't know anything about the steel coils industry, you can see what is going on. You can see the stock of raw material, you can see it being transformed by a series of machines, and you can see the stock of finished goods waiting to be shipped to the customers.
When you visit the office of a software company, it is hard to see all of this. Often all you can see is a bunch of people banging on their keyboards. It means that it's hard to answer the following questions:
- is customer demand satisfied?
- is the team experiencing issues during production?

## Visualize customer demand and current production using Kanban

Kanban can be used to visualize what has to be done, and what is being done right now. Kanban cards represent orders from the client, that have to be fulfilled. These cards can be in several states:
- waiting to be produced
- being produced right now
- already produced, waiting to be shipped

## Produce according to a takt time to detect issues

Detecting production issues is much easier is you already have a steady rythm. The takt time is the time interval at which work should be done. For instance, you can decide to have a takt time of a half day, so that every half day you ship to the client 3 features. Of course, these numbers should match the global customer demand.
Every half day, you can either fail or succeed to deliver, and every failure is an opportunity to learn. Why couldn't we produce these 3 features ? What went in our way ?

# Spend your time adding value

jidoka
andon

# Standardize, then continuously improve

standardized work
kaizen
