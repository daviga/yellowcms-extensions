Sitemap template 0.1.5
======================
Sitemap for website.

How do I install this?
----------------------
1. Download and install [Yellow](https://github.com/markseu/yellowcms/).  
2. Download [sitemap.php](sitemap.php?raw=true) and [sitemapxml.php](sitemapxml.php?raw=true), copy both files into your `system/templates` folder.  
3. Create a new folder 'sitemap' in your `content` folder.
4. Download [page.txt](page.txt?raw=true) and [sitemap.xml.txt](sitemap.xml.txt?raw=true), copy both files into your `content/sitemap` folder.

To uninstall delete the template files and folder.

How to use a sitemap?
---------------------
The sitemap is available as `http://website/sitemap/` and `http://website/sitemap/sitemap.xml`. It's an overview of the entire website, only visible pages are included. For search engines it's recommended to add a link to the header snippet, see example below.

Example
-------
Header snippet with sitemap:

    <!DOCTYPE html>
    ...
    <link rel="sitemap" type="text/xml" href="<?php echo $yellow->config->get("serverBase")."/sitemap/sitemap.xml" ?>" />
    <?php echo $yellow->page->getHeaderExtra() ?>
    </head>
    <body>
    <div class="page">

Footer snippet with sitemap:

    <div class="footer">
    <a href="<?php echo $yellow->page->base."/" ?>">&copy; 2015 <?php echo $yellow->page->getHtml("sitename") ?></a>.
    <a href="<?php echo $yellow->page->base."/sitemap/" ?>">Sitemap</a>. 
    <a href="http://datenstrom.se/yellow">Made with Yellow</a>.
    </div>
    </div>
    </body>
    </html>