# Copenhagen ZOO tracking requirement document (WEB) - Forms
This document contains tracking requirements for form events for https://www.zoo.dk/

## Table of content
[**1. Form tracking**](#error-tracking) <br/>
[1.1 Form views](#form-view) <br/>



## Form tracking
All error events and parameters are detailed in the following

## Form view
#### When users views a form in the browser    

````javascript

window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'event': 'Form view',
 'formLocation': 'footer' // or content blok (if something exists)
 'formType': 'Booking' // incert dynamic value 
 'formName':'Booking - Selskaber' // incert dynamic value
 'formID': '12343535' //  incert dynamic value
 });
 
````


b.	Form start (User starts filling out form 
i.	Specify form name 
ii.	Specify form location (page-path)
iii.	Specify form ID 
c.	Form submit (user submit form)
i.	Specify form name 
ii.	Specify form location (page-path)
iii.	Specify form ID 
d.	Form success (form is successfully submitted)
i.	Specify form name 
ii.	Specify form location (page-path)
iii.	Specify form ID 
