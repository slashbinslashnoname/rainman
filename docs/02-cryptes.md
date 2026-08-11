# Allée B — Cryptes ouvertes / partial

Pistes encore **vivantes** : équivalences non prouvées, affaiblissements productifs, programmes structurels.

| ID | Formulation | Status | Obstacle | Micro-exp faite |
|----|-------------|--------|----------|-----------------|
| B1 | Nyman–Beurling / Báez-Duarte | OUVERTE | densité L² | d_N ↓ 0.62→0.18 (N=4→80) |
| B2 | Balazard–Saias–Yor intégrale | OUVERTE | oscillations | tronqué seulement |
| B3 | Li λ_n ≥ 0 | OUVERTE | ill-conditionné | λ_n>0 via zéros (n≤50 trunc) |
| B4 | Weil positivity (maître) | OUVERTE | signature = RH | toy + arch indicatif |
| B5 | Hilbert–Pólya sérieux (BK, Connes) | BLOQUÉE/OUVERTE | domaine, bords, primes | non construit |
| B6 | Jensen / Laguerre–Pólya | PARTIELLE | uniformité d,n | GORZ large-n ; diag d≤7 OK (trunc) |
| B7 | Densité de zéros N(σ,T) | PARTIELLE | perte près σ=1/2 | littérature Guth–Maynard |
| B8 | Proportion κ = liminf N₀/N | PARTIELLE | barrière λ≤1 | classique ~41.7 % ; annonce 2026 ~67 % (**NEEDS_VERIFICATION**) |
| B9 | Robin/Lagarias structurels (tous CA) | OUVERTE | asymptotique CA | hold sur échantillon HC/CA |
| B10 | Gram Beurling / Vasyunin | OUVERTE | N fini | PSD + Cholesky N≤100 |

## Notes par crypte

### B1 — Nyman–Beurling
d_N monotone décroissante jusqu’à N=80. Fit empirique plus raide que la barrière inférieure de Burnol (~1/√log N). Pas de stagnation qui enterrerait la densité.

### B3 — Li
Positivité observée en troncature (somme sur zéros). La dérivation naïve de log ξ en s=1 est un **artefact** (voir A14). Préférer formule arithmétique Bombieri–Lagarias.

### B4 — Weil
Toute positivité complète sur la classe de test admissible ⇔ RH. Les jouets numériques sans calibration de référence ne sont pas des certificats (A13).

### B6 — Jensen
Hyperbolicité pour d fixe et n grand : progrès GORZ 2019. Les « N » à d≥8 via produit tronqué sont des artefacts de coefficients non convergés (A15).

### B8 — κ
Voir [06-audit-kappa.md](06-audit-kappa.md). Affaiblissement productif ; **ne prouve pas** RH.
