# Priorités si reprise

Ordre suggéré (haut levier / faible zombie-risk).

| # | Action | Crypte liée | Pourquoi |
|---|--------|-------------|----------|
| 1 | Weil **calibré** sur une identité publiée + base de test | B4 | Corrige A13 ; seul chemin « maître » |
| 2 | Li arithmétique (Bombieri–Lagarias / primes + Γ) | B3 | Évite le pôle s=1 (A14) |
| 3 | d_N pour N=200–500 (grille fine) | B1 | Approcher la constante de Burnol |
| 4 | Jensen via Taylor Ξ / Stieltjes (pas produit) | B6 | Évite A15 |
| 5 | Audit indépendant claim κ≈67 % | B8 | NEEDS_VERIFICATION → confirmer ou nuancer |
| 6 | Gram Beurling multiprécision N≪100+ | B10 | Stress conditionnement |
| 7 | Zero-push + forme de Weil complète | détecteur | Pédagogie / alarme, pas preuve |

## Ne pas refaire

- Checks finis présentés comme preuves (A1, A2)  
- Weil toy non calibré comme certificat (A13)  
- Li via `diff(log ξ)` naïf (A14)  
- Jensen produit haut degré non convergé (A15)  
- « κ élevé ⇒ RH » (A16)  
- GUE / Denjoy / HP naïf comme preuves (A5, A7, A17)

## Score session (2026-08-11/12)

| Métrique | Valeur |
|----------|--------|
| Routes « preuve facile » enterrées | ~18 |
| Oracles numériques stables | Gram, d_N↓, λ trunc>0, zéros bas |
| Contre-exemple RH | aucun |
| Preuve RH | aucune |
