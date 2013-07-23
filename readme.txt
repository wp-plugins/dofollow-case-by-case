=== DoFollow Case by Case ===
Contributors: apasionados, nunsys, netconsulting
Donate link: http://apasionados.es/
Tags: dofollow, nofollow, rel nofollow, comment, comments, link, links, seo, shortcode
Requires at least: 3.0.1
Tested up to: 3.5.2
Stable tag: 1.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

DoFollow Case by Case allows you to selectively apply dofollow to comments, either case by case or through a white-list of commenter’s emails.

== Description ==

This WordPress plugin gives you the possibility to remove the "nofollow" attribute from your wordpress blog's comments: from the author's links and/or from the comments text links. This can be done either case by case (editing each comment) or through a white-list of commenters emails, whose comments will allways be dofollow.

It also adds a checkbox in the insert link popup box for including rel="nofollow" in links as you create them, so that you can significantly increase the control of the rel="nofollow" tag on every link on your blog. It is designed to give you fine-grained control of linking for SEO purposes.

And it also adds a shortcode for making a link no follow in posts and pages. The usage is as follows: [nofollow] LINK [/nofollow] 

= What can I do with this plugin? =

This plugin allows you to set links in comments to be dofollow instead of nofollow. When editing a comment, now you have the option to remove the rel="nofollow" attributes from the links contained in them.
To make it easier, you can also setup commenters emails whose links in comments should always be dofollow and you can even set their Author URL when commenting to be dofollow.
On the other side you can also define URLs that when contained in a comment are always dofollow, so that you can setup links to your own sites to be always dofollow.

In order to add commenter's emails or URLs to the white list, please go to DoFollow > DoFollow.

DoFollow > White List Email: The Email White List contains a list of emails of commenters, whose links in comments are allways dofollow. And you can also choose to make the Author URL dofollow. By default the Author URL is not followed.
Here you can add for example the email addresses of your staff and collaborators.

DoFollow >White List URL: The URL White List contains a list of URLs that when linked to in a comment, are always dofollow, nevertheless who links to them.
Here you can setup for example links from your sites or from other sites.

And finally when adding a link to a page or post, you can mark it as NOFOLLOW through the link insertion pop-up or through a shortcode.


= What ideas is this plugin based on? =

We were looking for a plugin like [Nofollow Case by Case](http://wordpress.org/plugins/nofollow-case-by-case/ "Nofollow Case by Case") but that worked the other way round. Instead of removing the re="nofollow" from all comments links and have the possibilty to add the rel="nofollow" case by case, we wanted to leave the rel="nofollow" and all comments and have the possibility to remove them only from some comments.

Other functionality we wanted was the possibility to add a checkbox in the insert link popup box for including rel="nofollow" in links as you create them as seen in [Ultimate Nofollow](http://wordpress.org/plugins/nofollow/ "Ultimate Nofollow").

Another interesting plugin is [Nofollow Free](http://wordpress.org/plugins/nofollow-free/ "Nofollow Free"), but unfortunately it hasn't been updated in over 2 years.

And the last plugin we liked is [Smart DoFollow](http://wordpress.org/plugins/smart-dofollow/ "Smart DoFollow") which lets you automatically give DoFollow links to authors of comments that are longer than a given number of chars. This is intersting, but very dangerous as today all comment spam is quite long and has many characters.

= DoFollow Case by Case Plugin in your Language! =
This first release is avaliable in English and Spanish. In the i18n we have included the necessarry files to translate this plugin.

If you would like the plugin in your language and you're good at translating, please drop us a line at [Contact us](http://apasionados.es/contacto/index.php?desde=wordpress-org-dofollow-home).

= Further Reading =
You can access the description of the plugin in Spanish at: [DoFollow Case by Case en castellano](http://apasionados.es/blog/dofollow-case-by-case-1676/).


== Installation ==

1. Upload the `dofollow-case-by-case` folder to the `/wp-content/plugins/` directory
1. Activate the DoFollow Case by Case plugin through the 'Plugins' menu in WordPress
1. Configure the plugin by going to the `DoFollow` menu that appears in your admin menu

Please note that the plugin should not be used together with other plugins with similar funcionalities like: [Nofollow Case by Case](http://wordpress.org/plugins/nofollow-case-by-case/ "Nofollow Case by Case"),[Nofollow Case by Case](http://wordpress.org/plugins/nofollow-case-by-case/ "Nofollow Case by Case"), [Ultimate Nofollow](http://wordpress.org/plugins/nofollow/ "Ultimate Nofollow"), [Nofollow Free](http://wordpress.org/plugins/nofollow-free/ "Nofollow Free") or [Smart DoFollow](http://wordpress.org/plugins/smart-dofollow/ "Smart DoFollow").


== Frequently Asked Questions ==

= What is Dofollow Case by Case good for? =
Links have a value. With Dofollow Case by Case you can decide yourself where the value goes.

= Why should I make use of the Dofollow Case by Case SEO Plugin? = 
If you work with WordPress you normally have no chance to decide yourself if a link should be a real link or not. All your comment links and comment author links are deactivated for search engines by default. But for good reasons you might want to punish only those links that really seem to be spam. To make it easier for you the plugin comes with nofollow links by default but you can follow the links that are valuable.

= Does Nofollow Case by Case make changes to the database? =
Yes. It creates a new table: "nodofollow".
* If you activate the plugin and the table doesn't exist, the plugin creates it.
* If you desactivate the plugin, the table isn't deleted.
* If you delete the plugin, the table is deleted.

= How can I check out if the plugin works for me? =
After activating Dofollow Case by Case visit a post with comments and have a look into the source code of that page. All your comments should have rel="nofollow" or rel="external nofollow" attributes. 

Now visit your admin page and edit one of the comments for testing purposes: Check the dofollow checkbox.

Visit your post and make sure that every link works fine. Have a look into the source code again. Your modified comment links should now be follow links. All the other links in comments should be left as nofollow links. 

= Something seems not to work as expected. Why not? =
The primary job of Dofollow Case by Case is to find and replace variants of rel="nofollow". For this to work we need a proper link that can be analyzed and replaced. WordPress has several functions included. Some deliver a URL only, other functions deliver a complete link including an anchor, a link text and so on. 

Theme developers and plugin authors can choose from all these functions to include some links into the system whereever this makes sense. Dofollow Case by Case is normally not able to modify a single URL. This can not be modified by PHP directly because it hooks into other functions somewhere else (later). Those functions can be modified but not the original input, not the "comment author url" itself. Whenever possible you should use a standard function like "get_comment_author_link" to receive a complete link in your template that later can easily be modified with standard functions of Dofollow Case by Case. Let us know if you have issues. 

= How can I remove Dofollow Case by Case? =
You can simply activate, deactivate or delete it in your plugin management section.

= Are there any known incompatibilities? =
The plugin should not be used together with other plugins with similar funcionalities like: [Nofollow Case by Case](http://wordpress.org/plugins/nofollow-case-by-case/ "Nofollow Case by Case"),[Nofollow Case by Case](http://wordpress.org/plugins/nofollow-case-by-case/ "Nofollow Case by Case"), [Ultimate Nofollow](http://wordpress.org/plugins/nofollow/ "Ultimate Nofollow"), [Nofollow Free](http://wordpress.org/plugins/nofollow-free/ "Nofollow Free") or [Smart DoFollow](http://wordpress.org/plugins/smart-dofollow/ "Smart DoFollow").
If you find any other incompatibilities, please let us know.

= Do you make use of Dofollow Case by Case yourself? = 
Of course we do. ;-)

== Screenshots ==

1. The "DoFollow Case by Case" main screen. Here you can add email addresses of commenters and URLs to the white lists.
2. Email White List. Here you can edit the list of Email Addresses of the commenters whose comments are allways dofollow.
3. URL White List. Here you can edit the list of URLs that are allways dofollow.
4. Edit comment. Where you can edit a comment and make the links of the comment dofollow.
5. Insert link pop-up. Pop-up window for link insertion in a post or page where we added the option to make it nofollow.
6. Shortcode for making a link of a post or page nofollow.


== Changelog ==

= 1.0 =
* First stable release.

= 0.5 =
* Beta release.

== Upgrade Notice ==

= 1.0 =
This is the first stable release. Upgrade immediately.

== Contact ==

For further information please send us an [email](http://apasionados.es/contacto/index.php?desde=wordpress-org-dofollow-contact).
