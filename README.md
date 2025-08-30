# Class-Diagrams
Case Study: QuickShop E-Commerce Platform (Inspired by Takealot/Amazon)
Scenario: "Place Order" Functionality
Background
QuickShop is a growing e-commerce platform. Customers can browse products, add items to their cart, and place orders. Your team must design the core functionality for the "Place Order" use case described below.
Use Case Description: Place Order
1.	Actor: Customer (authenticated user)
2.	Preconditions:
o	Customer has items in their shopping cart
o	Customer has a valid default payment method
3.	Flow:
1.	Customer navigates to checkout page
2.	System displays:
	Cart items with prices
	Shipping address
	Payment method
	Order total (including tax + shipping)
3.	Customer clicks "Place Order"
4.	System verifies:
	Product availability
	Payment method validity
5.	If checks pass:
	Creates an Order with status "Confirmed"
	Creates OrderLineItem for each cart product
	Deducts product quantities from inventory
	Processes payment via Payment Gateway
	Sends order confirmation email
	Clears shopping cart
6.	If checks fail:
	Displays specific error (e.g., "Product out of stock")
