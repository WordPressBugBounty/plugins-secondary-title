=== Secondary Title ===
Contributors:        thaikolja
Donate link:         https://www.paypal.me/thaikolja/10
Tags: title,         alternative title, secondary title, second title, post title, title
Tested up to:        6.1
Stable tag:          2.1.0
Requires at least:   4.0
Requires PHP:        7.1
License:             GPLv3 or later
License URI:         https://www.gnu.org/licenses/gpl-3.0.en.html

Adds a secondary title to posts, pages and custom post types.

== Description ==

**Secondary Title** is a simple, light-weight plugin that adds an alternative title to posts, pages and/or [custom post types](http://codex.wordpress.org/Post_Types) which can be displayed automatically, with a shortcode or by using PHP.

The plugin comes with an extra settings page which allows you to customize the plugin according to your needs. You can change:

* [post types](http://codex.wordpress.org/Post_Types), categories and specific post IDs the secondary title will be
shown on,
* whether the secondary title should be automatically added to the standard title (*Auto show*),
* the format both titles are being shown (only works when *Auto show* is activated),
* the position where the secondary title input field should be displayed (above or below the standard title) within the admin interface (Classic Editor only),
* whether the secondary title should only be displayed in the main post and not within widgets etc.,
* if the secondary title should be usable in [permalinks](http://codex.wordpress.org/Using_Permalinks),
* and even more.

**Please see the [official website](https://www.kolja-nolte.com/wordpress/plugins/secondary-title/documentation/) for a full documentation.**

== Installation ==

= Quick Installation =

1. Install Secondary Title either by searching for the plugin with WordPress' native plugin installer found under *Plugins* → *Add New* or [download the plugin manually](https://downloads.wordpress.org/plugin/secondary-title.zip) and copy the *secondary-title* folder into the */wp-content/plugins/* directory of your WordPress installation.
2. Activate the plugin in the *Plugins* section of your admin interface.
3. Go to *Settings* → *Secondary Title* to customize the plugin as desired.

**IMPORTANT:** If the *Auto show* option is set to *Off*, you have to use either

`<?php echo get_secondary_title($post_id, $prefix, $suffix); ?>`

or

`<?php the_secondary_title($post_id, $prefix, $suffix); ?>`

in your theme file(s) (e.g. *single.php*) where you would like the secondary title to be displayed.

**For a more detailed documentation with parameters, functions and examples, please see the [official documentation](https://thaikolja.gitbooks.io/secondary-title/)**.

== Frequently Asked Questions ==

= More Frequently Asked Questions =

The full FAQ can be found in the [documentation](https://thaikolja.gitbooks.io/secondary-title/faq.html).

== Screenshots ==

1. Secondary Title with activated *Auto show* function that automatically adds the secondary title to the standard post/page title separated with a line break (`<br>`).

2. Secondary Title with activated *Auto show* function that automatically adds the secondary title to the standard post/page title with secondary title in bold (`<strong>`).

3. Secondary title input field using Gutenberg editor.

4. Secondary title input field using [Classic Editor plugin](https://wordpress.org/plugins/classic-editor/) (WordPress version below 5.0).

5. A section of Secondary Title's settings page.

== Changelog ==

= 2.9.0 =
* Critical security vulnerability fixed and measures taken to prevent future vulnerabilities

= 2.0.9.1 =
* Added support for WordPress 6.1.1
* Added padding to `<input>` for Post IDs
* Rebuilt the "Select all" link to toggle all categories
* Enlarged "Post IDs" input field

= 2.0.8 =
* Added support for WordPress 5.8

= 2.0.7.1 =
* HOTFIX: Reverted a change that caused [a bug](https://wordpress.org/support/topic/secondary-titles-showing-in-categories-sidebar/) when displaying the secondary title in sidebars

= 2.0.7 =
* Added support for [wp-Typography plugin](https://wordpress.org/plugins/wp-typography/)
* Fixed [bug](https://wordpress.org/support/topic/auto-show-secondary-titles-not-working-with-some-titles/) that caused some special characters to be displayed incorrectly when using [wp-Typography plugin](https://wordpress.org/plugins/wp-typography/) (thanks to [@msailer](https://wordpress.org/support/users/msailer/) and [@pepe](https://wordpress.org/support/users/pputzer/))
* [Reintroduced the "Input field position" option](https://wordpress.org/support/topic/above-or-below-the-standard-title/), but only if [Classic Editor]() is installed and activated (thanks to [@boborg](https://wordpress.org/support/users/boborg/))
* Removed localized files and its related PHP functions since this is now being handled and downloaded automatically by WordPress

= 2.0.6 =
* Fixed [bug resulting in `PHP fatal error`](https://wordpress.org/support/topic/latest-version-causes-posts-to-crash/) when using undeclared variables in function parameters (thanks to [@philsimon](https://wordpress.org/support/users/philsimon/))

= 2.0.5 =
* Added compatibility with WordPress 5.7
* Removed all previously (since version 1.9.5) deprecated functions from the plugin's codebase
* Removed "Input field position" option when using WordPress 5.0 and above
* Removed dismissible notice on all pages except for Secondary Title's settings page
* Fixed PHP notice
* Fixed code formatting in PHP file headers
* PHP files now use `die()` instead of `return` statement to prevent files from being accessed directly
* Code in SCSS files have been nested for better readability
* Updated language files (.pot)
* Added type annotation to certain PHP functions

= 2.0.4 =
* Fixed [bug](https://wordpress.org/support/topic/php-notice-trying-to-get-property-of-non-object-on-line-471/) printing `PHP Notice: Trying to get property of non-object on line 471`
* Fixed [bug](https://wordpress.org/support/topic/does-not-display-name-of-post-types-in-settings/) that resulted in not showing the correct post type names on the settings page
* Updated code to match current PHP standards
* Updated dead URLs leading to the documentation website

= 2.0.3 =
* Compatibility with WordPress 5.5 and below.
* Changed the minimum required PHP version to 7.1.

= 2.0.2 =
* Added full support for [All in One SEO Pack](https://wordpress.org/plugins/all-in-one-seo-pack/) 3.0. [Use `%secondary_title%`](https://semperplugins.com/documentation/title-settings/) to display.
* Added note reminding that *Input field* and *Column position* option only apply when using Classical Editor in WordPress versions with Gutenberg (>= 5.0).
* Cosmetic changes to the plugin's settings page.

= 2.0.1 =
* Hotfix: Moved file `admin/settings.php` to `includes/setings.php` due to PHP complications.

= 2.0.0 =
* Added support for Gutenberg editor. The secondary title can now be entered via a meta box on the sidebar of the editor.
* Added minimized versions for CSS (compiled from [SCSS](https://www.quora.com/What-is-SCSS-How-does-it-differ-from-CSS)) and JS files for performance improvement.
* Added partly support for [All in One SEO Pack](https://wordpress.org/plugins/all-in-one-seo-pack/). Use `%secondary_title%` to display.
* Updated Font Awesome to 5.8.1.
* Updated translations.
* Updated screenshots.
* Fixed bug with reoccurring donation notice.
* Minor style adjustments.
* Removed `/includes/gutenberg-info.php` and the notice saying "Secondary Title doesn't work anymore".
* Moved `/includes/settings.php` to `/admin/settings.php`.

= 1.9.9 =
* This version was skipped.

= 1.9.8 =
* This version was skipped.

= 1.9.7.5 =
* Hotfix and minor adjustments.

= 1.9.7 =
* Secondary Title is now compatible with PHP version 5.2.17 and above.
* Added info icons next to every setting which links to the official documentation where those settings are being explained in detail.
* Added "Settings" link to the "Plugins" section in the admin area which leads to Secondary Title's settings page.
* Updated Font Awesome to 5.2.0.
* Minor restructure of resources directories.
* Declared unused `secondary_title_get_default_setting()` as deprecated function.
* Donation notification dismissed by users will start to show up again if the  plugin is re-activated (please don't kill me!).
* Minor adjustments to the donation notification.

= 1.9.6 =
* Added new filter hook `secondary_title_columns_in_post_types`. Read more about it in the [documentation](https://thaikolja.gitbooks.io/secondary-title/filters.html).
* Added dismissable donation notice.
* Compatibility with WordPress 4.9.8.
* Fixed conflicts with standard meta queries when using "Include in search" (thanks to [@filmstarr](https://wordpress.org/support/users/filmstarr/)).
* Added textdomain constant.
* Updated Plugin URI in readme.txt.
* Removed commented (unused) code.
* Updated URLs on the plugin's settings page.
* Added copyright to file headers.
* Replaced `screenshot-3.png` with an updated one.

= 1.9.5 =
* Optimized display of title format preview on settings page.
* Added link to online [documentation on GitBooks](https://thaikolja.gitbooks.io/secondary-title/).
* Fixed bug concerning post columns (thanks to [Colin Ferm](http://www.fortytwosolutions.com/)).
* Updated Font Awesome to 5.0.9.
* Removed "Media" as post type for available display rules since it is not used anywhere.
* Minor fixes and cosmetic changes.

= 1.9.4 =
* Hotfix for 1.9.3.

= 1.9.3 =
* Removed JavaScript for changing the secondary title columns on post overviews and converted it into more reliable PHP.
* Removed HTML from the <head> tag and placed it into the body footer.
* Cosmetic changes.
* Major changes will follow soon.

= 1.9.2 =
* Introduced official documentary.
* Added WordPress 4.9.1 compatibility.
* Added [shortcode functionality](https://thaikolja.gitbooks.io/secondary-title/shortcodes.html) `[secondary_title allow_html="false" post_id="0"]`
* Updated Font Awesome to version 4.7.0.
* Cosmetic changes.

= 1.9.1 =
* Added WordPress 4.6 compatibility.
* Added WordPress.org translation compatibility.
* Updated translations.
* Updated Font Awesome to version 4.6.3.
* Cosmetic changes.

= 1.9.0 =
* Fixed [issue with "Include in search"](https://wordpress.org/support/topic/multiple-keyword-search-is-broken) when using more than one search terms (thanks to [lonefur](https://wordpress.org/support/profile/lonefur)).
* Added setting "Column position" to allow users to place the secondary title on post overview pages left or right of the primary title.
* JavaScript/jQuery code now follows JSLint and JSHint coding standards.
* Allowed to use placeholder more than once in "Title format" preview field on settings page.

= 1.8.0 =
* Added option "Only show in main post".
* Added option "Include in search".
* Secondary Title now (properly) installs default plugin settings on first activation.
* "Title format" preview on settings page now displays HTML (not just text as before).
* "Title format" doesn't reset itself anymore when "Auto show" is activated.

= 1.7.2 =
* Hotfix for 1.7.1.

= 1.7.1 =
* Hotfix for 1.7.0.

= 1.7.0 =
* Removed permalinks function from front-end.
* Redesigned plugin's settings page.
* Fixed small bugs.
* Updated translations.
* PHP 7 support.
* Minor tweaks and adjustments.

= 1.6.2 =
* Fixed bug occurring when clicking "Save Changes" on settings page.

= 1.6.1 =
* Fixed bug occurring when clicking "Save Changes" on settings page.

= 1.6.0 =
* Added new setting that can determine whether the secondary title should be displayed before or after the primary title on post, pages or custom post types overview site.
* Added [Font Awesome](http://fortawesome.github.io/Font-Awesome/) icons on Secondary Title settings page.
* General code optimization.
* Updated translations.

= 1.5.6 =
* Remove unnecessary slash in css link.

= 1.5.5 =
* Fixed bug preventing secondary title input field from displaying.
* Updated translations.

= 1.5.4 =
* Removed "Automatically append to permalinks" option because it turned out to cause several 404 errors.
* Added JS fix to let users jump from primary title to secondary title when tab is pressed.
* Fixed bug in "quick edit" dropdown (thanks to [madaplus](https://wordpress.org/support/profile/madaplus) for reporting and [simne7](https://wordpress.org/support/profile/simne7) for offering a fix.

= 1.5.3 =
* Removed [unnecessary character](https://wordpress.org/support/topic/plugin-adds-characters-at-top-of-edit-screens) from post screen (thanks to [Julie @Niackery](https://wordpress.org/support/profile/habannah)).

= 1.5.2 =
* Small bug fix for JavaScript in Firefox.

= 1.5.1 =
* Hotfix for 1.5.1.

= 1.5.0 =
* Fixed [notice error](https://wordpress.org/support/topic/notice-error-2) when deleting post (thanks to [master412160](https://wordpress.org/support/profile/master412160) and [wido](https://wordpress.org/support/profile/wido)).
* Fixed [bug](https://wordpress.org/support/topic/issue-when-filtering-posts-by-category) occurring when filtering posts within the admin area (thanks to [Chillington](https://wordpress.org/support/profile/chillington)).
* Code cleanup and JS refactoring.
* Performance fixes.
* Updated translations.
* Compatibility for WordPress 4.2.1.

= 1.4.0 =
* Added `$use_settings` parameter to `get_secondary_title()` and others which defines whether the secondary title should only be displayed if it matches the plugin's settings. Default `false`.
* Code rearrangements and improvements.
* Updated translations.

= 1.3.0 =
* Fixed [bug](https://wordpress.org/support/topic/missing-secondary-title-column-in-custom-post-type) causing secondary title not to be displayed on certain custom post types overviews (thanks to [saschapi](https://wordpress.org/support/profile/saschapi)).
* Updated translations.

= 1.2.0 =
* Small bug fixes and corrections.
* Updated translations.

= 1.1.0 =
* Removed `<?php secondary_title_plugins_settings_link(); ?>` due to compatibility problems.
* Added filter hook `secondary_title_show_overview_column` to disable the secondary title column on post overviews without using the screen values (thanks to [Alkorr](https://wordpress.org/support/topic/hide-secondary-title-description-column)).
* Added Dutch (thanks to [SilverXp](https://www.transifex.com/accounts/profile/SilverXp/)), Turkish (thanks to [mapazarbasi](https://www.transifex.com/accounts/profile/mapazarbasi/)) and other translation.
* Updated existing translations.
* Fixed bug that prevented the "Author" column on post overview page to be shown.
* Further bug fixes.

= 1.0.0 =
* Allows HTML tags within individual secondary titles (thanks to [brit77](http://wordpress.org/support/topic/adding-html-tags-to-secondary-title)).
* Updated documentation.

= 0.9.2 =
* Fixed [bug](http://wordpress.org/support/topic/secondary-title-field-missing-in-latest-update) that occasionally prevented the secondary title input box from being displayed when creating a new post (thanks to [howorks](http://profiles.wordpress.org/howorks) and [pesunites](http://profiles.wordpress.org/pesunites)).
* Changed the categories view on the settings page.
* jQuery changes.

= 0.9.1 =
* Bug fixes for 0.9.

= 0.9.0 =
* Removed *Report bug* e-mail form due to compatibility issues.
* Fixed [bug](http://wordpress.org/support/topic/bulk-edit-deletes-secondary-titles) that deleted the secondary
title on selected posts when using *Bulk edit* (thanks to [JacobSchween](http://wordpress.org/support/profile/jacobschween)).
* Fixed bug that occurred when saving a custom menu (only visible with WP_DEBUG).
* Updated translations.
* Several small changes that aren't important enough to be mentioned here.

= 0.8.0 =
* Some new minor functions and changes on the settings page.
* Allowed to use `%title%` and `%secondary_title%` variable on settings page in *Title format* more than once.
* Added option to [use secondary title in permalinks](http://wordpress.org/support/topic/feature-request-add-secondary-title-to-permalinks?replies=3).
* Added filter hooks to `<?php get_secondary_title(); ?>`, `<?php the_secondary_title(); ?>` and
`<?php get_secondary_title_link(); ?>`.
* Added French translation (thanks to [fxbenard](https://www.transifex.com/accounts/profile/fxbenard/)).
* Updated existing translations.
* Fixed bug that prevented the secondary title to be updated when empty.
* Renamed `<?php get_filtered_post_types(); ?>` to `<?php get_secondary_title_filtered_post_types(); ?>` to avoid
possible
conflicts.

= 0.7.0 =
* Restructured and split up plugin code into different files for better handling.
* Added *Secondary title* column to posts/pages overview.
* Added secondary title input field to quick edit box on posts/pages overview.
* Added bug report form to settings page.
* Removed secondary title from above/below the standard title on posts/page overview.
* Renamed functions to minimize conflicts with other plugins.
* Updated screenshots.
* Updated translations.
* Bug fixes.

= 0.6.0 =
* Added compatibility with Word Filter Plus plugin.
* Added *Only show in main post* setting.
* Fixed minor jQuery bug on admin interface.
* Updated FAQ.

= 0.5.1 =
* Fixed bug that falsely added slashes to HTML attributes in title format.
* Fixed jQuery bug in the admin posts/
* Added `<?php has_secondary_title(); ?>` function. See [the official documentation](http://www.kolja-nolte.com/kolja-nolte.com/wordpress/plugins/secondary-title/#Parameters) for more information.

= 0.5.0 =
* Fixed bug where the secondary title was not shown if the standard title contains "..." (thanks to Vangelis).
* Added *Select all* and *Unselect all* script for checkbox lists on settings page.
* Added secondary title display in admin posts/pages list.
* Added `<?php get_secondary_title_link($post_id, $values); ?>` and `<?php the_secondary_title_link($post_id, $values); ?>` functions
  to quickly create the secondary title as a link to its post. See [the official documentation](http://www.kolja-nolte.com/kolja-nolte.com/wordpress/plugins/secondary-title/#Parameters) for more information.
* Updated documentation/readme.txt.

= 0.4.0 =
* Fixed bug that showed secondary title input within the post/page overview.
* Added Italian translation (thanks to [giuseppep](https://www.transifex.com/accounts/profile/giuseppep/)).
* Added Polish translation (thanks to [pawel10](https://www.transifex.com/accounts/profile/pawel10/)).
* Updated existing translations.

= 0.3.0 =
* Added HTML support in title format (thanks to C0BALT).
* Added option to set the position of the secondary title input field within the admin interface (thanks to Vangelis).
* Added translation to Thai.
* Updated translation files.

= 0.2.0 =
* Installs default values on plugin activation.
* Added screenshots.
* Added `$prefix` and `$suffix` parameter for `<?php get_secondary_title(); ?>` and `<?php the_secondary_title(); ?>`.
* Updated FAQ.

= 0.1.0 =
* Initial Release.

== Upgrade Notice ==

= 2.0.8 =
WordPress 5.8 support.

= 2.0.7.1 =
* A hotfix that reverts a change that caused [a bug](https://wordpress.org/support/topic/secondary-titles-showing-in-categories-sidebar/) when displaying the secondary title in sidebars

= 2.0.7 =
This version reintroduces the "Input field position" option for WordPress 5.0 and above when using the [Classic Editor](https://wordpress.org/plugins/classic-editor/) plugin. It also adds support for [wp-Typography](https://wordpress.org/plugins/wp-typography/) plugin.

= 2.0.6 =
A hotfix to remove [a bug](https://wordpress.org/support/topic/latest-version-causes-posts-to-crash/) that might lead to a PHP fatal error.

= 2.0.5 =
Secondary Title is now compatible with WordPress 5.7, the latest WP version.

= 2.0.4 =
A few bugs have been fixed and some code sections rewritten.

= 2.0.3 =
To prepare you for future updates, Secondary Title requires now WordPress 7.1 (as does WordPress 5.2).

This update is mainly to tell the WordPress.org repository that Secondary Title is not a dead plugin. Expect more significant updates soon.

= 2.0.2 =
Support for [All in One SEO Pack](https://wordpress.org/plugins/all-in-one-seo-pack/) (version 3 and above).

= 2.0.1 =
Hotfix.

= 2.0.0 =
This version adds a secondary title input field to the Gutenberg editor, removes annoying admin notices and partly supports [All in One SEO Pack](https://wordpress.org/plugins/all-in-one-seo-pack/).

= 1.9.9 =
This version was skipped.

= 1.9.8 =
This version was skipped.

= 1.9.7.5 =
Hotfix and minor adjustments.

= 1.9.7 =
PHP > 5.2.17 compatibility and info icons next to options on settings page.

= 1.9.6 =
Version 1.9.6 contains a series of code and performance improvements and some new functions.

= 1.9.5 =
This update, among others changes, fixes a displaying error on posts/pages overview page.

= 1.9.4 =
Hotfix for 1.9.3 where obsolete JS code was being executed on the wrong page, destroying the layout.

= 1.9.3 =
Fixed HTML in <header> tag and converted the secondary title column on page overviews into more reliable PHP. **Major changes are expected to be included in the next release.**

= 1.9.2 =
Created a comprehensive [documentation]((https://www.kolja-nolte.com/wordpress/plugins/secondary-title/documentation/) and added [shortcodes](https://thaikolja.gitbooks.io/secondary-title/shortcodes.html) to display the secondary title inside your posts.

= 1.9.1 =
WordPress 4.6 and WP.org translations compatibility.

= 1.9.0 =
Fixed issue with "Include in search" option and added "Column position" setting.

= 1.8.0 =
You can now set whether you'd like the secondary title to be searchable. See plugin settings page.

= 1.7.2 =
Hotfix for 1.7.1.

= 1.7.1 =
Hotfix for 1.7.0.

= 1.7.0 =
Removed permalinks function from front-end; new settings page layout.

= 1.6.2 =
Fixed bug occurring when clicking "Save Changes" on settings page.

= 1.6.1 =
Fixed bug occurring when clicking "Save Changes" on settings page.

= 1.6.0 =
New setting added to change the position of the secondary title column on post, pages or custom post types overview sites.

= 1.5.6 =
Small CSS fix.

= 1.5.5 =
Urgent hotfix for 1.5.4.

= 1.5.4 =
The option "Automatically append to permalink" has been removed; please use "Yes, use custom permalink structure" on the plugin's settings page instead.

= 1.5.3 =
Removed unnecessary character from post screen.

= 1.5.2 =
Small bug fix for JavaScript in Firefox.

= 1.5.1 =
Hotfix for 1.5.1.

= 1.5.0 =
Two bugs fixed and some code cleanup.

= 1.4.0 =
Code rearrangements and added `$use_settings` parameter to `get_secondary_title()` and related functions that defines whether or not the plugin settings should be validated.

= 1.3.0 =
Fixed posts overview bug, added/updated translations.

= 1.2.0 =
Bug fixes, translation updates.

= 1.1.0 =
Fixed bug on posts overview page, new/updated translations.

= 1.0.0 =
HTML allowed in secondary title and small fixes.

= 0.9.2 =
Additional hotfix for 0.9.

= 0.9.1 =
Hotfix for 0.9.

= 0.9.0 =
Bug fixes.

= 0.8.0 =
Permalinks support, bug fixes, translation updates.

= 0.7.0 =
Major changes; restructured plugin files, added "Secondary title" column to posts/page overview and more.

= 0.6.0 =
Bug fixes, setting added, compatibility with Word Filter Plus plugin.

= 0.5.1 =
Hotfix for 0.5.

= 0.5.0 =
Bug fixes and some more features.

= 0.4.0 =
Bug fix and translation update.

= 0.3.0 =
HTML support and new features.

= 0.2.0 =
Major changes, screenshots, FAQ, parameters.

= 0.1.0 =
This is the first release of Secondary Title.