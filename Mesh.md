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

Rather than the central data team, what we need is a meeting of
stakeholders along which come together to help create the
infrastructure for a distributed solution. This means having standards
for *discovery* of resources, for encouraging micro-service style data
architectures which make the *data product marketplace* something
where you can easily get your consumables, and dealing with the
problems of *integration* of data products as they arise.

Discovery with distributed data products must be done differently than
the data catalog of old. We need to make it easy for domain teams to:

* Advertise what data they have on offer.

* Describe what it means and any associated documentation required to
  understand it.

* Do so on a searchable index of data.

Essentially the organisation needs a super-market, bazaar or mall
where people can find what they need.

The *data product health* should also be something looked after by the
governance team. Part of the problem in the Data Lake is that there is
simply so much data. You can *try* to index it all and use a query
engine, but that's simply not enough. When google ranks its results,
they do so not just by indexing what is there, but by looking at how
*useful* it is by counting the page rank (the inward link flow).

We want data products which are going unused to be noticeable as they
are taking up precious shelf-space. It is not the *disk space* that is
the problem, it's the noise.

And successes should also be noticed. The organisation should pay
attention to *why* they are successful and attempt to learn lessons
from this.

Integration is another issue that requires good governance. This
includes the ability to link to other resources, and approaches to
solving entity unification problems.

Linking to other resources requires that the governance team have
methods of a way to *name* resources so that they can be found. The
best naming scheme that the data community has yet found is still the
URI. It gives information about the protocol, the place where you
might find the data, the address of the data, and can be easily
disambiguated between different *meanings* of similar names.

The problems which must be addressed here include some strategy for
knowing when links are no longer valid. (Something which was
considered important in the original X
