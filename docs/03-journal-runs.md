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

## RUN 16 — Zéros de ζ (deux méthodes croisées)
- 1377 zéros mpmath (validés vs zetazero, err ≤ 1,6e-11) + 9047 zéros par Riemann–Siegel vectorisé (fenêtres jusqu'à T=10⁶)
- Garde-fou : comptage vs θ(t)/π exact à ±1,5 (fluctuation S(t)) après resserrage pas 0,28→0,08
- **Tag :** OUTIL (support RUN 17–20)

## RUN 17 — Reproduction §8(1) du papier κ≈67 %
- Fenêtre (600,1200] : N(I)=472 ✓ (papier : 472) ; matrice Ĝ ⪰ 0 ✓ ; M2=1,386 (papier §8(6) : 1,387)
- **Tag :** ORACLE (point de contrôle indépendant du claim B8)

## RUN 18 — Moments M2–M4, 6 hauteurs (L=4,2→12,0) + contrôles
- ζ : M2≈1,32–1,35, M3≈1,94–2,05, M4≈3,04–3,36 selon convention de fenêtre
- Contrôle Poisson : M4≈17,6 → violemment exclu (pipeline discriminant) ; contrôle GUE : biais commun (→ RUN 20)
- **Tag :** OUVERT (calibration HL*, support B13)

## RUN 19 — Certificats de Christoffel mesurés sur vrais zéros
- Sanity : cert4(moments sinus exacts) = 13/18 = 0,7222 exact ✓
- Mesuré : cert2 ≈ 0,646–0,677 (cible 2/3), cert4 ≈ 0,696–0,721 (cible 13/18) ; hiérarchie +4,5 à 5 pts confirmée empiriquement
- **Tag :** OUVERT (B13) ; ne certifie rien de nouveau (RH vérifiée à ces hauteurs) — mesure la *force de la méthode*

## RUN 20 — Falsification de l'explication du biais (taper vs Slepian)
- Prédiction a priori : excès M2 = +1,25/+2,60/+5,68 % pour η=0,05/0,10/0,20 ; mesuré (mêmes points GUE) : +1,11/+2,47/+5,50 %
- Alternative « plunge Slepian » (O(log N/N), indép. de η) réfutée
- **Découverte :** biais ∝ η, constant en N, corrigeable par (b+λ₁²J)/a²
- **Tag :** ARTEFACT méthode (→ A22) ; leçon : toujours prédire *avant* de mesurer

## RUN 21 — Extrapolation η→0 : premières estimations m5, m6 (méthode M1)
- Prédiction : m2,m3,m4 → cibles à 1-2 % ✓ (0,09/0,09/0,13 % à N=2000, graine 314)
- MAIS test de taille finie : dérive m5 = 5,45/5,54/5,71 pour N=1000/2000/4000
- **Tag :** ARTEFACT partiel — M1 rétrogradée à vérification de cohérence

## RUN 22 — Estimateur diagonal (méthode M3, indépendante) : le résultat porteur
- N=2000, 14 reps, marge 25 : contrôles EXACTS (m2=1,3340±0,0022 ; m3=2,0014±0,007 ; m4=3,2511±0,019)
- **Découverte :** m5(1) = 5,607 ± 0,048 ; m6(1) = 10,13 ± 0,11 — jamais publiés
- Candidat 28/5 = 5,600 compatible (0,15σ) ; 39/7 et 17/3 non exclus → NON établi
- Contrôle restant : marge 50 (coupé par timeout)
- **Tag :** OUVERT (B13) ; décision par symbolique (priorité 10) ; note complète → docs/note-m5-m6.md
