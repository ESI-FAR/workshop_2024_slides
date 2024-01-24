<!-- .slide: data-state="white_overlay 8 yellow_flag logo" id="split" data-background="./files/code_data.jpg" -->
<!-- https://pixabay.com/photos/coding-computer-hacker-hacking-1841550/ -->
<!-- https://pixabay.com/photos/files-paper-office-paperwork-stack-1614223/ -->
<h1 style="transform: translate(-15vw, 15vh);">Split Code,</h1>
<div style="transform: translate(15vw, 30vh);">
    <h1>Configuration<span class="fragment" data-fragment-index="1">,</span></h1>
    <h1 class="fragment" data-fragment-index="1">And Data</h1>
</div>


---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/code_data.jpg" -->
## Code? Data? Config? Parameters?

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

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/code_data.jpg" -->
## Benefits

- Facilitate self-documentation
- Change parameters without changing the script
- Reproducibility: store `config.py` with your results
