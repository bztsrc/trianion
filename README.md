New approach to three-dimensional space in mathematics
======================================================

Current approach of mathematics leads only to a two-dimensional space ([complex numbers](https://en.wikipedia.org/wiki/Complex_number)).
Hamilton tried to expand it into a three-dimensional structure with [quaternions](https://en.wikipedia.org/wiki/Quaternion),
although there are several problems with that. For one there's the noncommutativy of multiplication which leads to a strictly
skew field instead of real, complete field.

NOTE: this is not a mathematical proof per se, only a quick draft on my thoughts. But as I've used only well proven lemmas,
feel free to do the homework and write it down in detail. I guarantee it will check out.

Old Way
-------

Normally mathematical structures are originated from zerus element, existential element and the next operator along with
addition and multiplication. With the next operator you can build up natural numbers. Addition leads out of the field, which
can be solved by introducing negative numbers. Likewise multiplication leads out of the field, solved by introducing complex
numbers. Unfortunately there's no way to go from here, you can only describe two-dimensional space with this approach
(quaternions does not describe the three-dimensional space completely as mentioned earlier because they only form a skew field).

Proposed New Way
----------------

To came around this problem, I'm proposing to use a different operator instead of the next operator. It's the well known
Pythagorean Theorem, or Euclidean distance:

```
d(a,b) = sgn(a-b)*sqrt((a-b)^2)
```

But we'll keep the direction of the distance. With that we start with these axioms:
* zerus element (0)
* existential element (1)
* distance operator (d)
* addition operator (+)
* multiplication operator (*)

First we have to show it is possible to describe the next operator with the distance operator. That's trivial, as applying
the distance of zerus and existential element on the existential element will produce the next of the existential element.

```
0' = d(0,1) = 0 + d(0,1) = 1
1' = d(0,1+d(0,1)) = 1 + d(0,1) = 2
...etc.
```
So it is possible to describe natural numbers without the next operator, using recursively the distance operator only.

When used on the basic elements in one-dimensional space, this distance operator should lead out of natural numbers.

```
d(0,0) = 0
d(0,1) = 1
d(1,0) = -1
d(1,1) = 0
```

This is great as it lead us to the negative numbers. Now using the same direction keeping Euclidean distance on two
dimensions gives us:

```
d(0,0)         = sqrt(0)  = 0
d(0,1)         = sqrt(1)  = 1
d(1,0)         = sqrt(-1) = i
d((0,1),(1,0)) = sqrt(2)  = z
```

Here the combination of basic elements gives us 3 possible outcome. No surprise in that. Zerus element, existential
element, an so called imaginary element. These three describes a two-dimensional space called as complex numbers. Now the
interesting part is, applying it to two dimensions (two units on different axis gives a Phitagorean triangle), it also
gives us a fourth element, sqrt(2) which is known as an irrational number. This hints us the following on three-dimensional space:

Conclusion
----------

To properly describe a three-dimensional space in algebra, one should use the following basis:

* real part (r = 1)
* imaginary part (i = sqrt(-1))
* irrational part (z = sqrt(2))

```
n = ar + bi + cz = a + b*sqrt(-1) + c*sqrt(2)
```

I won't prove that these basis are forming exclusive dimensions as that has already been done by many mathematicians, and is a
well known fact. No number exists that could fullfill the following equations:

```
a*r = i
b*r = z
c*i = r
d*i = z
e*z = r
f*z = i
```
Therefore this newly proposed structure must form a complete field, and you can use addition and multiplication on it without
loosing commutativy and leaving the field.

Q.E.D.

For this new structure I'm proposing the name __trianion__. It's originated from the greek 'tria', which means 3, refering to
it's three-dimensional nature; but also in memoriam of a serious shock to my home country after WW II.

Copyright (c) 2017, Zoltan Baldaszti, All rights reserved.
