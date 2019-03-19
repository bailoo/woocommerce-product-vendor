# Product Vendors Developer Information
##Commission
Commissions are stored within the $prefix_wcpv_commissions table represented by the WC_PRODUCT_VENDORS_COMMISSION_TABLE global.

Commissions are calculated and persisted at checkout. The file responsible for managing the CRUD on commissions is `includes/class-wc-product-vendors-comissions.php`.

Discount applied to orders with product from multiple vendors are handled in the following manner. 
The percentage discount is applied on a per product basis. So each line equally gets the percentages applied and the commission is then adjusted downwards with the same percentage.


