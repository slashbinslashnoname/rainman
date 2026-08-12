# Découvertes numériques consolidées

> Support ou stress-test uniquement. **Aucun** de ces résultats n’est une preuve de RH.

## Zéros bas

- Premiers zéros non triviaux (mpmath) : Re = 1/2 (cohérent avec les tables connues).

## Robin / Lagarias (échantillon)

- Échec classique de Robin à n = 5040 (d’où le seuil).
- Hold sur un échantillon de nombres hautement / colossalement abondants > 5040 (jusqu’~10¹² dans les runs).
- **Ne prouve pas** l’inégalité pour tous les n.

## Gram Beurling / Vasyunin

| N | min eig (ordre) | Cholesky |
|---|-----------------|----------|
| 10 | ~3e-2 | OK |
| 40 | ~1.8e-2 | OK |
| 80 | ~1.6e-2 | OK |
| 100 | >0 | OK |

- Conditionnement croît fortement avec N (attendu).
- Aucun mineur ≤ 0 observé sur les plages testées.

## d_N (Nyman–Beurling, résidu L²)

| N | d_N (approx) |
|---|--------------|
| 4 | 0.62 |
| 20 | 0.34 |
| 40 | 0.25 |
| 80 | 0.18 |

- **Monotone décroissante** sur les plages testées.
- d_80 / d_4 ≈ 0.29.
- d_N² log N encore en baisse (pas collé à une constante type Burnol).
- Fit empirique log d_N vs log(log N) plus raide que α = 1/2.

## Li λ_n (somme tronquée sur zéros)

- λ_n > 0 pour les n testés (troncature 100–150 zéros).
- Écart à l’asymptotique ½ n log n dû à la troncature.
- Dérivation naïve de log ξ en s=1 : **instable** (pôle) — méthode abandonnée.

## Zero-pushing

| m zéros poussés (quadruplet FE) | Δλ₁₀ (ordre) |
|----------------------------------|--------------|
| 1 | +0.48 |
| 2 | +0.70 |
| 5 | +1.06 |
| 10 | +1.32 |

- Effet dominant = structure off-line (2 → 4 facteurs), pas la taille fine de δ.
- Détecteur structurel utile ; λ trunc > 0 **ne certifie pas** RH.

## Jensen (produit tronqué)

- Hyperbolicité OK pour d≤7 en proxy produit.
- Échecs apparents d≥8 : **artefact** — coefficients a_n non convergés quand on augmente le nombre de zéros dans le produit.

## Session 2026-08-11/12 (avec Claude) — consolidé

| Découverte | Valeur | Statut |
|------------|--------|--------|
| Reproduction §8(1) | N(I)=472, Ĝ⪰0, M2=1,386 vs 1,387 | ORACLE stable |
| Hiérarchie certificats sur vrais zéros | cert2≈0,65–0,68 < cert4≈0,70–0,72 (cible 13/18) | mesuré, 6 hauteurs |
| Correction de taper | excès M2 = (b+λ₁²J)/a² − 4/3 ∝ η ; vérifiée à 3 valeurs de η | falsifiée-et-survécue |
| Courbe famille | H_fam(λ)=1−1/(3λ²) ; 2/3 (λ=1) ↔ 11/12 (λ=2) | folklore (CLLR Lemme 9) |
| Contrôle Poisson | M4≈17,6 vs 3,25 attendu | discriminant du pipeline |

**Rétractations honnêtes de la session :** « excès arithmétique dû aux premiers » (mesure initiale +4–7 %) → réattribué au taper + convention de fenêtre (A22) ; premières valeurs m5/m6 → invalidées (pipeline non calibré au moment de la mesure).
