## Update perlobj to include pattern `$obj->foo::bar(...)`

You can call a fully qualified subroutine name as a method when using
an object, such as `$myobject->some::method::name(...)`.

This was documented in `perlobj` but removed.
[Perl #116945](http://rt.perl.org/Ticket/Display.html?id=116945)
requests to add it back.
