# dB Calculator

RF level toolkit in a single, dependency-free HTML page. Works offline; nothing leaves the browser.

**Live:** https://takewada.github.io/db-calculator/

## Tools

| Tool | What it does |
|---|---|
| **dBm Calculator** | Add / subtract any number of power levels in dBm, dBW, W, mW, µW. Levels are summed as watts. |
| **Voltage Calculator** | Add / subtract voltage levels (V, mV, dBV, dBµV) at a common impedance, either **uncorrelated** (√ΣV²) or **correlated** (ΣV). |
| **Unit Converter** | Enter one value in dBm, dBW, mW, W, mV, V, dBV, dBµV or dBu and get all the others, for any impedance. dBu is referenced to 0.775 V. |
| **dB Converter** | Linear power ratio ⇄ dB (10·log₁₀) or voltage/field ratio ⇄ dB (20·log₁₀). |
| **VSWR Converter** | VSWR ⇄ reflection coefficient Γ ⇄ return loss; also mismatch loss, reflected power % and — given a forward power/voltage — the reflected power/voltage. |

## Formulas

```
P[W]      = 10^(dBm/10) / 1000            dBW  = dBm − 30
V[V]      = √(P·Z)                        P    = V² / Z
dBV       = 20·log10(V)                   dBµV = dBV + 120
dBu       = 20·log10(V / 0.775)
Γ         = (VSWR−1)/(VSWR+1)             VSWR = (1+Γ)/(1−Γ)
RL[dB]    = −20·log10(Γ)                  ML[dB] = −10·log10(1−Γ²)
P_refl    = Γ²·P_fwd                      V_refl = Γ·V_fwd
```

## Usage

Open `index.html` in any browser, or visit the GitHub Pages link above. Light / auto / dark theme switch is in the header; the choice is remembered per browser.

## License

MIT
