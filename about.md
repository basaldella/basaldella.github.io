---
layout: page
title: About
permalink: about.html
---

# License
All material in this website is licensed under the <a href="https://creativecommons.org/licenses/by-nc/3.0/">CC-BY-NC 3.0 license</a> unless explicitly stated otherwise.

# Third-party software

This website is built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub pages](https://pages.github.com/). I wrote a custom theme for Jekyll using [Twitter Bootstrap](https://getbootstrap.com). The fonts I used are [Nunito](https://fonts.google.com/specimen/Nunito) font the sans-serif headings and [Cardo](https://fonts.google.com/specimen/Cardo) for the content; both fonts are provided by Google fonts. The syntax highlighter theme is a slightly modified version of [Pygments' pastie theme](http://pygments.org/) to make inline code look similar to fenced code. Finally, maths is rendered using [MathJax](https://www.mathjax.org/).

# Frequently asked questions

## How do you enable syntax highlighting in Jekyll?

To enable syntax highlighting in Jekyll, just add these lines to your ```_config.yaml```:

```ruby
markdown: kramdown
highlighter: rouge

kramdown:
  input: GFM
  syntax_highlighter: rouge
```

Now you can choose a style and call it from your web page. In my case, I used a style from Pygments and I put its ```.css``` file in the ```assets``` folder of my Jekyll installation.

## How did you integrate MathJax in your website?

MathJax offers support for inline formulae (like \\(\sin(x^{2y}) \\)) or centered equations like this:

$$a^2 + b^2 = c^2$$

To enable MathJax in Jekyll, you just have to call it from your HTML's page header:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
```

And then you can write 
* inline formulae like this: ``` \\( your LaTeX code here \\)``` 
* centered equations like this: ```$$ your LaTeX code here $$```.