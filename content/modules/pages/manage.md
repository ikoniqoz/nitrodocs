# Pages

The pages module is a simple but powerful way to manage static content on your site. Page layouts can be managed and widgets embedded without ever editing the template files.


* {{ docs:id_link title="Modifying Pages" }}
* {{ docs:id_link title="Default Pages" }}
* {{ docs:id_link title="Modifying Pages" }}
* {{ docs:id_link title="Adding a New Page" }}

</div>
<div class="doc_content">

## Modifying Pages

To modify a page, click it in the page tree. A data summary panel will show, with options for modifying the page.

{{ asset:img file="docs/pages/page\_options.png" alt="Page Options" class="doc_image" }}

The following options are available:

<table>
	<tr>
		<th width="30%">Option</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Add Child</td>
		<td>Adds a child page to the current page.</td>
	</tr>
	<tr>
		<td>Duplicate</td>
		<td>Duplicates a page <em>and all child pages</em>.</td>
	</tr>
	<tr>
		<td>Edit</td>
		<td>Edit a page.</td>
	</tr>
	<tr>
		<td>Delete</td>
		<td>Delete a page and its child pages.</td>
	</tr>
</table>


## Adding a New Page

To add a new page, click <samp>Add Page</samp>. If you only have one page type, your new page will automatically use that page type. However, if you have several page types, you'll be able to select each page type from a pop up menu.

{{ asset:img file="docs/choosept.png" alt="Choose a Page Type" class="doc_image" }}

Once you select your page type, you'll see the page form. The page form is divided into tabs:

### Page Details

This is the basic info about your page - title, content, etc.

<table>
	<tr>
		<th width="30%">Field</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Title</td>
		<td>The full title of your page. You can override the title of this field when editing your page type, by changing the value of the <samp>Title Label</samp> field.</td>
	</tr>
	<tr>
		<td>Slug</td>
		<td>The slug that your page will be called by in the URI. Along with the slug, a preview of the full URI of your page is provided.</td>
	</tr>
	<tr>
		<td>Status</td>
		<td>"Live" or "Draft". Draft pages can be seen by Administrators, but will not be available to other groups.</td>
	</tr>
</table>

### Page Content

If the page type for this page has fields added to it, those fields will show up here. You can override the name of this tab when editing your page type, using the <samp>Content Tab Label</samp> field. This is so you can name it something more descriptive like "Product Info".

### Meta data

The meta section allows you to control the meta data of your page. This is the data that is traditionally used by search engines (sans keywords) to populate the text preview of your page that shows up in search results.

<table>
	<tr>
		<th width="30%">Field</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Meta title</td>
		<td>The full title of your page.</td>
	</tr>
	<tr>
		<td>Meta Keywords</td>
		<td>Keywords the pretain to your page.</td>
	</tr>
	<tr>
		<td>Meta description</td>
		<td>A short (no more than 160 character) description of your page.</td>
	</tr>
</table>

### CSS

The CSS tab allows you to add extra CSS that will be added to your page (inline). NitroCMS will wrap the appropriate `<style>` tags around the CSS.

### Script

You may place javascript here that you would like appended to the `<head>` of the page. NitroCMS will wrap the appropriate `<script>` tags around the javascript.

### Options

<table>
	<tr>
		<th width="30%">Field</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Access</td>
		<td>Allows you to restrict access to this page to certain user groups. Groups without access will see a 404 page.</td>
	</tr>
	<tr>
		<td>Comments Enabled?</td>
		<td>Turns comments on and off for this page.</td>
	</tr>
	<tr>
		<td>RSS Enabled</td>
		<td>If the RSS feed is enabled an RSS feed will be created that a visitor can subscribe to. They will receive each child page in their rss reader.</td>
	</tr>
	<tr>
		<td>Is default (home) page?</td>
		<td>If this is checked, this page will be the page that loads up on your root URI.</td>
	</tr>
	<tr>
		<td>Require an exact uri match</td>
		<td>The "Require an exact uri match" field is a clever little tool that allows you to pass parameters in the url. By default NitroCMS looks for a page with the slug of "acme-widgets" that is the child of "products" when you visit products/acme-widgets. By un-checking this box in the Products page you are telling NitroCMS that it is now okay if there isn't a page named Acme Widgets. It will now load Products and 'acme-widgets' will just be a parameter. This makes it easy to pass parameters to embedded tags. An example using the Streams add-on to display the 'acme-widgets' stream on the Products page.</td>
	</tr>
</table>