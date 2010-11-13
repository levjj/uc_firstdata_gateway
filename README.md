UC First Data Gateway
=====================
Enables a payment gateway in [Ubercart](http://www.ubercart.org/) that allows users to pay via the
[First Data Web Service](http://www.firstdata.com).

Features
========
- Submits the following information to First Data: Order ID, User ID, Email,
  Billing Address, Shipping Address, Credit Card Info, Total Amount, Order
  products (in the comments section).

  NOTE: The User ID is only recorded for users who are logged in when they
  check out.

Installation Instructions
=========================
1.  Download the module.
1.  Untar it into sites/all/modules and enable it in Drupal.
1.  Navigate to the Payment settings in Ubercart
    (admin/store/settings/payment/edit/gateways).
    Click on "First Data Gateway settings" and fill in the settings (see below).
1.  Store Number. A valid store number is required.
1.  Certificate, PEM File and password. Also, you can‘t just generate your own
    PEM file. You‘ll need to use a special PEM file provided by First Data.
    To get it, login to First Data, then go to Support -> Download Center and
    click on Web Service (not Web API). You will get a zip file including the
    P12 certificate of First Data, your own Keyfile and the password for the
    keyfile. Save those files to a path on your server that is protected
    and not web-accessible.
1.  In the Payment settings you will also want to set First Data as the Default
    Gateway for credit cards.
1.  Ensure that you have the PHP curl module installed on your server and test
    it out.

Reference
=========
http://www.firstdata.com/support/manuals_and_guides/global_gateway.htm

Credits
=======
Developed by Christopher Schuster (http://livoris.de/ | cs@livoris.de).
Based on [UC Linkpoint API](http://drupal.org/project/uc_linkpoint_api).

