# python-benchmarking-public

Curated results from personal bench_runner benchmarks. The hosts differ
quite a bit:
 - "tc1" and "tc2" are identical 4Gb RAM, Intel Core i3 6100T systems with 4Gb RAM
   (fairly old, low-powered), running Debian testing. These are dedicated
   machines and so noise is limited.
 - "Pi5" is a dedicated Rapsberry Pi with 8Gb RAM and an SSD for storage,
   running raspbian.
 - "centurion" is an Intel Core Ultra 7 265 system with 64Gb RAM (fairly
   new, overpowered), running Debian unstable. This machine has other
   household duties so it's sometimes noisy.
 - "windows" is an Intel Core i5 14600 system with 32Gb RAM running Windows
   11 that I occasionally run benchmarks on.

The plots are produced by
[bench_runner](https://github.com/faster-cpython/bench_runner), which runs
[pyperformance](https://github.com/python/pyperformance) benchmarks and
tracks the results over time.

`bench_runner` builds Python with `--enable-optimizations` and
`--with-lto=full`, but _without_ BOLT or `--with-tail-call-interp`. The
compiler versions are from Debian/Ubuntu packages. (Clang versions 20 and 21 are
curently broken in my setups, as is BOLT. Adding them is on my TODO list.)

## Longitudinal results

Below are longitudinal timing results.

The plots named "Python 3.14.x vs. 3.13.0" compare performance across
pyperformance benchmarks by taking the geometric mean of all the benchmarks.
A result of 1.05x for a particular compiler means Python 3.14.x built with
that compiler performs 5% faster than Python 3.13.0 built with the same
compiler.

The plots named "Python 3.14.x (NOGIL) vs. 3.13.0" compare the same thing,
but with 3.14.x built with
[`--disable-gil`](https://peps.python.org/pep-0703/). The 3.13.0 it compares against
is _not_ built with `--disable-gil`. A result of 1.00x means that
_free-threaded_ Python 3.14.x (built with that compiler) is just as fast as
_regular_ Python 3.13.0 (built with the same compiler).

A note about the "centurion" plots: that system is a very fast one, which
seems to make the benchmarks very sensitive, making the performance
differences much more pronounced than on the much older "tc1" and "tc2"
systems. For instance, we had [a big regression on some versions of
gcc](https://github.com/python/cpython/issues/129987#issuecomment-2802989278)
(incidentally the reason I started collecting all this data) which seems
much bigger in the "centurion" plots than the "tc" plots. (The plots also
use different axes! So be careful when comparing them.) The same big swings
show up in the per-configuration plots.

![Longitudinal speed improvement](/longitudinal.svg)

## Results per configuration

These plots show the effect of different ways to build Python _at the same
version_.

The plots named "Effect of free-threading" show the performance difference
between free-threaded and gil-ful builds _of the same Python version_. A
result of 0.95x means free-threaded Python is 5% slower than the same
version of Python with the GIL.

The plot named "Effect of JIT" show the performance difference between a
build with the [experimental JIT](https://peps.python.org/pep-0744/) and
without it. I only ran one set of these manually, once, to verify the
performance effect was the same for all compiler versions. I measure this
more regularly in the future.

The plots named "Effect of gcc versions" and "clang versions" show the
performance difference between the same Python, built the same way (without
free-threading), using different _compilers_. The baseline is GCC 9.4 (GCC
11.3 for Pi5), because that's the compiler version used on [Faster CPython's
benchmarks](https://github.com/faster-cpython/benchmarking-public/). These
plots can be a bit more noisy since the baseline is more of a moving target
(Python compiled with GCC 9 getting faster makes the other compilers appear
to get worse). For the most part, all the compiler versions I'm tracking
seem pretty stable and of similar performance. The most notable outlier is
clang 19, which has a known regression in computed-goto handling that
significantly impacts Python. Again, the differences seem more pronounced on
"centurion" than the "tc" hosts.

![Configuration speed improvement](/configs.svg)

## Individual benchmarks

These plots show longitudinal results for a few compiler versions, with a
separate plot per benchmark in the `pyperformance` benchmark suite. They
compare the same thing as the longitudinal "Python 3.14.x vs. 3.13.0" plot
above: a result of 1.05x means that benchmark is 5% faster with 3.14.x than
3.13.0. These individual plots are useful to evaluate the noisiness of
individual benchmarks, as well as identifying consistent changes
(performance improvements or regressions in Python). **Be careful comparing
these plots by eye**, as they use different Y axes!

![Individual Benchmark Results](/benchmarks.svg)

