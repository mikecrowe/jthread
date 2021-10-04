# jthread in josuttis namespace

The [upstream version of this library](https://github.com/josuttis/jthread)
was designed to be imported into an existing standard library. This means
that it uses `namespace std`. This is dangerous if you want to make use of
the library in your project because your compiler is too old to support
C++20 and you upgrade your compiler to a version that does have native
support for the features. This version moves everything into the `josuttis`
namespace to increase safety.

This version also contains a Makefile that works on Linux at least and
cherry picks [a pending fix](https://github.com/josuttis/jthread/pull/43).

The original README now follows.

# jthread
C++ class for a joining and cooperative interruptible thread (std::jthread) with stop_token helper-
- Reference implementation
- Test suite
- Papers proposing it for the C++ standard
  -  http://wg21.link/p0660  (main proposal for C++20)
     - http://wg21.link/p1287  (initial proposal for stop callbacks, merged with p0660r7)
  -  http://wg21.link/p1869  (additional minor updates for C++20)

Main authors:  Nicolai Josuttis (http://www.josuttis.com/contact.html) and Lewis Baker

The code is licensed under a Creative Commons Attribution 4.0 International License 
(http://creativecommons.org/licenses/by/4.0/).

TOC:
====

<b>source/</b>
- source code for the reference implementation
  and the test suite
  - to test the CV class extensions they are applied to a class condition_variable_any2

<b>tex/</b>
- final paper and proposed wording using C++ standard LaTeX style
  - to create the latest version:  <b>pdflatex std</b> 

<b>doc/</b>
- current and old documentations
  - all proposals P0660*.pdf

