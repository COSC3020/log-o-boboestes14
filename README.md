[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12390548&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

To start off we can f(n) with $ (\log_{2} n) $ and $ (\log_{5} n) $ to get the two equations

$1.) T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot (\log_{2} n) \forall n \geq n_0$

$2.) T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot (\log_{5} n) \forall n \geq n_0$

Now we have to use a logarithm rule that states $ \log_{b} a = \frac{\log_{n} a}{\log_{n} b} $

Using this we can change the equations above to look like this

$1.) T(n) \leq c \cdot (\frac{1}{\log_{5} 2})(\log_{5} n)$

$2.) T(n) \leq c \cdot (\frac{1}{\log_{2} 5})(\log_{2} n)$

Now we can just say that c times $ \frac{1}{\log_{5} 2} $ is a new constant d, 
and that c times $ \frac{1}{\log_{2} 5} $ is a new constant d as well, since the constants in both
can be whatever and not effect eachother. 

$1.) T(n) \leq d \cdot (\log_{5} n)$

$2.) T(n) \leq d \cdot (\log_{2} n)$

This leads to the equations becoming the same as the other one. Meaning that 

$1.) T(n) \in O(\log_{5} n)$

$2.) T(n) \in O(\log_{3} n)$

Therefore logarithms with different bases don't affect the asymptotic complexity of an algorithm.