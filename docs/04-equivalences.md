# Équivalences, weakenings, false-strong

## Équivalences figées (oracles)

Toutes ⇔ RH. **Geler** comme routes de « preuve gratuite ».

```
RH  <=>  Weil_pos  <=>  Li_pos  <=>  NB_density
    <=>  Robin  <=>  Lagarias  <=>  Speiser  <=>  Riesz
    <=>  Jensen_all  <=>  kappa_1
```

| Critère | Forme courte |
|---------|----------------|
| Weil | positivité de la forme explicite sur tests admissibles |
| Li | λ_n ≥ 0 pour tout n ≥ 1 |
| NB / Báez-Duarte | densité de dilatations de {1/x} dans L² |
| Robin | σ(n) < e^γ n log log n pour n > 5040 |
| Lagarias | σ(n) ≤ H_n + exp(H_n) log H_n pour tout n ≥ 1 |
| Speiser | ξ′ sans zéro dans 0 < Re s < 1/2 |
| Riesz | fonction de Riesz ≪ x^{1/4+ε} |
| Jensen_all | tous les polynômes de Jensen de ξ hyperboliques |
| kappa_1 | tous les zéros non triviaux sur Re = 1/2 |

## Weakenings (n’impliquent **pas** RH)

| Énoncé | Commentaire |
|--------|-------------|
| κ ≥ 2/3 (ou 0.6725) | proportion sur la ligne ; plafond méthode bande ≤1 |
| Zero-density N(σ,T) ≪ … | presque tous près de la ligne, pas tous sur la ligne |
| Zéros vérifiés jusqu’à T | région finie seulement |
| Jensen pour d fixé, n grand (GORZ) | partial ; gap uniformité en d |

## False-strong (impliquent RH mais **faux**)

| Énoncé | Status |
|--------|--------|
| Mertens \|M(x)\| < √x | réfutée (Odlyzko–te Riele) |
| Turán anciennes power sums | réfutée (Haselgrove) |
| Pólya L(x) ≤ 0 | réfutée |
| M(x) = O(√x) sans logs | probablement faux ; plus fort que RH |
| ψ(x) = x + O(√x) sans logs | Ω-results connus |

## Heuristiques (pas des preuves)

- GUE / pair correlation (Montgomery–Odlyzko)
- Denjoy (μ comme marche aléatoire)
- Berry–Keating xp (spectre formel)
- Moments Keating–Snaith / CFKRS
