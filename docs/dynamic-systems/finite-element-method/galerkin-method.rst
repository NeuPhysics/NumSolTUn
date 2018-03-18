Galerkin Method
===================

Suppose we need to find the solution to equation

.. math::
   \mathcal L_{x} \psi(x) = f(x).

The key is that the solution can be approximated by

.. math::
   \psi(x) = \sum_i u_i \phi_i(x),

where :math:`\phi_i(x)` are the basis functions.

**The purpose is to find the the coefficients** :math:`u_i`. Galerkin method has three steps.

1. discretize the space :math:`x` and function space: triangulation,
2. discretize the function using weak form: assembly,
3. error estimation.

Triangulation is basically setting up the basis function in a discretized space :math:`x`. One of the choice is the hat function.

.. figure:: assets/plot-using-linear-combinations.png
   :align: center

   Triangulation from `comsol multiphysics <https://www.comsol.com/multiphysics/finite-element-method>`_.

At each point :math:`x`, there is a hat function responsible for the approximation within :math:`[x-\Delta x, x+\Delta x]`.

Those hat functions forms the basis for the approximated solution

.. math::
   \psi = \sum_i u_i \phi_i.

With this approximation, it requires the *test function* :math:`v` to write down the weak form. Basically we multiply :math:`v` on both sides of the equation then integrate by step. Then the differential equation can be rewrite into matrix form with basis :math:`\phi_i`,

.. math::
   \mathbf K \mathbf U = \mathbf L.

We solve the coefficients :math:`\mathbf U` from the matrix equation.



References and Notes
-----------------------

1. Freitag, K. J. (2007). Neural networks and differential equations.
2. `COMSOL Multiphysics has a nice article <https://www.comsol.com/multiphysics/finite-element-method>`_.
