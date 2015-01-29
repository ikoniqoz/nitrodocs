# NitroCMS Folder Structure

NitroCMS only has three root-level folders with its default install (once you delete the installer folder), so it's important to know what each does.

</div>
<div class="doc_content">

## /addons/

All extra modules, plugins, widgets, and themes you add to NitroCMS go here in their respective folders. However, inside /addons/ there will be at least two folders:

1. default (most likely)
2. shared_addons

Since NitroCMS Pro is multi-site enabled, even single install of NitroCMS get its own slug (also used as a prefix for all your MySQL database table names). Although NitroCMS Community is _not_ multi-site enabled, it still needs an identifier. The default identifier is **default**, which is why NitroCMS creates a folder named **default** in the addons folder.

**NitroCMS Community Edition users:** put your add-ons in either folder - NitroCMS will look in both.

**NitroCMS Pro users:** all add-ons you wish to be available to all sites go in your shared_addons folder. Add-ons that only belong to specific sites can go in their respective folder (matching the site slug) created on installation of the site.

## /assets/

This is where your cached assets (JS, CSS, etc) are stored so they are web accessible. 

## /system/

The system folder contains two main things: a copy of CodeIgniter (the PHP framework that NitroCMS runs on) and NitroCMS itself. You will most likely never have to go inside this folder, but there are two files you should know:

### /system/cms/config/database.php

When NitroCMS installs, it will create this file for you with your MySQL credentials. However, if you want to change this data or add another {{ link uri="guides/environments" title="environment" }}, you'll need to edit this file.

### /system/cms/config/config.php

The CodeIgniter application config file has a whole lot of items you'll never need to touch. In fact, NitroCMS automatically sets your base url so you may never need to look at this file and be fine!

However, if you began without mod_rewriting URLs (i.e. with index.php still in them), and you want to {{ link uri="guides/pyrocms-urls#forcing-clean-urls" title="remove index.php from links" }} later on, you can remove that easily by finding:

	$config['index_page'] = 'index.php';

and changing it to:

	$config['index_page'] = '';
