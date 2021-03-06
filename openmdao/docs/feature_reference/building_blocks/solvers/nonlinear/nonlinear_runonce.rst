.. _nlrunonce:

****************
NonLinearRunOnce
****************

The simplest solver in OpenMDAO is the NonLinearRunOnce solver, which executes the
system's components or subsystems sequentially. No iteration is performed by
this solver, so it can only be used in systems where the following conditions
are satisfied:

1. System does not contain a cycle, though subsystems may.
2. System does not contain any implicit states, though subsystems may.

Note that a subsystem may contain cycles or implicit states provided that it is
fitted with a solver that can handle them such as :ref:`NewtonSolver <openmdao.solvers.nonlinear.newton.py>`.

Here is an example of using an NonLinearRunOnce solver for a simple model with the <Paraboloid> component.

.. embed-test::
    openmdao.solvers.nonlinear.tests.test_nonlinear_runonce.TestNonLinearRunOnceSolver.test_feature_solver

NonLinearRunOnce Options
------------------------

.. embed-options::
    openmdao.solvers.nonlinear.nonlinear_runonce
    NonLinearRunOnce
    options

.. tags:: Solver, NonlinearSolver
