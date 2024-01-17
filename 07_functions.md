<!-- .slide: data-state="standard" -->
# Functions
Reuse code for readability and robustness

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1" class="fragment"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>bla_0.append([...][f"My bus 0"].iloc[0] * 180 / np.pi)
bla_1.append([...][f"My bus 1"].iloc[0] * 180 / np.pi)
bla_2.append([...][f"My bus 2"].iloc[0] * 18 / np.pi)
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    return radians * 180 / np.pi

bla_0.append([...][f"My bus 0"].iloc[0] * 180 / np.pi)
bla_1.append([...][f"My bus 1"].iloc[0] * 180 / np.pi)
bla_2.append([...][f"My bus 2"].iloc[0] * 18 / np.pi)
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    return radians * 180 / np.pi

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append([...][f"My bus 1"].iloc[0] * 180 / np.pi)
bla_2.append([...][f"My bus 2"].iloc[0] * 18 / np.pi)
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    return radians * 180 / np.pi

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append(radians_to_degrees([...][f"My bus 1"].iloc[0]))
bla_2.append([...][f"My bus 2"].iloc[0] * 18 / np.pi)
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    return radians * 180 / np.pi

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append(radians_to_degrees([...][f"My bus 1"].iloc[0]))
bla_2.append(radians_to_degrees([...][f"My bus 2"].iloc[0]))
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    return radians * 180 / np.pi  # in degrees

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append(radians_to_degrees([...][f"My bus 1"].iloc[0]))
bla_2.append(radians_to_degrees([...][f"My bus 2"].iloc[0]))
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    degrees = radians * 180 / np.pi
    return degrees

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append(radians_to_degrees([...][f"My bus 1"].iloc[0]))
bla_2.append(radians_to_degrees([...][f"My bus 2"].iloc[0]))
</code></pre>

---

<!-- .slide: data-state="standard" data-auto-animate -->

## Code to Functions

Are there repeating sections of code that could be a function?

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append(radians_to_degrees([...][f"My bus 1"].iloc[0]))
bla_2.append(radians_to_degrees([...][f"My bus 2"].iloc[0]))
</code></pre>

---

<!-- .slide: data-state="standard" -->

## Create a Function

<pre data-id="functions_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees

bla_0.append(radians_to_degrees([...][f"My bus 0"].iloc[0]))
bla_1.append(radians_to_degrees([...][f"My bus 1"].iloc[0]))
bla_2.append(radians_to_degrees([...][f"My bus 2"].iloc[0]))
</code></pre>

<img style="width: 2em; margin: 0; padding: 0em 1em 0em 10%; float: left;" src="./files/hacker-cat.png">
<div style="float: left; width: 70%; padding-top: .25em;">
  Create a <code>radians_to_degrees</code> function.
</div>

<br>
<br>

<div class="fragment" style="width: 100%; float: left;">
Hey, that's useful! Could we use this in other projects too? 🤔
<div>
