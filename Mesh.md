# The Philosphy of Data Mesh and The Problems of Data Management

While data mesh is not itself a technology or even a technology stack,
there are technologies and technology stacks which can be used to
bring the data mesh to your work. But to understand why and how to use
these technologies first we have to take a look at what problems data
mesh is solving and why.

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

In medium and large organizations, there are many teams using
operational data. 


## The Data Warehouse and The Data Lake vs. the Data Graveyard and the Data Swamp

The main approaches that have 

##
