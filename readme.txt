=== Offline Pages ===
Contributors: offlinepages
Tags: offline, offline WordPress, Offline Pages, Offline Pages Pro, Offline Forms, Offline Kiosk, offline browser, offline browsing, download, mirror, cache, cache manifest, Application Cache, website downloader, WordPress downloader
Requires at least: 3.1.0
Tested up to: 4.4.1
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

This plugin allows you to download and cache entire WordPress site locally on Mac or iOS device, then browse the local site while offline.

== Description ==

Offline Pages plugin allows you to cache your entire WordPress site locally on iPad, iPhone, or Mac, then browse it while working offline, e.g.
in Airplane Mode or when there is no network connection available. The plugin works in tandem with Offline Pages Pro or similar app. Together they efficiently synchronize
your WordPress articles with on-device cache to provide a complete offline browsing experience for the entire site. 

The plugin itself does not offer any useful functionality without the app. All it does is output a `<link>` element pointing to a special URL which serves XML document
with rules for synchronizing your site, e.g. `/blog/wp-admin/admin-ajax.php?action=opwp_rules`. The URL is ignored by any browser except Offline Pages app which uses
it as a guide to crawl the site and cache the resources according to rules contained in a document.

= Rules Document =

Unlike HTML5 cache manifest, Offline Pages rules documents don't require listing every individual resource used by the website. Instead, they provide high-level
instructions only. Examples of instructions are: block or allow certain URL patterns, customize caching policy, set update frequency, or add resource dependencies
not recognizable automatically by crawler (e.g. when URLs are computed by non-trivial JavaScript expressions).

You can find rules document DTD [here](http://codiumlabs.com/dtd/rules-1.0.dtd).

= Supported WordPress Features =

* Page layouts of any complexity
* Custom themes
* Caching of videos (plain HTML5 or YouTube/Vimeo embeds)
* Caching of AJAX requests
* Most public facing plugins
* Offline forms or surveys (setup required.)

Note that the plugin does NOT allow or support any admin functions, post editing or commenting while offline.

= Supported Apps =

The plugin works with following apps:

* Offline Pages Pro for iOS or Mac
* Offline Kiosk
* Offline Forms
* custom enterprise apps built on same platform ([http://codiumlabs.com/enterprise/](http://codiumlabs.com/enterprise/))

More information available can be found at plugin website ([http://codiumlabs.com/offline-wordpress/](http://codiumlabs.com/offline-wordpress/)).

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/` directory, or install the plugin through the WordPress plugins screen directly.
1. Activate the plugin through the 'Plugins' screen in WordPress.
1. Use the Settings->Offline screen to configure the plugin.
1. You can now start caching your WordPress site using the app.

== Upgrade Notice ==

This is initial release.
 
== Frequently Asked Questions ==

= Does it really allow browsing entire site offline? =

Yes.

= Including videos and AJAX? =

Yes, provided both plugin and mobile app are correctly set up.

= Can I browse entire WordPress site offline in Safari or Chrome? =

No. It requires Offline Pages Pro or similar app. Regular browsers don't support offline browsing functions required to manage large persistent caches, update them efficiently, or serve AJAX or media requests while working offline. 

= Does it support AJAX themes? =

Yes, but you will likely need to add custom rules to cache AJAX requests in Wordpress settings > Offline. See Offline Pages website or contact support with URL of your blog and someone will help you out.

= What about cache updates? =

You can update device cache manually, or configure automatic updates from the app. See Offline Pages website for more information.

= Does the app require admin access to WordPress site? =

Absolutely not! The app operates as a regular web browser with additional crawling and offline capabilities. The app only needs to access pages that your regular web visitors can access.

= Can mobile devices update cache automatically by Push Notification when I post new articles? =

Not yet, but it is planned.

= Is it available on Android? =

Not yet.

= Is it available on Windows? =

Not yet.

= Have any question not listed here? =

See Offline Pages website or contact support for more information.

== Screenshots ==

1. Offline Pages plugin settings page

== Changelog ==

= 1.0 =
* Initial release.

