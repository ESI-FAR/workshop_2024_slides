<!-- .slide: data-state="blue_overlay 6 yellow_flag logo" id="testing" data-background="./files/laboratory-217041_1280.jpg" -->
<!-- https://pixabay.com/photos/laboratory-apparatus-equipment-217041/ -->
# Testing

Just because code runs, does not mean it's correct...

<span class="fragment">Also, fearless refactoring, here we go!</span>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-background="./files/laboratory-217041_1280.jpg" -->

## About Purity

A function is <em>pure</em>, when

1. the same input produces the same output, and
1. there are no <em>side effects</em>.

<br>
<br>

<div class="fragment">

Examples of <em>impurities</em>:

- Random numbers
- Using/changing external/global variables
- Outputs: print to screen, plotting
- Inputs: user input, reading files

</div>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-background="./files/laboratory-217041_1280.jpg" -->

## Examples

<div style="width: 49%; float: left;">

### Impure

<pre><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def extend_list():
    my_list.append(5)
</code></pre>

<pre class="fragment" data-fragment-index="2"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>PI = 3.14
def mult_with_pi(number):
    return number * PI
</code></pre>

</div>


<div style="width: 49%; float: left;">

### Pure

<pre class="fragment" data-fragment-index="1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def extend_list(ext_list):
    return ext_list + [5]
</code></pre>

<pre class="fragment" data-fragment-index="3"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>PI = 3.14
def mult_with_pi(number, PI):
    return number * PI
</code></pre>

</div>


---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-background="./files/laboratory-217041_1280.jpg" -->

## Benefit of Purity

<ul>
  <li>Speed</li>
  <li class="fragment">Testing!</li>
</ul>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Assertions

<pre data-id="assertion_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>python
>>> assert(1 == 1)
</code></pre>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Assertions

<pre data-id="assertion_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>python
>>> assert(1 == 1)
>>>
</code></pre>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Assertions

<pre data-id="assertion_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>python
>>> assert(1 == 1)
>>> assert(1 == 2)
Traceback (most recent call last):
  File "&lt;stdin&gt;", line 1, in &lt;module&gt;
AssertionError
</code></pre>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-background="./files/laboratory-217041_1280.jpg" -->

## What's In A Name?

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># module.py
def myfunc():
    print("Function called")

if __name__ == "__main__":
    print("Module running directly")
</code></pre>

<pre style="width: max-content;"><code style="padding: .5em 1em;" class="language-python">$ python
>>> import module
>>> module.myfunc()
Function called

$ python module.py
Module running directly               
</code></pre>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Testing Your Module

<pre data-id="testing_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>def radians_to_degrees(radians: float) -> float:
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Testing Your Module

<pre data-id="testing_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="5-6">def radians_to_degrees(radians: float) -> float:
    degrees = radians * 360 / (2 * np.pi)
    return degrees

if __name__ == "__main__":
    [TESTING]
</code></pre>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Testing Your Module

<pre data-id="testing_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="5-7">def radians_to_degrees(radians: float) -> float:
    degrees = radians * 360 / (2 * np.pi)
    return degrees

if __name__ == "__main__":
    assert(radians_to_degrees(0) == 0)
    print("'radians_to_degrees' passed!")
</code></pre>

<span class="fragment">Let's allow for small numerical errors...</span>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Testing Your Module

<pre data-id="testing_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="5-7">def radians_to_degrees(radians: float) -> float:
    degrees = radians * 360 / (2 * np.pi)
    return degrees

if __name__ == "__main__":
    assert(abs(radians_to_degrees(0) - 0) < 0.01)
    print("'radians_to_degrees' passed!")
</code></pre>

<span class="fragment">&#42;frantically googling some conversion values...&#42;</span>

---

<!-- .slide: data-state="blue_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/laboratory-217041_1280.jpg" -->

## Testing Your Module

<pre data-id="testing_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="5-9">def radians_to_degrees(radians: float) -> float:
    degrees = radians * 360 / (2 * np.pi)
    return degrees

if __name__ == "__main__":
    assert(abs(radians_to_degrees(0) - 0) < 0.01)
    assert(abs(radians_to_degrees(1) - 57.30) < 0.01)
    assert(abs(radians_to_degrees(2) - 114.59) < 0.01)
    print("'radians_to_degrees' passed!")
</code></pre>

<div class="fragment">
  <img style="width: 2em; margin: 0; padding: 0em 0em 0em 20%; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 60%; padding-top: .25em;">
    Test your <code>conversion</code> module.
  </div>
</div>
