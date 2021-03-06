# Installing NitroCMS

NitroCMS is simple to download and install - all you need is a basic development environment and you're ready to go! This page will walk you through the installation process.

</div>
<div class="doc_content">

## Download NitroCMS

Once you have an environment that meets {{ link uri="reference/server-requirements" title="the requirements" }}, you'll need to <a href="http://nitrocart.net/download">download NitroCMS</a>.

If you are familiar with [git](http://git-scm.com/), you can clone a copy of the repository from our [GitHub repo](https://github.com/nitroweb/nitrocms) page:

    git clone -o pyrocms https://github.com/nitroweb/nitrocms -b 1.0/master

Make sure you are using the correct branch - the {{ link title="NitroCMS versions guide" uri="reference/nitrocms-versions" }} explains the difference between branches. If you are using git to pull down changes from NitroCMS, check out our {{ link title="example git workflow" uri="guides/git-workflow" }}.

## Open the Installer

Download and extract the NitroCMS files into your development folder of choice. Next, visit the URL where your install is. For example, if we extracted NitroCMS into a folder called <strong>nitro</strong> on our development environment, we'd visit:

    http://localhost/nitro/

The installer will load an walk you throught the necessary steps to install NitroCMS.

<div class="note"><p>Installation troubles? Check out some troubleshooting tips in our <a href="reference/troubleshooting">Troubleshooting Guide</a>.</p></div>

Once it's done, you'll have a link to your NitroCMS site as well as the admin area so you can log in. The admin panel is always located at /admin, in our **nitro** folder example, you can find your admin panel at:

    http://localhost/nitro/admin

<div class="note"><p>Once you log into your admin panel for the first time, NitroCMS may prompt you to delete your installation folder if it wasn't able to do so autmoatically. <strong>It's very important to delete your install folder!</strong></p></div>

Go ahead and log into NitroCMS for the first time with the account you created during the installation process. You're now ready to get started!

<hr>

{{ link uri="getting-started/configuring-nitrocms" title="Next: Configuring NitroCMS" }}
