---
name: Backend Projects
tools: [JavaScript, React, SQL, Spotify API]
image: ../assets/images/BackendProjects/ReactLogo.png
description: Three projects from a full stack class, moving from consuming an external API to designing my own database to building an ecommerce site on top of one.
---
# Backend Projects

## Situation
I took a full stack class built around web applications, where the focus was on how the part of a site a person interacts with connects to the data behind it. Rather than one large final project, the course worked through a series of builds, with each one adding something the previous project had not required.

## Task
I built three projects over the course. Looking at them together, they form a progression. The first consumed data that belonged to someone else, the second required me to design and own the data, and the third built a working application on top of data I controlled. Each project was assigned as its own build, but the sequence is what actually taught the material.

## Action

### Spotify Artist Search
The first project was an artist search built in React against the Spotify API. A user searches for an artist and the app returns that artist along with their albums and songs.

The work here was learning to consume an external API. The data lived on Spotify's servers rather than mine, which meant the app had to request it, wait for a response that might take time or fail, and then turn whatever came back into something rendered on screen. That is a different way of thinking from building a page where the content is already there when it loads.

### Pokemon Database Lookup
The second project moved the data to my side. I built a SQL database holding Pokemon records with fields for name, type, images, and other details, then built a site that queried it so the information could be looked up.

This was where I had to make decisions about the data rather than just receive it. Choosing what fields a record needs and how the table is structured determines what the site can do later, since a query can only ask for something the schema actually stores.

### Ecommerce Site
The third project brought both halves together. I used React and SQL to build a working ecommerce site with a homepage, product listings, featured products, a contact form, and shipping and checkout pages. Product information could be added to the site rather than being written into the code.

That last part is the difference between a website and an application. Product listings and featured products both read from the database, so adding a product puts it on the site without anyone touching the code, which is the whole reason a real store runs on a database in the first place. This project also involved the most page structure of the three, since a shopping flow has to carry a user from browsing through to checkout rather than living on a single screen.

The site was built as a functioning project rather than a live store, so it was never opened to real customers or real orders. Everything on it works, but it worked as a build rather than as a business.

## Result
All three projects worked, and taken together they gave me a picture of how React and SQL fit on either side of an application. The sequence mattered more than any single build. By the third project I was not learning what a database was or how to fetch data, so I could spend that time on how the pieces connected instead.

The clearest thing I took from the class is that the frontend and the data layer are separate problems that meet at a defined boundary. A React component does not care where a product came from, and a database does not care how a product is displayed, which is what makes it possible to change one without breaking the other.
