Open Password Safe
==================

Password safe and management application (with sharing), fully based on open technologies (HTML + JS + GPG).

Version: 0.0.1 (Concept)

**License:** CC-BY-SA, By: 2013 www.github.com/amenk, 2016 iMi digital GmbH (License is not yet finally decided)

If you have any ideas or comments, please submit an issue or a pull request.

Requirements
============

* Bullet Proof / no server required
* At least viewing passwords should be possible for non-technical users
* GPG client and web browser installed
* All major platforms supported (Linux / Mac / Win) - nice to have: mobile OSs

Security
========

* Server stores passwords
* No web client, but browser extensions, desktop apps and mobile apps - so that compromising the server does not allow phishing the master keys


Pseudo Code
===========

Adding a New Account
---------------------

* Create the HTML structure to represent the record
* Encrypt for all users
* Wrap a `<code>` tag
* Note their email addresses in the data-access field of the `<code>`
* Distribute the updated HTML document

Access an Account
-----------------

* Find an account where your email is contained in the `<code>`'s `data-access` tag
* Decrypt the PGP scrambled text via your PGP client & private key


Share an Account
----------------

* Decrypt the password (see "Access an Account")
* Encrypt for all current users (obtained from data-access) plus the new user
* Update the `data-access` property (append new user)
* Replace the inner HTML of the `<code>` tag
* Distribute the updated HTML document

Challenges
==========

* How to properly modify and save the HTML document?
* Ensure that always the correct public keys are used (standard PGP problem -> signed keys / secure keyserver), i.e. all keys should be signed by the companies trust center (HR / CEO / whatever)

Links
=====

Possible Base

* http://openpgpjs.org/
* WebPG
* JQuery / AJS / VanillaJS
* HTML5
* CSS

Similar Projects

* Based on PGP in JS / also node.js (local server) https://github.com/tanx/SafeWith.me

Sponsors
========

* iMi digital GmbH - Main development

<a><img src="https://www.browserstack.com/images/layout/browserstack-logo-600x315.png" height="75"></a>

BrowserStack Browser / Extension Testing factilities
