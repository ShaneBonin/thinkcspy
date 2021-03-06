..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell. Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts. A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

.. qnum::
   :prefix: list-27-
   :start: 1

.. index:: tuple assignment, swap

Tuple Assignment
----------------

Python has a very powerful **tuple assignment** feature that allows a tuple of variables on the left of an assignment to be assigned values from a tuple on the right of the assignment. For example, given the tuple ``julia`` that we looked at in the previous section, we can do the following:

.. sourcecode:: python

    (name, surname, birth_year, movie, movie_year, profession, birth_place) = julia

This does the equivalent of seven assignment statements, all on one easy line. One requirement is that the number of variables on the left must match the number of elements in the tuple.

Once in a while, it is useful to swap the values of two variables. With conventional assignment statements, we have to use a temporary variable. For example, to swap ``a`` and ``b``:

.. sourcecode:: python

    temp = a
    a = b
    b = temp

Tuple assignment solves this problem neatly:

.. sourcecode:: python

    (a, b) = (b, a)

The left side is a tuple of variables; the right side is a tuple of values. Each value is assigned to its respective variable. All the expressions on the right side are evaluated before any of the assignments occur. This feature makes tuple assignment quite versatile.

Naturally, the number of variables on the left and the number of values on the right have to be the same.

.. sourcecode:: python

    >>> (a, b, c, d) = (1, 2, 3)
    ValueError: need more than 3 values to unpack
