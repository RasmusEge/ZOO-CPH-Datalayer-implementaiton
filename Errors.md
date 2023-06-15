Form-related errors (like “some required fields are not filled in: first name, address”)
Form-field-related errors (like “invalid shipping address”)
Payment-related errors (like “insufficient funds” or “card declined”) (just make sure things like credit card data is not tracked)
After identifying groups of errors that you want to track, ask a developer to push those errors to the Data Layer, here’s a sample code:

<script>
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  'event': 'error',
  'errorType': 'checkout error', // this value should depends on the type of error, e.g. form error, checkout error, etc.
  'errorMessage' : 'card declined' // some descriptive message about the error
});
</script>
