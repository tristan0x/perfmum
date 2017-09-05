.. _specifications:

==============
Specifications
==============

This page gathers use-cases, requirements, and technical specifications of
**perfmum** utility.

Feel free to use-cases and requirements by creating a
`pull-request <https://github.com/tristan0x/perfmum/edit/master/docs/specifications.rst>`__


Use-cases
=========

Micro-benchmarks in CI
----------------------
As a HPC developer, given a C++ library maintained by HPC team, when I
push a Git changes, then continuous integration
executes micro-benchmarks of some critical C++ sections of the library.

Micro-benchmarks CMake helpers
------------------------------
As a HPC developer, given a C++ library built with CMake, **perfmum**
provides dedicaded CMake modules to add new micro-benchmarks to the ``test``
target.

Micro-benchmarks monitoring over time
-------------------------------------
As a HPC developer, given a C++ library maintained by HPC team with 
a micro-benchmark integrated in the continuous integration process, I can
review the history of metrics of this benchmark in a web browser.

Launch coreneuron simulation
----------------------------
As a HPC developer, I can use **perfmum** to describe a coreneuron simulation
from the different build configurations to the runtime parameters. **perfmum**
will take care of the different phases: build, run, and archive results.

Simulations for coreneuron UT
-----------------------------
As a HPC developer, I can describe the different simulations the continuous
integration workflow of coreneuron has to use to validate a pull-request.

Coreneuron integration tests
----------------------------
As a HPC developer, I can describe the different simulations that must be executed
once a week to validate **coreneuron**.

Alerting in case of performance regression
------------------------------------------
As a HPC developer owner of a component, if continuous integration
detects a performance regression, then I am notified via email or Matrix.

Requirements
============

* Can configure build according to several dimensions:
   * toolchain: gcc+mvapich, intel+intelmpi, ...
   * architectures: cpu, gpu, knl
   * variants: profile, non-profile, optimization-types
* Can configure the runtime environment of the simulation/test:
   * datasets
   * input parameters
* Can configure what metrics to extract
* Push all metrics and row results to a DB (Elasticsearch, GPFS)

Technical Specifications
========================
*To be defined*
