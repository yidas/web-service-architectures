Third Party Payment
===================

Categories
----------

- [Master Card](master-card)
- [PayPal](paypal)

---

Theories
--------

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
