C++ Basics
===================



Make it Work
-------------------

Apart from the tranditional way of running C++ code, Jupyter notebook has a clingkernel that make it possibel to run C++ in a Jupyter notebook. Here is the post: `Interactive C++ for HPC <http://johntfoster.github.io/posts/interactive-c%2B%2B-for-hpc.html>`_.


Concepts
-----------------

1. Namespace
2. Operators: assignment operators (=,+=,-=,*=,/=,%=), increment/decrement operator (++x,x++,--x,x--), relational operators (>,<,>=,<=,==,!=), left shift (<<), extration operator (>>, or right shift), understand the operator precedence
3. Variables: variable name starts with underscore or latin letters
5. if/else and Loops: if (condition is true ){ then something }
6. Class: private, public, atrributes, method, constructor, destructor, polymorphism


Clarifications
~~~~~~~~~~~~~~~~~~~~~~~~

Increment/decrement operator has a very high precedence if applied from the left.

.. code-block:: c++

   x = 2;
   y = ++x;
   // prefix: x=3, y=3; ++ is calculated first then assigned to y;

   a = 3;
   b = a++;
   // postfix: a = 4, b= 3; ++ is calculated after the asignment


Omitted curly braces in if/else statement works if it has only one statement. If you like Python, this is an excellent practice.

.. code-block:: c++

   #include <iostream>
   using namespace std;

   int main() {
      int i = 2, j=3;

      if (i > j)
         cout << "i>j";
      else
         cout << "j<=i";

      return 0;
   }


default statement for swtich must be at the end of the statements of switch.


.. code-block:: c++

   int age = 18;
   switch (age) {
     case 1:
       cout << "Baby";
       break;
     case 6:
       cout << "Boy";
       break;
     default:
       cout << "Oh yeah?";
   }
