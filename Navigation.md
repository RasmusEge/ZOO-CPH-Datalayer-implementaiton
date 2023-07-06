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


![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/8cd5cb1d-3ec7-4d3e-99eb-83ba876ce084)



### Top Navigation - submenu 1 
When the user clicks a menu item in the top navigation dropdown-menu submenu_1 (see image below), the following event should be dispatched:

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/dd819bb8-e411-4530-87f2-3873abb09496)

````javascript
dataLayer.push({
     event: 'navigationTracking'
     eventCategory: 'Navigation',
     eventAction: 'Top Navigation-submenu_1',
     eventLabel: '[Menu item name]'
 }); 
````

### Top Navigation - submenu 2 
When the user clicks a menu item in the top navigation dropdown-menu submenu_2 (see image below), the following event should be dispatched:

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/b2803b19-a93f-4199-91ad-230fb0ae12bd)

````javascript
dataLayer.push({
     event: 'navigationTracking'
     eventCategory: 'Navigation',
     eventAction: 'Top Navigation-submenu_2',
     eventLabel: '[Menu item name]'
 }); 
````

### Top Navigation - submenu 3 
When the user clicks a menu item in the top navigation dropdown-menu submenu_3 (see image below), the following event should be dispatched:

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/5b9e88be-59f9-4654-888c-bb732f02f336)

````javascript
dataLayer.push({
     event: 'navigationTracking'
     eventCategory: 'Navigation',
     eventAction: 'Top Navigation-submenu_3',
     eventLabel: '[Menu item name]'
 }); 
````
