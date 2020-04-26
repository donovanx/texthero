<p align="center">
   <a href="https://github.com/jbesomi/texthero/stargazers">
    <img src="https://img.shields.io/github/stars/jbesomi/texthero.svg?colorA=orange&colorB=orange&logo=github"
         alt="Github stars">
   </a>
   <a href="https://pypi.org/search/?q=texthero">
      <img src="https://img.shields.io/pypi/v/texthero.svg?colorB=brightgreen"
           alt="pip package">
   </a>
   <a href="https://pypi.org/project/texthero/">
      <img alt="pip downloads" src="https://img.shields.io/pypi/dm/texthero">
   </a>
   <a href="https://github.com/jbesomi/texthero/issues">
        <img src="https://img.shields.io/github/issues/jbesomi/texthero.svg"
             alt="Github issues">
   </a>
   <a href="https://github.com/jbesomi/texthero/blob/master/LICENSE">
        <img src="https://img.shields.io/github/license/jbesomi/texthero.svg"
             alt="Github license">
   </a>   
</p>

<p align="center">
    <img src=".github/logo_v2.png">
</p>

<p align="center">Text preprocessing, representation and visualization from zero to hero</p>

<p align="center">
    <img src=".github/demo.gif?raw=true" width="700">
</p>

<p align="center">
  <a href="#zero-to-hero">From zero to hero</a> •
  <a href="#installation">Installation</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#documentation">Documentation</a> •
  <a href="#contributions">Contributions</a>
</p>


<h2 align="center">From zero to hero</h2>

Texthero is a python toolkit for quick handling of text data. Texthero is concise, simple to learn and integrates smoothly with Pandas.

Given a Pandas DataFrame with one or more _text_ columns, texthero help to preprocess the text data, map it into vectors using different algorithms and models and visualize it on screen.

You can think of texthero as an utility tool to quickly _understand_ text-based dataset. Given a tabular dataset such as stock predictions or most selled items, it's easy to _grasp the main insights_, but given a text dataset, it's harder to quickly have an understanding of the underline data. That's when texthero jump in and help you quickly achieve what you wants: work with text data quickly and effortlessly.

To start using texthero, you don't have to spend hours understanding complex and messy code. To keep thing simple, Texthero is composed of only three python modules containing each helper functions *preprocessing.py*, *representation.py*, *visualization.py*.

<h2 align="center">Installation</h2>

```bash
pip install texthero
```

> ☝️Under the hoods, texthero make use of multiple NLP/mL toolkit such as Gensim, NLTK, SpaCy and Sklearn. You don't need to install them separately; pip will take care of that.

<h2 align="center">Getting started</h2>

The best way to quickly and efficiently learn Texthero is through the <a href="">Getting started</a> official documentation.

<h2 align="center">Example</h2>

...

```python
import texthero.texthero as hero
import pandas as pd

df = pd.DataFrame(["hello world", "hello", "world"], columns='text')
df = hero.do_preprocess(df)
df = hero.do_tfidf(df)
df = hero.do_pca(df)
hero.scatterplot(df)
```

(The same example can also be found as a "getting-started guide" here: ...)

<h2 align="center">API</h2>

All Texthero code is well-documented and therefore should be easy to understand and work.

If you are a superuser oh python, then all you need is to call `help(hero)`, otherwise keep reading.

Texthero is composed of only three modules: [preprocessing.py](/texthero/preprocessing.py), [representation.py](/texthero/representation.py) and [visualization.py])(/texthero/visualization.py).

<h3>⚒️ 1. Preprocessing</h3>

**Scope:** prepare the **text** data for further analysis.

Complete documentation: [preprocessing](https://jbesomi.github.io/texthero/preprocessing.html)

<h3>📒 2. Representation</h3>

**Job:** map text data into vectors and do dimensionality reduction.

Supported representation algorithms:
1. Term frequency, inverse document frequency (`do_tfidf`)
3. Word2Vec from Gensim [🔜]
4. GloVe [🔜]
5. Transformers [🔜]

Supported dimensionality reduction algorithms:
1. Principal component analysis (`do_pca`)
2. Non-negative matrix factorization (`do_nmf`)

Complete documentation: [representation](https://jbesomi.github.io/texthero/representation.html)

<h3>🔮 3. Visualization</h3>

**Job:** collection of functions to both summarize the main facts regarding the data and visualize the results. This part is very opinionated and ideal for anyone that needs a quick solution to visualize on screen the text data for instance during a text exploratory data analysis (EDA).

Most common functions:
   - Text scatterplot. Handy when coupled with dimensionality reduction algorithms such as pca.
   - Most common words
   - Most common words between two entities [🔜]

Complete documentation: [visualization](https://jbesomi.github.io/texthero/visualization.html)

<h2 align="center">Contributions</h2>

Any help, feedback and contribution are very welcome. You can simply fork this repository and [open an issue](https://github.com/jbesomi/texthero/issues).
