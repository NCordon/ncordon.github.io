---
layout: page
title: "LaTeX in Telegram Desktop"
date: 2016-10-15
categories: latex telegram maths
---

Yesterday [@M42](https://github.com/m42), a good friend of mine told me there was a partial solution to render $$\LaTeX$$ equations in Telegram Desktop, [ChatJax](http://www.math.ucla.edu/~robjohn/math/mathjax.html), a code line that inserts a `<script>` html tag in the current page's `<head>`, allowing sent $$\LaTeX$$ code in a Telegram Desktop Window to render. This could be saved as a handy boomark and be executed every time we'd like to render sent equations.

However, this had a big problem, appart from the obvious necessity of clicking the boomark every time we'd like to use it. If we started to use it in an open conversation, it would render the sent equations properly, but from now on, it would also try to render all non sent equations, producing a (curious) unwanted result.

![Unsent message](/images/2016-10-15-latex-in-telegram-unsent.png){: .center}

Unsent $$\LaTeX$$ already rendered

![Sent message](/images/2016-10-15-latex-in-telegram-sent.png){: .center}

Sent $$\LaTeX$$ as a rare encoding

So I started finding a solution, and after one hour of trying to make this code work automatically (with `GreaseMonkey`), once started the browser, and realizing that I have to target only a part of the Telegram Desktop Window to be rendered, I arrived to an useful [MathJax Documentation](http://docs.mathjax.org/en/latest/advanced/typeset.html?highlight=queue) about doing so with `MathJax.Hub.Queue` and it worked out!.

I've written a public `gist` [here](https://gist.github.com/NCordon/090a6c208e61a1059357d6e8fba03087) with the an `user.js GreaseMonkey` extension to render equations properly in Telegram Desktop. I've only given it a try in `Firefox`, and it works well!.

![Sent message](/images/2016-10-15-latex-in-telegram-final-result.png)

To download it, `GreaseMonkey` extension must be installed in the current browser, and it suffices to click `Raw` from the `gist` page, and it will pop up a confirmation to install it as an user script. To write inline $$\LaTeX$$, use a simple `$`. To write centered $$\LaTeX$$, use `$$`.

The script is also available from `GreasyFork` [here](https://greasyfork.org/en/scripts/24067-tex-for-telegram).
