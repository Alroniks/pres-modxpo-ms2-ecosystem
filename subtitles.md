#0
Hello, friends! Penguin here :)
Sorry for my English, I am in the process of studying and hope you will understand what I want to tell you.

#1
I would tell you history, how one extra for e-commerce changed MODX world in the russian language community. I hope this history will be a good example for you to try.

#2
Slides available by this link, if you want to open it on your devices.

#3
Who I am? My name is Ivan Klimchuk. I am from Belarus. But I had the privilege to present all Russian-language community here. 
I am working as full stack developer, related to web technologies of course. Met MODX in far 2010, in 2011 started work for a local community.
Since February of 2013, I am MODX Ambassador in Belarus, also I had a status of MODX Professional.
I love MODX and open source. 
Also, I try to do small business related to developing and store extras and themes for MODX. I am at the start but move step by step. 
And of course, work for the local community as MODX Ambassador.
Ok, now you are know everything about me.

#4
So, let's talk about e-commerce at first. What is it? Goals of e-commerce - sell things and earn money. For doing it successfully, you should always find ways how to encrease the sales and improve your e-shop every time. 

#5
Despite that each e-shop should find the own way, many things in stores are common.
Eash shop requires categories and products, of course. And many related functions on this pages: list of products, photos, reviews, functions like sorting, filtering, and others.
Of course, cart and orders. Very important part of e-commerce. Orders can be made by phone, but we live in the twenty-first century.
Variants of deliveries and shipments. Depends on distance, weight, sizes.
Variant of payments: cards, payment gates, paypal for example.
And options and characteristics of product for search and filtering.
It's not all, but the most frequent.

#6
Some years ago exists some solutions for e-commerce, based on modx, but it wasn't enough. And such was created MiniShop, as replacing to VisionCart and Shopkeeper.
It did include categories and products, that worked as usual resources and for set category or product you did need use special template, that was set in system settings.
Warehouses was a good feature, but not supported in your version yet.
Also, cart, orders, orders statuses and once payment method. It was simple e-commerce solution, that you can install and start use at the same time. No tuning. 
And of course, to be good alternative existing e-commerce solution, this functions not enough. 

#7
Minishop2 became the continuation of first versions, but with changes in core.

#8
First stable versions were released in April of two thousand thirteen.
Warehouses were removed, categories and products were rewritten as CRC classes.
Cart and orders also were rewritten, was added extendable deliveries and payments methods, late was added the gallery, ability set relationships between products. For example, when you see the product page, at the bottom showing related products. And in latest versions was added ability define customisable options for products.

#9
Here some screenshots.
Orders list as a table with a search. 
Settings. List of deliveries, the list of payments, the list of statuses, brands or manufacturers, links between products. Options.
It's Category. Base settings of the page and at the bottom list of products, related to this category.
Product page. Name, price, weight - base fields. Additional attributes. Gallery and links.

#10
Like MODX, minishop use the same paradigm.
For now you have ability extends four classes. Cart, Delivery, Order and Payment.
You just create an own class in the special folder and set it to row in minishop settings.
Also, you can use all features of MODX for extending and change behavior. 
Now in modstore exists about 50 extras for minishop only.

#11
Time to code!
Each class, that you want to add, should implement the special interface.
Cart handler can adding to cart, removing from the cart, changing, cleaning, you also can check status and get or set the whole cart.
Link to full code at the bottom.

#12
It's similar, just do other things.
You can add products to order and validate its. Also remove, clean, get/set.
And after you should submit the order. It's mean that order placed and manager can start work with it. Also method getCost, that count the cost of delivery, payments, applies rules for discounts and return the latest cost for the order.

#13
Delivery handle very similar. Main method - getCost. It returns cost of delivery, calculations encapsulated in the class.

#14
Payment the same, but has two additional methods - send and receive. Send - prepares information about payment and sends to the external payment system, receive process returned answer.
I hope it's clear.

#15
Awesome thing, special minishop plugins. Not MODX plugins.
For example, you want to add a new field to database (for natural search and filtering by SQL-queries), but want to save the ability to update minishop. This plugin works as hot hooks.

#16
All plugins should be stored in the special folder with the name of the plugin. Minishop saves this folder during an upgrade.
And you need create 3 files.
All based on meta-map files from xpdo.
In the index.php, you define which files you need include.

#19
And for the manager we need define code on ExtJS, that will be added before load manager panel.

#20
Results. New field.

#21
Also exists a lot of ways to extend minishop by a power of MODX. Really. A am not kidding!

#22
It's works. Installed on four and a half thousands of sites.
But have some annoying bugs, wait to refactor a long time. And of course, needs docs.

#23
Will be a version three! As Vasily said.
It will bring refactoring of current code, more APIs, documentation, on English too.
More details Vasily will tell on MODX Meetup in Minsk in this December.

#24
Let's see how minishop helped to the community and how was built the ecosystem.

#25
What difference between store and marketplace?
Both allow to sell extras and applications, but... Below some pros and cons for stores and marketplaces.
One developer or team for the store, an independent developer does not have the ability to come and sell own extra (not easy). In marketplace he can. It's cons of the marketplace.
But the store also has pros. Higher quality of packages and support. In marketplace it not always promised.
Official MODX repository - looks like as marketplace, but not has the market.
modstore.pro - real marketplace.

#26
Stores, which I know.
modmore.com of course, extras.io too. A few days ago Russian developer created own store. And my store, that will be launched, I hope.
And I hope, all stores will be a marketplace in near future. I would want it.

#27
Started on the eleventh of June in 2013. Was names as store.simpledream.ru. SimpleDream agency main company that support MODX initiatives in Russia.
At the start in the store was placed basically extras from stuff.
Started actively growth after the release of minishop.
On our local community, every extra developer dreams to create something for this marketplace. 

#28
Developer sends request for adding extra and stuff of store do check and validate extra and developer. After developer can upload new versions by himself. Store provide billing and show statistics by extra and can pay to the developer if somebody bought this extra. The developer should provide support to client, who bought extra. By rules of the marketplace. So, in a fact, store sell support from the developer, not the just package.
The average fee is 30%, but can be discussed.

#29
Only two years. Revenue grows more than ten times. Twenty-five authors now represented in the marketplace. 

#30
And here only small part of all extras, placed in the marketplace.

#31
Is it ease to create the same?
I guess yes. It is not simple. But not impossible.

#32
At first, you need package repository. For automate installations.
Then you should create a system for manage of users account and their keys for access to the repository and paid content.
Content management. On MODX no problem.
Support interface. Not difficult to in common cases.
Billing. Can be complex, depends on the country. Not difficult technically, but can be issued with laws.

#33
Very important support and improve your marketplace. It's e-commerce too, just with extras :)
You can hire a designer for logos and UI, also you can hire people for support, for texts. It's can be expensive, at the start you can do it by self.

#34
Of course, if you want, you can. It'needs impact, but not difficult.
If you can, just do it. 
If you want to develop extras, thinks as modx. Because one good extra can create many satellites and it's really good. You will involve more people.
Competitions are good, of course. But I think owners of stores and marketplaces should collaborate and exchange of experience. And do their stores better and better.
And! As we about MODX - Creative Freedom! 

# 35
It's absolutely no problem find me on the Internet but on screen some my contacts. Twitter as the fastest way to get touch with me. My developer accounts on Github, where I share almost all of my code.
Below my website and email. And :) If you anywhere see a penguin like this, most likely it is I.

# 36
I guess that's all that I want to tell you, so, please, ask me. I will try answer.
