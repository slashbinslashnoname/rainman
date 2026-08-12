# Note — Premières estimations numériques des moments spectraux m₅(1) et m₆(1) du noyau sinus

**Auteurs : Romain Lafforgue · Claude Fable 5 (Anthropic)**
Session des 11–12 août 2026 · dépôt `rainman` · statut : note numérique, non revue par les pairs

---

## Résumé

Nous donnons les premières estimations numériques des moments spectraux limites d'ordre 5 et 6 de la matrice de Gram à noyau sinus sur le processus sinus à densité 1 :

> **m₅(1) = 5,61 ± 0,05  ·  m₆(1) = 10,13 ± 0,11**

Ces quantités sont l'entrée manquante du certificat de Christoffel à 6 moments évoqué au §7.5 du papier « More than two thirds of the zeros of the Riemann zeta function lie on the critical line » (Claude/Anthropic, août 2026), dont les moments publiés s'arrêtent à m₄ = 13/4. À notre connaissance, m₅ et m₆ n'apparaissent nulle part dans la littérature (diligence effectuée : Rudnick–Sarnak, Hejhal, Bogomolny–Keating, Chirre–Gonçalves–de Laat, Gonçalves–de Laat–Leijenhorst, littérature des opérateurs à noyau sinus tronqués).

La valeur rationnelle **28/5 = 5,600 est compatible avec m₅ à 0,15 écart-type** ; nous la signalons comme **candidat conjectural**, sans l'établir : les rationnels voisins 39/7 = 5,5714 et 17/3 = 5,6667 ne sont pas exclus au niveau de précision atteint. La décision relève du calcul symbolique (expansion en partitions, §5).

## 1. Objet

Soit S(u) = sin(πu)/(πu) et {xᵢ} le processus déterminantal sinus à densité 1 (corrélations ρ_b = det[S(xᵢ−xⱼ)]). On définit

  m_k(1) = lim_{N→∞} E[ tr Ĝᵏ ] / N,  Ĝᵢⱼ = S(xᵢ−xⱼ).

Valeurs connues (papier Claude §7.5(f)) : m₁ = 1, m₂ = 4/3, m₃ = 2, m₄ = 13/4. Nous avons re-dérivé analytiquement m₂ = 4/3 et m₃ = 2 par l'expansion en partitions (les intégrales se réduisent à ∫S² = 1, ∫S⁴ = 2/3, ∫ĝ³ = 1/2 avec ĝ le noyau triangle ; le terme connexe triple s'annule exactement), validant le cadre.

## 2. Méthodes (deux, indépendantes)

**M1 — pipeline de Gabor + extrapolation η→0.** Grille τ à pas h = 2π/L (L = 2π, λ = 1), taper C³ à rampe relative η, points GUE dépliés à densité 1 (universalité de Gaudin–Mehta), moments spectraux de Ĝ = G/(aL²), puis extrapolation linéaire/quadratique en η ∈ {0,03 ; 0,08 ; 0,15}. Le biais de taper (∝ η, constant en N) a été prédit par la formule (b+λ₁²J)/a² puis vérifié par falsification directe (excès M₂ mesuré +1,11/+2,47/+5,50 % pour η = 0,05/0,10/0,20, prédit +1,25/+2,60/+5,68 %).

**M3 — estimateur diagonal (méthode de référence).** Matrice brute Ĝ sur une fenêtre du bulk GUE déplié, moments estimés par la moyenne des entrées diagonales (Ĝᵏ)ᵢᵢ sur les points de cœur (marge m du bord de fenêtre). Aucun taper, aucune grille, aucune extrapolation : zéro paramètre commun avec M1.

## 3. Résultats et tests de robustesse

**Validation (M3, N = 2000, 14 répliques, marge 25) — les trois contrôles tombent sur leurs cibles :**

| moment | mesuré | cible exacte | écart |
|---|---|---|---|
| m₂ | 1,3340 ± 0,0022 | 4/3 = 1,3333 | +0,3σ |
| m₃ | 2,0014 ± 0,007 | 2 | +0,2σ |
| m₄ | 3,2511 ± 0,019 | 13/4 = 3,25 | +0,06σ |
| **m₅** | **5,6071 ± 0,048** | inconnu | — |
| **m₆** | **10,133 ± 0,114** | inconnu | — |

**Tests de torture effectués :**
1. *Taille finie (M1)* : m₅ extrapolé dérive avec N (5,45/5,54/5,71 pour N = 1000/2000/4000) → M1 rétrogradée au rang de vérification de cohérence ; son accord avec M3 (±0,1) est satisfait mais c'est M3 qui porte l'estimation.
2. *Dépendance de modèle (M1)* : linéaire vs quadratique en η, écarts ≤ 0,1 — secondaire devant la dérive en N.
3. *Dépendance de marge (M3)* : marge 10 → sous-estimation (contamination de bord : m₄ = 3,216) ; marge 25 → contrôles exacts. **Contrôle restant à faire : marge 50** (coupé par limite de calcul) — si les valeurs remontaient encore, l'estimation serait à réviser à la hausse.
4. *Prédiction avant mesure* : toutes les valeurs de contrôle ont été prédites avant exécution (protocole du RUN 20).

## 4. Ce que cela permet — et ne permet pas

Avec (1, 1, m₂, m₃, m₄, m₅, m₆) on peut évaluer numériquement le certificat de Christoffel Λ₃(0) à 6 moments (masse minimale de multiplicité simple), prochain barreau de l'échelle 2/3 → 13/18 → … → 100 % du §7.5 du papier. **Mise en garde** : ce certificat resterait doublement conditionnel (asymptotique des moments d'ordre >2 hors plage Rudnick–Sarnak à λ = 1 ; et « 100 % » signifierait densité 1, pas RH). Rien ici ne rapproche de RH ; cela calibre la force d'une méthode.

## 5. Question ouverte (le juge de paix)

Calculer m₅(1) exactement par l'expansion en partitions (52 partitions de {1,…,5} ; intégrales de cluster réductibles par idempotence S⋆S = S aux intégrales ∫S^{2p} et aux volumes de sections de cubes en Fourier — tous rationnels). Verdict attendu : m₅ ∈ ℚ ; le candidat 28/5 est alors confirmé ou réfuté. Idem m₆ (203 partitions).

## 6. Reproductibilité

Scripts de la session : `eta_test.py` (falsification du taper), `eta_extrap.py` (M1), `torture1.py` (tests 1–2), `torture2.py` (M3). GUE N = 2000, dépliage par CDF semi-circulaire, graine explicite dans chaque script. Erreurs = écart-type de la moyenne sur répliques indépendantes.

## Attribution et honnêteté

Exploration, calculs et rédaction : Claude Fable 5 (Anthropic), sous direction, questions sceptiques et décisions de Romain Lafforgue. Le cadre mathématique appartient au papier Claude/Anthropic (août 2026) et à la littérature citée. Cette note a volontairement **rétrogradé** sa revendication initiale (« m₅ = 28/5 ») après échec partiel du test de taille finie de M1 : la revendication finale est l'estimation avec barres d'erreur, le rationnel n'étant qu'un candidat. Les résultats négatifs des tests figurent au journal (`docs/03-journal-runs.md`, RUN 20–22).
