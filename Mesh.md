# The Philosophy of the Data Mesh

Data mesh is a philosophical approach to overcoming the organisational
and technical problems encountered while doing *data management in the
large*. The philosophy has been honed as a *praxis* in real projects
which have attempted to overcome the [problems of data
management](./Problems.md). We will therefore make frequent references
to these problems and how we solve them.

There are a number of general principles and rules of thumb that we
will repeatedly make reference to, and which we will describe some
techniques to address. Data Mesh is not a technology stack, but it
should give you a map which can help you to choose an effective
technology stack.

## The Data Product

The tech world is rife with stories about Data being the new oil, or
data being the new gold. Data forward organisations are capable of
beating their competition by having better understanding of themselves
and the market allowing them to better cut costs with increased
efficiency and take advantages of opportunities by having more
developed senses of what is going on in the market.

Yet while we talk about data as being critical to the way we do
business, we tend to treat it like it is, in itself, valuable. Data is
*not* gold, and it is *not* oil. It isn't even 24k gold or high-octane
performance refined petrol. These are completely fungible commodities
which simply grow value as their quantity grows.

Data is *nothing* like this at all. Instead, data is a *product*. It
is closer to a BMW or an iphone than it is to oil or gold although
this too stretches the analogy.

What do we mean that data is a product? It means that we have to
carefully assemble our data for the *data consumer* to ensure a
successful user-experience. It is a complex assemblage that might
require joining many disparate parts and refining mountains of input
data to create something small which exposes the insights which can be
operationalised successfully by your organisation.

And when this product is complete, it needs to be advertised to the
people who need it to solve their problem. It needs to come with the
support necessary (both static documentation and human availability)
for them to use the product effectively for their needs.

Who are the consumers of the data product?

The *data consumer* themselves might also be involved in the
production of another data product. And so our data product becomes an
input commodity in a potentially complex supply chain inside (or even
outside) of our organisation.

This means that we will refine the product to meet customer needs as
these needs are voiced. We must have *empathy* for the consumers of
our data product.

The data product *must not* be like an excel spreadsheet or csv dumped
into the lake. Its internal success in providing a product will be
viewed if its *consumption* is measured and monitored. KPIs around
data consumption will give us a window into *data product health*.

To have successful data products *data product health* must be
available easily and with low overhead to those producing the data
product. This is part of the problem of *governance*.

This data product is being created by a domain team so they should be
tailoring it first for their own consumption. The data product health
for internal consumption is a first measure of success.

However the sign that we have a true data product is if the data
product is used by others in the organisation. To make this successful
we will need to pay attention to devloping the *data marketplace*
(which we will discuss in more detail later).

If *all* data products go unused, then the internal *data marketplace*
is broken. The discovery tools and APIs for data product consumption
need to be before we can go forward.

Supposing this marketplace has been developed but our data product
still goes unused, we need to know this! And once we know it is
unused, we need to know why. It could be that the data product is:

* Hard to find: It might be poorly advertised.
* Impossible to understand: The documentation of the *meaning* of the
  data is poor.
* Too complex: The data surfaces too much information so that
  consumers lose the forest for the trees.
* The wrong data: The data simply does not contain what is needed by
  the consumer to solve thier own problems.
* Poor in quality: If data is often wrong, consumers stop trusting it
  and use other approaches.

Many of these problems can be solved by the domain team if they are
*aware* that there is a problem in the first place. As with a physical
product, success is what sells. So if we don't even know what sells,
we can't know if we are successful!

## The Domain Team

The Data Mesh approach is essentially *cybernetic* in philosophy in
that Data Mesh views the problems of data management to be fundamentally
technical-organisational.

Data management is done *by* and *for* people, using the tools we have
at our disposal. And because of this how we organise people is an
absolutely critical part of finding solutions.

The core of our approach to solving the problems of data management is
the domain team. We should embrace specialisation and leverage
it. This doesn't mean that we create a marketing team which is 100% MBAs!
Quite the contrary, we need a *cross-functional* domain team, which is
staffed with all of the people which are necessary to carry out the
responsibilities of our unit.

But what *are* the responsibilities of our unit. This is where Data
Mesh comes in: we have to change *what* we do and because of this, we
will have to change *how* we perform and *who* will be in our team.

The domain team, aside from its core function of carrying out the
operational function with which it is tasked, must also build *data
products*. This may feel like a burden to a team who is trying to
carry out a business function, so we need to make the process as easy
as possible, and make the results as *internally* useful as
possible. The value to the enterprise in *having access* to these data
products is enormous so encouraging incentive alignment between the
domain team and the organisation here is critically important.

## Governance

In rejecting the over-centralisation of the data warehouse, one might
suppose that we can simply decentralise all of the tasks. The sad
reality is that this will simply lead back to the data silos which we
are trying to overcome. Without organisation wide *governance* we will
descend into the anarchy of fiefdoms.

The process of good governance is *empowering* the domain teams to
produce for the general health of the organisation. The focus is not
simply in imposing processes, but in *enabling* people to do the right
thing. A well regulated marketplace for data is the central role of
governance.

Rather than the central data team, what we need is a team which
includes access to:

* Stakeholders: Representatives of various domain teams which will
  generate or consume data.

* Management: The people responsible for aligning the governance teams
  priorities with business objectives.

* IT Staff: The software engineering and data modelling specialists
  who will be needed to carry out any global governance tasks in
  conjunction with the various domain teams.

This governance group should create the *infrastructure* for a
distributed solution. This means having standards for *discovery* of
resources, for encouraging micro-service style data architectures
which make the *data product marketplace* something where you can
easily get your consumables, and dealing with the problems of
*integration* of data products as they arise.

Discovery with distributed data products must be done differently than
the data catalog of old. We need to make it easy for domain teams to:

* Discovery: Advertise what data they have on offer.

* Accessiblity: The data product must be easily accessible in a
  consumable format using simple interoperatble APIs.

* Semantics: Describe what data *means* along with any associated
  documentation required to understand it.

Essentially we need a super-market, a bazaar or a mall where people
can find what they need when they're looking for the data. The
products should be in shop windows, and we should have as much detail
as we need: automated documentation first, but then human contact
second.

The *data product health* should also be looked after by the domain
team, but easily viewable by the governance team. Part of the problem
in the Data Lake is that there is simply so much data. You can *try*
to index it all and use a query engine, but that's simply not
enough. When google ranks its results, they do so not just by indexing
what is there, but by looking at how *useful* it is by counting the
page rank (the inward link flow).

We want data products which are going unused to be noticeable as they
are taking up precious shop-front windows-space and shelf space. In
the data lake it is not really the *disk space* that is a primary
problem of too much data, it's the noise.

And successes should also be noticed. The organisation should pay
attention to *why* they are successful and attempt to learn lessons
from this.

Integration is another issue that requires good governance. This
includes the ability to link to other resources, and approaches to
solving entity unification problems.

The problems which must be addressed here include:

* Naming and Linking
* Unification

### Naming and Linking

Linking to other resources requires that the governance team have
methods of a way to *name* resources so that they can be found. The
best naming scheme that the data community has yet found is still the
URI. It gives information about the protocol, the place where you
might find the data, the address of the data, and can be easily
disambiguated between different *meanings* of similar names.

URIs are vastly better than the typical RDBMs concept of identity
which is often simply an integer, together with the *local* concept of
a *foreign key*. That is, we understand the integer is to represent a
customer record because it is the index of the user table, and other
tables must explicitly mark that they are talking about this integer
as a user.

Some companies have used UUIDs (Universal Unique IDentifiers) which
have the form: `123e4567-e89b-12d3-a456-426614174000`. Of course this
is better than simply a number, because it's possible use these UUIDs
universally for linking across different databases without a very
large chance of collision (collision probabilities are exceptionally
low). However, this doesn't say anything about *what* it is, or
*where* it *is*.

By contrast, an appropriately imagine the customer record:

`iri://customer_accounts_department/Customer/912ec803b2ce49e4a541068d495ab570`

As against:

`363`

Clearly the former gives more information about the data in terms of
both *where* and *what* the data refers to. The universality is
similar to situation with the UUID, but also more transparent, while
also not disclosing the *content* of the Customer record in the event
that we should not *know* anything about the Customer directly. This
content opacity coupled with universality helps when we attempt to
reason about our Customers in *abstract* which is useful to avoid
disclosure of *Personally Identifying Information* and reducing the
number of place which data exists which might be subject to *General
Data Protection Regulation* (GDPR) or similar regulatory requirements.

### Unification

Unification on the other hand is a very hard problem. It can't be
solved completely in the abstract. It requires understanding of the
type of unification problem that is being encountered. The governance
team must *understand* the kinds of unification questions that must be
answered, and produce a strategy for attacking them as they arise.

In some cases this can be done at the *domain team* level, when the
data sources are really domain specific, but often the unification
problem arises from attempting to consolidate the *meaning* of records
from multiple sources. This means that there may be a larger,
multi-domain project for the integration. Clearly this requires
oversight and assistance by the govnernance team.

## Conclusion

Data-mesh is a philosophy and theoretical framework for how to attack
our data management problems. It will not give a concrete stack of
technical solution to your data-management problems. These questions
are not possible to decide in general, as different organisations will
face different challenges and have different business
priorities.

However the *data mesh* framework *will* give us powerful insights
into *how* to implement solutions in a concrete technical sense. We
will see more about this in the
