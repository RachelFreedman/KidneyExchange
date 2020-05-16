Kidney Exchange
==============

Kidney failure is a life-threatening health issue that affects hundreds of thousands of people worldwide. In the US alone, the waitlist for a kidney transplant has over 100,000 patients. This list is growing: demand far outstrips supply.

A recent innovation, kidney exchange, allows patients to bring an (incompatible) donor to a large pool where they can swap donors with other patients.  As of 2012&ndash;2013, roughly 10% of US kidney transplants occurred through a variety of kidney exchanges.  Outside of the US, many countries (the UK, the Netherlands, Portugal, Israel, ...) are fielding exchanges.

This Codebase
==============

This codebase includes: structural elements of kidney exchange like "pools", "hospitals", and "pairs", a couple of kidney exchange graph generators, a couple of kidney exchange solvers (max weight, failure-aware, fairness-aware, individually rational, ethical, variational), and a dynamic kidney exchange simulator.

If you use the core structural codebase, please cite one of Dr. John Dickerson's recent papers like:

John P. Dickerson, Ariel D. Procaccia, and Tuomas Sandholm. 2014. "Price of Fairness in Kidney Exchange." In _Proceedings of the 2014 International Conference on Autonomous Agents and Multi-agent Systems_ (AAMAS-2014).  Paris, France (pp. 1013&ndash;1020). 

If you use the ``Ethics`` or ``Variation`` packages, please cite:

Rachel Freedman, Jana Schaich Borg, Walter Sinnott-Armstrong, John P. Dickerson, Vincent Conitzer. 2020. "Adapting a kidney exchange algorithm to align with human values." In _Artificial Intelligence_ (2020): 103261.


**NOTE:** This is _not_ the code used in the UNOS [Kidney Paired Donation Pilot Program](http://optn.transplant.hrsa.gov/resources/KPDPP.asp "Kidney Paired Donation Pilot Program information via OPTN") (KPDPP).  The solvers here are meant to be accessible research code for the community and do not use branch-and-price, hopefully resulting in greater ease of use (at the cost of scalability).  Forks and pull requests welcome!


External Dependencies
=====================

To use any of the solvers that inherit from `CPLEXSolver`, you will need to add [cplex.jar](http://www-01.ibm.com/software/commerce/optimization/cplex-optimizer/) to `lib/`.  This will allow compilation; to run, you'll also need a VM argument like

   `-Djava.library.path=/path/to/CPLEX_Studio/cplex/bin/your-architecture/`

IBM offers a free academic license for CPLEX as well as a 90-day free trial available on their website.