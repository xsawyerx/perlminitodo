## Add RT custom fields to remove META tickets

Currently Perl 5 uses RT (Request Tracker). Instead of using "labels",
which RT does not have, we create tickets that only serve to list other
tickets ("meta tickets").

RT has support for "custom fields", which is arguably even stronger,
because it allows us to create additional fields. These provides us
with a finer-grained "label"-esque feature.

Let's take an example. There are some errors we consider "BBC" (Blead
Breaks CPAN) which is applied to any commit in blead (Perl 5 main
development branch) that breaks something on CPAN. We can have a custom
field "BBC", which can be a flag of true or false. (This is how labels
are - you either have them or not.) However, we can also have a custom
field called "Type of ticket", in which "BBC" is one of several
optional types. You can even mark more than one.

What we need is to decide on the various types of tickets and nominate
to the list the appropriate field name and possible values. We will
then ask RT to create the appropriate field in our
[RT](http://RT.perl.org).

Here are several examples:

* Blockers (blocking a release)
* Types of errors:
  * BBC (Blead Breaks CPAN)
  * Stack-referencing
  * Fuzzing errors (usually stack referencing, so maybe not.)

More on custom fields:

http://kb.mit.edu/confluence/display/istcontrib/Creating+and+managing+Request+Tracker+Custom+Fields
