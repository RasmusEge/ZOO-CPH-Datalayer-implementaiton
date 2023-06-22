# Copenhagen ZOO tracking requirement document (WEB) - Forms
This document contains tracking requirements for form events for https://www.zoo.dk/

## Table of content
[**1. Form tracking**](#error-tracking) <br/>
[1.1 Form views](#form-view) <br/>
[1.2 Page errors](#page-errors) <br/>
[1.3 Server errors](#server-errors) <br/>
[1.4 Checkout errors](#checkout-errors) <br/>


## Form tracking
All error events and parameters are detailed in the following

## Form view
#### When users views a form in the browser    

````javascript

window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
 'event': 'new_subscriber',
 'formLocation': 'footer'
 });
````

a.	Form view (user sees form in browser)
i.	Specify form name 
ii.	Specify form location (page-path)
iii.	Specify form ID 
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
