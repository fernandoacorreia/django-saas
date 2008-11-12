======
Design
======

TODO: Document project design.

Architecture
============

TODO: Complete architecture definition.

* Integrate with standard Django user and authentication modules.
* Integrate with a Pinax website.
* Integrate with a billing application like Satchmo.

Busines entities
================

TODO: Complete business entity definition.

Service plan
    A collection of services with associated service levels (usually resource
    limits) and pricing. A plan can be fundamental or additional. Additional
    service plans can be added to selected fundamental service plans to add
    services or increase service levels. Pricing may be free, periodic or
    one-time.

Service
    An individual feature available to customers, like image hosting or
    record keeping.

Resource
    An element used by the services, like processing time, storage space,
    communication bandwidth.

Subscription
    An assignment of a service plan to a customer. Can have a trial or grace
    period.

Role
    The condition in what the user uses the services. For instance, as a
    sales representative or an office clerk.
