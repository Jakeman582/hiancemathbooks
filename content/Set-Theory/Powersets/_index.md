+++
title = 'Powersets'
date = 2024-08-25T01:26:29Z
draft = false
weight = 5
+++

Often, we find ourselves wanting to pick out certain subsets from a given set. Of course, we can choose to include some items and omit others, yielding a wide variety of possible subsets to choose from. It is common to consider the set of all such possibilities.

## Definition of a Powerset
As stated in the introduction to this section, whenever we want to pick certain subsets of elements from a given set, we commonly collect all possible subsets into one encompassing set.

{{% notice color="blue" icon="pen" title="Powerset" %}}
For any given set A, the **powerset** of A, typically denoted {{< math >}}$\mathcal{P}(A)${{< /math >}}, is the set consisting of all possible subsets of A.

In other words, we have that 
{{< math >}}$$\mathcal{P}(A) = \\{X\ |\ X \subseteq A\\}$${{< /math >}}

{{% /notice %}}

## Examples
It is useful to consider a few small examples, allowing us to get a concrete grasp on how to determine the powerset of a given set.

{{% notice color="green" icon="book" title="Example 3.5.1" %}}
Consider the set A consisting of only one element a, meaning we have that {{< math >}}$A = \\{a\\}${{< /math >}}.

Here, we see there are only two possible subsets: 
{{< math >}}$$\emptyset \text{ and } \\{a\\}$${{< /math >}}

Hence, we would say that 
{{< math >}}$$\mathcal{P}(A) = \\{ \emptyset,\ \\{a\\}\\}$${{< /math >}}
{{% /notice %}}

{{% notice color="green" icon="book" title="Example 3.5.2" %}}
Consider a set B with two elements where {{< math >}}$B = \\{a,\ b\\}${{< /math >}}.

In order to calculate the powerset of B, we must first consider all subsets with zero of the elements from B. Of course, the only such set is the empty set, yielding 

{{< math >}}$$\emptyset$${{< /math >}}

Now we consider all the subsets of B consisting of only one of the elements from B. Since there are two elements in B, we see that there are only two such subsets: 

{{< math >}}$$\\{a\\},\ \\{b\\}$${{< /math >}}

Next, we must consider all subsets of B consisting of exactly two elements. Since B contains exactly two elements itself, there is only one such subset: 

{{< math >}}$$\\{a,\ b\\}$${{< /math >}}

Because B only has two elements, there is no way to form a subset of B consisting of three or more elements. This means we've found all the necessary subsets. As such, we conclude that 
{{< math >}}$$\mathcal{P}(B) = \\{\emptyset,\ \\{a\\},\ \\{b\\},\ \\{a,\ b\\}\\}$${{< /math >}}

{{% /notice %}}

From Example 3.5.2, we see that we can calculate a powerset by simply considering what happens when we take exactly zero elements from the set, then exactly one element from the set, and then exactly two. The process stops once we start taking all of the elements from the set simultaneously because we can't form subsets that are larger than the original set. Naturally, this pattern extends to finite sets with cardinality of three or more.

{{% notice color="green" icon="pen" title="Example 3.5.3" %}}
Consider the set 

{{< math >}}$$C = \\{x,\ y,\ z\\}$${{< /math >}}

We begin by considering what happens when choosing exactly zero of the elements from C, which of course yields the empty set: 

{{< math >}}$$\emptyset$${{< /math >}}

Next, we consider what happens when we take exactly one of the elements from C. Since there are three elements in C, there are three such subsets: 

{{< math >}}$$\\{x\\},\ \\{y\\},\ \\{z\\}$${{< /math >}}

Next, we take consider taking exactly two elements from C: 

{{< math >}}$$\\{x,\ y\\},\ \\{x,\ z\\},\ \\{y,\ z\\}$${{< /math >}}

Finally, we consider what happens when taking all three elements together in a subset: 

{{< math >}}$$\\{x,\ y,\ z\\}$${{< /math >}}

Thus, we conclude that 

{{< math >}}$$\mathcal{P}(C) = \\{\emptyset,\ \\{x\\},\ \\{y\\},\ \\{z\\},\ \\{x,\ y\\},\ \\{x,\ z\\},\ \\{y,\ z\\},\ \\{x,\ y,\ z\\}\\}$${{< /math >}}
{{% /notice %}}

As can be seen by the previous examples, the size of a powerset can grow very quickly, even for finite sets with small cardinalities. As such, powersets are not typically written out as we've done in the examples. Instead, we simply just use the shorthand involving the script P to refer to a powerset.

With that said, we'll finish this section by looking at one more example.

{{% notice color="green" icon="book" title="Example 3.5.4" %}}
Consider the empty set {}. What is it's powerset?

Remember that we always start by considering what happens when we take exactly exactly zero elements. Since {} has zero elements in it, this is valid, and so we see that this simply yields the empty set again: 

{{< math >}}$$\emptyset$${{< /math >}}

However, since there is no way to pick one or more elements from the empty set, we are now done. As such, we conclude that 

{{< math >}}$$\mathcal{P}(\emptyset) = \\{\emptyset\\}$${{< /math >}}
{{% /notice %}}