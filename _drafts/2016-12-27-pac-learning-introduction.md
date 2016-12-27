---
title:  "PAC Learning introduction"
date:   2016-12-27
categories: computer-science artificial-intelligence
---

# Machine learning, introduction
Think in a mechanism to predict wheter a patient may be ill. We could have a database of characteristics of each already examined patient, and by comparison with the current patient we could stablish an hypothesis about the patient's healthiness or sickness. But that way the database should be huge to be representative of all the cases.

Instead, it would be desirable being able to *generalize* all the possible cases from a few of them, since they're infinite for real characteristics. Therefore, our mechanism should use *inductive reasoning*. Here is where Machine Learning concepts arise.

We could think of Machine Learning as a way of solving difficult or tedious *human/animal tasks*, even tasks beyond *human limits*, with a certain adaptativity (that is, solution should be user and time independent).

Although machine learning is profoundly related to field like statistics, there is a main distinction between both of them. Statistics take care of validating hypothesis, wheter Machine Learning takes care of finding suitable hypothesis that maybe a human being could not find at first sight.

# Notations

- Domain: $\mathcal{X}$
- Label set: $\mathcal{Y} = \{0,1\}$. This limit us to binary paradigm.
- Training set: $S=((x_1,y_1), \ldots (x_m, y_m))$ sequence of pairs in $\mathcal{X} \times \mathcal{Y}$
- Predictor/hypothesis/classifier: learner's output shaped as a function $h:\mathcal{X}\rightarrow \mathcal{Y}$. $A(S)$ denotes the hypothesis that a certain algorithm $A$ would output for a training set $S$.
