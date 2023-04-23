---
title: >-
  Design for a Scalable Superconducting Quantum Chip Package and its Performance
  Analysis
date: 2022-06-02 23:41:50
updated: 2022-08-01 23:41:50
tags: 
- Physics
categories: 
- gallery
featured_image: /img/package.png
---

## Why Superconducting Quantum Chip Package?

- EM noise shielding
- Microwave signal fan-out
- Securing and protecting the chip

Design Requirement for the package:

- Modular & scalable
- High level of integration
- Low dissipation rate
- High fidelity 

## Designing Principles

Engineering concerns:

- Low dissipation rate
	- Material selection
	- Supression of coupling to vibration mode
		- Cavity mode
		- PCB chip mode
- High fidelity
	- Signal integrity engineering
		- Impedance matching
		- Reducing crosstalk

### Cavity Mode

![](Pasted%20image%2020230422152012.png)

Half-integer times base frequency.

### PCB Mode

![](PCB.gif)

$$f_{PCB}\approx 10.4 \rm{GHz}, Q=55$$

### Impedance Matching

$Z=\sqrt{L/C}\approx 200\Omega \rightarrow$ 3-4 wirebonds to match standard impedance $Z_0=50\Omega$

Where 

$$L\approx \frac{\mu_0l}{2\pi} \rm{arccosh}(2h/d)$$
$$C\approx \frac{2\pi l \varepsilon_0}{\rm{arccosh(h/d)}}$$


![](Pasted%20image%2020230422152834.png)

Verifying impedance by Time-Domain Reflectometry (TDR), matching is optimized for 3 wires diameter $d=50\mu m$.

![](Pasted%20image%2020230422153542.png)

### Grouding wires for crosstalk supression

![](Pasted%20image%2020230422153745.png)

Saturation after 1 grounding wire.

## 3D Pogo-pin-based Wiring Package Design

![](Pasted%20image%2020230422154452.png)

### Pogo-pin-based 3D wiring

![](Pasted%20image%2020230422222233.png)

### Scalable Quantum Chip Design

- $3\times 3$ cell forming a scalable 2D array
- 36 tunable transmon qubits
- Through silicon via (TSV) for front and back surface

![](Pasted%20image%2020230422223447.png)

- +2MHz ~ -40MHz tunable coupling strength
- multiplexed readin and readout.

### Supression of Chip Mode

![](Pasted%20image%2020230422223855.png)

With the added central pillar, the band becomes much flatter, and cut-off freqency greatly increased to above 30GHz.

### Supression of crosstalk

![](Pasted%20image%2020230422224105.png)

Coaxial microwave cable, nearest neighbor crosstalk < -100dB.
