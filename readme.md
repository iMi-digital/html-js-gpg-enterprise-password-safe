Concept for a HTML + JS + GPG based password safe
=================================================

* License: CC-BY-SA, By: 2013 www.github.com/amenk (License is not yet finally decided)

Requirements
============

* Bullet Proof / no server required
* At least viewing passwords should be possible for non-technical users
* GPG client and web browser installed
* All major platforms supported (Linux / Mac / Win) - nice to have: mobile OSs

Pseudo Code
===========

Adding a New Account
---------------------

* Create the HTML structure to represent the record
* Encrypt for all users
* Wrap a <code> tag
* Note their email addresses in the data-access field of the <code> tag
* Distribute the updated HTML document

Access an Account
-----------------

* Find an account where your email is contained in the code's data-access tag
* Decrypt the PGP scrambled text via your PGP client & private key


Share an Account
----------------

* Decrypt the password (see "Access an Account")
* Encrypt for all current users (obtained from data-access) plus the new user
* Update the data-access tag (append new user)
* Replace the inner HTML of the code tag
* Distribute the updated HTML document
