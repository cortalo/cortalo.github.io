---
title:  "Analog Circuits"
date:   2023-07-30 07:00:00 +0200
categories: analog-circuit
tags: analog
math: true
---

# Impedance Formula

$$
R \Vert \dfrac{1}{sC} = \dfrac{R}{1+sRC}
$$

# Oscillator

From [Prof. Jri Lee's Lectures](https://space.bilibili.com/1629031600)

## Barkhausen Criteria

If the closed-loop transfer function is

$$
H(s) = \dfrac{A(s)}{1+A(s)\beta(s)}
$$

then for oscillator

$$
A(j\omega_o)\beta(j\omega_o) = -1
$$

When the oscillator just starts to oscillate, we can use small signal model.
It must be unstable at the equilibrium point, thus from the concept of gain margin

$$
\begin{align}
\angle A(j\omega_{\text{x}})\beta(j\omega_{\text{x}}) &= -180^\circ\\
\vert A(j\omega_{\text{x}})\beta(j\omega_{\text{x}}))\vert &> 1
\end{align}
$$

## Wien-Bridge Oscillator

<img src="/assets/img/2023-07-30-analog-circuits/001.png" style="width:50%;height:50%;">

we assume the input is at

<img src="/assets/img/2023-07-30-analog-circuits/002.png" style="width:50%;height:50%;">

let

$$
\begin{align}
Z_p &= \dfrac{R}{1+sRC}\\
Z_s &= R + \dfrac{1}{sC}
\end{align}
$$

the closed-loop transfer function can be calculated as

$$
H(s) = \dfrac{V_{out}(s)}{V_{in}(s)} = \dfrac{(R_1 + R_2)/R_1}{1 - \dfrac{R_2}{R_1} \dfrac{Z_p}{Z_s}}
$$

$$
\dfrac{R_2}{R_1} \dfrac{Z_p}{Z_s} = \dfrac{R_2}{R_1} \dfrac{j\omega RC}{1-\omega^2 R^2C^2 + 2j\omega RC}
$$

$$
\omega_x = \dfrac{1}{RC}
$$

$$
\dfrac{R_2}{2R_1} > 1
$$

## Impedance Transformation

For inductor

$$
Q = \dfrac{\omega L_s}{R_s} = \dfrac{R_p}{\omega L_p}
$$

if $$Q$$ is large, $$L_s \approx L_p$$ (with error $$1 + \dfrac{1}{Q^2}$$)

$$
R_s R_p = (\omega L)^2
$$

For capacitor

$$
Q = \dfrac{1}{\omega R_s C_s} = \omega R_p C_p
$$

if $$Q$$ is large, $$C_s \approx C_p$$ (with error $$1 + \dfrac{1}{Q^2}$$)

$$
R_s R_p = \dfrac{1}{(\omega C)^2}
$$

## Colpitts Oscillator

<img src="/assets/img/2023-07-30-analog-circuits/003.png" style="width:50%;height:50%;">

<img src="/assets/img/2023-07-30-analog-circuits/006.png" style="width:70%;height:70%;">