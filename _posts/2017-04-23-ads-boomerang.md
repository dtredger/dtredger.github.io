---
layout: post
title: "Ads Boomerang"
description: Rails SaaS for self-serve advertising for eCommerce.
---

This repo contains 3 separate systems [[github](https://github.com/dtredger/ads_boomerang)]:

**Ads Boomerang** was an idea for a self-service SaaS platform for small ecommerce stores that would deliver 
advertising focused on driving more sales. This included a script to be inserted into the client's store, a dashboard to upload ads, an integration with an ad-inventory API, and reporting.

------

Technical Aspects
----------

The system used:
* Rails 5
* Postgres and Redis for storage and queues
* Memcached for caching
* payola-payments and Stripe for handling payments
* Beeswax for buying accessing Ad Inventory

What went well
-------------
From a technical perspective, most of the bits worked as expected; specifically:

* Integration with Shopify made setup easy
* Integration with Beeswax PaaS provided the ability to buy ads on a variety of ad exchanges
* Dashboard accepted uploads for most standard image formats (300x250, 728x90, 160x600, etc.)

Why didn't it work?
---------------
The main issue is that there was too much support and explanation required versus the target client's budget:

* most small store owners weren't very tech-savvy, so had to be explained the benefits of retargeting.
* Store owners needed ads designed.
* some store owners were skeptical of online ads generally: many small sellers didn't want to be the type of business that advertised.
* Retargeted ads are cheap, but limited to a site's existing pool of users. This capped the amount that a given client could spend on retargeted ads.
* Non-retargeted ads are totally ineffective without huge amounts of data. Given the amount of fraud/non-viewable ad inventory on most ad-exchanges, buying without extensive data brings zero return.