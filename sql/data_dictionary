This data dictionary documents the structure of the Olist e-commerce dataset.  
It describes each table’s granularity, primary keys, and how tables relate to each other, serving as a reference to support analysis and SQL querying.
-------------------------------------------------------------------------------------------

## customers
Granularity:
- One row per customer

Primary key:
- customer_id

Relationships:
- customers.customer_id → orders.customer_id
-------------------------------------------------------------------------------------------
  
## orders
Granularity:
- One row per order

Primary key:
- order_id

Relationships:
- orders.customer_id → customers.customer_id
  -------------------------------------------------------------------------------------------

## order_items
Granularity:
- One row per order item 

Primary key:
- order_id, product_id

Relationships:
- orders.order_id → order_items.order_id
  -------------------------------------------------------------------------------------------

## order_payments
Granularity:
- One row per order payment

Primary key:
- order_id, payment_sequential

Relationships:
- orders.order_id → order_payments.order_id
  -------------------------------------------------------------------------------------------

## order_reviews
Granularity:
- One row per order review

Primary key:
- order_id

Relationships:
- orders.order_id → order_reviews.order_id
  -------------------------------------------------------------------------------------------

## products
Granularity:
- One row per product 

Primary key:
- product_id

Relationships:
- product_category.product_category_name → products.product_category_name
  -------------------------------------------------------------------------------------------

## product_category
Granularity:
- One row per product category

Primary key:
- product_category_name

Relationships:
- product_category.product_category_name→ products.product_category_name
  -------------------------------------------------------------------------------------------

## geolocation
Granularity:
- One row per geolocation

Primary key:
- none (non-unique zip code prefixes)


Relationships:
- geolocation.geolocation_zip_code_prefix → customers.customer_zip_code_prefix
  -------------------------------------------------------------------------------------------

## sellers
Granularity:
- One row per seller

Primary key:
- seller_id

Relationships:
- sellers.seller_zip_code_prefix → geolocation.geolocation_zip_code_prefix
