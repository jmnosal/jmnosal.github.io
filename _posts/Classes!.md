---
layout: post
title: Classes - Online Store Manager
---

This assignment involved creating several classes, beginning with an 'Online Store Manager' (OSM) which instantiates new instances of another class, 'OnlineStore'. The OSM defines the types of inventory its OnlineStores can sell (for example all stores created by the 'Books' OSM can only sell 'books', 'newspapers' and 'cds') and keeps a running total of all stores created. The OnlineStore, in turn, is able to control said inventory by adding and selling stock, can summarize current inventory levels and keeps a running total of all items sold. The OnlineStore can also create new instances of the third and final class, 'Customer', each of whom have a unique name and a function allowing them to purchase inventory.

I kept most of the functionality at the OnlineStore level, and kept 'inventory' as an attribute of the OnlineStore rather than create a separate class for it. There were no methods I could see to ascribe to the inventory, and felt it could be easily manipulated in a dictionary with item/quantity key/value pairs. Once that decision was made it was just a matter of defining the add/sell inventory methods, and putting in checks to ensure that when a Customer made a purchase A) That item was sold at the store, and B) That the item was in stock. 

If I were to continue on with this assignment, I would like to enhance the Customer class so that one customer can have IDs at several stores (right now they are linked exclusively to the OnlineStore that instantiated them) and would look to introduce prices and money into the equation, where customers are further limited in what they can buy based on account balances, and stores are only able to add stock if they have a positive balance from selling current inventory.
