# Asymptotic Equivalences
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

I overheard gage my classmate talking about using change of base. I ended up talking to gage and learning and understanding
what his proof means and how it works. I benefitted from talking to him because I now understand the proof a lot better.

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$g(n) \in O(f(n)) \iff \exists c, n_0: g(n) \leq c \cdot f(n) \forall n \geq n_0$

To prove that $O(\log_{2} n)$  is the same as $O(\log_{5} n)$, we must show that $f(n) \in O(\log_{2} n)$
and that $f(n) \in O(\log_{5} n)$.

Let $f(n) \in O(\log_2 n)$. Using the definition of Big O, this means there is a constant c such that $f(n) \leq c \log_2 n$.
Using change of base: $\log_2 n = {\log_5 n}/{\log_5 2}$, we can substitute to get, $f(n) \leq c {\log_5 n}/{\log_5 2}$. Since
c is defined as any constant $c \g 0$, we can take $c = c/{\log_5 2}$. Thus, $f(n) \leq c {\log_5 n}$  proving $f(n) \in O(\log_2 n)$.

Again, let $f(n) \in O(\log_5 n)$. Using the definition of Big O, this means there is a constant c such that $f(n) \leq c \log_5 n$.
Using change of base: $\log_5 n = {\log_2 n}/{\log_2 5}$, we can substitute to get, $f(n) \leq c {\log_2 n}/{\log_2 5}$. Since
c is defined as any constant $c \g 0$, we can take $c = c/{\log_2 5}$. Thus, $f(n) \leq c {\log_2 n}$  proving $f(n) \in O(\log_5 n)$.

This proves that $O(\log_2 n) = O(\log_5 n)$ because they are both an element of each other. Therefor they are asymtotically equivalent.


