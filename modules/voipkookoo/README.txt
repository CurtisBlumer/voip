== Introduction ==

The voipkookoo.module makes it possible for the VoIP Drupal platform to make and receive calls via the KooKoo Cloud Telephony service (http://www.kookoo.in/).


== Requirements ==

In order to install the voipkookoo.module, you will need:

1. A KooKoo account

2. The PHP Curl extension in your system. For Debian systems, just run
  $ sudo apt-get install php5-curl
  $ sudo /etc/init.d/apache2 restart


== Installation ==

Installing voipkookoo.module is very simple.  It requires a few configuration steps on your Drupal site to let it know how to reach your KooKoo account It also requires a few settings in your KooKoo account to make sure it knows which Drupal site to use.

Drupal configuration:

1. Install and enable voipkookoo.module

2. Set KooKoo as the default voip server
  - Go to admin/voip/servers

  - Click on KooKoo's "configure" link

  - Fill in the "KooKoo API Key" associated with your KooKoo account. API Key can be found in the your KooKoo account's "Dashboard"

  - Go back to admin/voip/servers

  - Select the 'KooKoo' option

  - Press the 'set default voip server' button


KooKoo configuration:

1. Login into your KooKoo account

2. Click on the "Settings" section.

3. Set the URLs associated with your site

  - Fill the "Application URL" field with
    http://mysite.com/voip/kookoo/callhandler/process_inbound_calls/ (for clean URLs)
    or http://mysite.com/?q=voip/kookoo/callhandler/process_inbound_calls/

  - Press the "Save" button

  - Enjoy!

4. In the "Dashboard" section of the account, click on the "Add New Number" link and add a phone number you would like to use for your Drupal site

5. By default Outbound is disabled for all the KooKoo users and if you want to enable outbound for your account please send
   a mail to support@kookoo.in with subject as:Enable Outbound and it will be enabled at the earliest for Paid Accounts.
   KooKoo limits the number of outbound calls to 50/day for some accounts.
   Also due to TRAI regulations the calls are not allowed from 9pm to 9am IT.

6. To use Inbound SMS login to your account, go to settings and assign a keyword to your application
   (Only for gold and silver eggs, normal eggs do not have this feature).
   Do this fast as keywords are unique and you may not get the exact keyword you are looking for if someone has already acquired it.
   Ask your users to send an SMS to 0-922-750-751-2 with "your_keyword <space> message" as a message.
   More info http://blog.kookoo.in/2011/08/kookoo-now-with-sms-integration.html

7. Currently KooKoo doesn't support international outbound SMS.




== About ==

This module was originally designed and implemented by Tamer Zoubi and Leo Burd under the sponsorship of Terravoz (http://terravoz.org).
