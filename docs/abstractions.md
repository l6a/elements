# Abstractions

## Derivability of Data

Derivability is the degree of something can be calculated or obtained
from something else.
The concept is applicable to things more general than just math,
including data and data processing.

* Given an experiment setup, is it possible to obtain the same data?

* Given some source codes, is it possible to run the same analysis?

* Given some data and codes, is it possible to reach the same results?

For a piece of well defined software, given the same software
environment and input, it should be able to create bit-to-bit
reproducible output.
We define this as "absolute derivable", as in math.
On the other hand, there are observations, e.g., in weather, that the
measurements depend mainly on the physical environment---is it a sunny
or rainy day?
We define this as "non-derivable", where each measurement is
considered an independent realization.
And then there are something in between.
It is possible that a piece of software uses the system clock as its
random number seed so its results are different but statistically
consistent with each other.
We define this as "partial-derivable" and the results are correlated.
