# Equity_Order_Matcher
Equity Order Matcher is a platform for matching active equity orders in an orderbook according to the type of order. It also facilitates addition of new orders,cancellation of orders or updation of order details.

## Command Description
* **Actions** :  N(New),  A(Amend),  X(Cancel),  M(Match).
* **OrderID** : An integer value in the range $$[1,2^{63}-1]$$ inclusive.
* **Timestamp** : An integer value, typically milliseconds since epoch.
* **Symbol** : Varying length string containing only alphabets.
* **OrderType** : M(Market), L(Limit) or I(IOC).
* **Side** : B(Buy) or S(Sell)
* **Price** : A float value, $$0.00$$ if OrderType is M(Market). The price is given exactly to two places of decimal.
* **Quantity** : An integer value in the range $$[1,2^{63}-1]$$ inclusive.

## Operations

* **$$NEW$$** : Adds a new order into the orderbook
	`N`,*`OrderId,Timestamp,Symbol,OrderType,Side,Price,Quantity`*
* **$$AMEND$$** : Updates an existing order as per details in this command.
	`A`,*`OrderId,Timestamp,Symbol,OrderType,Side,Price,Quantity`*
* **$$CANCEL$$** : Requests an existing order to be canceled 
	`X`,*`OrderId,Timestamp`*
* **$$MATCH$$** : Matches the existing orders in the order book at that timestamp 
	`M`,*`Timestamp,[Symbol]`*

For further information:  Visit https://github.com/Souradip-sopho/Equity_Order_Matcher/blob/master/question.txt
## Built With
C/C++

## Author
Souradip Pal | [GitHub](https://github.com/Souradip-sopho) | [LinkedIn](https://www.linkedin.com/in/souradip-pal-a9693111b/)