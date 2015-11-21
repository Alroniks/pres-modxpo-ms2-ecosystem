# 0 - Greeting
Hello friends! Pinguin here :)

Sorry for my Eglish, I am in process of studding and hope you will understand what I want tell you.

# 1 - Cover
I would tell you history, how one extra for ecomerce changed MODX world in russian language community. I hope this history will be a good example for you to try.

#2 - Slides link 
Slides available by this link, if you want open it on your devices.

# 3 - I am
Who I am? My name is Ivan Klimchuk. I am from Belarus. But I had a privilege to present all russian-language community here. 

I am work as full stack developer, related to web technologies of course. Met MODX in far 2010, in 2011 started work for local community.

Since Febrary of 2013 I am MODX Ambassador in Belarus, also I had status of MODX Professional.

I love MODX and open source. 

Also I try to do small business related to develop and store extras and themes for MODX. I am at start, but move step by step. 

And of cource work for local community as MODX Ambassador.

Ok, now you are know everything about me.

#4 - E-commerce - what is it?

So, let's talk about ecomerse at first. What it is? Goals of e-commerse - sell things and earn money. For do it successfully you should always find ways how encrease the sales and improve your e-shop every time. 

# 5 - Required elements of shop

Despite that eash e-shop shoult find own way, many things in stores are common.

Eash shop require categories and products, of course. And many related function on this pages: list of products, photos, reviews, functions like sorting, filtering and others.

Of cource, cart and orders. Very important part of e-commerce. Orders can be made by phone, but we live in twenty first century.

Variants of deliveries and shipments. Depends on distance, weight, sizes.

Variant of payments: cards, payment gates, paypal for example.

And options and characteristics of prioduct for search and filtering.

It's not all, but the most frequent.

# 6 - Minishop. First generation.

Some years ago exists some solutions for e-comerce, based on modx, but it wasn't enough. And such was created MiniShop, as replacing to VisionCart and Shopkeeper.

It did include categoroies and products, that worked as usual resources and for define category or product you did need use special template, that was set in system settings.

Warehouses was a good feature, but not supported in you version yet.

Also, cart, orders, orders statuses and once payment method. It was simple e-commerce solution, that you can install and start use at the same time. No tuning. 

And of cource, to be good alternative existing e-commerce solution, this functions not enough. 

# 7 - MS2 - Cover

Minishop2 became the continuation of first versions, but with changes in core.

# 8 - MS2 History

First stable versions was relieased in April of two thousands thirtheen.

Warehouces was removed, categories and products was rewriten as CRC classes.

Cart and orders also was rewriten,

was added extendable devliveries and payments methods, late was added gallery, ability set relationships between products. For example, when you see product page, at the bottom showing related products. And in latest versions was added ability define cutomisible options for products.

# 9 - Screenshots

Here some screenshots.
Orders list as a table with search. 
Settings. List of deliveries, list of payments, list of statuses, brands or manufacturers, links bettwen products. Options.

It's Category. Base settings of page and at the bottom list of products, related to this category.

Product page. Name, price, weight - base fields. Additional attrubites. Gallery and links.

# 10 - Modular and extedable

Like MODX, minishop use the same paradigm.

For now you have ability extends four classes. Cart, Delivery, Order and Payment.

You just create own class in special folder and set it to row in minishop settings.

Also you can use all features of MODX for extend and change behavior. 

Now in modstore exists about 50 extras for minishop only.

# 11 cart handler

Time to code!

Each class, that you want add, should implement special interface.

Cart handler can adding to cart, removing from cart, changing, cleaning, you also can check status and get or set whole cart.

Link to full code at the bottom.

# 12 Order handler

It's similar, just do other things.

You can add products to order and validate its. Also remove, clean, get/set.

And after you should submit order. It's mean that order placed and manager can start work with it. Also method getCost, that count cost of delivery, payments, applies rules for discounts and return latest cost for order.

# 13 - Delivery handler

Delivery handler very similar. Main method - getCost. It return cost of delivery, calculations incapsulated in class.

# 14 - Payment handler

Payment the same, but has two additional methods - send and recieve. Send - prepares informations about payment and sends to externat payment system, receive process returned answer.

I hope it's clear.

# 15 - Special plugins

Awesome thing, special minishop plugins. Not MODX plugins.

For example, you want add new field to database (for natural search and filtering buy sql-queries), but want save ability to update minishop. This plugins works as hot hooks.

# 16 - Special plugins 2

All plugins should be stored in special folder with name of plugin. Minishop save this folder during upgrade.

And you need create 3 files.

All based on meta-map files from xpdo.

In index you define which files you need include.

# 19

And for manager we need define code on extjs, that will be added before load manager panel.

# 20 Results

Results. New fields.

# 21 - MODX Power

Also exists a lot of ways to extend minishop by power of MODX. Really. A am not kidding!

# 22 Current status of minishop

It's works. Installed on four and half thounsands of sites.

But have some annoying bugs, wait refactoring a long time. And of cource needs docs.

# 23 Future

Will be a versions three! As Vasily said.

It will brings refactoring of current code, more apis, documentaions, on english too.

More details Vasily will tell on MODX Meetup in Minsk in this December.

# 24 Ecosystem

Let's to see how minishop helped to comminity and how was built ecosystem.

# 25 Store vs Marketplace

What diference beetwen store and marketplace?

Both allow to sell extras and applications, but... Below some pros and cons for stores and marketplaces.

One developer or team for store, independent developer not have ability to come and sell own extra (not yeasy). In marketplace he can. It's cons of marketplace.

But store also has pros. Higher quality of packages and support. In marketplace it not always promised.

Official MODX repository - looks like as marketplace, but not has market.
modstore.pro - real marketplace.

# 26 Stores

Stores, which I know.

modmore.com of cource, extras.io too. A few days ago russian developer created own store. And my store, that will be launched, I hope.

And I hope, all stores will be a marketplace in near future. I would want it.

# 27 - History of modstore

Started on eleventh of june in 2013. Was names as store.simpledream.ru. SimpleDream agency main company that support MODX initiatives in Russia.

At start in store was placed basically extras from stuff.

Started activly growth after release of minishop.

On our local community every extra developer dreams to create something for this marketplace. 

# 28 - How it works

Developer send request for adding extra and stuff of store do check and validate extra and developer. After developer can upload new versions by himself. Store provide billing and show statistict by extra and can pay to developer, if somebody bougth this extra. Developer should provide support to client, who bouth extra. By rules of marketplace. So, in a fact, store sell support from developer, not just package.

Average fee is 30%, but can be discussed.

# 29 - Some statistics

Only two years. Revenue grows more then ten times. Twenty five authors now represented in marketplace. 

# 30 - Cloud

And here only small part of all extras, placed in marketplace.

# 31 - Is it ease?

Is it ease to create the same?

I guess yes. It is not simple. But not impossible.

# 32 - how create it

At first, you need package repository. For automate installations.

Then you should create system for manage of users account and their keys for access to repository and paid content.

Content managment. On MODX no problem.

Support interface. Not difficult to in common cases.

Billing. Can be complex, depends of country. Not difficult technically, but can be issues with laws.

# 33 - How it suport

Very important support and improve your marketplace. It's e-commerce too, just with extras :)

You can hire designer for logos and UI, also you can hire people for support, for texts. It's can be expencive, at start you can do it by self.

# 34 - Concusions

Of cource, if you want, you can. It'need impact, but not difficult.

If you can, just do it. 

If you want develop extras, thinks as modx. Because one good extra can be create many satelits and it's really good. You will involve more people.

Competitions is good, of cource. But I think owners of stores and marketplaces should collaborates and exchange of experience. And do their stores better and better.

And! As we about MODX - Creative Freedom! 

# 35 - Contacts

It's absolutlly no problem find me in the Internet, but on screen some my contacts. Twitter as the most fastest way to get touch with me. My developer account on Github, where I share almost all of my code.

Below my website and email. And :) If you anywhere see a pinguin like this, most likely it is I.

# 36 - Thanks. Questions

I guess that's all that I want tell you, so, please, ask me. I will try answer.
