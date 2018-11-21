Master Card
===========

Some bank's online payment use Master Card payment service such as HSBC.

Legacy Payment Service
----------------------

Master card has a legacy Payment Service implemented by two-way authorization in a pair redirect request.

![payment-master-card](https://raw.githubusercontent.com/yidas/web-service-architectures/master/third-party-payment/master-card/payment_master-card.io.png)

1. The token is a hash value which contains specified order information referred to GET parameters from application to Master Card payment's landing page.
The payment endpoint will verify the token depended on giving merchant account ID information.

2. When the client successfully finished the payment, Master Card payment's page will redirect back with received order information and a token for application verification.

> The two-way hash authorization is based on Master Card standard.

