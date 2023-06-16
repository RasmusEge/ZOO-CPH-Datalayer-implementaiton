# Copenhagen ZOO tracking requirement document (WEB) - Errors
This document contains tracking requirements for error events for https://www.zoo.dk/

## Table of content
[**1. Error tracking**](#error-tracking) <br/>
[1.1 Form errors](#form-errors) <br/>
[1.2 Select Item](#select-item) <br/>
[1.3 View Item](#view-item) <br/>
[1.4 Add to cart](#add-to-cart) <br/>
[1.5 View cart](#view-cart) <br/>
[1.6 Remove from cart](#remove-from-cart) <br/>
[1.7 Add Shipping info](#add-shipping-info) <br/>
[1.8 Add Payment info](#add-payment-info) <br/>
[1.9 Purchase](#purchase) <br/>


## Error tracking
All error events and parameters are detailed in the following

Documentation:

##Form errors
When user sees form in browser

a.	 (Registration, login, signup (newsletter) and booking forms)
i.	Specify error type 
ii.	Specify error message 
iii.	Specify form name 
iv.	Specify which field throws an error 
v.	Specify form location (page-path)
b.	Page errors  (fx 404)
i.	Specify error type 
ii.	Specify error message 
c.	Checkout errors 
i.	Specify error type 
ii.	Specify error message (fx card declined)


Form-related errors (like “some required fields are not filled in: first name, address”)

Form-field-related errors (like “invalid shipping address”)

Payment-related errors (like “insufficient funds” or “card declined”) (just make sure things like credit card data is not tracked)

After identifying groups of errors that you want to track, ask a developer to push those errors to the Data Layer, here’s a sample code:

````javascript
<script>
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  'event': 'error',
  'errorType': 'checkout error', // this value should depends on the type of error, e.g. form error, checkout error, etc.
  'errorMessage' : 'card declined' // some descriptive message about the error
});
</script>
````
