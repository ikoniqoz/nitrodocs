# Admin Theme Helper

This helper is intended to be used with your Admin Theme.

## Functions



### file_partial($file = '', $ext = 'php')

Loads a file partial from your Theme Views Partials folder. `echo`'s directly to the page.

<table cellpadding="0" cellspacing="0">
	<tbody>
		<tr>
			<th width="100">Name</th>
			<th width="100">Default</th>
			<th width="100">Required</th>
			<th>Description</th>
		</tr>
		<tr>
			<td>file</td>
			<td></td>
			<td>Yes</td>
			<td>The path to the view. Inside <dfn>THEME_VIEWS_FOLDER/partials/</dfn></td>
		</tr>
		<tr>
			<td>ext</td>
			<td>php</td>
			<td>No</td>
			<td>Extension of the file of other than <em>php</em></td>
		</tr>
	</tbody>
</table>


### template_partial($name = '')

Loads a template partial previously set with `$this->template->partial()`. `echo`'s directly to the page.

<table cellpadding="0" cellspacing="0">
	<tbody>
		<tr>
			<th width="100">Name</th>
			<th width="100">Default</th>
			<th width="100">Required</th>
			<th>Description</th>
		</tr>
		<tr>
			<td>name</td>
			<td></td>
			<td>Yes</td>
			<td>The name you set the partial as</td>
		</tr>
	</tbody>
</table>

{{# Internal only?
### accented_characters()

Returns the array of the accented characters and their replacements set in <dfn>config/foreign_chars.php</dfn>.
#}}


### add_template\_section($obj,$section,$text,$path,$shortcust=[])

Adds a section to the current view.

<table cellpadding="0" cellspacing="0">
	<tbody>
		<tr>
			<th width="100">Name</th>
			<th width="100">Default</th>
			<th width="100">Required</th>
			<th>Description</th>
		</tr>
		<tr>
			<td>$obj</td>
			<td>$this</td>
			<td>Yes</td>
			<td>Pass singleton (this) from the controller only</dfn></td>
		</tr>
		<tr>
			<td>$section</td>
			<td></td>
			<td>Yes</td>
			<td>String literal of the section to add</td>
		</tr>
		<tr>
			<td>$text</td>
			<td></td>
			<td>Yes</td>
			<td>Display Text</td>
		</tr>		
		<tr>
			<td>$path</td>
			<td></td>
			<td>Yes</td>
			<td>URI to link to</td>
		</tr>
		<tr>
			<td>$shortcust</td>
			<td></td>
			<td>No</td>
			<td>Array of shortcusts to add to the section</td>
		</tr>					
	</tbody>
</table>


     	$shortcuts = 
		[
		    ['name' => 'Categories', 'uri' => 'admin/blog/categories/'], 
		    ['name' => 'Posts', 'uri' => 'admin/blog/posts'], 
		];

        add_template_section($this,'sectionname','Section Text','admin/blog',$shortcuts); 



### add_template\_shortcuts($obj,$section,$shortcust=[])

Ads shortcusts to an existing section

<table cellpadding="0" cellspacing="0">
	<tbody>
		<tr>
			<th width="100">Name</th>
			<th width="100">Default</th>
			<th width="100">Required</th>
			<th>Description</th>
		</tr>
		<tr>
			<td>$obj</td>
			<td>$this</td>
			<td>Yes</td>
			<td>Pass singleton (this) from the controller only</dfn></td>
		</tr>
		<tr>
			<td>$section</td>
			<td></td>
			<td>Yes</td>
			<td>String literal of the section to add the shortcuts to</td>
		</tr>
		<tr>
			<td>$shortcust</td>
			<td></td>
			<td>Yes</td>
			<td>Array of shortcusts to add to the section</td>
		</tr>					
	</tbody>
</table>

     	$shortcuts = 
		[
		    ['name' => 'Categories', 'uri' => 'admin/blog/categories/'], 
		    ['name' => 'Posts', 'uri' => 'admin/blog/posts'], 
		];

        add_template_section($this,'sectionname',$shortcuts); 