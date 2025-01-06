# Understanding Euler's Identity and Trigonometric Derivations

Euler's identity `e^(ix) = cos(x) + i*sin(x)` is a powerful tool for deriving trigonometric identities. Here's a breakdown:

## 1. Sum of Angles
Using `e^(i(a+b)) = e^(ia) * e^(ib)`, expand `(cos(a) + i*sin(a)) * (cos(b) + i*sin(b))`.

The real and imaginary parts of the expansion yield:
- `cos(a+b) = cos(a)*cos(b) - sin(a)*sin(b)`
- `sin(a+b) = sin(a)*cos(b) + cos(a)*sin(b)`

## 2. Expressing `sin(x)` and `cos(x)` Using `e^(ix)` and `e^(-ix)`
From `e^(ix) = cos(x) + i*sin(x)` and `e^(-ix) = cos(x) - i*sin(x)`:
- `cos(x) = (e^(ix) + e^(-ix)) / 2`
- `sin(x) = (e^(ix) - e^(-ix)) / (2i)`

## 3. Key Properties of Sine and Cosine
- **Sine is odd**: `sin(-x) = -sin(x)`
- **Cosine is even**: `cos(-x) = cos(x)`

---

# Simple Application of Euler’s Formula in AC Circuits

Euler's formula is commonly used in representing sinusoidal waveforms as complex numbers, simplifying calculations in alternating current (AC) circuits.

## Example: Representing a Sinusoidal Voltage Waveform
In AC circuits, voltages and currents often vary sinusoidally with time. For example:
`v(t) = V_m * cos(ωt + φ)`

Where:
- `V_m`: amplitude (maximum voltage)
- `ω`: angular frequency (`ω = 2πf`, where `f` is frequency)
- `φ`: phase angle

Using Euler’s formula, this can be rewritten as:
`v(t) = Re[V_m * e^(i(ωt + φ))]`

Instead of working directly with `cos(ωt + φ)`, we use its complex exponential form:
`V(t) = V_m * e^(i(ωt + φ))`

Here, the **real part** represents the physical voltage, while the **imaginary part** is useful for calculations.

## Why It’s Useful
1. **Simplifies AC Calculations**: Using the exponential form, adding, subtracting, and multiplying sinusoidal signals becomes easier, especially when considering phase differences.
2. **Phasors**: AC signals are represented as phasors (rotating vectors in the complex plane). Euler's formula is the foundation for this representation.

---

## Simple Application: Adding Two AC Voltages
Suppose two AC voltages have the same frequency but different amplitudes and phases:
- `v1(t) = 10 * cos(ωt)`
- `v2(t) = 5 * cos(ωt + π/3)`

Using Euler’s formula:
- `v1(t) = Re[10 * e^(iωt)]`
- `v2(t) = Re[5 * e^(i(ωt + π/3))]`

Add them in the complex plane:
`V_total = 10 * e^(iωt) + 5 * e^(i(ωt + π/3))`

This simplifies the addition using complex arithmetic. The result can then be converted back to the **real part** to obtain the physical waveform.

---

## Key Takeaway
Euler’s formula simplifies sinusoidal signal analysis in AC circuits, making it a cornerstone of circuit theory, particularly in **phasor analysis** and **impedance calculations**.

