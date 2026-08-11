# Journal des RUN

Expériences numérotées. Chaque RUN a un **tag cimetière** (preuve / oracle / artefact).

## RUN 1 — Weil toy φ = e^{-at²} cos(bt)
- Grid min W négatif **sans** arch → toy incomplet  
- **Tag :** ENTERRER comme certificat (→ A13)

## RUN 2 — Vasyunin / Beurling Gram
- N=10…40 : min eig >0, Cholesky OK, mineurs leaders >0  
- **Tag :** OUVERT (support B10)

## RUN 3 — d_N asymptotique
- N=4→42 : d_N 0.62→0.25 ; fit plus raide que ½ log log  
- **Tag :** OUVERT (B1)

## RUN 4 — Jensen diagonal d=n
- Y pour d≤7 ; N à d≥8  
- **Découverte :** artefact troncature produit (a_n non convergés)  
- **Tag :** ARTEFACT méthode (→ A15), pas enterrement de Jensen

## RUN 5 — Matrice d’implications
- 8+ équivalences classiques ⇔ RH  
- Mertens / zeros_to_T / GUE / κ≥2/3 : ne prouvent pas RH  
- **Tag :** taxonomie figée (voir 04-equivalences)

## RUN 6 — Zero-pushing (1 zéro)
- Premier zéro → quadruplet FE : Δλ₁₀ ≈ +0.48  
- Sensibilité δ faible ; effet structurel dominant  

## RUN 7 — Weil + digamma arch
- w2 >0 sur grille a (indicatif)  
- Convention Fourier non calibrée sur papier de référence  
- **Tag :** OUVERT, pas certificat

## RUN 8 — Gram N≤80
- min eig ~1.6e-2 à N=80, cond ~3e6, Cholesky OK  

## RUN 9 — d_N N≤80 + fit Burnol
- Monotone ; d_80/d_4 ≈ 0.29  
- α empirique ~1.69 vs barrière Burnol 0.5  

## RUN 10 — Li via dérivées log ξ
- n impairs OK (λ>0) ; n pairs ERROR pôle  
- **Tag :** méthode dérivée naïve ENTERRÉE (→ A14)

## RUN 11 — Multi-zero push
- Δλ₁₀ ≈ +0.48 (m=1), +0.70 (m=2), +1.06 (m=5), +1.32 (m=10)  
- Scaling approximativement additif en m  

## RUN 12 — Li zeros-sum + asymptotique
- λ_n >0 pour n testés (trunc 100 zéros)  
- Ratio vs ½ n log n incomplet (troncature)

## RUN 13 — d_N / Gram N=100
- d_N continue de baisser ; Gram PSD, Cholesky OK à N=100  

## RUN 14 — Taxonomie d’équivalences
- Closure documentée dans 04-equivalences.md  

## RUN 15 — Zero-push scaling
- Δ/m relativement stable ; détecteur structurel opérationnel  

---

## Synthèse tags RUN

| RUN | Tag principal |
|-----|----------------|
| 1, 7, 10, 13 (méthode Weil/Li fragile) | artefact / pas certificat |
| 2, 3, 8, 9, 12, 13 | oracle numérique stable |
| 4 | artefact Jensen produit |
| 5, 14 | taxonomie |
| 6, 11, 15 | détecteur zero-push |
