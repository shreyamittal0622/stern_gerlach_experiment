# The Stern–Gerlach Experiment

A self-contained explainer of the Stern–Gerlach experiment (SGE): why it was done, how the apparatus works, what was expected versus what was seen, the mathematics behind the deflection, the sequential (multi-stage) version, and what the experiment tells us about measurement, superposition, and entanglement.

> **One-line summary:** Silver atoms sent through an inhomogeneous magnetic field land in **two** discrete spots instead of one smeared band. That two-spot pattern is direct evidence that angular-momentum projections are quantized.

---

## Table of contents

1. [Background and motivation](#1-background-and-motivation)
2. [Experimental setup](#2-experimental-setup)
3. [The physics of the deflection](#3-the-physics-of-the-deflection)
4. [Expected vs. observed](#4-expected-vs-observed)
5. [The central mystery: how does alignment happen?](#5-the-central-mystery-how-does-alignment-happen)
6. [Quantum description: superposition and entanglement](#6-quantum-description-superposition-and-entanglement)
7. [Predictive vs. retrodictive measurement](#7-predictive-vs-retrodictive-measurement)
8. [Comparison with the double-slit experiment](#8-comparison-with-the-double-slit-experiment)
9. [Evidence for "early collapse"](#9-evidence-for-early-collapse)
10. [Sequential Stern–Gerlach (SG-z → SG-x → SG-z)](#10-sequential-stern-gerlach-sg-z--sg-x--sg-z)
11. [Directional quantization as a universal feature](#11-directional-quantization-as-a-universal-feature)
12. [Milestones and significance](#12-milestones-and-significance)
13. [Glossary](#13-glossary)

---

## 1. Background and motivation

- By the early 1920s, evidence for quantized behaviour on atomic scales was mounting. Planck's resolution of the ultraviolet catastrophe and the Stern–Gerlach experiment (1922, Frankfurt) were key evidence that nature is quantum and that physical quantities can be quantized.
- The **Bohr model** successfully explained discrete atomic spectra through quantized electron orbits and quantized angular momentum. It was later found incomplete, but it motivated Stern and Gerlach to test **quantized angular momentum** directly.
- Bohr's quantized orbits implied quantized *orbital* angular momentum, which is what Stern and Gerlach set out to observe. The experiment turned out to also reveal **spin**, which was only proposed in 1925, three years after the original experiment.
- The experiment demonstrates not merely that angular momentum is quantized, but that its **projection onto a chosen axis** takes only discrete values (*directional* or *space* quantization).
- Because it separates atoms into distinct angular-momentum states, selecting one outgoing beam yields a **polarized quantum state**. So an SG apparatus is not only a *detector* but also a **state-preparation device**.

### The core puzzle

Before entering the field, the silver atoms' magnetic moments could point in *any* direction. Why would they end up in only specific directions once inside the field? Stern could not imagine a physical mechanism for this (see [section 5](#5-the-central-mystery-how-does-alignment-happen)).

---

## 2. Experimental setup

```
 silver oven  ──►  collimator  ──►  inhomogeneous magnetic field  ──►  detector
```

The whole apparatus is held in **high vacuum**. Otherwise silver atoms would collide with air molecules and their trajectories would be disturbed.

### 2.1 Silver oven
Silver metal is heated in an oven. The vapor escapes through a small opening and forms an atomic beam.

**Why silver?**
- Silver atoms are electrically **neutral**, so deflection comes from the atom's magnetic moment and not from a charge moving in a field.
- It is a noble metal and chemically well-behaved, so the observed effect is attributable purely to the magnetic field.
- Its single outer electron sits in a **5s** state, which has **zero orbital angular momentum**, while the atom has one **unpaired electron spin**. Silver is therefore a clean system for studying the magnetic moment associated with the electron's (spin) angular momentum.

### 2.2 Collimator
Atoms leaving the oven do not travel in a narrow, well-defined direction. They pass through narrow slits/apertures (Slit 1, Slit 2), producing a **thin, well-directed beam** with approximately the same momentum along the beam axis (x).

### 2.3 Inhomogeneous magnetic field
The beam then passes through a deliberately **non-uniform** magnetic field. The magnet uses specially shaped pole pieces: one pole has a sharp **knife-edge**, the other is flatter. This creates a strong field **gradient** in the vertical (z) direction.

### 2.4 Detector
Historically, a glass/condenser plate recorded where the silver atoms landed. **Two separated regions of silver deposition** were observed.

### Schematic

```
                       ┌──────────────┐
                       │    N pole    │ ─────────────►  ● spin up   (deflected one way)
 Oven ──► Slit1 ──► Slit2 ──►  beam ───┤              ╲
 (Ag vapor)            │  (gradient)  │               ╲ ● spin down (deflected the other way)
                       │    S pole    │
                       └──────────────┘            Detector plate: two distinct spots
```

*oven makes atoms → slits make a clean beam → magnet forces each atom's internal "compass needle" into one of two directions → atoms land in two separate spots instead of one smeared blob.*

---

## 3. The physics of the deflection

A magnetic dipole moment $\boldsymbol{\mu}$ in a field $\mathbf{B}$ has potential energy

$$U = -\boldsymbol{\mu}\cdot\mathbf{B}.$$

so the force on the atom is

$$\mathbf{F} = \nabla(\boldsymbol{\mu}\cdot\mathbf{B}).$$

If the important direction is $z$ (field mainly along $z$, varying with $z$):

$$F_z = \mu_z \frac{\partial B_z}{\partial z}.$$

### Why the field must be non-uniform

A **uniform** field exerts only a **torque** on a dipole. It tries to rotate it, causing precession, but gives **no net sideways push**. If the field were uniform, $\partial B/\partial z = 0$, hence $F_z = 0$ and the atoms would not separate. A strong gradient is what actually *deflects* the atoms, which is why the pole pieces have the knife-edge shape.

### Size of the deflection

For an atom of mass $m$ and forward speed $v$ crossing a magnet of length $L$, the transit time is $t = L/v$. The transverse displacement is

$$\Delta z = \frac{1}{2}\frac{F_z}{m}t^2 = \frac{\mu_z}{2m}\frac{\partial B_z}{\partial z}\frac{L^2}{v^2}.$$

Since the deflection is proportional to $\mu_z$, measuring where atoms land measures the **z-component of the magnetic moment**. A continuous range of $\mu_z$ would give a continuous smear. Discrete $\mu_z$ gives discrete spots.

### Connecting to spin

For a spin-½ electron (with $g \approx 2$), the z-component of the moment is

$$\mu_z = -g\,\mu_B\, m_s, \qquad m_s = \pm\tfrac12 \;\;\Rightarrow\;\; \mu_z \approx \mp\mu_B,$$

where $\mu_B = \dfrac{e\hbar}{2m_e}$ is the **Bohr magneton**. This matches the milestone that each silver atom carries a magnetic moment of about **one Bohr magneton**, and it gives exactly **two** allowed values, hence a **doublet**.

---

## 4. Expected vs. observed

**Classical expectation.** Each atom is a tiny magnet. Before the magnet, these tiny magnets should point in *random* directions, like compass needles scattered every which way. After deflection you would expect a **continuous band** on the screen: some atoms deflected a lot, some a little, some not at all, depending on how each happened to be oriented.

**What actually happens.** The atoms land in **just two separate spots**, as if every atom's moment pointed either straight "up" or straight "down" relative to the magnet. Nature allows two options, not a continuous range.

| | Classical prediction | Observation |
|---|---|---|
| Orientation of $\boldsymbol\mu$ | Any direction | Only two projections along the field |
| Pattern on plate | Continuous smear | Two distinct spots (doublet) |
| $\mu_z$ values | Continuous | Discrete ($\approx\pm\mu_B$) |

> **Historical footnote.** In the Bohr–Sommerfeld picture, orbital angular momentum with $l=1$ was assigned projections that excluded zero, which also gave two beams. The correct explanation, however, is electron **spin** (silver's $l = 0$), so "two beams" was initially right for the wrong reason.

---

## 5. The central mystery: how does alignment happen?

The two-spot result implies each atom's moment has "committed" to being aligned **with** or **against** the field. But what interaction makes that happen?

A useful classical analogy is a spinning top: tilt its axis and apply gravity, and it does not suddenly snap upright or flip over. Instead it **wobbles around a cone** (precession). For a magnetic moment this is **Larmor precession**.

So classical physics says: once in the field, the atom's needle should just precess around the field direction while keeping whatever random tilt it started with, and it should never lock into alignment. Yet the data show a full commitment to one of two directions almost immediately.

- **Classical:** continuous wobbling, a continuous range of outcomes.
- **Quantum experiment:** only two fixed outcomes.

**Einstein and Ehrenfest** tried to explain the alignment with familiar classical mechanisms, **momentum-exchange forces** and **radiation exchange**, but could not find a mechanism that explains it.

### Why the trajectory itself isn't the problem

The atom's path through the apparatus can still be described using ordinary force/momentum equations. Trajectories behave classically. Only the **internal magnetic orientation** behaves in this non-classical way, which is what makes the puzzle so localized and so strange.

---

## 6. Quantum description: superposition and entanglement

An unpolarized or arbitrarily polarized spin-½ state can be written in the $z$-basis:

$$|\chi\rangle = \alpha\,|{+z}\rangle + \beta\,|{-z}\rangle, \qquad |\alpha|^2 + |\beta|^2 = 1.$$

Before the magnet, the atom's spatial wavepacket $\psi(\mathbf r)$ and spin are unentangled:

$$|\Psi_{\text{in}}\rangle = \psi(\mathbf r)\,\big(\alpha|{+z}\rangle + \beta|{-z}\rangle\big).$$

The field gradient gives the two spin components **opposite momentum kicks** ($\pm \mu_B\,\partial_z B\,t$), so the two parts of the wavepacket separate in space:

$$|\Psi_{\text{out}}\rangle = \alpha\,\psi_{+}(\mathbf r)\,|{+z}\rangle + \beta\,\psi_{-}(\mathbf r)\,|{-z}\rangle.$$

This is an **entangled** state of the internal (discrete) spin degree of freedom with the external (continuous) spatial degree of freedom. The probabilities of landing in the upper/lower spot are $|\alpha|^2$ and $|\beta|^2$.

**The open conceptual question:** while the atom travels through the magnet, is it in a quantum superposition of "spin up" and "spin down" (like Schrödinger's cat) until it hits the detector?

---

## 7. Predictive vs. retrodictive measurement

- **Predictive:** *before* the measurement you do not know the outcome. Quantum superposition rules apply.
- **Retrodictive:** *after* detection you can trace back exactly which path the atom took.

In the SGE you can **retrodictively identify which spin state** an atom had, unlike, say, a double-slit experiment with photons, where there is no way to know which slit a photon went through.

---

## 8. Comparison with the double slit

| | Double slit | Stern–Gerlach |
|---|---|---|
| Can you tell which path was taken (even in principle)? | No | Yes, paths are physically distinguishable almost immediately |
| State of the particle | Superposition of slit 1 and slit 2 | Spin entangled with spatial path |
| Interference observed? | Yes, continuous wave-like fringes | No interference between up and down beams |

In the double slit, since there is no way to tell which slit was used, the wavefunction stays in superposition and produces interference.

In the SGE, the inhomogeneous field **entangles the internal spin with the spatial wavepacket's trajectory**, so a single path **forks into discrete trajectories**. The experiment therefore demonstrates both **spin quantization** and **state entanglement**: an internal discrete property couples to continuous physical space.

---

## 9. Evidence for "early collapse"

In the original setup the magnet was **asymmetric**, with one knife-edge pole creating a strong gradient. As a result the silver deposit on the plate was asymmetric too, forming a characteristic **"lip" or "cusp"** near the sharp edge.

If the atom's wavefunction had stayed a coherent, perfectly symmetric superposition throughout its flight, one might expect a symmetric distribution on the screen. Instead the observed spatial trace mirrors the **local profile of the classical magnetic force field**. This is interpreted as suggesting that **decoherence**, or effective "collapse", occurs **inside the field region** almost immediately as the spin becomes entangled with the field gradient. Each atom is forced onto a localized "up" or "down" trajectory early in its flight rather than only at the detector.

**David Bohm** suggested one could, in principle, think of the measurement as happening via the **momentum transferred** to the particle by the field, which matches the "early collapse" picture.

> *Interpretation note:* this section is an interpretation, not a settled experimental conclusion. The cusp shape also arises simply because the field gradient is not uniform across the beam's cross-section. Different interpretations of quantum mechanics describe "collapse" differently.

---

## 10. Sequential Stern–Gerlach (SG-z → SG-x → SG-z)

Placing two or more SG magnets in series along the beam path shows that the SG apparatus is a **state-preparation device** and exposes the non-classical nature of spin.

Consider three stages:

**Stage 1: SG-z (state preparation).**
An unpolarized beam enters a z-aligned magnet and splits into $|{+z}\rangle$ and $|{-z}\rangle$. The $|{-z}\rangle$ beam is blocked with a beam stop. The remaining beam is **100% prepared** in $|{+z}\rangle$.

**Stage 2: SG-x (basis change).**
The pure $|{+z}\rangle$ beam passes through a magnet oriented along $x$. In the $x$-basis the state is an equal superposition:

$$|{+z}\rangle = \frac{1}{\sqrt2}\,|{+x}\rangle + \frac{1}{\sqrt2}\,|{-x}\rangle.$$

The beam splits into two equal parts. The $|{-x}\rangle$ beam is blocked, leaving only $|{+x}\rangle$.

**Stage 3: SG-z (re-measurement along the original axis).**
The pure $|{+x}\rangle$ beam enters a third z-oriented magnet. **Classically**, no downward ($-z$) deflection should occur, since all $|{-z}\rangle$ atoms were removed in Stage 1. **Quantum mechanically**, because

$$|{+x}\rangle = \frac{1}{\sqrt2}\big(|{+z}\rangle + |{-z}\rangle\big),$$

the beam splits again into **equal** $|{+z}\rangle$ and $|{-z}\rangle$ outputs.

### Summary table

| Stage | Axis | Action | Beam after |
|---|---|---|---|
| 1 | z | Block $\lvert{-z}\rangle$ | 100% $\lvert{+z}\rangle$ |
| 2 | x | Block $\lvert{-x}\rangle$ | 100% $\lvert{+x}\rangle$ (50% of previous intensity) |
| 3 | z | Measure again | 50% $\lvert{+z}\rangle$, 50% $\lvert{-z}\rangle$ |

**Takeaway:** measuring spin along $x$ **erases** the earlier $z$-information. Spin components along different axes do not commute ($[S_x, S_z] \neq 0$), so they cannot all have definite values simultaneously.

---

## 11. Directional quantization as a universal feature

**Core idea:** whenever a quantum system's angular momentum is measured along a specified axis, the component along that axis cannot take arbitrary values. It is restricted to **discrete, quantized values**:

$$L_z = m_\ell\hbar,\quad m_\ell = -\ell,\dots,+\ell \qquad\text{and}\qquad S_z = m_s\hbar,\quad m_s = \pm\tfrac12.$$

### Relation to the Zeeman effect

The **Zeeman effect** is the splitting of atomic spectral lines in an external magnetic field. It happens because the atom's magnetic moment aligns only in specific quantized directions relative to the field. Both phenomena are closely related. Yet the Zeeman effect was readily accepted as evidence for quantum mechanics, since spectral lines were familiar territory, whereas the SGE was found "miraculous" even though the two are tightly connected.

### Modern example: ion–atom scattering

In experiments colliding a helium ion with a helium atom, the momentum distribution of the ejected electrons was recorded. Instead of a smooth classical distribution, the detector registered distinct **curved, "banana-shaped"** angular-momentum patterns. These arise because the orbital angular momentum of the colliding system is directionally quantized along the collision axis. This is presented as confirmation that directional quantization is an intrinsic feature of quantum interactions generally, well beyond magnetic fields and silver atom beams.

---

## 12. Milestones and significance

The SGE:

- Verified that each silver atom has a magnetic moment of about **one Bohr magneton**.
- Gave the **first direct experimental evidence** that angular momentum is quantized in units proportional to Planck's constant.
- Confirmed the hypothesis of **directional quantization** of magnetic (and electric) moments of quantum objects in external fields.
- Showed a **doublet splitting** for silver atoms.
- Was the first measurement where a **ground-state quantum property** of an atom could be determined directly.
- Produced the **first fully spin-polarized atomic beam**, an atomic beam in a well-aligned state.
- Was the first fully successful **molecular-beam experiment in high vacuum**, showing that molecular beams can probe internal atomic properties with high precision.
- Showed that an atom's angular momentum **cannot point in just any direction**. When measured, only specific quantum orientations are possible.
- Established the SG apparatus as both a **detector** and a **state-preparation device**, a conceptual ancestor of modern qubit state preparation and measurement.

---

## 13. Glossary

| Term | Meaning |
|---|---|
| **Magnetic moment ($\boldsymbol\mu$)** | Vector measuring how strongly an object behaves like a tiny magnet |
| **Bohr magneton ($\mu_B$)** | Natural unit of electron magnetic moment, $e\hbar/2m_e$ |
| **Inhomogeneous field** | A field whose strength varies in space, giving a nonzero gradient |
| **Collimator** | Slits that shape particles into a narrow, directed beam |
| **Directional (space) quantization** | Only discrete orientations of angular momentum relative to an axis are allowed |
| **Larmor precession** | Classical wobble of a magnetic moment around a magnetic field |
| **Superposition** | A quantum state that is a combination of several basis states |
| **Entanglement** | Correlation between subsystems (here: spin and position) that cannot be described separately |
| **Decoherence / collapse** | Loss of coherence between components of a superposition, giving a definite-looking outcome |
| **Predictive / retrodictive** | Reasoning forward to an outcome vs. backward to which path was taken |
| **State preparation** | Producing a beam of particles all in a known quantum state |

---

*Source: course/presentation notes on the Stern–Gerlach experiment (`stern-gerlach.pdf`), expanded with the underlying mathematics.*
