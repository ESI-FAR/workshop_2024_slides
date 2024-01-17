<!-- .slide: data-state="standard" -->
# Modules
Reusable functions and layers of abstractions

---

<!-- .slide: data-state="standard" -->

## Yet Another File

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># conversion.py

import numpy as np

def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
import conversions as conv

degrees = conv.radians_to_degrees(0.5)   
</code></pre>

<div class="fragment">
  <img style="width: 2em; margin: 0; padding: 0em 1em 0em 10%; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 60%; padding-top: .25em;">
    Create a <code>conversions.py</code> module.
  </div>
</div>

---

<!-- .slide: data-state="standard" -->

## Python, Help!

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>$ python
>>> import conversions as conv
>>> help(conv.radians_to_degrees)
radians_to_degrees()
</code></pre>

<br>

<div class="fragment">
  Huh. Well that's not very useful. 🤷‍♀️
</div>
