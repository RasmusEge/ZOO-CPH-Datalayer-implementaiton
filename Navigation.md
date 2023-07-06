# Copenhagen ZOO tracking requirement document (WEB) - Navigation
This document contains tracking requirements for navigation events for https://www.zoo.dk/

### Top Navigation
When the user clicks a menu item in the top navigation bar (see image below), the following event should be dispatched:

![image](https://github.com/RasmusEge/ZOO-CPH-Datalayer-implementaiton/assets/122262884/50660504-e184-47d9-8388-30a1b294690e)

´´´´javascript
dataLayer.push({
     event: 'navigationTracking'
     eventCategory: 'Navigation',
     eventAction: 'Top Navigation',
     eventLabel: '[Menu item name]'
 }); 
´´´´
