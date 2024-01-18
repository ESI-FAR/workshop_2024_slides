<!-- .slide: data-state="purple_overlay yellow_flag logo" id="comments_2" data-background="./files/paper-623167_1280.jpg" -->
<!-- https://pixabay.com/photos/paper-writing-old-antique-write-623167/ -->
# # Comments [2/2]

`"""docstrings"""`

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Module Docstrings

<pre data-id="module_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># conversion.py
"""SHORT DESCRIPTION
[EMPTY LINE]
LONG DESCRIPTION
OVER MULTIPLE LINES
"""

import numpy as np

def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Module Docstrings

<pre data-id="module_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># conversion.py
"""Angle conversions
[EMPTY LINE]
LONG DESCRIPTION
OVER MULTIPLE LINES
"""

import numpy as np

def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Module Docstrings

<pre data-id="module_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># conversion.py
"""Angle conversions

LONG DESCRIPTION
OVER MULTIPLE LINES
"""

import numpy as np

def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Module Docstrings

<pre data-id="module_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers># conversion.py
"""Angle conversions

Convert angles between radians and degrees,
and vice versa.
"""

import numpy as np

def radians_to_degrees(radians):
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-background="./files/paper-623167_1280.jpg" -->

## Function Docstrings

- Google
- reST
- Numpydoc
- ...

Choose one within your team and stick to it.

💡 Editors can often help generating docstrings.

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Function Docstrings

<pre data-id="function_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="10-17"># conversion.py
"""Angle conversions

Convert angles between radians and degrees,
and vice versa.
"""

import numpy as np

def radians_to_degrees(radians):
    """SHORT DESCRIPTION
    [EMPTY LINE]
    LONG DESCRIPTION
    OVER MULTIPLE LINES
    """
    degrees = radians * 360 / (2 * np.pi)
    return degrees



</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Function Docstrings

<pre data-id="function_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="10-17"># conversion.py
"""Angle conversions

Convert angles between radians and degrees,
and vice versa.
"""

import numpy as np

def radians_to_degrees(radians):
    """Convert radians to degrees
    [EMPTY LINE]
    LONG DESCRIPTION
    OVER MULTIPLE LINES
    """
    degrees = radians * 360 / (2 * np.pi)
    return degrees



</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Function Docstrings

<pre data-id="function_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="10-17"># conversion.py
"""Angle conversions

Convert angles between radians and degrees,
and vice versa.
"""

import numpy as np

def radians_to_degrees(radians):
    """Convert radians to degrees

    LONG DESCRIPTION
    OVER MULTIPLE LINES
    """
    degrees = radians * 360 / (2 * np.pi)
    return degrees



</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Function Docstrings

<pre data-id="function_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="10-17"># conversion.py
"""Angle conversions

Convert angles between radians and degrees,
and vice versa.
"""

import numpy as np

def radians_to_degrees(radians):
    """Convert radians to degrees

    Args:
        radians: Angle to be converted
    """
    degrees = radians * 360 / (2 * np.pi)
    return degrees



</code></pre>

---

<!-- .slide: data-state="purple_overlay 9 yellow_flag logo" data-auto-animate data-background="./files/paper-623167_1280.jpg" -->

## Function Docstrings

<pre data-id="function_doc_1"><code style="padding: .5em 1em;" class="language-python" data-line-numbers="10-20"># conversion.py
"""Angle conversions

Convert angles between radians and degrees,
and vice versa.
"""

import numpy as np

def radians_to_degrees(radians):
    """Convert radians to degrees

    Args:
        radians: Angle to be converted

    Returns:
        Radians angle converted to degrees
    """
    degrees = radians * 360 / (2 * np.pi)
    return degrees
</code></pre>

