<!-- .slide: data-state="blue_overlay 7 yellow_flag logo" id="debugging" data-background="./files/broom-6310388_1280.jpg" -->
<!-- https://pixabay.com/photos/broom-cleaning-sweep-outdoors-6310388/ -->
# Debugging 🐞

---

<!-- .slide: data-state="blue_overlay yellow_flag logo" data-background="./files/broom-6310388_1280.jpg" -->
## Powerful Weapons

<br>

<span class="fragment"><code>print()</code></span>

<span class="fragment"><code>exit()</code></span>

---

<!-- .slide: data-state="blue_overlay yellow_flag logo" data-auto-animate data-background="./files/broom-6310388_1280.jpg" -->
## Gather Intelligence

<pre data-id="print_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="1-5">network.add(
    "Bus",
    "My bus 2",
    v_nom=20.0  # Nominal Voltage
)
network.add(
    "Line",
    "My line 0",
    bus0="My bus 0",  # Origin
    bus1="My bus 1",  # Target
    x=0.1,  # Series Reactance
    r=0.01  # Series Resistance
)
network.add(
    "Generator",
    "My generator",
    bus="My bus 0",
    p_set=100,  # Active Power Setpoint
    control="PQ"  # Control Strategy
)
network.add(
    "Load",
    "Datacenter",
    bus="My bus 2",
    p_set=70,  # Active Power Setpoint
    q_set=0  # Reactive Power Setpoint
)
</code></pre>

---

<!-- .slide: data-state="blue_overlay yellow_flag logo" data-auto-animate data-background="./files/broom-6310388_1280.jpg" -->
## Gather Intelligence

<pre data-id="print_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="1-9">print()
print("### Empty network:")  # Tip: findable prints ###
print(network)
print()
network.add(
    "Bus",
    "My bus 2",
    v_nom=20.0  # Nominal Voltage
)
network.add(
    "Line",
    "My line 0",
    bus0="My bus 0",  # Origin
    bus1="My bus 1",  # Target
    x=0.1,  # Series Reactance
    r=0.01  # Series Resistance
)
network.add(
    "Generator",
    "My generator",
    bus="My bus 0",
    p_set=100,  # Active Power Setpoint
    control="PQ"  # Control Strategy
)
network.add(
    "Load",
    "Datacenter",
    bus="My bus 2",
    p_set=70,  # Active Power Setpoint
    q_set=0  # Reactive Power Setpoint
)
</code></pre>

---

<!-- .slide: data-state="blue_overlay yellow_flag logo" data-auto-animate data-background="./files/broom-6310388_1280.jpg" -->
## Gather Intelligence

<pre data-id="print_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="1-17">print()
print("### Empty network:")  # Tip: findable prints ###
print(network)
print()
network.add(
    "Bus",
    "My bus 2",
    v_nom=20.0  # Nominal Voltage
)
print()
print("### Added bus 'My bus 2")
print("### Network:")
print(network)
print("### Buses:")
print(network.buses)
print()
exit()
network.add(
    "Line",
    "My line 0",
    bus0="My bus 0",  # Origin
    bus1="My bus 1",  # Target
    x=0.1,  # Series Reactance
    r=0.01  # Series Resistance
)
network.add(
    "Generator",
    "My generator",
    bus="My bus 0",
    p_set=100,  # Active Power Setpoint
    control="PQ"  # Control Strategy
)
network.add(
    "Load",
    "Datacenter",
    bus="My bus 2",
    p_set=70,  # Active Power Setpoint
    q_set=0  # Reactive Power Setpoint
)
</code></pre>

<pre class="fragment"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="1">print(dir(network))  # Tip: List object attributes
</code></pre>

---

<!-- .slide: data-state="blue_overlay yellow_flag logo" data-background="./files/broom-6310388_1280.jpg" -->
## Find Bugs

<div>
  <img style="width: 2em; margin: 0; padding: 0em 0em 0em 20%; float: left;" src="./files/hacker-cat.png">
  <div style="float: left; width: 60%; padding-top: .25em;">
    Find the bug in the network setup.
  </div>
</div>
