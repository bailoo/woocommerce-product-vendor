# woocommerce-product-vendor
WooCommerce Product Vendor Plugin

This provides a fix that works for a large number of vendors on a shared server. Tested to work with 15k+ vendors on WPEngine start-up plan shared server.

The issue is that `woocommerce product vendor plugin` queries for all vendors whenever a `vendor manager` logins and then searches through the entire vendor list to find out which vendors are managed by the given user. This results in long SQL queries that are killed on a shared server. 

We have fixed the issue by introducing a user meta field `_sc_wcpv_vendor` that stores the vendor id for each user. 
