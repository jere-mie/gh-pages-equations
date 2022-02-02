# gh-pages-equations

Instructions on how to get latex equations to render on GitHub pages

## Set up

Basically, all you need to do is create a `_includes/head-custom.html` file with the following text:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.15.2/dist/katex.min.css" integrity="sha384-MlJdn/WNKDGXveldHDdyRP1R4CTHr3FeuDNfhsLPYrq2t0UBkUdK2jyTnXPEK1NQ" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.2/dist/katex.min.js" integrity="sha384-VQ8d8WVFw0yHhCk5E8I86oOhv48xLpnDZx5T9GogA/Y84DcCKWXDmSDfn13bzFZY" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.2/dist/contrib/auto-render.min.js" integrity="sha384-+XBljXPPiv+OzfbB3cVmLHf4hdUFHlWNZN5spNQ7rmHTXpd7WvJum6fIACpNNfIR" crossorigin="anonymous"></script>
<script>
    document.addEventListener("DOMContentLoaded", function() {
        renderMathInElement(document.body, {
            // customised options
            // • auto-render specific keys, e.g.:
            delimiters: [
                {left: '$$', right: '$$', display: true},
                {left: '$', right: '$', display: false},
                {left: '\\(', right: '\\)', display: false},
                {left: '\\[', right: '\\]', display: true}
            ],
            // • rendering keys, e.g.:
            throwOnError : false
        });
    });
</script>
```

## Rendering Latex Equations

Latex quations are rendered by putting them in between \$ symbols.  
For example, `$\int_a^b{x^2}$` renders to $\int_a^b{x^2}$  

### Is the above equation not rendering for you?

Congratulations! You've found one of the quirks with this solution. Equations will only render on **GitHub Pages**, not on the actual GitHub website. If you only care about GitHub pages anyways (like me) this shouldn't be a big deal. However, if you were hoping to get it to work on the GitHub website, this won't work for you.  
Want to see what it looks like rendered anyway? Go to the GitHub pages version of this site [here](https://jere-mie.github.io/gh-pages-equations/)