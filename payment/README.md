Payment
=======

- Domain
  - [3DS (3-Domain Secure)](3ds)

- Payment Gateway
  - [CyberSource](cybersource)
 
- PSP (Payment service providers ) - 第三方支付
  - [PayPal](paypal)

---

Outline
--------

- [Credit Card Payment Systems](#credit-card-payment-systems)
  - [Process Flow](#process-flow)
  - [Card Scheme Working Principle](#card-scheme-working-principle)
  - [Apply Pay Flow](#apply-pay-flow)

---

Credit Card Payment Systems
---------------------------

### Process Flow

![Credit Card Process Flow 01](https://raw.githubusercontent.com/yidas/web-service-architectures/master/payment/transaction_flow_01.png)

![Credit Card Process Flow 02](https://raw.githubusercontent.com/yidas/web-service-architectures/master/payment/transaction_flow_02.png)

![Credit Card Process Flow 03](https://raw.githubusercontent.com/yidas/web-service-architectures/master/payment/transaction_flow_03.png)

> Reference: [WalletHub](https://wallethub.com/edu/credit-card-transaction/25511/)


### Card Scheme Working Principle

![How does VISA Work](https://github.com/ByteByteGoHq/system-design-101/raw/main/images/visa_payment.jpeg)

![How does card scheme make money](https://github.com/ByteByteGoHq/system-design-101/raw/main/images/how%20does%20visa%20makes%20money.jpg)

> Reference: [ByteByteGoHq/system-design-101 - Github](https://github.com/ByteByteGoHq/system-design-101#why-is-the-credit-card-called-the-most-profitable-product-in-banks-how-does-visamastercard-make-money)

### Regional Card Network

#### Authorization

#### Cleaering

![](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/yidas/web-service-architectures/master/payment/local-card-services-clearing.plantuml)

### Apply Pay Flow

![Apply Pay Flow](https://raw.githubusercontent.com/yidas/web-service-architectures/master/payment/flow_apple_pay.png)

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
