Introduction
============

The `Django SaaS`_ project is a collection of reusable Django applications that
provides basic functionality for a subscription-driven website.

.. _Django SaaS: http://django-saas.info/

Objectives
----------

* Offer services to multiple customers in contained way so each customer only
  has access to its own data.
* Allow for the selection of a service plan among several options.
* Enforce service levels according to the selected plan (for instance,
  limiting the ammount of resources that can be used).
* Manage security, allowing many users per customer.
* Allow account management by the customer account administrators and by the
  service administrators.
* Integrate with a billing application.
