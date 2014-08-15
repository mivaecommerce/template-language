# Page Reference Guide

| Page Code | Page Name | Page Description |
| -- | -- | -- |
|ABUS|About Us|This is a content page for your About Us page.|
|ACAD|Customer Create|This is the page that is used for customer account creation.|
|ACED|Customer Edit|This is the page that gets displayed when a user logs into their account and click edit my account.|
|ACLN|Customer Account|This is the customer account landing page. A customer is taken here after they login. It gives them the option to edit their account information and view order history.|
|ACRT|Customer Password Reset|This is the page that is used for customer account password resets|
|AFAD|Affiliate Create|This page is similar to customer create but for affiliates. Used when affiliates create a new account.|
|AFCL|Affiliate Login|This is the login page specifically for affiliates.|
|AFED|Affiliate Edit|This page is the affiliate edit page. It is displayed when an affiliate logs into their account and edits their affiliate information.|
|BASK|Basket Contents|This page displays the shopping basket contents.|
|BSKE|Checkout: Basket Empty|This page is displayed if you attempt to checkout and you have nothing in your cart.|
|CEML|Change Email Address|This is the page that is used for customer account email changes.|
|CPWD|Change Password|This is the page that is used for customer account password changes.|
|CTGY|Category Display|This page controls the layout of the category page.|
|CTUS|Contact Us|This is a content page for your Contact Us page.|
|EMAIL_BACKORDER_NOTICE*|Backorder Notice|This is the page template for the backorder notice email. It gets sent to the customer when you mark an item within an order as backordered.|
|EMAIL_CUSTOMER_CREATED*|Customer Created|This is the page template for the customer created email. It gets sent to the customer when they create an account.|
|EMAIL_ORDERCONF_CUSTOMER*|Order Confirmation: Customer|This is the page template for the customer confirmation email. It gets sent to the customer immediately after they place an order.|
|EMAIL_ORDERCONF_MERCHANT*|Order Confirmation: Merchant|This is the page template for the merchant confirmation email. It gets sent to the merchant (store owner) immediately after an order is placed.|
|EMAIL_RETURN_RECEIVED*|Return Received|This is the page template for the return received email. This gets sent to the customer when the item they returned gets marked as received in the admin.|
|EMAIL_RMA_ISSUED*|RMA Issued|This is the page template for the RMA issued email. It gets sent to the customer when an RMA (Return Merchandise Authorization) number is generated in the admin.|
|EMAIL_SHIPMENT_SHIPPED*|Shipment Shipped|This is the page template for the shipment shipped email. This gets sent when you mark and item as shipped the admin.|
|FAQS|FAQs|This is a content page template for frequently asked questions.|
|FPWD|Forgot Password|This is the page template used for customers who request to reset thier passwords. It is displayed immediately after the forgot email is sent.|
|INVC|Invoice|This is the page template for the invoice (order confirmation) page. It is the last step in the checkout process and is displayed immediately after the order is placed.|
|LOGN|Customer Login|This is the customer login page template.|
|MNTN|Maintenance Mode|This is the maintenance mode page template. When an store is placed in maintenance mode all page requests will show this template.|
|NTFD|Not Found|This is the page not found template. It acts like a 404 page. If you try to access a page that does not exist in Miva Merchant this template will be displayed.|
|OCST|Checkout: Customer Information|This is the customer information page template. It is the first page of checkout and provides the inputs for the customer bill to / ship to fields.|
|OMIN|Checkout: Minimum Purchased Required|This page is displayed during the checkout process if you attempt to checkout and do not meet the minimum order quantity or dollar value requirements set within the admin.|
|OPAY|Checkout: Payment Information|This is the page template for payment information. It provides the fields needed to collect the customers credit card information.|
|OPRC|Order Already Processed|The page is shown if the customer tries to refresh the invoice page once the order has been placed.|
|ORDER_INVOICE*|Printable Invoice|This is the page template for the invoice batch report. This is commonly used for printing a formatted order summary and is triggered from the manage orders screen by selecting orders and hitting the Batch Report button.|
|ORDH|Order History List|This is the order history page template. It is displayed after a customer logs into their account and clicks on order history.|
|ORDL|Order: Customer Login|This is the login page when the customer is in the act of checking out. The main difference between this page and LOGN is it has a hidden input of Order=1 to tell Miva to keep them in the checkout process after they login or create a new account.|
|ORDS|Order Status|This is the page template that shows the order detail when a customer is looking up their order history.|
|ORHL|Lookup Order History|This is the page template for the landing page when a customer clicks on order history and they are not logged in. It will allow them to login to their account if they have one or lookup their order using their email address and zip code.|
|OSEL|Checkout: Shipping/Payment Selection|This is the shipping selection and payment method selection page template during the checkout process.|
|OUS1|Checkout: Upsell Product (Single)|This is the single upsell page template. This page gets inserted after OCST if you have upsell turned on and there is a single upsell product.|
|OUSM|Checkout: Upsell Product (Multiple)|This is the multiple upsell page template. This page gets inserted after OCST if you have upsell turned on and there are more than one upsell products.|
|PATR|Missing Product Attributes|The page is displayed if a customer tries to add a product to the cart that has attributes but they don’t select one or more of the required attributes.|
|PLMT|Product Limited Stock|This page is shown to the a customer has a product in their basket and attempt to change the quantity to a quantity higher than is available.|
|PLST|Product List|This page lists every active product in your store. By default it is paginated for every 10 products.|
|POUT|Product Sold Out|This page template gets displayed to the customer if they attempt to purchase a product that is no sold out or currently out of stock.|
|PROD|Product Display|This is the product page page template. It controls the layout of the product display page.|
|PRPO|Privacy Policy|This is a content page for your Privacy Policy page.|
|SARP|Shipping and Return Policy|This is a content page for your Shipping and Return Policy page|
|SFNT|Storefront|This is the page template for your storefront page. (home page, index page)|
|SHIPMENT_PICKLIST*|Shipment Picklist|This page is used to print shipment picklist and packing slips. It is triggered in the manage shipments section after you select a shipment(s) and click batch report.|
|SRCH|Search|This is the page template for the search results page.|
|UATM|Upsell: Missing Product Attributes (Multiple)|This page is displayed after a user selects an single upsell product but does not select a required attribute.|
|UATR|Upsell: Missing Product Attributes (Single)|This page is displayed after a user selects multiple upsell products but does not select a required attribute.|

*PR8 or Newer. These pages not visible from a web browser and only used in the admin.

## Pseudo Page Reference Guide

|Page Code|Page Name|Page Description|
| -- | -- | -- |
|ACNT|Customer Account|This pseudo page will take a customer to ACAD (account create) if they are not logged in or take them to ACED (account edit) if they are logged in.|
|AFAE|Affiliate Account|This pseudo page takes an affiliate to either AFAD (Affiliate Add) or AFED (Affiliate Edit) depending if the affiliate is logged in or not.|
|OINF|Initiate Checkout|This pseudo page takes the customer to ORDL (Order Login) or OCST (customer information page) depending on which setting you have set in the Miva admin and also if they are already logged in as a customer.|
|OUSL|Upsell Page Selection|The OCST (customer information) page submits its form to this pseudo page. If an upsell is available it will either show OUS1 (for a single upsell) or OUSM (for multiple). If no upsells are available it takes the user to the next step in checkout, OSEL (payment/shipping selection)|
