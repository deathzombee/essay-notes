---
marp: true
theme: default
paginate: true
math: mathjax
---

# APL: The Evolution of a Tool of Thought
## Philosophy, Crisis, and the Ultimate Hack (1979-1984)

---

# Three Eras in the Life of a Language

* **1979: The Philosophy.** Kenneth E. Iverson's Turing Award Lecture establishes APL as a superior, executable mathematical notation.
* **1981: The Existential Crisis.** Michael F. C. Crick's warning about syntax fragmentation and the push for Generalized Objects. Symbols: $\div, |^\wedge_{41}\leftarrow$.
* **1984: The Ultimate Hack.** J. B. Gunn's radical engineering of Virus Functions to rewrite the APL interpreter on the fly.

---

# The Limits of Traditional Mathematics

> "By relieving the brain of all unnecessary work, a good notation sets it free to concentrate on more advanced problems..." - A.N. Whitehead

* **Mathematical Notation**: Highly compressed meaning but lacks universality and is ambiguous based on context.
* **Programming Languages**: Universal, unambiguous, and executable for precise thought experiments.
* **Iverson's Thesis**: Combine executable programming advantages with the power of mathematical notation.

---

# Executable Mathematics in Action

* **Sum Reduction**: $+/ \iota 5$.
    * Integer function $\iota$ produces a vector of first 5 integers.
    * Sum reduction $+/$ adds them to yield $15$.
* **Sum Scan**: $+\backslash \iota 5$.
    * Yields partial sums: $1 \ 3 \ 6 \ 10 \ 15$.
    * Represents atoms in successive planes of a close-packed tetrahedron.

---

# Characteristics of Great Notation

* **Economy**: Expressing a large number of ideas with a small vocabulary. Symbols represent both monadic and dyadic functions.
* **Suggestivity**: Expression forms suggest related concepts. Example: $\times/$ and $+/$ suggest similarity between power ($x/M\rho N$) and multiplication ($+/M\rho N$).
* **Subordination of Detail**: Using arrays and derived functions to hide complexity. Outer product $\circ . \times$ generates function tables without verbose loops.

---

# Should APL be a Declining Language?

* **Natural Language Evolution**: Ancient Greek (complex declensions) $\rightarrow$ Latin $\rightarrow$ English (progressive simplification).
* **Programming Language Evolution**: Early APL (curiosity) $\rightarrow$ 1981 APL (bloated with special cases) $\rightarrow$ Future APL (requires unified syntax).

---

# The Fragmentation of Syntax

* **LISP**: 1 Declension (S-expressions/atoms) with homogenous functions and data.
* **APL**: 6 Declensions.

| Object | Syntax Example |
| :--- | :--- |
| Array | $Y \leftarrow X$ |
| File | $\square TIE$ |
| Function | $\square CR$ |
| Workspace | $) LOAD$ |
| Group | $) GROUP$ |
| Package | $\square PACK$ |

* Constraint: Standard subscript notation cannot access file components or execute workspaces directly.

---

# The "Generalized Object" Solution

* **Extended Nested Arrays**: Unified data structure for Workspaces, Files, and Functions.
* Domain of subscripts extended to nested arrays.
* Objects shareable by multiple processes.
* Access matrix at every node for security.
* Result: A workspace becomes a niladic function returning no result.

---

# The Meta-Programming Dream

* Concept: "What if you could rewrite the interpreter on the fly, without leaving the language?"
* Transformation: Standard APL Workspace $\rightarrow$ Virtual Interpreter.
* Principle: Virtual interpreter can be arbitrarily different from the host interpreter.

---

# Enter the "Virus Function" (VFN)

* **Injection Point**: Single standardized statement inserted at the absolute beginning of a Host Function (HFN).
* **Statement**: $\rightarrow VFN$.
* **The Virus**: A global function hijacking the execution path. The host is completely subverted to the virus's ends.

---

# Anatomy of a Viral Subversion

1. **Discovery**: VFN finds host function name using state indicator.
2. **Extraction**: Obtains canonical representation ($\square CR$) of host code.
3. **Reconstruction**: Reconstruction function (RCS) rewrites code to simulate modified interpreter.
4. **Execution**: Establishes modified representation in local environment and executes it ($\bar{e}$).

---

# Preventing the Infinite Loop

* **Dormant State**: VFN checks global control variable. If dormant, returns null result and host executes normally.
* **Active State**: Virus creates local host version.
* **Logic**: Strips $\rightarrow VFN$ call from the local version to prevent recursive virus calls during reconstructed execution.

---

# Modifying Reality: Viral Applications

* **App 1: Extended Iota**: Applying $\iota$ to arbitrary shape arrays.
* **App 2: Timing Control Vectors**: Injecting hidden CPU timing statements per line to output execution metrics.
* **App 3: Syntax Display**: Forcing recursive self-application for automatic documentation.

---

# The Enduring Legacy of APL

* **Notation (1979)**: Unambiguous tool of mathematical thought.
* **Unification (1981)**: Collapsing boundaries between data, files, and functions via generalized objects.
* **Flexibility (1984)**: Users building virtual interpreters from within.
* **Core**: An executable philosophy of computation.

---

# Sources & Further Reading

1. Iverson, Kenneth E. "Notation as a Tool of Thought." 1979 ACM Turing Award Lecture.
2. Crick, Michael F. C. "Should APL be a Declining Language?" 1981.
3. Gunn, J. B. "Use of virus functions to provide a virtual APL interpreter under user control." IBM Research, 1984.
