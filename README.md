# Asymptotic Equivalences
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

I overheard gage my classmate talking about using change of base. I am not sure if I will use it in this but it seems like it could be useful.

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$g(n) \in O(f(n)) \iff \exists c, n_0: g(n) \leq c \cdot f(n) \forall n \geq n_0$

Lets use the arbitrary function $log_a(n)$  and $log_b(n)$ for all constants $a$  and $b$ such that $a > b$,

We must prove that $O(log_a(n)) = O(log_b(n))$

Using change of base:

$log_a(n) = log_a(n)/{log_a(b)}$

Using the big O definition, $g(n) \leq c \cdot f(n)$, we can set $c = 1/{log_a(b)}$  , $g(n) = log_a(n)$  and $f(n) = log_b(n)$  to show:

$g(n) \leq c * f(n)$

This fulfills the definition of big O and therefor proves that a difference in logarithmic base does not affect the asymptotic complexity of an algorithm.
To show now that $O(\log_{2} n)$ is the same as $O(\log_{5} n)$, we must simply choose our a and b values.

Let $a = 2$  and $b = 5$, using change of bases:

$log_2(n) = log_2(n)/{log_2(5)}$

Letting $c = 1/{log_2(5)}$, we now know that $O(log_2(n)) = O(log_5(n))$, using the definition of $O$
