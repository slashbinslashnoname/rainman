# Allée A — Tombes

Routes de preuve **mortes**, **bloquées**, **piégées** ou **artefacts de méthode**.

| ID | Hypothèse / route | Status | Découverte / leçon |
|----|-------------------|--------|-------------------|
| A1 | N premiers zéros sur la droite ⇒ RH | ENTERRÉE | Assertion ∀ ; vérif finie ≠ preuve |
| A2 | Robin/Lagarias check jusqu’à X ⇒ RH | ENTERRÉE | Contre-exemples possibles aux CA arbitrairement grands |
| A3 | Preuves arXiv « élémentaires » via partitions Lagarias | ENTERRÉE | Classes infinies non contrôlées ; non acceptées |
| A4 | Log complexe univoque (style Rademacher) | ENTERRÉE | Monodromie / branche ignorée |
| A5 | Hilbert–Pólya naïf (opérateur auto-adjoint ad hoc) | ENTERRÉE | Manque correspondance spectrale avec ζ |
| A6 | de Branges (positivité espaces de fonctions entières) | BLOQUÉE | Conrey–Li (2000) : positivités nécessaires échouent pour ζ |
| A7 | Denjoy « μ aléatoire ⇒ RH p.s. » | HEURISTIQUE | μ n’est pas i.i.d. |
| A8 | Speiser mal lu (« ξ′ suffit ») | PIÉGÉE | Équivalence vraie, pas plus facile |
| A9 | Transfert Weil/Deligne (corps finis) ⇒ RH sur ℤ | ENTERRÉE | Pas de Frobenius sur Spec ℤ |
| A10 | Turán anciennes sommes de puissances | ENTERRÉE | Haselgrove 1958 |
| A11 | Mertens \|M(x)\| < √x | FALSE_STRONG | Réfutée (Odlyzko–te Riele) ; implique RH mais fausse |
| A12 | Pólya L(x) ≤ 0 | FALSE_STRONG | Réfutée |
| A13 | Weil toy sans terme archimédien comme certificat | ENTERRÉE | Signe convention-sensible ; pas l’identité de référence |
| A14 | Li via `diff(log ξ)` naïf en s=1 | ARTEFACT | Pôle ζ(1) dans représentation ; méthode fragile |
| A15 | Jensen via produit ∏(1−z²/γ²) haut degré | ARTEFACT | Coeffs a_n n≥7 non convergés (rel change >100 %) |
| A16 | κ ≥ 2/3 ⇒ RH | ENTERRÉE | Affaiblissement ; plafond bande Fourier ≤1 |
| A17 | GUE / pair correlation ⇒ RH | HEURISTIQUE | Stats locales ≠ tous les zéros sur la ligne |
| A18 | ML / fit de zéros sans majoration | ENTERRÉE | Pas de preuve analytique |

## Pipeline auto-enterrement (false friends)

À rejeter d’office comme « preuves » :

1. Robin fini jusqu’à X  
2. Branche du log  
3. Opérateur Hilbert–Pólya circulaire  
4. Li / Keiper tronqué ⇒ RH  
5. Reformulation équivalente présentée comme démonstration  
6. N zéros numériques ⇒ RH  
7. Mollifier MSE fausse / θ injustifié  
8. Pair correlation sous RH recyclée inconditionnellement  
9. Beurling « fake primes » sans densité de Chebyshev  
10. Weil avec test function inadmissible  
11. Heuristique GUE = théorème  
12. Comptage multiplicités mal défini  
13. GRH ⇒ RH sans argument de densité  
14. « Preuve » ML / réseau  
15. Lagarias jusqu’à N ⇒ RH  

## Leçons transverses

- Un théorème `A ⇒ RH` est inutile si `A` est faux ou hors d’atteinte (de Branges).
- Une équivalence `A ⇔ RH` reformule ; elle ne résout pas.
- Un check fini d’un énoncé `∀` n’est jamais une preuve.
