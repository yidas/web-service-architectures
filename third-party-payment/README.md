Third Party Payment
===================

Categories
----------

Take a look to see the API flow of third-party payments:

- [Master Card](master-card)
- [PayPal](paypal)

---

Theories
--------

This page provides theries of online payment:

- [Credit Card Process Flow](#credit-card-process-flow)
- [Apply Pay Flow](#apply-pay-flow)

---

Credit Card Process Flow
------------------------

![Credit Card Process Flow 01](https://raw.githubusercontent.com/yidas/web-service-architectures/master/third-party-payment/transaction_flow_01.png)

![Credit Card Process Flow 02](https://raw.githubusercontent.com/yidas/web-service-architectures/master/third-party-payment/transaction_flow_02.png)

![Credit Card Process Flow 03](https://raw.githubusercontent.com/yidas/web-service-architectures/master/third-party-payment/transaction_flow_03.png)

> Reference: [WalletHub](https://wallethub.com/edu/credit-card-transaction/25511/)

---

Apply Pay Flow
--------------

![Apply Pay Flow](https://raw.githubusercontent.com/yidas/web-service-architectures/master/third-party-payment/flow_apple_pay.png)

1. Encrypted payment information is sent
2. Payment processing based on the encrypted payment information  
(Merchant -> GMO-PG)
3. Payment processing based on the token number  
(GMO-PG -> Acquirer)
4. Notification of payment processing result  
(Acquirer -> GMO-PG)
5. Notification of payment processing result  
(GMO-PG-> Merchant)
6. Notification of the completed payment  
(Merchant -> Consumer)
7. Service delivery / product delivery  
(Merchant -> Consumer)
8. Sales deposit  
(Consumer -> Acquirer)
9. Sales deposit  
(Acquirer -> GMO-PG)
10. Sales deposit  
(GMO-PG -> Merchant)

> Reference: [Apple Pay | GMO Payment Gateway](https://www.gmo-pg.com/en/service/mulpay/apple-pay/)

---

CyberSource (CYBS)
------------------

CyberSource payment services provide the objects and methods you need for making calls to carry out a payment transaction. The following sequence outlines a payment transaction:
1. A consumer places an order.
2. Using a payment API, the merchant securely transfers the order information to CyberSource.
3. CyberSource formats the transaction detail and, through its payment gateway, routes the transaction authorization request to the processor.
4. The processor routes the transaction to the consumer’s payment card-issuing bank to request transaction authorization.
5. The issuing bank (issuing the payment card for Discover or American Express transactions) authorizes or declines the transaction.
6. CyberSource returns the response to the merchant.
7. The issuing bank approves the transfer of money to the acquiring bank.
8. The acquiring bank credits the merchant's account.

This diagram shows how real-time electronic card processing works:

![cybs]([https://developer.cybersource.com/content/dam/cybsdeveloper2019/dita/dita-payments/cybs_how.jpg/_jcr_content/renditions/original](https://developer.cybersource.com/content/dam/new-documentation/transitional/en/dita-payouts/PayoutsTransactionFlow.jpg/_jcr_content/renditions/cq5dam.web.1280.1280.jpeg)https://developer.cybersource.com/content/dam/new-documentation/transitional/en/dita-payouts/PayoutsTransactionFlow.jpg/_jcr_content/renditions/cq5dam.web.1280.1280.jpeg)

> Reference: [CyberSource’s Payment Process](https://developer.cybersource.com/docs/cybs/en-us/payouts/developer/all/rest/payouts/HowItWorks.html)
