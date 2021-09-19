# The Problems of Data Management

To understand why and how to use Data Mesh as a methodology its
important to take a look at what problems data mesh is intending to
solve and why.

Forward looking organisations have realised that data is critical to
their mission. Whether that be small, medium or large enterprises, or
even NGOs and volunteer organisations. Without an effective view on
the *data* of an organisation, decisions are made *blind*.

This blindness leads to failure in the market place since better
decisions will be made by competitors who have understood their data
better.

Many of the most successful companies of the last ten years have been
*data forward* in their thinking. The Amazons, Ubers and XXXX of this
world got where they are by making effective use of their data. This
includes understanding their own production process, their consumer
and how to lubricate the entire pathway from inputs to outputs, as
well as understanding clearly where market signals are happening and
how to respond to them.

While all of these things are now widely understood, progress towards
solutions to the problems has been slow and and frought with
failures. The number of data transformation disasters encountered has
been large, many of them extremely costly and some of them fatal.

There is also a difference in scaling-up your organisation with a
data-forward approach, versus bringing a data-forward approach to an
already large organisation.

Knowing the necessity of data transformation is not enough. One also
needs to know how to do it successfully. This is the problem which we
need to attack.

## Shadow Data

Shadow data affects organisations of all sizes, from the very small
team to the enormous corporation. What is shadow data?  It's the data
that is required for business function, and *should* be available to
everyone in the organisation who needs it, but is instead
inaccessible. Shadow data is locked up in Excel files, CSVs, word
documents and all manner of files and e-mail attachments.

The "Golden Source" of data, the data which contains the critical
insights may be in a single excel file of which only one key employee
has the latest version. They are responsible for obtaining the updates
from all of the sources necessary within the organisation, sometimes
by e-mailing it to the appropriate person to make changes.

For instance, we may have an employee, Kate, who has the excel file
for the next yearly budget which has to collate information from
multiple departments - a process which is iterative and requires
update by each of the departments in turn.

This shadow data is not immediately accessible for review by others as
changes are made. Instead everyone *but one* is working with an old
version and to ensure that changes dont get lost the updates must be
serialised, each department, one at a time.

Essentially what we are doing is turning Kate, a human, into a file
server with a serial read-write lock. This is a really poor approach
to software design, but an even worse approach to human organisation.

Shadow data needs to come into the light. It needs to be made
*visible*. This means that the data should be discoverable, the data
itself should be visible. In addition, it should be managed in such a
way as to enable collaboration and audit. It should be possible for
many people to work on the data simultaneously *safely*. The chain of
custody should be apparent: who made which changes when. The state of
the data should be recoverable: we should be able to undo a change.

It will not be easy however. The reason that data remains in the
shadows is that it seems *easier* for the user of the data. The
alternatives seem more difficult, more process heavy and the
advantages appear insufficient *at least in the immediate term to
those responsible*. To enlighten, we need tools, processes and the
inclusion of the voices of other stake-holders in the organisation who
will benefit in the longer term.

## The Data Silos

In medium and large organizations, there will be many teams using
operational data in their day to day tasks. This might be shared
files, or it might be a relational database management system. This
team does its job, and it does it well.

However, the data which is needed to carry out the tasks, is
*siloed*. That is, it might be accessible to the team, and
understandable to the team, but nobody else in the organisation can
make use of it.

This problem is almost as ubiquitous as the shadow data problem. Teams
have a transactional database which they can generate reports from,
where they know all of the details of the meaning of the fields, how
to get the data they need etc. but there is no *discoverability* for
others in the organisation. Not only do others not know what is in the
silo, they may not even know they don't know what is in the silo as
they don't know that data exists at all. And they have no way to
overcome this ignorance.

If they are lucky enough to discover some data, perhaps through word
of mouth or searching etc. then they still have the problem of getting
access to the data. This is non-trivial enough as finding the right
connector, or interchange is a chore in itself. But then if you figure
that out, you may not *understand* the data.

The data is best understood by the people doing the day-to-day
operations with the data. There is tacit knowledge about data-points
which is very relevant. Codes might be used to talk about data
elements - for instace you might have a csv with a column
`gd_src_nr`. Good luck interpreting that without a conversation!

You'll have to find the person who understands the title. And what is
*in* the data might also be opaque. If `gd_src_nr` is a number, what
kind of number is it? Is it dimensionless? Is it meters? Often times
the semantics contained within is only apparent by the way the
information is used.

Discovering this might require talking to someone. However, in a
transactional database even *this* may not be known. Automatic systems
have a way of becoming complete black-boxes as employees cycle through
an organisation and tacit knowlege is lost. Then we have to begin a
process of data archaeology. Essentially trying to interpret the past
based on limited knowledge.

## The Data Warehouse or the Data Graveyard

The most common and broadly advocated approach to overcome this
difficulty in the last years has been the *data warehouse*. A data
warehouse centralises the data that your organisation is
generating. It exposes much of the data that was formerly in data
silos, so that everyone in the organisation can get access.

If we want people in the organisation to be able to find the data and
what we can couple this data warehouse with a data catalog. The data
catalog can advertise what is in the data warehouse and what the data
elements are intended to mean.

However this approach also has serious problems. First, we have to
create a new IT team to manage the data warehouse. First they have to
find the siloed data that exists in the organisation. Then they have
to transform it into a queryable format and create the data catalog.

This process also doesn't end. New data is produced in operational
teams, methods change, and somehow the data warehouse is always
behind.

The quality of the data is also a very serious issue. In the
individual departments, the daily users will have methods of cleaning
the data, checking the data for correctness and curation of the data
which change and are improved on a regular basis. It is very difficult
for these changes to be included in the pipeline process of
integration into the central data warehouse. The team responsible for
the data warehouse does not understand the data and has difficulty
learning about new and improved processes when they arise.

This poor data quality often results in data being imported into the
data warehouse only to die a silent death. The processes which import
the data keep running. The transformation and load process ticks
along. The data catalog remains, and yet the data simply sits there
because nobody will use it because they still do not know how (because
they do not know what it *is*), or they do not trust its veracity.

In the end the central data warehouse team ends up over-subscribed
with demands to find data which should be available, to catalog this
data accurately and to verify and clean data which they simply don't
understand because they did not produce it and do not have detailed
operational knowledge of the problem domain.

Specialisation is the cornerstone of civilisation. And specialisation
is precisely what makes teams function efficiently. Not everyone
should have to know everything and some people should get good at a
few things.

How then can we demand our data warehouse teams understand marketing,
sales, human resources, billing and the best methods of big data IT
management all at the same time?

While data siloes promote organisational blindness to important data,
they have a *major* advantage over data warehouses. They promote
specialisation and only have to respond to the domain needs of the
operational teams using them for their own purposes. This is a big win
in terms of labour efficiency, as well as promoting data quality and
correctness. Domain teams can leverage domain knowledge, and immediate
needs along with a sparing use of IT experts to make the silo function
like a well oiled machine.

While data warehouses solve one serious problem, they do so by
creating another one just as serious. Is there some way we can have
our cake and eat it to?

## The Data Lake or the Data Swamp

The Data Lake provides us with a strategy to overcome the problems of
overcentralisation and lack of visibility at the same time.  Now that
scalable cloud infrastructure is easy to deploy it is possible to
create a *Data Lake* which can store all of the operational data for
each team directly in a giant repository.

This allows us to have our silo up where everyone can see it. You can
now get the latest cleaned operational data that marketting is using
without having to wait for the central data warehouse IT team to
figure out that it exists and import it.

Visibility has increased, the tempo of updates in the organisation
wide acscessable data has increased. Have we solved our problem?

Unfortunately visibility has increased so much that we can easily end
up mired in a *data swamp*. Every excel spreadsheet and csv used by
every domain team is now visible. While *availability* has increased,
ensuring that *discoverability* has also increased becomes a problem.

We have now created a difficult *governance* problem which we must now
solve. How is the data catalog updated and where does it live? Who
updates it? How do we know what the latest bit of data for a
particular problem is?

Imagine the latest website traffic results after a recent marketting
campaign are stored in a file in the lake
`website_traffic_18_sept.csv`. This might be the raw traffic feed, an
aggregated synopsis, enriched data from cross reference with other
data sources. And what does the field `apr_ks` in this csv mean? The
presence of the file does not make the file automatically *useable*.

All of the tacit knowledge about what the data means which data set
should be considered useful for analysis is missing. It must be
surfaced and the lake, *in and of itself*, can not solve this problem.

And *who* is responsible for cataloging this file? *What* kinds of
data need to be surfaced to the organisation and which can remain as
invisible operational data so as not to muddy the lake. *Where* do we
say what is the golden source of data and what is merely staging data
waiting to be cleaned. *How* do we notate that something is merged
data or what a data field means?

The data lake gets us part way there by giving us a scalable
infrastructure which enables us to overcome silos, but it does not *do
it* for us. We need to make this task of governance a
technical-organisational goal in itself and overcome the various
problems which we have encountered by taking them each seriously as
part of our philosophy of attack.

## Joined up Thinking

The data warehouse, whatever its problems, had another advantage over
the Data Lake. It made *joining* data possible, even if it did not
make it easy. The central team could be tasked with allowing sets of
data to pivot around various join-points, such as customers,
employees, accounts etc.

Of course this joining of data creates an enormous burden on the data
warehouse team. In practice we *will* get joined data, but only on a
limited number of join points for a limited number of entities based
on organisation wide priorities which can be imposed on the data
warehouse team. The process is hard, expensive but *possible*.

With the data lake, we have a much more difficult *governance* problem
in trying to join up data. CSVs, excels, and big tables may *look*
flat, but they are not intended to *be* flat. The `customer_id` field
is meant to be a *link* which can be used to pivot.

Having this id does not mean we know what it refers to. If it is a
number it is very possible to have two departments with different
methods of assigning the id. In an RDBMS it is common for ids to be
generated in sequence based on nothing more than the order that the
record was added. So multiple different RDBMS operational systems may
yield different ids very easily.

This process is called *entity unification* and unifying the entities
is tricky.

Tamr CTO Dr. Michael Stonebraker gives this discription of the typical
traditional process of *entity unification*:

> * Have a programmer interview the business owner to discover the local schema used.
> * Have the programmer write the conversion routines from the local schema to the global schema.
> * Have the programmer write cleaning and transformation routines.
> * Have the programmer write a script to load the global schema, and then update it over time.

This is the process which is generally being used in the data
warehouse in practice. And clearly this is not happening at all in the
Lake without unless we impose another layer of process. The lake
allows us to scale up but without a scaffold to guide us it will scale
up to an unjoinable mess.

The Linked Data community has been advocating a different process
since the inception of the Semantic Web by Tim Berners-Lee
in 1999. That is we should use *universal identifier* for entities.

This is a huge undervalued contribution. Instead of just a customer id
field, we need to have a field which describes *where* this was the
`customer_id` and this should disclose to us something about the
*semantics* of the name. Instead of the number `1232` for our record
we have:

`iri://www.example.com/accounts_database/Customer/1232`

Then at least when we *mean* for this to be the *same* pivot we can
actually know! It will not, however, magically solve the issues of
entity unification for us. In particular it does not tell us what can
be in a `Customer`, or how to join up this `Customer` entity with
other `Customer` entities in the organisation located in different
places.

This process of organisational governance of identity, will prove
central to creating an effective data *mesh*.
