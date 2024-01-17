<!-- .slide: data-state="standard" -->
# Code Environments

---

<!-- .slide: data-state="standard" -->
## Environment Definition

So you've got the code file. Now what...?

<ul>
  <li>What language is it written in? <span class="fragment">Python</span></li>
  <li class="fragment">What version of Python? <span class="fragment">🤔</span></li>
  <li class="fragment">What libraries does it use? <span class="fragment">🧐</span></li>
  <ul class="fragment">
    <li><code>matplotlib</code></li>
    <li><code>numpy</code></li>
    <li><code>pypsa</code></li>
  </ul>
  <li class="fragment">What versions of those libraries...? <span class="fragment">🤔🤔</span></li>
</ul>

---

<!-- .slide: data-state="standard" -->
## Encapsulation

Say you install `pypsa` on your system. What if you need a different `pypsa` version for a different project?

Can we create separate environments for different projects?


---

<!-- .slide: data-state="standard" -->
## Python Environments

<div style="width: 29%; float: left; margin-left: 15%;">

- `venv`
- `conda env`
- `poetry`
- `pmd`
- `nix`
- ...

</div>

<div style="width: 49%; float: right; margin-right: 5%;" class="fragment">
☯ Zen of Python ☯
<blockquote><b>Rule 13</b> <br> There should be one - and preferably only one - obvious way to do it. </blockquote>
</div>

---

<!-- .slide: data-state="standard" -->
## Create a Library File

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash"># requirements.txt
black
matplotlib
numpy
pypsa
</code></pre>

<br>

<div class="fragment">
    <img style="width: 3em; margin: 0; padding: 0 2em; float: left;" src="./files/hacker-cat.png">
    <div style="float: left; width: 50%;">
        Create a <code>requirements.txt</code> file containing all the libraries we use.
    </div>
</div>

---

<!-- .slide: data-state="standard" -->
## Virtual Environment

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash" data-line-numbers>$ python -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
</code></pre>

<br>

<div class="fragment">
    <img style="width: 3em; margin: 0; padding: 0 2em; float: left;" src="./files/hacker-cat.png">
    <div style="float: left; width: 50%;">
        Create a virtual environment and install libraries.
    </div>
</div>


---

<!-- .slide: data-state="standard" -->
## Pinning Libraries

If your code runs, find out your libraries- and Python versions.

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash">$ pip freeze
attrs==23.2.0
blosc2==2.4.0
Bottleneck==1.3.7
certifi==2023.11.17
[...]
</code></pre>

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash">$ python --version 
Python 3.10.13
</code></pre>

<div class="fragment">
  <img style="width: 3em; margin: 0; padding: .5em 2em; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 70%;">
    Update the <code>requirements.txt</code> file with pinned libraries. Mention the Python version in the <code>README.md</code> file.
  </div>

</div>

