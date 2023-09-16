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

Note that absolute derivable does not imply correctness.
If the upstream data is wrong, or there is a serious bug in the data
processing algorithm, the result is obviously wrong.
Nevertheless, even when the result is wrong, absolute derivable can
help track mistakes and hence make correction possible.
Therefore, absolute derivable should be a goal in a scientific
process.

To reach absolute derivable in the final results, we simply track all
inputs of the data processing and version control anything that is not
absolute derivable.
Intermedia data products that are absolute derivable do not needed to
version controlled, but may be cached to speed up data processing,
reviews, and inspection.
In this sense, depending on the compilers and programming languages
used, software binaries or envirnments may needed to be version
controlled "data" themselves.
