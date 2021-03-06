Imagelist snippet
=================
List of images for website.

How do I install this?
----------------------
1. Download and install [Yellow](https://github.com/markseu/yellowcms/).  
2. Download [imagelist.php](imagelist.php?raw=true), copy into your system/snippets folder.  
3. Use the snippet on your website, edit templates in your system/templates folder.

To uninstall delete the snippet.

How to create a list of images?
-------------------------------
Add imagelist to your templates: `$yellow->snippet("imagelist", PATTERN)`.  
PATTERN is optional, it's a regular expression to specify media files.

Example
-------
Template with list of images from your media/images folder:

    <?php $yellow->snippet("header") ?>
    <?php $yellow->snippet("sitename") ?>
    <?php $yellow->snippet("navigation") ?>
    <div class="content imagelist">
    <h1><?php echo $yellow->page->getHtml("titleContent") ?></h1>
    <?php echo $yellow->page->getContent() ?>
    <?php $yellow->snippet("imagelist", ".*screenshot.jpg") ?>
    </div>
    <?php $yellow->snippet("footer") ?>
