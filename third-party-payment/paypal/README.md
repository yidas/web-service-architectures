PayPal
======

PayPal Checkout Integration
---------------------------


### Set up the payment

![Set up the payment](https://developer.paypal.com/img/docs/checkout/setting-up-paypal-payment-server-integration.svg)

1. Your buyer clicks the PayPal button.
2. The PayPal button calls your server.
3. Your server calls the PayPal API to set up the payment.
4. The button launches the checkout flow in the buyer's browser.

### Execute the payment

![Execute the payment](https://developer.paypal.com/img/docs/checkout/executing-paypal-payment-server-integration-continue.svg)

1. Your buyer clicks the Pay Now button in the PayPal Checkout flow.
2. Buyer reviews their order and clicks the Agree & Pay button.
3. The browser calls your server.
4. Your server calls the PayPal API to execute the payment.
5. You show a payment receipt page to the buyer.

> [PayPal Developer - Implement a PayPal Checkout Server Integration](https://developer.paypal.com/docs/checkout/how-to/server-integration/)

---

Express Checkout (End to 2017)
------------------------------

<img src="https://raw.githubusercontent.com/yidas/web-service-architectures/master/third-party-payment/paypal/overview-ec-ecapiflow.gif" />

This old payment checkouot API has a big mistake that the PayPal page's total amount showed to customer is not same as final total amount dealed by merchant. This happens on step 6 which merchant sends a final transaction detail request with actual amount to PayPal API server for charging.


---

Reference
---------

[PayPal Developer](https://developer.paypal.com/)
