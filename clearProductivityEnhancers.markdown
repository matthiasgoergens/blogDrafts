In software development practices come and go.  Some are fads.  Some
are here to stay.  The practices have advantages and drawbacks.  I
want to talk about practices whose advantages clearly outweigh their
drawback.

1. automatic memory management / garbage collection
2. automated testing / quickcheck
3. purity by default
4. type inference
5. version control
6. higher order functions
7. expressions
8. REPL
9. Strong types

Purity by default
=================

The holy grail of software development is composability, because if
you have better glue, you can chop up your problem into smaller bits.
Purity by default helps here.  It also helps with testing (and proving
(!)).

There is a duality of strong restrictions leading to easy reasoning,
and vice versa.  This is duality is related to the maxim: "Be liberal
in what you expect, and conservative in what you produce." (Which is
at odds with "Fail early, fail loudly.")

Automated testing
=================

Humans make mistakes.  Testing catches coding mistakes, and also
serves as a way to communicate intended semantics of a system.
Because a system's semantics are not only what it does at the moment,
but also what variations are still allowed.

Humans make more mistakes under pressure.  And under time pressure is
exactly when you will slip in manual testing.  Automatic testing is
the opposite of technical debt.  It is a technical asset, in that it
allows you to build up an infrastructure now, that allows you to move
faster later.

Type Inference
==============

Type inference makes source code less verbose, and makes strong static
type systems viable for exploratory programming at all.

Version Control
===============

Modern solutions like git have made version control so cheap and
beneficial, that even single developers benefit.  For multiple
developers version control is absolutely essential.  Why?

Higher order functions
======================

Even Java and C++ are getting "lambdas".  The attraction is not so
much that you can have anonymous functions, but that it is easy to
create functions that are only used as arguments to other functions.

REPL
====

Read-Eval-Print-Loop-s help shorten the Edit-Test cycle, and help with
exploratory programming.

Strong Types
============

PHP and JavaScript will happily accept

    1 + "0"

and try `their best' to do something.  Python, Haskell, C etc will
reject this with an error.  Python and Haskell do not agree on
everything, but they do agree on failing loudly here (if at runtime vs
compile time).

Not universally good
--------------------

Object oriented programming.  I predict we will see more functional
programming approaches.


Useful concepts and metrics
---------------------------

Iteration length of Edit-[Compile]-Test cycle.

Some predicitions
-----------------

Parser combinators will become mainstream

Static Types or perhaps Racket's contracts: static types allow you to
express a great number of unit tests statically, and checked by the
compiler.
