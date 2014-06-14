About
=====

A simple tool based on `stress`_ used to stress test CPUs on your system.

.. _`stress`: http://manpages.ubuntu.com/manpages/precise/man1/stress.1.html


Building the Docker image
=========================

Clone this repository and run::

    $ docker build -t petarmaric/cpu_stress_test .


How to use this image
=====================

Quick start::

    $ docker run -ti petarmaric/cpu_stress_test

The following environment variables are honored for configuring ``stress``:

    * ``-e STRESS_SYSTEM_FOR=...`` (defaults to ``5m``)

    * ``-e MAX_CPU_CORES=...`` (defaults to ``1``)

Changing the defaults::

    $ docker run -ti -e MAX_CPU_CORES=4 -e STRESS_SYSTEM_FOR=30s petarmaric/cpu_stress_test
