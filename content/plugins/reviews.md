# Reviews Plugin (E-commerce|NitroCart)


The _reviews_ plugin allows you to access user user reviews for the Ecommerce NitroCart system.



# reviews:product 

Allows you display reviews of on a product. You can set optional params to limit to a number of reviews and only count reviews above a rating.

### Example

	{{ noparse }}
	{{ reviews:product id='PRODUCT_ID' limit='5' above='0' }}​
		{{id}}
		{{review}}
		{{rating}}
		{{comment}}
	{{ /reviews:product }}​
	{{ /noparse }}

Returns:

	{{ noparse }}
	An array of reviews

		{{id}}
		{{review}}
		{{rating}}
		{{comment}}
	{{ /noparse }}


# reviews:average 

Get the average product review rating

### Example

	{{ noparse }}
	The average rating of this product is 
	{{ reviews:average product='PRODUCT_ID' }}​
	{{ /noparse }}

Returns:

		The average rating of this product is 3.5





# reviews:num_reviews 

Get the total # of reviews for a product

### Example

	{{ noparse }}
		Total of  
		{{ reviews:num_reviews product='PRODUCT_ID' }}​ reviews
	{{ /noparse }}

Returns:

		Total of 3.5 reviews





# reviews:info 

This is a powerful plugin to access review ingo on a product.

### Example

	{{ noparse }}
		{{ reviews:info product_id='PRODUCT_ID' }}​ 

			{{if has_reviewed}}
				You have reviewed this item.
			{{endif}}
			
			{{if can_review}}
				....html...
			{{else}}
				You can not review the product again
			{{endif}}

		{{ /reviews:info }}​ 
	{{ /noparse }}

Returns:

		You have reviewed this item.
		You can not review the product again
