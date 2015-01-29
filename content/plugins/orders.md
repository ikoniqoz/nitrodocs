# Orders Plugin


The orders plugin allows you to display customer order info.





# orders:orders 

List all client orders

### Example

	{{ noparse }}
	{{ orders:orders user='4' }}​
	{{ /noparse }}

Returns:

	0 => ['1','paid',..]
	1 => ['2','notpaid',..]
	2 => ['3','paid',..]
	




# orders:get 

Get an order from the system. Must be valid by logged in user.

### Example

	{{ noparse }}
	{{ orders:get id='1' }}​
	{{ /noparse }}


Returns:

	{{ noparse }}
		Order info
	{{ /noparse }}



# orders:status 

Gets the status of an order

### Example

	{{ noparse }}
	{{ orders:status id='1' }}​
	{{ /noparse }}


Returns:




