# StatProfilerHTML

This module formats the output from Julia's Profile module into an html
rendering of the source function lines and functions, allowing for interactive
exploration of any bottlenecks that may exist in your code.

Have a look [at this example output](http://www.infty.nl/StatProfilerHTML.jl/example-output/), which
is the result of profiling

    using MultivariatePolynomials
    @polyvar x y z
    @profile (x + y + z)^120;


This module contains a fork of the rendering part of Mattia Barbon and Steffen
Müller's excellent
[Devel::StatProfiler](https://github.com/mbarbon/devel-statprofiler), which is
a statistical profiler for Perl. It depends on Text::MicroTemplate, which for
convenience, we ship as part of this bundle.
