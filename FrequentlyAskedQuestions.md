# FAQ #

I am no longer able to update/support the Ajax Event Calendar plugin for `WordPress`.

Alternative Free Calendar Plugins:
http://www.blazdesign.com/5-free-wordpress-calendar-plugins/


## Eeek! Ajax Event Calendar Stopped Working / Doesn't Work ##
This is typically caused by a conflict with another plugin/theme.  Before submitting a bug to the issue tracker, follow these troubleshooting tips to isolate and identify the problem accurately:
  * Switch to the default WordPress Theme ([Twenty Twelve](http://wordpress.org/extend/themes/twentytwelve) as of this update). If the calendar works, the conflict is caused by your theme - ask the theme author to investigate.

  * Still doesn't work...?  Disable all plugins except the Ajax Event Calendar. With all possible external conflicts now disabled, the calendar should work.

  * Still no luck...?  Check your /wp-content folder for a file called "debug.log" - it may contain errors regarding the cause of the conflict.  If there are no errors that directly mention Ajax Event Calendar, check for JavaScript errors via your browser's JavaScript console.

  * JavaScript errors may appear in the console, listing both the filename and the line number of each error.  Reload the calendar page in the browser and note any errors you find.  If any errors mention Ajax Event Calendar, be sure to include them in your bug report.

  * If you use Firefox browser, and I highly recommend using the [Firebug plugin](http://getfirebug.com/) to debug JavaScript conflicts.


---


  * If the calendar works as expected, begin restoring your original plugins one by one, check the calendar after each.

  * When the calendar stops functioning, you'll have a culprit.  Note the error in the console, it will be helpful when reporting the error to the  plugin/theme developers.


---


  * If no errors appear in either the Firebug Console or the PHP logs, search the [Issue Tracker](http://code.google.com/p/wp-aec/issues/list?can=1) for known bugs and resolutions.

  * If you can't find your issue, submit a bug report on the  [Issue Tracker](http://code.google.com/p/wp-aec/issues/list?can=1), be sure to include ALL STEPS necessary to reproduce the issue - if I am unable to reproduce the problem I will not be able to assist.

  * Finally, I do not freely offer WordPress implementation assistance.  If you are interested in hiring me for consultation, I am available at a fare hourly rate.

## I added the `[calendar]` shortcode to a page, but I can't see the calendar.  I only see the link for "Add Events" and the filter color boxes. ##
  * See Answer One

## The administrative calendar appears, but the front-end calendar does not ##
  * Did you add the `[calendar]` shortcode to a page, post or text widget?
  * Read the plugin [installation guide](http://wordpress.org/extend/plugins/ajax-event-calendar/installation/).
  * See Answer One

## Your server has PHP magic\_quotes\_gpc set to active. This produces formatting errors in the Ajax Event Calendar plugin. Learn how to disable this setting in this forum thread. Ask your host provider for help. ##
  * If the recommendations in the forum don't work out, try adding the following line in your .htaccess file: php\_value magic\_quotes\_gpc off

## I have a feature request for the plugin, what steps should I take? ##
Search the [issue tracker](http://code.google.com/p/wp-aec/issues/list?can=1) for enhancement requests.
  * If you find your request already in queue, **click on the star** beside the issue number to indicate your interest in the feature.
  * If you don't find your request in queue, submit a feature request include the purpose of the feature and detailed scenarios of how it would be used.

## I want to change the appearance of the calendar/eventlist ##
  * View your site using Firefox browser with [Firebug plugin](http://getfirebug.com/) activated.  Read about using Firebug and learn how to "inspect" page elements for styling.
  * Firebug allows you to adjust the style on a live site, so once you have the desired look, just add the style to **your theme's css** not the custom.css file (the custom.css file will not be preserved when the plugin is updated).
  * REMEMBER: edits to existing style definitions require use of the **!important** flag after the property value, for example: `#aec-calendar{background:#blue !important;...}`.<br><b>BE CAREFUL</b> this can have unanticipated effects on your design when applied to elements used throughout your theme.  For that reason, it is good practice to use the most specific selectors possible when performing these overrides.<br>
<ul><li>If you're stuck post your questions on the forum so that others can try to help.</li></ul>

<h2>The front-end calendar does not work in my custom theme</h2>
<ul><li>Make sure your theme templates contain <code>&lt;?php wp_head(); ?&gt;</code> just before the closing <code>&lt;/head&gt;</code> tag and <code>&lt;?php wp_footer(); ?&gt;</code> just before the closing <code>&lt;/body&gt;</code> tag.</li></ul>

<h2>All apostrophes in the event detail form, returns \' when I save the event.  And returns \\' on subsequent saves</h2>
<ul><li>This will occur when your PHP server is configured to use magic quotes gpc.<br>
</li><li>The developers of PHP <a href='http://php.net/manual/en/security.magicquotes.php'>strongly recommend against using magic quotes</a>
</li><li>This functionality has been removed from the current PHP versions.<br>
</li><li>To correct this behavior: edit your php.ini file, <a href='http://php.net/manual/en/security.magicquotes.disabling.php'>as described here</a>, or ask your host provider.</li></ul>

<h2>How do I manage events?</h2>
<ul><li>To add a new event: in the administrative calendar page click on a date (or range of dates) in the month view, or click on a half-hour (or range of hours) timeslot in the week view.<br>
</li><li>To edit, delete or copy an event, click on an existing event and select the desired option in the event detail modal.</li></ul>

<h2>How do I manage event categories?</h2>
<ul><li>To add a category: simply enter the desired category name in the input field, select a background color via the colorpicker or enter the hex value in the field provided.<br>
</li><li>Only users assigned the aec_manage_calendar capability can manage categories.</li></ul>

<h2>I want to grant calendar rights to a user without giving them access to all administrative menus</h2>
<ul><li>First, install a Capabilities/Roles management plugin to your blog, such as  <a href='http://wordpress.org/extend/plugins/members/'>Members</a>
</li><li>Next, based on your needs assign any/all of the capabilities listed below, to existing or new custom roles.<br>
<ul><li>Users assigned the <b>aec_add_events</b> capability can edit and delete events they create by clicking on events in the administrative calendar page.<br>
</li><li>Users assigned the <b>aec_manage_events</b> capability can edit and delete all events.<br>
</li><li>Users assigned the <b>aec_manage_calendar</b> capability can manage categories, and calendar settings.</li></ul></li></ul>

<h2>Is there a way to configure the WordPress to allow users that come to the site to can register and create their own events (so not every event would need to be created by the administrator)?</h2>
<ul><li>Absolutely!  If you allow users to self-register and you'll need to change WordPress settings so that the default role assigned to new users is Calendar Contributor.</li></ul>

<h2>What happens when the plugin is deleted?</h2>
<ul><li>The event and category databases, custom roles, plugin capabilities, plugin options and widget settings are permanently removed.</li></ul>

<h2>What happens to events when a user account is deleted?</h2>
<ul><li>All events associated with a deleted user are permanently removed.</li></ul>

<h2>What happens to events when a category is deleted?</h2>
<ul><li>Upon deletion, all events associated with a deleted category will be reassigned to the primary category.</li></ul>

<h2>How can I include the calendar directly in my theme without using shortcodes?</h2>
<ul><li>Place this code in your template at the desired location <code>&lt;?php echo do_shortcode('[calendar]') ?&gt;</code>.</li></ul>

<h2>Does the AEC support the WordPress Network (Multisite) feature? When I tried to implement it on a multisite I was unable to add events or categories on any of the sub sites except the primary.</h2>
<ul><li>The plugin does not specifically support multisite setups.  However, one user claims the plugin works if "activated on a site-by-site basis."</li></ul>

<h2>How can I add "print calendar" functionality on the calendar page?</h2>
<ul><li>To add print functionality, open a post or page, select the HTML tab in !Wordpress Post editor, and enter this code snippet above or below the calendar shortcode: <code>&lt;a href="javascript:window.print();"&gt;Print Page&lt;/a&gt;</code>.<br>
</li><li>If you want to hide certain page elements, such as sidebars you'll need to add print specific rules to your theme stylesheet.<br>
</li><li>For helpful resources to start you off, search for "Print Style Sheets" in your favorite search engine.</li></ul>

<h2>How can I add images to the event detail?</h2>
<ul><li>Insert a hot-linked or local image anywhere in the description field, just don't forget to include a height parameter or your event detail box will not size correctly.<br>
</li><li>For example: <code>&lt;img src="mywebsite.com/images/myimage.jpg" height="300px"\&gt;</code></li></ul>

<h2>How can I hide the Duration box and text?</h2>
<ul><li>Add <code>#aec-modal .duration{display:none}</code> to <b>your theme css file</b>.</li></ul>

<h2>How can I change current day background and font color?</h2>
<ul><li>Add the <code>.fc-state-highlight</code> class to your theme stylesheet and apply the desired color rules.</li></ul>

<h2>How can I put the calendar on the home page?</h2>
<ul><li>Create a front-end calendar as described in the plugin installation page, then follow <a href='http://codex.wordpress.org/Creating_a_Static_Front_Page'>these instructions</a>.</li></ul>

<h2>Is there a way to link directly to a post/page/anything from the calendar?</h2>
<ul><li>No, this plugin was created to function independently of posts and uses a different set of database tables.<br>
</li><li>However, you can input links in the Event Link field to any URL of your choosing.</li></ul>

<h2>Can I import/link Google calendars to the Ajax Event Calendar?</h2>
<ul><li>No, this calendar emulates the look and feel of Google Calendar but also extends the field options beyond what is offered by Google.</li></ul>

<h2>How can I configure WordPress to display in my language?</h2>
<ul><li><a href='http://codex.wordpress.org/WordPress_in_Your_Language'>Configure WordPress in Your Language</a></li></ul>

<h2>The calendar does not work when SSL logins for WordPress Administrators are forced with “define('FORCE_SSL_ADMIN', true);” in the wp-config.php file.</h2>
This issue can be resolved by overriding the URL in the plugin code to the http:// version instead of the https:// version that is returned by the "admin_url()" function.