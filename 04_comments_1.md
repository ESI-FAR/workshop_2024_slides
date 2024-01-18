<!-- .slide: data-state="purple_overlay 7 yellow_flag logo" id="comments_1" data-background="./files/paper-623167_1280.jpg" -->
<!-- https://pixabay.com/photos/paper-writing-old-antique-write-623167/ -->

# # Comments [1/2]

<div class="fragment">

`code`__#_comment

</div>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-background="./files/paper-623167_1280.jpg" -->
## Improvements

<img style="width: 3em; margin: 0; padding: 1em 1em; float: left;" src="./files/hacker-cat.png">
<div style="float: left; width: 75%;">

- Read the code of <code>script.py</code>.
- Ask questions and understand every variable.
- Add comments for comprehension.

<b>More comments are better!</b>
</div>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Understanding the Code

<pre data-id="comments_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>network.add("Bus", "My bus 2", v_nom=20.0)
network.add("Line", "My line 0", bus0="My bus 0", bus1="My bus 1", x=0.1, r=0.01)
network.add("Generator", "My generator", bus="My bus 0", p_set=100, control="PQ")
network.add("Load", "Factory", bus="My bus 1", p_set=70, q_set=0)
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Understanding the Code

<pre data-id="comments_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="1-5|6-13|14-20|21-27">network.add(
    "Bus",  # Component type
    "My bus 2",  # Component name
    v_nom=20.0  # Nominal Voltage
)
network.add(
    "Line",  # Component type
    "My line 0",  # Component name
    bus0="My bus 0",  # Origin
    bus1="My bus 1",  # Target
    x=0.1,  # Series Reactance
    r=0.01  # Series Resistance
)
network.add(
    "Generator",  # Component type
    "My generator",  # Component name
    bus="My bus 0",  # Location
    p_set=100,  # Active Power Setpoint
    control="PQ"  # Control Strategy
)
network.add(
    "Load",  # Component type
    "Datacenter",  # Component name
    bus="My bus 2",  # Location
    p_set=70,  # Active Power Setpoint
    q_set=0  # Reactive Power Setpoint
)
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-background="./files/paper-623167_1280.jpg" -->
## Less Comments Are Better

Wait, what?

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Verbose Variable Names

<pre data-id="var_names_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># bus load angles
bla_0 = []
bla_1 = []
bla_2 = []
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Verbose Variable Names

<pre data-id="var_names_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># bus load angles
bus_0_load_angles = []
bla_1 = []
bla_2 = []
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Verbose Variable Names

<pre data-id="var_names_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># bus load angles
bus_0_load_angles = []
bus_1_load_angles = []
bla_2 = []
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Verbose Variable Names

<pre data-id="var_names_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># bus load angles
bus_0_load_angles = []
bus_1_load_angles = []
bus_2_load_angles = []
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Verbose Variable Names

<pre data-id="var_names_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>bus_0_load_angles = []
bus_1_load_angles = []
bus_2_load_angles = []
</code></pre>

---

<!-- .slide: data-state="purple_overlay yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->
## Verbose Variable Names

<pre data-id="var_names_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers>bus_0_load_angles = []
bus_1_load_angles = []
bus_2_load_angles = []
</code></pre>

<br>

<div>
  <img style="width: 3em; margin: 0; padding: 0em 1em; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 75%;">
    Replace incomprehensible variable names with good ones.
  </div>
</div>
