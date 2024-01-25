<!-- .slide: id="problem" data-state="white_overlay yellow_flag logo" data-background="./files/wires-7997980_1280.jpg" -->
<!-- https://pixabay.com/photos/wires-electrical-current-electricity-7997980/ -->
# Problem

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/wires-7997980_1280.jpg" -->
## Power Grid Simulation

Your colleague Sam has written a simulation of a power grid:

<img style="height: 2.5em; padding-right: 2em;" src="./files/grid.svg">

- Circular architecture of identical <span style="color: #bf8d2e"><b>Lines</b></span>
- One <span style="color: #9259a3"><b>Generator</b></span>
- Two loads: <span style="color: #ca3c32"><b>Datacenter</b></span> and <span style="color: #399746"><b>Factory</b></span>

They want to analyze how changing reactive power of the load <span style="color: #399746"><b>Factory</b></span> changes the reactive load angles of the lines.

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/wires-7997980_1280.jpg" -->
## Flashback: Physics

![Phase Shift](./files/Phase_shift.svg)

<div style="font-size: small;">

Adapted, from [commons.wikimedia.org/wiki/File:Phase_shift.svg](https://commons.wikimedia.org/wiki/File:Phase_shift.svg) under [CC BY-SA 3.0 Deed](https://creativecommons.org/licenses/by-sa/3.0/deed.en)

</div>

---

<!-- .slide: data-state="white_overlay 9 yellow_flag logo" data-background="./files/wires-7997980_1280.jpg" -->
## Problem

Sam's code does not scale well. There might be bugs. They know you have been following the ESI-far workshop and ask you to refactor their code.
