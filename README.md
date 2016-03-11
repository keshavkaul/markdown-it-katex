# markdown-it-katex

Add Math to your Markdown

[KaTeX](https://github.com/Khan/KaTeX) is a faster alternative to MathJax. This plugin makes it easy to support in your markdown.

Need convincing?

* Check out the comparative benchmark: [KaTeX vs MathJax](https://jsperf.com/katex-vs-mathjax/42)
* Try it in your browser: [markdown-it-katex demo](http://waylonflinn.github.io/markdown-it-katex/)

## Usage
Install markdown-it
```
npm install markdown-it
```

Install the plugin

```
npm install markdown-it-katex
```

Include it in your javascript

```javascript
var md = require('markdown-it')(),
    mk = require('markdown-it-katex');

md.use(mk);

// double backslash is required for javascript strings, but not html input
var result = md.render('# Math Rulez! \n  $\\sqrt{3x-1}+(1+x)^2$');
```

Include the KaTeX stylesheet in your html:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.5.1/katex.min.css">
```

If you're using the default markdown-it parser, I also recommend the github stylesheet:
https://github.com/sindresorhus/github-markdown-css

## Examples

### Inline
Surround your LaTeX with a single `$` on each side for inline rendering.
```
$\sqrt{3x-1}+(1+x)^2$
```

### Block
Use two (`$$`) for block rendering. This mode uses bigger symbols and centers
the result.

```
$$\begin{array}{c}

\nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} &
= \frac{4\pi}{c}\vec{\mathbf{j}}    \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\

\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\

\nabla \cdot \vec{\mathbf{B}} & = 0

\end{array}$$
```

## Math Syntax Support

KaTeX is based on TeX and LaTeX. Support for both is growing. Here's a list of
currently supported functions:

[Function Support in KaTeX](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX)
