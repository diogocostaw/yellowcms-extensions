Blogarchive snippet
===================
Monthly archive for blog.

How do I install this?
----------------------
1. Download and install [Yellow](https://github.com/markseu/yellowcms/).  
2. Download and install [Yellow blog template](https://github.com/markseu/yellowcms-extensions/blob/master/templates/blog/README.md).  
3. Download [blogarchive.php](blogarchive.php?raw=true), copy into your system/snippets folder.  
4. Use the snippet on your website, edit templates in your system/templates folder.
5. Customise style sheets in your system/themes folder.

To uninstall delete the snippet and remove it from templates.

Example
-------
Blog template with archive:

    <?php $yellow->snippet("header") ?>
    <?php $yellow->snippet("sitename") ?>
    <?php $yellow->snippet("navigation") ?>
    <div class="content blog">
    ...
    <?php $yellow->snippet("blogarchive", $yellow->page->getParentTop()) ?>
    </div>
    <?php $yellow->snippet("footer") ?>

Blog articles template with archive:

    <?php $yellow->snippet("header") ?>
    <?php $yellow->snippet("sitename") ?>
    <?php $yellow->snippet("navigation") ?>
    <div class="content blogarticles">
    ...
    <?php $yellow->snippet("blogarchive", $yellow->page) ?>
    <?php $yellow->snippet("pagination", $pages) ?>
    </div>
    <?php $yellow->snippet("footer") ?>

Style for blog archive:

    .blogarchive ul { margin:0; padding:0; list-style:none; }