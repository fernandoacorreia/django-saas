============
Requirements
============

Actors
======

Account administrator
    One or more persons that have the authority to manage the relationship
    between the customer and the service provider. They select services and
    answer for the payments. They can also authorize other people to use the
    services that were contracted by the customer.

Account user
    Also referred to as just "user", is a person authorized to use the services
    contracted by the customer, within the limits of their roles. An account
    administrator is also an account user.

Customer
    Also referred to as "customer account" or just "account", is an
    organization or a person that has contracted the services that are offered
    by the Web application.

Service administrator
    Is a representative of the service provider that manages the services that
    are offered by the Web application.

Service provider
    Is the organization that offers services through the hosted Web
    application.

Use Cases
=========

Service administration
----------------------

Define service plans
    The service administrator defines the services, resources and service plans
    that are offered.

Manage customer accounts
    The application shows the service administrator a list of customer
    accounts. The administrador can add, edit or disable customer accounts and
    change service plans. He can also change billing options and add billing
    instructions like additional charges or credit.

Integrate with billing application
    The application sends to the billing application the list of billings to
    be processed. At a later time, the application receives from the billing
    application the results of the billing process (success, failure,
    payment received).

Account administration
----------------------

Create new account
    The future account administrator selects a service plan and enters the
    basic information required to create a new customer account and his own
    user account. The application creates the accounts and directs the user
    to the setup procedure.

Setup new account
    The application offers the user options and forms to prepare the newly
    created account for use. This may include selecting additional services,
    configuring application-specific objects and creating user accounts.

Manage account
    The account administrator enters account information like customer
    name, subdomain, location, contact information and payment information.

Manage users
    The application shows the account administrator a list of account users.
    The administrador can add, edit or disable user accounts and assign
    roles to users.

Select service plans
    The account administrator selects a fundamental service plan and optionally
    one or more additional service plans. This represents a contract between
    the customer and the service provider. The application validates the change
    and updates the customer account with the selected service plans.

Service utilization
-------------------

Provide account subdomains
    The user types in the browser a subdomain in the form customer.service.com.
    The application authenticates the user and provides the services for
    the specified customer.

Edit user profile
    The user changes his profile information.

Change password
    The user enters the old and the new passwords. The application updates
    his profile with the new password.

Enforce service levels
    When the user request service operations that need to consume or allocate
    metered resources, the application verifies if the request can be granted
    within the service levels that were contracted and payed for by the
    customer. In case they exceed limits, the application may block the
    operation or allow some grace period or excess margin.

Enforce permissions
    When the user request service operations, the application verifies if his
    roles grant permission and blocks the operation if they don't.

Characteristics
===============

* Security, at all levels, shall be treated as a concept of paramount
  importance.
* Any operation with security implications, related to customer account,
  service plans, user accounts, permissions and similar entities will be
  recorded with extensive details in an audit log and the people involved
  will be notified.
* All attempts to execute operations beyond security permissions must be
  recorded and notified.
* No object in this application domain can ever be deleted, just disabled.
  This does not necessarily applies to objects of other applications that
  use Django SaaS.
* The application must support internationalization and localization.
* Data owned by each customer must be separated in a way that each account user
  only has access to data of the customer he belongs to.
