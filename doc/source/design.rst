======
Design
======

Architecture
============

*Note:* These are initial thoughts about the architecture. It will be detailed
further during the initial iterations.

The project is implemented as a pluggable Django application that implements
the use cases.

The Audit log may be implemented as a reusable application.

Django middleware will be used for customer subdomains and possibly for
user authorization (validating customer and role).

The application will be integrated with standard Django user and authentication
modules and it will also be deployable inside a Pinax website.

It will also integrate with Satchmo for billing.

Busines entities
================

Audit log
    Log of operations for security, monitoring and auditing.

Customer
    A person or organization that has subscribed to services.

Resource
    An element used by the services, like processing time, storage space,
    communication bandwidth, user accounts.

Role
    The condition in what the user uses the services. For instance, as a
    sales representative, an office clerk or an account administrator.

Service
    An individual feature available to customers, like image hosting or
    record keeping.

Service plan
    A collection of services with associated service levels (usually resource
    limits) and pricing. A plan can be fundamental or additional. Additional
    service plans can be added to selected fundamental service plans to add
    services or increase service levels. Pricing may be free, periodic or
    one-time.

Subscription
    An assignment of a service plan to a customer. Can have a trial or grace
    period.

User profile
    Details about a user, in addition to basic user information.
