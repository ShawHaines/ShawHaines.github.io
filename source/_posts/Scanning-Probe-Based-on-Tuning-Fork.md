---
title: Scanning Probe Based on Tuning Fork
updated: 2021-12-13 00:23:35
date: 2021-06-09 16:26:00
tags: 
- Physics
categories:
- gallery
featured_image: "/img/Scanning demo.gif"
---

# Introduction

Point-contact methods

* Soft Point-contact
* Mechanical Point-contact

![](Soft_Mechanical.png)

Difficult to operate when faced with samples shown in (c)

![Different Sample Surfaces](sample.png)

# Methods

## Device & Apparatus Design

![Assembly of Scanning Probe Device](Device.png)

![Apparatus](Apparatus.png)

## Detection of Resonance Frequency

The electric properties of a tuning fork can be well described using simple RLC model.[^1]

![](RLC Model.png)

$$
\begin{gathered}
\omega_{r}=2 \pi f_{r}=\frac{1}{\sqrt{L C}} \\
Y(\omega)=\frac{I(\omega)}{U(\pi)}=i \omega C_{S}+\frac{1}{R+\frac{1}{i \omega C}+i \omega L} \\
Y(f)=\frac{I(\omega)}{U(\pi)}=i 2 \pi f C_{S}+\frac{A_{0} \Delta f\left(\Delta f-2 i\left(f-f_{r}\right)\right)}{\Delta f^{2}+4\left(f-f_{r}\right)^{2}}
\end{gathered}
$$


[^1]:Kamra et al., “An All-Electrical Torque Differential Magnetometer Operating under Ambient Conditions.”

Using these formula to fit the measurement curve, we can recover the quality factor of the tuning fork.

![](Peak.png)

## Engaging Detection

![(a) shift on resonating frequency (b) the amplitude of voltage on versus steps of displacement in $z$ direction](Engaging Detection.png)

## Controlling Strategy

![Naive Controlling Strategy that performs retraction on each step](Naive.png)

![Labview block diagrams of the naive program](Naive_Labview.png)

### Improvement

* Eliminate retracting
* Change routing scheme to zig-zag

![illustration of no retracting scheme](No Retract.png)

Avoid discontinuities in $x, y$ direction.

![Straight-Forward routing scheme (left) vs. Zig-Zag routing scheme (right)](Zig-Zag.png)

## Modular Design & Developping

![Debugging interface on zig-zag routing scheme](/img/Scanning demo.gif)

![Modular diagram of improved driver. Measuring has been packaged into subVI.](Modular.png)

# Results

We can recover the shape of a wire using the prototype scanning probe, indicating that the prototype has reached Micron-level resolution.

![](Wire.png)