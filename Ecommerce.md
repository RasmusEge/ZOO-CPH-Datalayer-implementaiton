# Copenhagen ZOO tracking requirement document (WEB) Ecommerce 
This document contains datalayer tracking requirements for ecommerce events on https://www.zoo.dk/


## Table of content
[**1. Ecommerce tracking**](#ecommerce-tracking) <br/>
[1.1 Items array](#items-array) <br/>
[1.2 Select Item](#select-item) <br/>
[1.3 View Item](#view-item) <br/>
[1.4 Add to cart](#add-to-cart) <br/>
[1.5 View cart](#view-cart) <br/>
[1.6 Remove from cart](#remove-from-cart) <br/>
[1.7 Add Shipping info](#add-shipping-info) <br/>
[1.8 Add Payment info](#add-payment-info) <br/>
[1.9 Purchase](#purchase) <br/>



## Ecommerce tracking
Detailed below are all ecommerce events and parameters for
checkout 1 - without zoo-card in the basket
checkout 2 - with a zoo-card in the basket

Google documentation: [https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag](https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag)

## Items array
Items array is used throughout all ecommerce events and includes all items in a purchase for both chekout 1 and 2    
````javascript
items: [
    {
      item_id: "SKU_12345",
      item_name: "ZOO-kort_voksen",
      affiliation: "CPH-ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 0,
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      price: 500.00,
      quantity: 2
    },
    {
      item_id: "SKU_12345",
      item_name: "Billet_barn",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 1,
      item_category: "ZOO-billet",
      item_category2: "Barn",
      price: 200.00,
      quantity: 2
    }
     {
      item_id: "SKU_123456", // Id from backend 
      item_name: "Boerne-foeselsdag", // name from backend 
      discount: 500,
      index: 2,
      item_category: "ZOO-event",
      item_category2: "Barn",
      price: 275.00,
      quantity: 12
    }
         {
      item_id: "SKU_12345343", // Id from backend 
      item_name: "ZOO-camp 3 dage 10-12 aar", // name from backend 
      discount: 500,
      index: 3,
      item_category: "ZOO-event",
      item_category2: "Barn",
      price: 275.00,
      quantity: 12
    }

]
````

## Select item

Send event when user clicks on a product
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'select_item',
  ecommerce: {
  items: [{ 
            // insert items array with dynamic values   
          }]    
     }
});
````

## View Item
Send event when a user a loads a productpage 
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'view_item',
  ecommerce: {
   items: [{ 
            // insert items array with dynamic values   
          }]    
     }
});
````

## Add to cart
Send event when a user adds product to cart
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_to_cart',
  ecommerce: {
  items: [{ 
            // insert items array with dynamic values   
         }]    
     }
});  
````

## View cart
Send event when user views cart
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'view_cart',
  ecommerce: {
  items: [{ 
            // insert items array with dynamic values   
         }]    
     }
});
````

## Remove from cart
Send event when user removes product from cart  
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'remove_from_cart',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Begin checkout
Send event when user starts checkout flow
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'begin_checkout',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Add shipping info
Send event when user has successlfully added shipping info 
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_shipping_info',
  ecommerce: {
  items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Add payment info 
Send event when user has successfully added payment info
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'add_payment_info',
    ecommerce: {
    payment_type: "creditcard" // eller FF (forbrugsforeningenskort) 
      items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

## Purchase 
Send event when user has successfully made a purchase
````javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'purchase',
    ecommerce: {
    currency: 'DKK',
    value: 116.47,
    tax: 7.18,
    shipping: 10.00
    transaction_id: 'p115-20202000',
    coupon: 'free_back_rub', //if
      items: [{ 
           // insert items array with dynamic values   
         }]    
     }
});
````

 
