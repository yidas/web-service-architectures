Cybersource
===========

This diagram shows how real-time electronic card processing works:

![cybs](https://developer.cybersource.com/content/dam/new-documentation/transitional/en/dita-payouts/PayoutsTransactionFlow.jpg/_jcr_content/renditions/cq5dam.web.1280.1280.jpeg)

1. Collect debit card information and initiate payments. To manage PCI scope, you can use CyberSource Secure Acceptance and the Token Management Service.
2. Initiate the CyberSource Payouts API to disburse funds to the recipient.
3. CyberSource sends the payment instruction to the acquirer processor or, if CyberSource is providing acquirer processing functions, to VisaNet directly.
4. The processor routes the transaction to the Visa or Mastercard payment network.
5. The network routes the transaction to the card issuer for approval.
6. If the funds are approved by an issuer participating in Fast Funds,1 funds become available within thirty minutes; if not, funds become available within two business days.
7. Payment networks settle with the acquirer by withdrawing funds from the acquirer's settlement account.
9. The payment network delivers settlement and reconciliation data for reporting.
9. CyberSource transaction detail and summary-level reporting is available to you as well as the acquirer.
10. Funds are transferred from your business bank account to the acquirer for daily settlement.

> Reference: [CyberSource’s Payment Process](https://developer.cybersource.com/docs/cybs/en-us/payouts/developer/all/rest/payouts/HowItWorks.html)

---

## EMV3DS (3DS 2.0)

![](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/yidas/web-service-architectures/master/payment/cybersource/payer-authentication-emv3ds.plantuml)


---

## References
