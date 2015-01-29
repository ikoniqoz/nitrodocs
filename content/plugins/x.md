# X Plugin


The _x_ plugin allows you to quickly access and repidly interact with the Ecommerce features and subsystems of NitroCMS.

The _x_ label was chosen instead of _nitrocart_ as we know it would be utilised many times so as a time saving effort _x_was voted in.



It is currently marked as experimental and added ontop of the older 'PyroCMS' platform.


# x:uri 

A short hand to access Store URI/URL without having to know what the store slug was labelled.
Additionally, this allows your store slug to be dynamically changed and all your links will update as they are not hard coded.

### Example

	{{ noparse }}{{ x:uri }}​{{ /noparse }}

Returns:

	'http://www.example.com/store'
	




### Example

	{{ noparse }}{{ x:uri }}​/checkout{{ /noparse }}

Returns:

	'http://www.example.com/store/checkout'






# x:bool 

A helpful plugin to display Boolean values or convert values

### Example

	{{ noparse }}{{ x:bool value='1' }}​{{ /noparse }}

Returns:

	'Yes'
	



### Example

	{{ noparse }}{{ x:bool value='0' }}​{{ /noparse }}

Returns:

	'No'


### Example

	{{ noparse }}{{ x:bool value='1' tt='Cool' ft='Damn' }}​{{ /noparse }}

Returns:

	'Cool'


