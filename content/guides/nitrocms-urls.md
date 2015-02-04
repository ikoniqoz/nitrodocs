# NitroCMS URLs

One of the most important concepts to understand about NitroCMS is where URLs resolve to and how to create your site's URLs using the tools available. This page explains how URLs are structured in NitroCMS.

* {{ docs:id_link title="Page URLs" }}
* {{ docs:id_link title="The Home Page" }}
* {{ docs:id_link title="404 Page" }}
* {{ docs:id_link title="Module URLs" }}
* {{ docs:id_link title="Forcing Clean URLs" }}

</div>
<div class="doc_content">

## Page URLs

By default, most URLs are routed to the NitroCMS Pages module, which is where your site's page tree is stored. If you go to **Content &rarr; Pages**, you'll see something like this:

{{ asset:img file="docs/pages.png" alt="Page Tree" class="doc_image" }}

If you are familiar with a page tree, you should be right at home! This represents pages in a nested hierarchy, so if you have a page at <samp>yoursite.com/about</samp>, a nested page with the slug of <samp>history</samp> will be accessed at <samp>yoursite.com/about/history</samp>. Pretty simple!

By default, URLs are _strict_ meaning that if you create a page with the URL <samp>yoursite.com/team</samp> and you tried to access <samp>yoursite.com/team/bob</samp>, the Pages module would only look for a page with the URI of <samp>team</samp> and return a 404. However, in the <dfn>Options</dfn> tab of your pages, you can turn strict URLs, so that <samp>yoursite.com/team/bob</samp> will display the page you created at <samp>yoursite.com/team</samp> (so will <samp>yoursite.com/team/foo</samp> and anything else, for that matter). See the {{ link uri="modules/pages" title="Pages module documentation" }} for more information.

## The Home Page

Although NitroCMS comes with a default home page, _any_ page in NitroCMS can be the home page. Just go into the <dfn>Options</dfn> tag in the page and select the check box that says "Is default (home) page?". This will tell NitroCMS to load this page whenever your site's root URL is loaded.

{{ asset:img file="docs/homepage.png" alt="Home Page" class="doc_image" }}

## 404 Page

All pages that are not found in NitroCMS are routed to the Pages module, where a special 404 page handles them. This page simply has to have a slug of <dfn>404</dfn>, and NitroCMS will use it as the 404 and set the correct 404 headers accordingly.

## Module URLs

NitroCMS is a _modular_ CMS, and modules in NitroCMS can have their own front-end URLs in additon to back-end URLs.

The first segment in a URL will be the module name, so to access the "news" module you would call <samp>/news</samp>. This would then load the news.php controller in your news module (because the names match) and reference the index() method. Calling <samp>/news/category</samp> would call the method foo() inside the news.php controller.

The second segment could be a method inside the default controller as outlined above, or it could be a secondary controller. For example, <samp>/news/gallery/view/some-article</samp> would load the gallery.php controller inside the news module, and reference the view() method.

Most modules do not use front-end URLs, but some do. Check with the documentation of your modules to see if they have any front-end URLs.

## Forcing Clean URLs

During installation, NitroCMS will ask you if you have Apache's [mod_rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html) installed. This has to do with the PHP framework NitroCMS is built on,
[CodeIgniter](http://www.codeigniter.com).

In CodeIgniter, everything is routed through the index.php file, so your URL might look like:

     http://www.example.com/index.php/about

Obviously, we want to remove that ugly index.php, and you can do so with an .htaccess file, and Apache's mod_rewrite.

To remove the index.php, create a file at the root of your NitroCMS site called **.htaccess**. You can [find out more about .htaccess here](http://httpd.apache.org/docs/current/howto/htaccess.html), but for our purposes here we just want to use it to hide index.php in our URLs.

Not every web server is the same, but something along these lines should work for your purposes:

    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ /index.php?/$1 [L]

This tells Apache to remove the index.php from the URL entirely (whilst still serving any 'real' files -f or directories -d from your docroot.)

Your URLs will now look clean and smooth:

     http://www.example.com/about

If you chose the no mod_rewrite during installation and your links keep adding the index.php, open up **system/cms/config/config.php** and change:

     $config['index_page'] = 'index.php';

to:

     $config['index_page'] = '';

This will stop NitroCMS from prefixing links with index.php when URLs are automatically generated by the system.