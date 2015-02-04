# Pages

The pages module is a simple but powerful way to manage static content on your site. Page layouts can be managed and widgets embedded without ever editing the template files.

* {{ docs:id_link title="How Pages Work in NitroCMS" }}
* {{ docs:id_link title="The Page Tree" }}
* {{ docs:id_link title="Re-Ordering Pages" }}
* {{ docs:id_link title="Default Pages" }}

</div>
<div class="doc_content">

## How Pages Work in NitroCMS

Every page on a website has a purpose. For instance, a page's purpose could be to display a member of a company's staff. It could be to display a product. It could be a combination of things. Every page has some common elements as well. For instance, a page will always have metadata, privacy settings, etc.

NitroCMS's pages module let's you take all of this into account when managing pages on your site. Each page has common fields (like metadata), but you can also create data structures that allow you to enter only the data you need for that page. We call these **page types**. For instance, for your staff member page you can create a <samp>Staff Member</samp> page type and add a <samp>Bio</samp> and <samp>Headshot Image</samp> field. You could create a <samp>Product</samp> page type with all sorts of fields like product description, price, etc.

Page types even house how those fields are displayed in the page type layout field, so you can define your fields and also define how they should be displayed on a page.

## The Page Tree

The page tree is a visual, heirarchical overview of all the pages on your site. Module URIs don't show up here (see {{ link title="NitroCMS URLs" uri="guides/pyrocms-urls" }} for an overview of how URLs work in NitroCMS), just pages.

You can have any combination of page types in your page tree as well - they'll all show up in your page tree.

## Re-Ordering Pages

Page re-ordering is achieved via simple drag and drop. You can drag/drop individual pages or entire sections (by dragging the parent page). There will be a shadow to show you where your page drag will end up.

{{ asset:img file="docs/pages/dragdrop.png" alt="Drag and Drop Pages" class="doc_image" }}

## Default Pages

You'll notice that on a default install of NitroCMS there are some pages already there in the tree:

<table>
	<tr>
		<th width="20%">Page</th>
		<th>Notes</th>
		<th>Status</th>			
	</tr>
	<tr>
		<td>Home</td>
		<td>Every site needs a home page! The home page is like any other page, it just has <strong>Is default (home) page?</strong> selected under the <strong>Options</strong> tab.</td>
		<td>live</td>			
	</tr>
	<tr>
		<td>Page Missing</td>
		<td>A 404 page that will be called when a page cannot be found.</td>
		<td>live</td>			
	</tr>
	<tr>
		<td>Contact</td>
		<td>This is an example page, using the contact module.</td>
		<td>live</td>			
	</tr>
	<tr>
		<td>Store</td>
		<td>TA default store page</td>
		<td>draft</td>		
	</tr>	
</table>