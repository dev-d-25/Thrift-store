# Thrift-store
ER diagram from thrift-store DB design 
## There is some notes written below image check it out

<img width="4015" height="5862" alt="image" src="https://github.com/user-attachments/assets/810fdac4-f690-47ca-9963-bc1c1105f5dc" />



## Products

It is divided in to 2 diff tables 
This acts as a base table, extended by subtype tables bcz each one diff attributes and they have one to one relation ((ISA relationship) like Product is parent and it is inheritated by handmade ot thrift) 
- handmade_products 
- thrift_products

## Snapshot Strategy
Order stores:
price_at_purchase
product_name_snapshot
Prevents issues when product data changes later

## Decoupled Payment & Shipping
BecauseSupport of :
multiple payment flows

## Jumping tables 
- it is added for cart -> cart_items 
- also for order -> order_items 
