<!-- .slide: id="environments" data-state="black_overlay 7 yellow_flag logo" data-background="./files/augmented-reality-1853592_1280.jpg" -->
<!-- https://pixabay.com/photos/augmented-reality-bicycle-girl-bike-1853592/ -->
# Code Environments

---

<!-- .slide: data-state="standard" data-state="black_overlay yellow_flag logo" data-background="./files/augmented-reality-1853592_1280.jpg" -->
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

<!-- .slide: data-state="standard" data-state="black_overlay yellow_flag logo" data-background="./files/augmented-reality-1853592_1280.jpg" -->
## Encapsulation

Say you install `pypsa` on your system. What if you need a different `pypsa` version for a different project?

Can we create separate environments for different projects?


---

<!-- .slide: data-state="standard" data-state="black_overlay yellow_flag logo" data-background="./files/augmented-reality-1853592_1280.jpg" -->
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
<blockquote><b>Line 13</b> <br> There should be one - and preferably only one - obvious way to do it. </blockquote>
</div>

---

<!-- .slide: data-state="standard" data-state="black_overlay yellow_flag logo" data-background="./files/augmented-reality-1853592_1280.jpg" -->
## Create a Requirements File

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash"># requirements.txt
black
matplotlib
numpy
pypsa
</code></pre>

<div class="fragment">
    <img style="width: 3em; margin: 0; padding: .5em 1em; float: left;" src="./files/hacker-cat.png">
    <div style="float: left; width: 80%;">
      <ul>
        <li>Create a <code>requirements.txt</code> file containing the requirements (libraries) we use.</li>
        <li>Mention the Python version in <code>README.md</code>.</li>
      </ul>
    </div>
</div>

<footer>
What about the library versions?<br>
<a href="https://stackoverflow.com/questions/28509481/should-i-pin-my-python-dependencies-versions">Should I pin dependencies?</a> / <a href="https://www.codyhiar.com/blog/tips-for-pinning-python-requirements-files/">Tips for pinning</a>
</footer>

---

<!-- .slide: data-state="standard" data-state="black_overlay yellow_flag logo" data-background="./files/augmented-reality-1853592_1280.jpg" -->
## Virtual Environment

<div style="width: max-content; float: left; padding-bottom: 1em;">
<h3>Linux</h3>
<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash" data-line-numbers>$ python -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
</code></pre>
</div>

<div style="width: max-content; float: right; padding-bottom: 1em;">
<h3>Windows</h3>
<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-bash" data-line-numbers>$ python -m venv .venv
$ source .venv/Scripts/activate
$ pip install -r requirements.txt
</code></pre>
</div>

<br>

<div class="fragment">
    <img style="width: 3em; margin: 0; padding: 0 2em; float: left;" src="./files/hacker-cat.png">
    <div style="float: left; width: 50%;">
        Create a virtual environment and install libraries.
    </div>
</div>
