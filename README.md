# OJS Publons Plugin
---------------------------
Version: 1.1
Developed and maintained by: Publons Ltd.
Original code from: Media Sphera Publishing House, Moscow, Russian Federation (http://mediasphera.ru/)

### About
This plugin provides the ability to send and publish reviews to Publons (https://publons.com).

### License
This plugin is licensed under the GNU General Public License v4.
See the accompanying OJS file docs/COPYING for the complete terms of this license.

### System Requirements
OJS 2.4.5 or greater.
PHP 5.2 or greater.
CURL support for PHP.
ZipArchive support for PHP.

### Installation
To install the plugin:
 - On the OJS site go to Home > User > Journal Management > Plugin Management > Install a New Plugin,
   select the .tar.gz file with the plugin and click "Continue"
 - Install the database schema: run the following command from your OJS directory:
    ```$ php tools/dbXMLtoSQL.php -schema execute plugins/generic/publons/schema.xml```
 - Enable the plugin by going to:  Home > User > Journal Management > Plugin Management > Generic Plugins and selecting "ENABLE" under "Publons Plugin"
 - Set up correct credentials to post reviews to Publons by going to Home > User > Journal Management > Plugin Management > Generic Plugins and click “CONNECTION” under "Publons Plugin"
   - Enter the username and the password of the Publons user who has API access to Publons so that the plugin can retrieve the authorisation token required.
   - Enter the API key of the journal found on the Publons partner dashboard under 'Integrations'.
   - __Optional__. Add the link to your journal landing page on publons so users can find more info about this.

### Usage
For the plugin to work correctly the journal should be registered at http://publons.com. (See https://publons.com/partner/info/ for more info). Then the corresponding registration data should be entered in the appropriate fields on the plugin page "Connection": Home > User > Journal Management > Plugin Management > Generic Plugins > Publons.

The link "Published" in the settings
Here the Journal Manager can see the list of reviews transferred to Publons for the current journal.

When the plugin is enabled, a button “Publish my review on Publons” will be present on all submission pages after the review has submitted their review. After the reviewer has clicked on this button and confirmed they want to send their review to Publons, the review data is sent to Publons automatically and reviewer receives an invitation to claim it (or it is automatically added if reviewer has profile with Publons and opted in to automatically add reviews from partnered journals).
The Publons website certifies only the fact the reviewer has completed peer review for the current journal. The text of the review can be disclosed on Publons website only after publication of the article. To disclose the text of the review reviewer should input the DOI of published article on Publons.

### Contact/Support
Please email us for support, bugfixes or comments.
Email: <ojs@publons.com>
Original version written by Natalya Mollecker for the Media Sphera Publishing House, Moscow, Russian Federation

### Version History
1.0 - Initial Release
1.1 - Fixed small issues
2.0 - Refactor of how plugin works, large bugfixes, styling changes.