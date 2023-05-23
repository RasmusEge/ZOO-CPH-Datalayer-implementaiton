# Copenhagen ZOO tracking requirement document (WEB) Ecommerce 
This is a document of the tracking requirements for

## Table of content
[**1. Ecommerce**](#ecommerce-tracking) <br/>
[1.1 Items array](#items-array) <br/>

## Ecommerce tracking
All ecommerce events and parameters are detailed in the following

## Items array
Items array is used throughout all ecommerce events   
````javascript
items: [
    {
      item_id: "SKU_12345",
      item_name: "ZOO-kort_voksen",
      affiliation: "CPH-ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 0,
      item_brand: "CPH",
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      item_variant: "ZOO-Kort",
      price: 500.00,
      quantity: 2
    },
    {
      item_id: "SKU_12345",
      item_name: "Billet_barn",
      affiliation: "CPH ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 1,
      item_brand: "CPH-ZOO",
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      item_variant: "ZOO-Kort",
      price: 200.00,
      quantity: 2
    }
]
````

## Select item
Send event when user clicks on a product
````javascript
window.datalayer.push({
  event: 'select_item',
   ecommerce: {
   items: [{
      item_id: "SKU_12345",
      item_name: "ZOO-kort_voksen",
      affiliation: "CPH-ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 0,
      item_brand: "CPH",
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      item_variant: "ZOO-Kort",
      price: 500.00,
      quantity: 2
    },
    {
      item_id: "SKU_12345",
      item_name: "Billet_barn",
      affiliation: "CPH ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 1,
      item_brand: "CPH-ZOO",
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      item_variant: "ZOO-Kort",
      price: 200.00,
      quantity: 2
    }]
}
});
````

## View Item
Send event when a user a loads a productpage 
````javascript
  event: 'view_item',
  ecommerce: {
   items: [{
      item_id: "SKU_12345",
      item_name: "ZOO-kort_voksen",
      affiliation: "CPH-ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 0,
      item_brand: "CPH",
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      item_variant: "ZOO-Kort",
      price: 500.00,
      quantity: 2
    },
    {
      item_id: "SKU_12345",
      item_name: "Billet_barn",
      affiliation: "CPH ZOO",
      coupon: "Sommmer_sjov20",
      discount: 100,
      index: 1,
      item_brand: "CPH-ZOO",
      item_category: "ZOO-Kort",
      item_category2: "Voksen",
      item_variant: "ZOO-Kort",
      price: 200.00,
      quantity: 2
    }]
}
});
````

