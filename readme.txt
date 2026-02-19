=== Wello ServiceDesk API ===
Contributors: odswello
Tags: servicedesk, helpdesk, support, ticketing, api
Requires at least: 6.0
Tested up to: 6.9
Requires PHP: 7.4
Stable tag: 1.0.0
Donate link: https://wello.solutions/
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Wello ServiceDesk allows users to securely connect their WordPress site to the Wello ServiceDesk platform for authentication and ticket management.

== Description ==

Wello ServiceDesk integrates your WordPress website with the Wello ServiceDesk platform.

Features include:

* Secure OTP-based authentication
* Token generation via external API
* ServiceDesk interface rendering via React app
* Admin configuration panel
* Secure communication with remote API

This plugin requires an active Wello ServiceDesk account.

== Installation ==

1. Upload the plugin folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Navigate to **Settings → Wello ServiceDesk**
4. Enter your ServiceDesk credentials
5. Save settings

== Frequently Asked Questions ==

= Does this plugin require an external account? =

Yes. You must have an active Wello ServiceDesk account to use this plugin.

= Does the plugin send data externally? =

Yes. See the "External Services" section below for full details.

== Screenshots ==

1. Admin settings page
2. OTP authentication screen
3. ServiceDesk dashboard view

== Source Code & Build Instructions ==

This plugin includes minified and compiled JavaScript and CSS files to optimize performance and plugin size.

=== Source Code Location ===

The source code for this plugin, including the React application source files and build configuration, is publicly available on GitHub:
**https://github.com/wello-solutions/wello-servicedesk-api**

You can review, fork, and contribute to the source code at the GitHub repository.

=== Building from Source ===

To build the plugin from source:

1. Clone the repository: `git clone https://github.com/wello-solutions/wello-servicedesk-api.git`
2. Install dependencies: `npm install`
3. Build the project: `npm run build`
4. The compiled files will be generated in the `build/` directory

=== Technologies Used ===

* React - JavaScript library for the UI
* Webpack - Module bundler and build tool
* npm - Package manager and build scripts

All source code is available for review and modification. The compiled files in `/build/static/` are automatically generated from the source files using Webpack and npm build tools.

== Changelog ==

= 1.0.0 =
* Initial release

== Upgrade Notice ==

= 1.0.0 =
Initial stable release.

== External Services ==

This plugin connects to an external API service provided by Odyssee Mobile in order to authenticate users and retrieve ServiceDesk data.

Service Name:
Wello ServiceDesk API

Service Provider:
Odyssee Mobile

API Domain:
https://servicedeskapi.odysseemobile.com

What data is sent:

• User email address (when requesting OTP)
• User password (during authentication)
• OTP token and OTP code (during verification)

When is data sent:

• Only when a user submits the authentication form
• Only when an administrator configures or refreshes authentication

No data is transmitted automatically without user action.

Purpose of data transmission:

• To authenticate the user
• To generate an access token
• To retrieve ServiceDesk interface data

Terms of Service:
https://servicedeskapi.odysseemobile.com/terms

Privacy Policy:
https://servicedeskapi.odysseemobile.com/privacy

== Development ==

This plugin uses React and Webpack to build the frontend interface.

The distributed version contains compiled JavaScript located in:

/build/

The human-readable source code is publicly available here:

https://github.com/yourusername/wello-servicedesk-plugin

To build the plugin locally:

1. Install Node.js (v18+ recommended)
2. Run `npm install`
3. Run `npm run build`

This will generate the production files inside the /build directory.

== License ==

This plugin is licensed under the GPLv2 or later.

All included third-party libraries are GPL-compatible.