<!-- .slide: data-state="black_overlay 7 yellow_flag logo" id="formatting" data-background="./files/vehicle-3090246_1280.jpg" -->
<!-- https://pixabay.com/photos/vehicle-car-transportation-vintage-3090246/ -->
# Bonus: Formatting

<blockquote>
Any color the customer wants,<br>as long as it's black.
<div style="text-align: right; padding-top: 1em;">- Henry Ford (supposedly)</div>
</blockquote>

---

<!-- .slide: data-state="black_overlay 9 yellow_flag logo" data-background="./files/vehicle-3090246_1280.jpg" -->

## Style Conventions

- How many newlines between functions?
- Whitespace around operators?
- Max linewidth?

<span class="fragment"><em>Argue! Fight! Throw cake at each other!</em></span>

---

<!-- .slide: data-state="black_overlay 9 yellow_flag logo" data-background="./files/vehicle-3090246_1280.jpg" -->

## Choices

- AutoPEP8
- Black
- Ruff
- ...

Just like with docstring styles, choose one and stick to it.

---

<!-- .slide: data-state="black_overlay 9 yellow_flag logo" data-background="./files/vehicle-3090246_1280.jpg" data-auto-animate -->

## Demo

<pre><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
j = [1,
     2,
     3
]

ImportantClass.important_method(exc, limit, lookup_lines, capture_locals, extra_argument)
</code></pre>

---

<!-- .slide: data-state="black_overlay 9 yellow_flag logo" data-background="./files/vehicle-3090246_1280.jpg" data-auto-animate -->

## Demo

<pre><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
j = [1,
     2,
     3
]

ImportantClass.important_method(exc, limit, lookup_lines, capture_locals, extra_argument)
</code></pre>

<pre data-id="run_black_1"><code style="padding: .5em 1em;" class="language-python">$ black script.py
</code></pre>

---

<!-- .slide: data-state="black_overlay 9 yellow_flag logo" data-background="./files/vehicle-3090246_1280.jpg" data-auto-animate -->

## Demo

<pre><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
j = [1,
     2,
     3
]

ImportantClass.important_method(exc, limit, lookup_lines, capture_locals, extra_argument)
</code></pre>

<pre data-id="run_black_1"><code style="padding: .5em 1em;" class="language-python">$ black script.py
reformatted script.py

All done! ✨ 🍰 ✨
1 file reformatted.
</code></pre>

---

<!-- .slide: data-state="black_overlay 9 yellow_flag logo" data-background="./files/vehicle-3090246_1280.jpg" data-auto-animate -->

## Demo

<pre><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
j = [1,
     2,
     3
]

ImportantClass.important_method(exc, limit, lookup_lines, capture_locals, extra_argument)
</code></pre>

<pre><code style="padding: .5em 1em;" class="language-python">$ black script.py
reformatted script.py

All done! ✨ 🍰 ✨
1 file reformatted.
</code></pre>

<pre><code style="padding: .5em 1em;" class="language-python" data-line-numbers># script.py
j = [1, 2, 3]

ImportantClass.important_method(
    exc, limit, lookup_lines, capture_locals, extra_argument
)
</code></pre>
