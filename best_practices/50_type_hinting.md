<!-- .slide: data-state="white_overlay 6 yellow_flag logo" id="type_hinting" data-background="./files/man-5888558_1280.jpg" -->
<!-- https://pixabay.com/photos/man-pointing-gesture-hand-gesture-5888558/ -->
# Type Hinting

<br>
<br>
<br>

`type(object)`

<br>
<br>
<br>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/man-5888558_1280.jpg" -->

## What Are Types?

<pre data-id="types_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>$ python
&gt;&gt;&gt; x = 5
</code></pre>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/man-5888558_1280.jpg" -->

## What Are Types?

<pre data-id="types_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>$ python
&gt;&gt;&gt; x = 5
&gt;&gt;&gt; type(x)
&lt;class 'int'&gt;</code></pre>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/man-5888558_1280.jpg" -->

## Dynamic Typing

Types in Python can change. Often you don't know what types you are working with.

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>$ python
>>> x = 5
>>> print(x)
5
>>> x = "abcde"
>>> print(x)
abcde
</code></pre>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/man-5888558_1280.jpg" -->

## Type Hinting

<pre data-id="hints_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>var_1: TYPE  # Only hint the type, do not assign yet
var_1 = 1  # Assign value
</code></pre>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/man-5888558_1280.jpg" -->

## Type Hinting

<pre data-id="hints_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>var_1: TYPE  # Only hint the type, do not assign yet
var_1 = 1  # Assign value

var_2: TYPE = 2  # Both type hint and assign
</code></pre>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/man-5888558_1280.jpg" -->

## Type Hinting

<pre data-id="hints_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>var_1: TYPE  # Only hint the type, do not assign yet
var_1 = 1  # Assign value

var_2: TYPE = 2  # Both type hint and assign

def my_func(arg_one: TYPE, arg_two: TYPE = value) -> RETURN_TYPE:
    return something
</code></pre>

<div class="fragment">
    Unless you check for it (e.g. with <code>mypy</code>), type hinting does not do anything! It does, however, make the code more readable.
</div>

<br>

<div class="fragment">
  <img style="width: 2em; margin: 0; padding: 1.25em 1em 0em 10%; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 60%; padding-top: .25em;">
    Type-hint <code>radians_to_degrees</code>.<br>Check your documentation with <code>help(radians_to_degrees)</code> in a Python console.
  </div>
</div>
