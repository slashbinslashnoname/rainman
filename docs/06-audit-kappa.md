# Audit — proportion κ des zéros sur la droite critique

**Objet :** annonce (août 2026) type « more than two thirds of the zeros… » (Claude / Anthropic, lecture Conrey–Goldston, dépôt Lean allégué).

## Claim

\[
\liminf_{T\to\infty} \frac{N_0(T,2T)}{N(T,2T)} \ge \frac{2}{3} - o(1),
\]
optimisé ≈ **0,6725** (fenêtre Montgomery–Taylor).  
Même ordre pour zéros simples sur la ligne ; distincts plus élevés.

## Tag honnête

**`NEEDS_VERIFICATION`**

Annoncé + lecture experte courte + formalisation alléguée ≠ absorption communautaire complète / revue journal.

## Historique (mollifiers)

| Résultat | κ ≳ |
|----------|-----|
| Levinson 1974 | 1/3 |
| Conrey 1989 | 2/5 ≈ 0.41 |
| Bui–Conrey–Young 2011 | ≈ 0.4105 |
| Pratt–Robles–Zaharescu–Zeindler ~2020 | > 5/12 ≈ 0.4167 |

Record « classique » mollifier ≈ **41,7 %**.

## Méthode annoncée (schéma)

1. Forme hermitienne de Weil / formule explicite  
2. Matrice de Gram sur un système de fonctions test (bande Fourier ≤ 1)  
3. Rank–trace / inertie (zéros sur la ligne vs paires hors ligne)  
4. Côté premiers via facteur de forme de Montgomery **inconditionnel** (BGSTB, |α|≤1)  
5. Optimisation de fenêtre → ≈ 0,6725  

Rupture par rapport au cadre Levinson : algèbre linéaire globale sur Gram, pas seulement mollifier de ζ′/ζ.

## Pourquoi cela ne prouve **pas** RH

- **Plafond bande ≤ 1** : ~0,68 pour les simples dans ce formalisme ; 2/3 est proche du plafond, pas de κ=1.
- Pousser κ vers 0,8–0,9 exigerait de la pair correlation au-delà de λ=1 (ouvert majeur).
- Argument type **Davenport–Heilbronn** : le même style de comptage de proportion s’applique à des fonctions L-like **sans** RH ; donc le mécanisme ne force pas l’absence de zéros hors ligne.
- Les auteurs le formulent comme proportion, pas comme preuve de RH.

## Checklist auditeur

- [ ] Montgomery F(α) pour |α|≤1 **sans RH** (citation BGSTB exacte)  
- [ ] Restes de N(T) / multiplicités  
- [ ] Support Fourier strictement dans [−1,1]  
- [ ] Constantes rank–trace et optimisation 0,6725  
- [ ] Lean : absence de `sorry`, axiomes, enclosures numériques externes  
- [ ] Alignement énoncé papier ↔ énoncé formel  
- [ ] Revue hors cercle d’origine  

## Lien cimetière

- **B8** : crypte partielle (affaiblissement productif)  
- **A16** : « κ≥2/3 ⇒ RH » est **ENTERRÉE** comme preuve  
