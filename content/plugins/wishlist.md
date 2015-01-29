# Wishlist Plugin


The _wishlist_ plugin allows you to access user wishlist data when the _NitroCMS_ module is installed.



# wishlist:in_wishlist 

Allows you display the Double Tag content if the item is in the wishlist.

### Example

	{{ noparse }}
	{{ wishlist:in_wishlist id='PRODUCT_ID' }}​
		This item is in your wishlist
	{{ /wishlist:in_wishlist }}​
	{{ /noparse }}

Returns:

	'This item is in your wishlist'
	



# wishlist:notin_wishlist 

Allows you display the Double Tag content if the item is NOT in the wishlist. (Same as in_wishlist but it is the direct opposite.)

### Example

	{{ noparse }}
	{{ wishlist:notin_wishlist id='PRODUCT_ID' }}​
		This item is NOT in your wishlist
	{{ /wishlist:notin_wishlist }}​
	{{ /noparse }}

Returns If item Does NOT exist in list:

	
		'This item is NOT in your wishlist'
