== Introduction ==

Plivo Cloud (http://plivo.com/) is API platform to build Voice & SMS Applications. There is no need for server installation.

******************************************************************************************************************************
2. Plivo Cloud:
== Requirements ==

In order to install the voipplivocloud.module, you will need:

1. A Plivo Cloud account

2. The PHP Curl extension in your system. For Debian systems, just run
  $ sudo apt-get install php5-curl
  $ sudo /etc/init.d/apache2 restart

3. Pear package HTTP_Request2 - This is a HTTP utility; go to pear.php.net and
  search for HTTP packages to install this utility. HTTP 1.4.1 is the most stable
  release of HTTP; a Beta version of HTTP2 is also released.


== Installation ==

Installing voipplivocloud.module is very simple.  It requires a few configuration steps on your Drupal site to let it
know how to reach your Plivo account It also requires a few settings in your Plivo account to make sure it knows which Drupal site to use.

Drupal configuration:

1. Install and enable voipplivocloud.module

2. Set Plivo Cloud as the default voip server
  - Go to admin/voip/servers

  - Click on Plivo Cloud "configure" link

  - Fill in the fields with the "Auth ID" and "Auth Token" associated with your Plivo account.
    Both of those values can be found in your Plivo account's "Dashboard" (https://www.plivo.com/dashboard/)

  - Go back to admin/voip/servers

  - Select the 'Plivo Cloud' option

  - Press the 'set default voip server' button


Plivo Cloud configuration:

1. Login into your Plivo Cloud account

2. Create new application from "Applications" section
   Set the URLs associated with your site

  - Fill the "Answer url" field with
    http://mysite.com/voip/plivocloud/callhandler/process_inbound_calls (for clean URLs)
    or http://mysite.com/?q=voip/plivocloud/callhandler/process_inbound_calls

  - Fill the "Message url" field with
    http://mysite.com/voip/plivocloud/callhandler/process_inbound_text (for clean URLs)
    or http://mysite.com/?q=voip/plivocloud/callhandler/process_inbound_text

  - Fill the "Hangup url" field with
    http://mysite.com/voip/plivocloud/callhandler/process_hangup (for clean URLs)
    or http://mysite.com/?q=voip/plivocloud/callhandler/process_hangup

  - Make sure Answer method, Message method and Fallback method are set to use "POST"

  - Press the "Save" button

  - Enjoy!

3. In the "Numbers" section of the account, click on the "Rent Phone Number" link and choose a number for your application.

4. Enter this number at VoIP Drupal default call configuration at admin/voip/call/settings

== About ==

The VoIP Plivo module has been originally developed by Leo Burd, Tamer Zoubi and Blair MacNeil under the sponsorship of the MIT Center for Civic Media (http://civic.mit.edu).
