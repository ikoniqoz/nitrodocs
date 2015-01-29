# Products Plugin


The _products_ plugin allows you to quickly access Product information  about any live product in the NitroCart/Ecommerce system.


* {{ docs:id_link title="products-link" }}
* {{ docs:id_link title="products-variant" }}	
* {{ docs:id_link title="products-fromprice" }}
* {{ docs:id_link title="products-products" }}	
* {{ docs:id_link title="products-htmloptions" }}
* {{ docs:id_link title="products-options" }}	


# products:link 

! This is an experimental plugin
Creates a dynamic link to your product. No need to know the ROUTE/slug of the store.

### Example

	{{ noparse }}
	{{ products:link product_id='5'}}​
	{{ /noparse }}

Returns:

	"<a href='http://www.example.com/store/products/product/5'>Click me</a>"
	



### Example with custom text and Css Class

	{{ noparse }}
	{{ products:link product_id='5' text='Click Here' class='alink'}}​
	{{ /noparse }}

Returns:

	"<a class='alink' href='http://www.example.com/store/products/product/5'>Click Here</a>"
	



# products:variant 

Retrieves the Variant name

### Example

	{{ noparse }}
	{{ products:variant id='3'}}​
	{{ /noparse }}

Returns:

	Size=200ml&Color=Green



# products:fromprice 

Retrieves the from price of a product

### Example

	{{ noparse }}
	{{ products:fromprice product='8' na='N/A' fromtext='from' x='ASTERIX'}}​
	{{ /noparse }}

Return if multiple prices:

	from $7.00* 

Return if NO multiple prices:		
	
	$7.00 




# products:products 

Get a listing of products

### Example

	{{ noparse }}
	{{ products:products }}​
		{{id}},
		{{name}},
		{{slug}}
	{{ /products:products }}​	
	{{ /noparse }}


Return 		
	
	0 => 7, Tonka Truck, tonka-truck 	
	1 => 8, Racing Car, racing-car 	



# products:featured 

Get a listing of featured products. This is exactly identicle to products:products but only shows featured items.

### Example

	{{ noparse }}
	{{ products:featured }}​
		{{id}},
		{{name}},
		{{slug}}
	{{ /products:featured }}​	
	{{ /noparse }}	




# products:product 

Get a Product

### Example

	{{ noparse }}
	{{ products:product }}​
		{{id}}
		{{name}}
		{{slug}}
	{{ /products:product }}​	
	{{ /noparse }}		



# products:options 

Get a Product's list of options

### Example

	{{ noparse }}
	{{ products:options product_id='5'}}​
	{{ /products:options }}​	
	{{ /noparse }}			

# products:htmloptions 

A simpler way to display options

### Example

	{{ noparse }}
	{{ products:htmloptions product_id='5'}}​
	{{ /noparse }}				

