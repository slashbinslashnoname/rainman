# Cimetière d'hypothèses — Conjecture de Riemann

**Projet :** rainman  
**Mode :** exploration structurée (pas de prétention de preuve)  
**Période :** 2026-08-11 → 2026-08-12  
**Statut global RH :** **OUVERTE**

---

## 0. Protocole

```
hypothèse → type?
  EQUIVALENCE seule        → GELER (oracle, pas preuve)
  FALSE_STRONG             → ENTERRER
  check fini d'un ∀        → ENTERRER comme preuve
  WEAKENING / OPEN_MICRO   → EXÉCUTER micro-exp
  STRUCTURAL sans objet    → BLOQUER
  résultat négatif clair   → TOMBE + leçon
  résultat positif partiel → CRYPTE + borne exacte
```

| Tag | Signification |
|-----|----------------|
| **ENTERRÉE** | Fausse, réfutée, ou morte comme *preuve* |
| **PIÉGÉE** | Équivalence correcte, pas plus facile que RH |
| **BLOQUÉE** | Programme sérieux, obstacle structurel |
| **OUVERTE** | Encore vivante ; partial results possibles |
| **HEURISTIQUE** | Indice fort, pas une démonstration |
| **ARTEFACT** | Échec numérique de méthode, pas de l'énoncé |

---

## 1. Décisions structurantes

1. **Ne pas promettre une preuve de RH.** Objectif = triage, calcul, archivage.
2. **Équivalence ≠ preuve.** Speiser, Robin, Lagarias, Li, NB, Weil, Jensen_all sont des oracles.
3. **Le fini ne tue pas l'infini.** N zéros, Robin jusqu'à X, λ_n jusqu'à N₀ ≠ RH.
4. **Enterrer vite les zombies** pour ne pas y reperdre du temps.
5. **Archiver en markdown** pistes, status, découvertes, RUN IDs.

---

## 2. Allée A — Tombes (routes de preuve mortes)

| # | Hypothèse / route | Status | Découverte / leçon |
|---|-------------------|--------|-------------------|
| A1 | N premiers zéros sur la droite ⇒ RH | ENTERRÉE | Assertion ∀ ; vérif finie ≠ preuve |
| A2 | Robin/Lagarias check jusqu'à X ⇒ RH | ENTERRÉE | Contre-exemples possibles aux CA arbitrairement grands |
| A3 | Preuves arXiv « élémentaires » via partitions Lagarias | ENTERRÉE | Classes infinies non contrôlées ; non acceptées |
| A4 | Log complexe univoque (style Rademacher) | ENTERRÉE | Monodromie / branche ignorée |
| A5 | Hilbert–Pólya naïf (opérateur auto-adjoint ad hoc) | ENTERRÉE | Manque correspondance spectrale avec ζ |
| A6 | de Branges (positivité espaces de fonctions entières) | BLOQUÉE | Conrey–Li (2000) : positivités nécessaires échouent pour ζ |
| A7 | Denjoy « μ aléatoire ⇒ RH p.s. » | HEURISTIQUE | μ n'est pas i.i.d. |
| A8 | Speiser mal lu (« ξ′ suffit ») | PIÉGÉE | Équivalence vraie, pas plus facile |
| A9 | Transfert Weil/Deligne (corps finis) ⇒ RH sur ℤ | ENTERRÉE | Pas de Frobenius sur Spec ℤ |
| A10 | Turán anciennes sommes de puissances | ENTERRÉE | Haselgrove 1958 |
| A11 | Mertens \|M(x)\| < √x | FALSE_STRONG | Réfutée (Odlyzko–te Riele) ; implique RH mais fausse |
| A12 | Pólya L(x) ≤ 0 | FALSE_STRONG | Réfutée |
| A13 | Weil toy sans terme archimédien comme certificat | ENTERRÉE | Signe convention-sensible ; pas l'identité de référence |
| A14 | Li via `diff(log ξ)` naïf en s=1 | ARTEFACT | Pôle ζ(1) dans représentation ; méthode fragile |
| A15 | Jensen via produit ∏(1−z²/γ²) haut degré | ARTEFACT | Coeffs a_n n≥7 non convergés (rel change >100%) |
| A16 | κ ≥ 2/3 ⇒ RH | ENTERRÉE | Affaiblissement ; plafond bande Fourier ≤1 |
| A17 | GUE / pair correlation ⇒ RH | HEURISTIQUE | Stats locales ≠ tous les zéros sur la ligne |
| A18 | ML / fit de zéros sans majoration | ENTERRÉE | Pas de preuve analytique |

### Pipeline auto-enterrement (false friends)

1. Robin fini jusqu'à X  
2. Branche du log  
3. Opérateur HP circulaire  
4. Li / Keiper tronqué ⇒ RH  
5. Reformulation équivalente présentée comme démonstration  
6. N zéros numériques ⇒ RH  
7. Mollifier MSE fausse  
8. Pair correlation sous RH recyclée inconditionnellement  
9. Beurling « fake primes »  
10. Weil avec test function inadmissible  
11. Heuristique GUE = théorème  
12. Comptage multiplicités mal défini  
13. GRH ⇒ RH sans argument  
14. Preuve ML  
15. Lagarias jusqu'à N ⇒ RH  

---

## 3. Allée B — Cryptes ouvertes / partial

| # | Formulation | Status | Obstacle | Micro-exp faite |
|---|-------------|--------|----------|-----------------|
| B1 | Nyman–Beurling / Báez-Duarte | OUVERTE | densité L² | d_N ↓ 0.62→0.18 (N=4→80) |
| B2 | Balazard–Saias–Yor intégrale | OUVERTE | oscillations | tronqué seulement |
| B3 | Li λ_n ≥ 0 | OUVERTE | ill-conditionné | λ_n>0 via zéros (n≤50 trunc) |
| B4 | Weil positivity (maître) | OUVERTE | signature = RH | toy + arch indicatif |
| B5 | Hilbert–Pólya sérieux (BK, Connes) | BLOQUÉE/OUVERTE | domaine, bords, primes | non construit |
| B6 | Jensen / Laguerre–Pólya | PARTIELLE | uniformité d,n | GORZ large-n ; diag d≤7 OK |
| B7 | Densité de zéros N(σ,T) | PARTIELLE | perte près σ=1/2 | littérature Guth–Maynard |
| B8 | Proportion κ = liminf N₀/N | PARTIELLE | barrière λ≤1 | classique ~41.7% ; annonce 2026 ~67% **NEEDS_VERIFICATION** |
| B9 | Robin/Lagarias structurels (tous CA) | OUVERTE | asymptotique CA | hold sur échantillon HC/CA |
| B10 | Gram Beurling / Vasyunin | OUVERTE | N fini | PSD + Cholesky N≤100 |

---

## 4. Journal des RUN

### RUN 1 — Weil toy φ = e^{-at²} cos(bt)
- Grid min W négatif **sans** arch → toy incomplet  
- **Tag :** ENTERRER comme certificat  

### RUN 2 — Vasyunin/Beurling Gram
- N=10..40 : min eig >0, Cholesky OK, mineurs leaders >0  
- **Tag :** OUVERT (support)  

### RUN 3 — d_N asymptotique
- N=4→42 : d_N 0.62→0.25 ; fit plus raide que ½ log log  
- **Tag :** OUVERT  

### RUN 4 — Jensen diagonal d=n
- Y pour d≤7 ; N à d≥8  
- **Découverte :** artefact troncature produit (a_n non convergés)  
- **Tag :** ARTEFACT méthode, pas enterrement de Jensen  

### RUN 5 — Matrice d'implications
- 8+ équivalences classiques ⇔ RH  
- Mertens / zeros_to_T / GUE / κ≥2/3 : ne prouvent pas RH  

### RUN 6 — Zero-pushing (1 zéro)
- Premier zéro → quadruplet FE : Δλ₁₀ ≈ +0.48  
- Sensibilité δ faible ; effet structurel dominant  

### RUN 7 — Weil + digamma arch
- w2 >0 sur grille a (indicatif)  
- Convention Fourier non calibrée sur papier de référence  
- **Tag :** OUVERT, pas certificat  

### RUN 8 — Gram N≤80
- min eig ~1.6e-2 à N=80, cond ~3e6, Cholesky OK  

### RUN 9 — d_N N≤80 + fit Burnol
- Monotone ; d_80/d_4 ≈ 0.29  
- α empirique ~1.69 vs barrière Burnol 0.5  

### RUN 10 — Li via dérivées log ξ
- n impairs OK (λ>0) ; n pairs ERROR pôle  
- **Tag :** méthode dérivée naïve ENTERRÉE  

### RUN 11 — Multi-zero push
- Δλ₁₀ ≈ +0.48 (m=1), +0.70 (m=2), +1.06 (m=5), +1.32 (m=10)  
- Scaling approximativement additif en m  

### RUN 12–15 — (session archive)
- Li zeros-sum stable  
- d_N / Gram poussés  
- Taxonomie figée  
- Scaling push documenté  

---

## 5. Audit κ ≈ 67% (annonce août 2026)

| Champ | Contenu |
|-------|---------|
| Claim | liminf N₀/N ≥ 2/3, optimisé ≈ 0.6725 |
| Méthode | Gram Weil + rank–trace + pair correlation λ≤1 (BGSTB) |
| Avant | Levinson/Conrey/… ≈ 41.7% (mollifiers) |
| Tag | **NEEDS_VERIFICATION** |
| Prouve RH ? | **Non** — plafond ~0.68 en bande 1 ; argument type Davenport–Heilbronn |

---

## 6. Équivalences figées (oracles)

```
RH  <=>  Weil_pos  <=>  Li_pos  <=>  NB_density
    <=>  Robin  <=>  Lagarias  <=>  Speiser  <=>  Riesz
    <=>  Jensen_all  <=>  kappa_1
```

**Weakenings (n'impliquent pas RH) :** κ≥2/3, zero-density estimates, zeros jusqu'à T  
**False-strong :** Mertens, Turán old, Pólya L(x)≤0  

---

## 7. Découvertes numériques (résumé)

| Observation | Interprétation |
|-------------|----------------|
| 20+ premiers zéros Re=1/2 | Cohérent ; pas une preuve |
| Robin hold sur CA/HC >5040 (échantillon) | Cohérent ; seuil 5040 classique (échec à 5040) |
| Gram Beurling PSD N≤100 | Pas de bombe anti-RH |
| d_N monotone décroissante | Compatible densité NB |
| λ_n trunc >0 | Support faible |
| Zero-push Δλ proportionnel à m | Détecteur structurel opérationnel |
| Jensen haut degré « N » | Artefact troncature, pas violation |

---

## 8. Ce qui n'a **pas** été accompli

- Preuve de RH  
- Contre-exemple à RH  
- Weil calibré sur identité publiée + SDP complet  
- Li arithmétique Bombieri–Lagarias multiprécision robuste  
- d_N pour N≫500  
- Audit Lean complet de l'annonce κ≈67%  

---

## 9. Priorités suivantes (si reprise)

1. Weil **référencé** (formule Guinand–Weil d'un papier + base test)  
2. Li arithmétique (primes + Γ, sans pôle s=1)  
3. d_N N=200–500  
4. Jensen via Taylor Ξ / Stieltjes (pas produit tronqué)  
5. Audit indépendant claim κ≥2/3  

---

## 10. Méta

- **Langue de travail :** français (requête utilisateur)  
- **Outils :** mpmath, numpy, calcul local  
- **Règle d'or :** enterre ce qui est mort ; ne force pas ce qui est ouvert  
- **Score session :** ~18 routes de « preuve facile » enterrées ; oracles numériques stables ; RH toujours ouverte  

---

*Dernière mise à jour : 2026-08-12 — archivage markdown rainman*
