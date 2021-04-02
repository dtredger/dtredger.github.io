---
layout: post
title: "ShowRoom"
description: "A site for people to save their fashion likes"
---

_{{ page.description }}_ [[github](https://github.com/dtredger/showspace)]

Showroom is a standard Rails 4.1 app that allows users to view fashion items in a grid interface and save them to a 
"closet" for later. 

The app uses Devise for authentication, Carrierwave for images (uploaded to s3), RSpec + FactoryGirl for tests. Tests are mostly around Model and Controller tests (only a few request specs, since we aren't really settled on the ui).

Scrapers 
----------
Items are harvested via webscraper. Currently there are three custom scrapers, but they all inherit basic functionality from a BasicScraper class. The scrapers are run as rake tasks. For now they will be run locally, but connected to the live database. 

When items are created, their attributes are checked against existing items (name, price, designer, etc), and given a "match score" based on similarity. This score is accessible in the admin interface, so an admin can verify whether the items created are duplicates or new.

Admin Interface 
------------
The site uses Active Admin for the default admin dashboard, which allows for managing items. The main focus is allowing an admin to change the "state" of an item. When items are first scraped, they are given a "pending" status, and will not be shown until they are set "live". The Admin dashboard also allows batch deletes of items that have duplicate-warnings, so you can easily remove a bunch of new scraped items that are the same as existing items.

Workflow
----------
Using a _**Git Flow(-ish)**_ strategy:

* Feature branches are merged into Develop when they are complete. 
* No Release branches for now
* Master is the source of the latest release. 
* Trello for to-dos.
