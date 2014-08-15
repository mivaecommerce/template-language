# Pseudo Pages

These are Pages in Miva Merchant that don’t have Page Templates associated with them in the Miva Merchant Admin. An example of this would be the OINF page. It is used to initiate the checkout process however it does not have its own page template. Instead, the OINF page has logic built in that will direct you to either the OCST Page (Customer Information Page) if you are logged in or the ORDL Page (Order Login Page) if you are not logged in. This functionality is all built into the Pseudo Page, OINF.

Luckily there are only 4 Pseudo Pages in Miva: OINF, ACNT, AFAE and OUSL. A detailed description of each can be found in the Page Reference Guide.

## Reference Guide

|Page Code|Page Name|Page Description|
| -- | -- | -- |
|ACNT|Customer Account|This pseudo page will take a customer to ACAD (account create) if they are not logged in or take them to ACED (account edit) if they are logged in.|
|AFAE|Affiliate Account|This pseudo page takes an affiliate to either AFAD (Affiliate Add) or AFED (Affiliate Edit) depending if the affiliate is logged in or not.|
|OINF|Initiate Checkout|This pseudo page takes the customer to ORDL (Order Login) or OCST (customer information page) depending on which setting you have set in the Miva admin and also if they are already logged in as a customer.|
|OUSL|Upsell Page Selection|The OCST (customer information) page submits its form to this pseudo page. If an upsell is available it will either show OUS1 (for a single upsell) or OUSM (for multiple). If no upsells are available it takes the user to the next step in checkout, OSEL (payment/shipping selection)|
