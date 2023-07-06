# Copenhagen ZOO tracking requirement document (WEB) - Navigation
This document contains tracking requirements for navigation events for https://www.zoo.dk/

### Top Navigation
When the user clicks a menu item in the top navigation bar (see image below), the following event should be dispatched:

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/50660504-e184-47d9-8388-30a1b294690e)

````javascript
dataLayer.push({
     event: 'navigationTracking'
     eventCategory: 'Navigation',
     eventAction: 'Top Navigation',
     eventLabel: '[Menu item name]'
 }); 
````

### Top Navigation - submenu 1 
When the user clicks a menu item in the top navigation dropdown-menu submenu_1 (see image below), the following event should be dispatched:

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/dd819bb8-e411-4530-87f2-3873abb09496)

````javascript
dataLayer.push({
     event: 'navigationTracking'
     eventCategory: 'Navigation',
     eventAction: 'Top Navigation - submenu_1  ',
     eventLabel: '[Menu item name]'
 }); 
````
