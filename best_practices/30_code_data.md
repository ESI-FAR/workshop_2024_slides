<!-- .slide: data-state="white_overlay 8 yellow_flag logo" id="split" data-background="./files/code_data.jpg" data-auto-animate -->
<!-- https://pixabay.com/photos/coding-computer-hacker-hacking-1841550/ -->
<!-- https://pixabay.com/photos/files-paper-office-paperwork-stack-1614223/ -->
<h1 data-id="code_1" style="transform: translate(-15vw, 15vh);">Split Code,</h1>
<div style="transform: translate(15vw, 15vh);">
    <h1 data-id="data_1">Data<span class="fragment" data-fragment-index="1">,</span></h1>
    <h1 data-id="config_1" class="fragment" data-fragment-index="1">And Config</h1>
</div>


---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/code_data.jpg" data-auto-animate -->
<div style="width: 50%; margin: auto; padding-bottom: 1em;">
<h1 data-id="code_1">Code?</h1>

<ul class="fragment">
  <li>"What's happening?"</li>
  <li>Energy System Model</li>
  <li>Version control</li>
</ul>

</div>

<div style="width: 49%; float: left;">
<h1 data-id="data_1">Data?</h1>

<ul class="fragment">
  <li>"What are we working with?"</li>
  <li>List of energy system nodes</li>
  <li>No touchey! Version control</li>
</ul>

</div>

<div style="width: 49%; float: right;">
<h1 data-id="config_1">Config?</h1>

<ul class="fragment">
  <li>"How exactly?"</li>
  <li>Which nodes to disrupt?</li>
  <li>Store with results</li>
</ul>

</div>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/code_data.jpg" -->
## Why Split?

Imagine you want to change simulation parameters. All resistances of 0.1 Ohm shall be replaced by 1 Ohm.

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>x_1 = 0.1
x_2 = 0.1
r_1 = 0.1
r_2 = 0.1
</code></pre>

<span class="fragment">Which values to replace?</span>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/code_data.jpg" -->
## Config File

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># config.py
reactance = 0.1  # [Ohm]
resistance = 1.0  # [Ohm]
</code></pre>

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
import config

x_1 = config.resistance  
x_2 = config.resistance
r_1 = config.reactance
r_2 = config.reactance
</code></pre>

<div class="fragment">
  <img style="width: 2em; margin: 0; padding: 0em 0em 0em 10%; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 70%; padding-top: .25em;">
    Create a config file to split code and configuration.
  </div>
</div>

<footer>
Also consider <a href="https://toml.io/en/">TOML</a>: More robust, built-in Python support
</footer>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/code_data.jpg" -->
## Benefits

- Facilitate self-documentation
- Change parameters without changing the script
- Reproducibility: store `config.py` with your results
