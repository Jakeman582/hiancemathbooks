+++
title = 'Subsets and Supersets'
date = 2024-08-25T15:15:25Z
draft = false
weight = 2
+++

Sets can contain wide varieties of objects. They can contain objects that most people interact with on a daily basis. They can consist of automotive parts that can be used to service a 1967 Camaro, tools used to carve statues out of wood, or art supplies needed to paint a picture. Likewise, they can contain a wide variety of mathematical objects like numbers, shapes, or axioms.

Sometimes, we may only care about some of the objects in a set. For example, we may only be interested in automotive parts needed to service a car’s head lights, or we may only be interested in art supplies needed for a fresco painting. Regardless, we are able to build a lot of structure by simply constructing new sets from old ones by simply restricting what elements are included in the new set.

On the other hand, a set may not contain all of the elements we want. Here, we explore such relationships between these kinds of sets.

## Starting with a Base Set

If we are interested in selecting only some of the elements from a set, we’ll need to know what the original, or underlying, set contains. The idea is exactly the same from Section 7 of Chapter 1. There, we defined what the *Universe of Discourse* is. Using our new terminology, we recognize that for an open proposition, a *Universe of Discourse* (or simply *Universe*) is the set of all values we allow to be substituted in for the variables of a propositional function.

It’s the exact same situation here. We even commonly use the same script letter 𝒰 to denote the base set, though we can still use any symbol we want.

{{% notice color="green" icon="book" title="Example 3.2.1" %}}
Suppose we were presented with the set 
{{< math >}}$$X = \\{x\ |\ 1 \leq x \leq 10\\}$${{< /math >}}

Is {{< math >}}$1.5 \in X${{< /math >}}?

Without knowing the kinds of numbers being used to construct X, it's hard to answer the question. Does X include all the real numbers from 1 to 10 inclusive? Does X only consist of the whole numbers from 1 to 10 inclusive?

Let's remedy this situation by stating that X is only going to contain elements from the set 𝒰 of all integers. Knowing this allows us to conclude that 
{{< math >}}$$X = \\{1,\ 2,\ 3,\ 4,\ 5,\ 6,\ 7,\ 8,\ 9,\ 10\\}$${{< /math >}}

Furthermore, because we now know that X only contains integers, we can write 

{{< math >}}$$X = \\{x\ |\ 1 \leq x \leq 10\\}$${{< /math >}}

without any ambiguity. We could also write something like 

{{< math >}}$$X = \\{x\ \in\ \mathcal{U}\ |\ 1 \leq x \leq 10\\}$${{< /math >}}

or even something like 
{{< math >}}$$X = \\{x\ |\ 1 \leq x \leq 10\ \land\ x\ \in\ \mathcal{U}\\}$${{< /math >}}

Because we've established some base set, or *universe* set, all these different ways of describing a set yield the exact same set X of integers between 1 and 10 inclusive.

As such, since we know that X only consists of integers, we can definiteivly say that {{< math >}}$1.5 \notin X${{< /math >}}.
{{% /notice %}}

{{% notice color="green" icon="book" title="Example 3.2.2" %}}
Consider the universal set 
{{< math >}}$$\mathcal{U} = \\{x\ |\ x \text{ is an even integer}\\}$${{< /math >}}

In this case, since the allowable elements are the even integers, we have that 

```math{}
\begin{align*}
    X &= \{ x\ \in\ \mathcal{U}\ |\ 1\ \leq\ x\ \leq\ 10 \}\\
    &= \{ 2,\ 4,\ 6,\ 8,\ 10 \}
\end{align*}
```

If however we were dealing with the universe $\mathcal{V}$ of all the perfect squares, we would instead have that 

```math{}
\begin{align*}
    X &= \{ x\ \in\ \mathcal{V}\ |\ 1\ \leq\ x\ \leq\ 10 \}\\
    &= \{ 1,\ 4,\ 9 \}
\end{align*}
```

But because we are now dealing with two separate universal sets, just saying $X = \\{x\ |\ 1\ \leq\ x\ \leq\ 10\\}$ is not enough. We would have to explicitly state which universe is being used, as we did above.
{{% /notice %}}

## Subsets

Starting with a universal set $\mathcal{U}$, we construct a new set A by only taking elements from that universal set. We could go even farther by constructing another set B using only elements from A.

{{% notice color="blue" icon="pen" title="Subset" %}}
Consider two sets A and B.

A is called a **subset** of B, and we write 

$$A \subseteq B$$

if (and only if) every element of A is also an element of B.

Logically, we would write 

$$\forall x\ [x \in A \implies x \in B]$$

If A is not a subset of B, we can write 

$$A \nsubseteq B$$
{{% /notice %}}

Let's examine the logical implication 
$$x \in A \implies x \in B$$
a little more closely, which states that the proposition 
$$x \in A \longrightarrow x \in B$$
is always a true proposition. We start by constructing a truth table:

|$x \in A$|$x \in B$|$x \in A \rightarrow x \in B$|
|:-:|:-:|:-:|
|0|0|1|
|0|1|1|
|1|0|0|
|1|1|1|

Notice that the only row in which the proposition $x \in A \rightarrow x \in B$ is false is in the third row where we have 
\\[
\begin{align*}
    x \in A &= 1 \\\\
    x \in B &= 0
\end{align*}    
\\]
This means that even if there is exactly one element that is in A, but not in B, then A is not a subset of B.

{{% notice color="green" icon="book" title="Example 3.2.3" %}}
Consider the universal set 𝒰 consisting of all the positive integers 

$$\mathcal{U} = \\{1,\ 2,\ 3,\ 4,\ \ldots\\}$$

along with the following two sets 

\\[
\begin{align*}
    X &= \\{x\ |\ x^2\ \leq\ 100\\}\\\\
    &= \\{1,\ 2,\ 3,\ 4,\ 5,\ 6,\ 7,\ 8,\ 9,\ 10\\}\\\\
    \\\\
    Y &= \\{y\ |\ y^2\ \leq\ 37\\}\\\\
    &= \\{1,\ 2,\ 3,\ 4,\ 5,\ 6\\}\\\\
\end{align*}    
\\]

In order to verify that $Y \subseteq X$, we need to verify that the proposition

$$\forall n\ [n \in Y \longrightarrow n \in X] = 1$$

First, we recognize that if n is not in $\mathcal{U}$, then we would have that $n \notin Y$, which is another way of saying $n \in Y = 0$. This tells us that 

\\[
\begin{align*}
    \(n \in Y \rightarrow\ n \in X\ \) &=\ \( 0 \rightarrow\ n \in X\)\\\\
    &=\ 1
\end{align*}    
\\]

Thus, we don't have to bother checking numbers that are not in Y, we can just check numbers that are in Y, so let's check each of the six numbers that are in Y:

|$n$|$n \in Y$|$n \in X$|$n \in Y \rightarrow n \in X$|
|:-:|:-:|:-:|:-:|
|1|1|1|1|
|2|1|1|1|
|3|1|1|1|
|4|1|1|1|
|5|1|1|1|
|6|1|1|1|

The column representing the proposition $n \in Y \rightarrow n \in X$ has all 1s. Hence that proposition is a tautology, meaning it's a logical implication and we can indeed write 

$$n \in Y \implies n \in X$$

Thus, we have shown that Y is a subset of X and we can write 

$$Y \subseteq X$$

It's also worth point out that $Y \subseteq \mathcal{U}$ and $X \subseteq \mathcal{U}$ as well.
{{% /notice %}}

{{% notice color="green" icon="book" title="Example 3.2.4" %}}
Reconsider all of the sets from Example 3.2.3. Suppose we wanted to know whether or not $X \subseteq Y$. In order to determine if that was the case, we would need to show that every element in X was also in Y, or in other words that 

$$\forall n\ [n \in X \implies n \in Y]$$

As discussed in Example 3.2.3, we don't need to consider any elements not in X, so we could just make another table: 

|$n$|$n \in X$|$n \in Y$|$n \in X \rightarrow n \in Y$|
|:-:|:-:|:-:|:-:|
|1|1|1|1|
|2|1|1|1|
|3|1|1|1|
|4|1|1|1|
|5|1|1|1|
|6|1|1|1|
|7|1|0|0|
|8|1|0|0|
|9|1|0|0|
|10|1|0|0|

As we can see, there are values in X that are not in Y, such as 8. Thus we conclude that 

$$X \nsubseteq Y$$

Of course, we don't need to construct a table everytime if there is an obvious value that demonstrates one set is not another subset of another. The existence of that one value is justification enough.

{{% /notice %}}

## The Empty Set

Just because we can put anything in a set does not mean we need to add anything to the set at all. There is a special term used to describe such a set.

{{% notice color="blue" icon="pen" title="Empty Set, Null Set" %}}
The **empty set** is the unique set containg no elements at all, and is often depicted by $\emptyset$.

The empty set is sometimes referred to as the **null set**.
{{% /notice %}}

There are a couple of thigs worth pointing out. Note that because the empty set contains no elements in it, we see that 

$$|\emptyset| = 0$$

but one common mistake is to equate the empty set with {0}, which is false since {0} is a set containing an element, namely the number 0. As such we have that 

$$\emptyset \neq \\{0\\}$$

Instead, since the empty set contains no elements, we could just write two curly brackets without anything in between like so: 

$$\emptyset = \\{\\}$$

For similar reasons we have that 

$$\emptyset \neq \\{\emptyset\\}$$

because $\\{\emptyset\\}$ is a set containing en element, namely the empty set itself.

## The Empty Set is Always a Subset

We examined the logic behind the logical implication 

$$n \in A \implies n \in B$$

We use that definition, along with the definition of empty set in our next theorem.

{{% notice color="blueviolet" icon="star" title="Theorem 3.2.1" %}}
For any universe $\mathcal{U}$, let A be any set such that $A \subseteq \mathcal{U}$, then we have that 

$$\emptyset \subseteq A$$

{{% /notice %}}

---

{{% expand title="Proof 3.2.1" %}}
*General Strategy: Because $\emptyset$ doesn't contain any elements, the proposition $x \in \emptyset$ is always false for any element x taken from $\mathcal{U}$. Thus, when $x \in \emptyset$ is the hypothesis of any proposition, that proposition will always be trivially true.*

Let x be any arbitrarily picked element from $\mathcal{U}$.

Because $\emptyset$ contains no elements, it is impossible for $x \in \emptyset$, thus it is always true that 

$$(x \in \emptyset) = 0$$

Now, because the proposition $x \in \emptyset$ is always false, we have that 

\\[
\begin{align*}
    x \in \emptyset \rightarrow x \in A\ &=\ 0 \rightarrow x \in A\\\\
    &=\ 1
\end{align*}
\\]

Notice that it does not matter whether or not $x \in A$ because the hypothesis $x \in \emptyset$ is always false, meaning the overall implication is always (trivially) true. Thus, because the implication is always true, we have that 

$$x \in \emptyset \implies x \in A$$

We therefore have that 

$$\emptyset \subseteq A$$

as desired.

{{% /expand %}}

---

Notice that in Theorem 3.2.1 that there were no special requirements that set A had to satisfy, it just had to be some subset of the universal set $\mathcal{U}$. Then by the Rule of Universal Generalization, since A was an arbitrary set, and we have that $\emptyset \subseteq A$, then $\emptyset$ must be a subset of every possible set, even including the empty set itself and $\mathcal{U}$.

## Every Set is a Subset of Itself

Consider the proposition 

$$x \in A \longrightarrow x \in A$$

The same proposition $x \in A$ is on both sides of the implication, meaning that there are only two scenarios to consider:

$$0 \longrightarrow 0$$
$$1 \longrightarrow 1$$

Either way, the proposition always evaluates to true. Let's formalize this observation with a theorem.

{{% notice color="blueviolet" icon="star" title="Theorem 3.2.2" %}}
For any universal set $\mathcal{U}$, and set $A \subseteq \mathcal{U}$, we have that 

$$A \subseteq A$$
{{% /notice %}}

---

{{% expand title="Proof 3.2.2" %}}
*General Strategy: This is basically true by definition of subset. Since A contains all of the elements from A (tautologically true), we'll have that the proposition $x \in A \rightarrow x \in A$ will always be true.*

Consider some arbitrary element x from $\mathcal{U}$.

If it were the case that $x \notin A$, then we would have that 

\\[
\begin{align*}
    x \in A \rightarrow x \in A\ &=\ 0 \rightarrow 0\\\\
    &=\ 1
\end{align*}
\\]

Similarly, if it were the case that $x \in A$, then we would have that 

\\[
\begin{align*}
    x \in A \rightarrow x \in A\ &=\ 1 \rightarrow 1\\\\
    &=\ 1
\end{align*}
\\]

Either way, the proposition is always true, meaning we have that 

$$x \in A \implies x \in A$$

and so we have by definition that 

$$A \subseteq A$$

as desired.
{{% /expand %}}

---

## Proper Subsets

When we assert that $A \subseteq B$, all we're saying is that whenever x is in A, it also happens to b in B. However, this definition does not say whether or not every single element within B also has to be within A. We have a special term to describe the scenario when A is a subset of B, but B has elements that are not in A.

{{% notice color="blue" icon="pen" title="Proper Subset" %}}
Consider two sets A and B.

A is said to be a **proper subset** of B if (and only if) every element in A is also in B, but B has at least one element that is not in A. We denote this by writing 

$$A \subset B$$

Logically, we would write this as 

$$(\forall a \in A\ [a \in B])\ \land\ (\exists b \in B\ [b \notin A])$$

If A is not a proper subset of B, we can write 

$$A \not\subset B$$
{{% /notice %}}

{{% notice color="green" icon="book" title="Example 3.2.5" %}}
Consider the following two sets:

$$M = \\{x\ |\ x \text{ is an odd integer}\\}$$
$$N = \\{x\ |\ x \text{ is an integer}\\}$$

Every odd integer is an integer, that would mean that every element within M would also be in N as well, and so we could write 

$$M \subseteq N$$

However, notice that $0 \in N$ but that $0 \notin M$, meaning N has at least one element that isn't in M.

Thus, because M is a subset of N, and N has atleast one element not in M, we can write 

$$M \subset N$$
{{% /notice %}}

By Example 3.2.5, we see that for any two sets A and B, it is possible to have both 

$$A \subseteq B$$
$$A \subset B$$

{{% notice color="green" icon="book" title="Example 3.2.6" %}}
Consider the following two sets: 

$$\Psi = \\{a,\ b,\ c,\ 1,\ 2,\ 3,\ x,\ y,\ z,\ \\{1,\ 2,\ 3\\}\\}$$
$$\Omega = \\{b,\ 1,\ z,\ \\{1,\ 2,\ 3\\}\\}$$

By Theorem 3.2.2, we clearly have that $\Psi \subseteq \Psi$ and $\Omega \subseteq \Omega$. However, we can't say that $\Psi \subset \Psi$, nor can we say that $\Omega \subset \Omega$  because it's impossible for a set to contain an element it doesn't contain (that would be a contradiction).

We can see that every element within $\Omega$ is also an element of $\Psi$.

|n|$n \in \Psi$|
|:-:|:-:|
|b|1|
|1|1|
|z|1|
|{1, 2, 3}|1|

Thus, we have verified that $\Omega \subseteq \Psi$.

Notice though that there is at least one element in $\Psi$ that is not in $\Omega$, such as a, meaning we have that $\Omega \subset \Psi$ as well.
{{% /notice %}}

Based on the previous two examples, it seems that whenever $A \subset B$, we also have that $A \subseteq B$ as well.

{{% notice color="blueviolet" icon="star" title="Theorem 3.2.3" %}}
If $A \subset B$, then $A \subseteq B$
{{% /notice %}}

---

{{% expand title="Proof 3.2.3" %}}
*General Strategy: This is basically true by definition, so we just appeal to the definitions of subset and proper subset.*

Since we know that $A \subset B$, we have by definition that for any element a in A, we also have that a is an element of B as well. Thus, we have by definition that $A \subseteq B$ as desired.
{{% /expand %}}

---

Notice that the converse of Theorem 3.2.3 is not true. For example, by Theorem 3.2.2 that for any set A, we have that $A \subseteq A$, but in Example 3.2.6, we demonstrated why A is not a proper subset of itself, and so we have that $A \not\subset A$.

## Supersets

As can be inferred, a superset of a given set is simply a set containing all the same elements of the given set, but possibly with additional elements.

{{% notice color="blue" icon="pen" title="Superset" %}}
Consider two sets A and B.

A is called a **superset** of B, and we write 

$$A \supseteq B$$

if (and only if) every element of B is an element of A.

Logically, we would write 

$$\forall x\ [x \in B \implies x \in A]$$
{{% /notice %}}

There is an analogous definition for *proper superset* as well.

Of course, whenever we find that $A \supseteq B$, that is the same thing as saying that $B \subseteq A$. In other words, we find that B is a subset of A, while A is a superset of B. Really, subsets and supersets go hand-in-hand.