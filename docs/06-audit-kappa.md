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

## Compléments d'audit (session 2026-08-11/12)

- **Plafond auto-établi du mécanisme : 0,68185** (Rem. 1.1) ; atteindre 0,70/0,80/0,90 exigerait support Fourier ≈1,04/1,26/1,70 — hors du connu.
- **Nature du 67 % :** proportion *asymptotique* (liminf de densité), pas une jauge de complétude. Même « 100 % » (densité 1) ≠ RH — un ensemble de densité nulle peut contenir une infinité de contre-exemples (analogie : les carrés parfaits sont de densité nulle mais infinis). Le résultat est *insensible à o(N) zéros hors droite* (§1.5).
- **Lieu de la mort de toute extension :** F(α) pour |α|>1 ⟺ variance des premiers en petits intervalles (Goldston–Montgomery) ⟺ Hardy–Littlewood ⟸ barrière de parité de Selberg. En famille, le plateau f=1 sur (1,2) est prouvé (CLLR) mais **sous GRH côté premiers** (A20).
- Contrôle numérique indépendant : RUN 17 (reproduction exacte du §8(1)).
