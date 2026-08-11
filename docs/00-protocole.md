# Protocole de triage

## Flux

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

## Tags

| Tag | Signification |
|-----|----------------|
| **ENTERRÉE** | Fausse, réfutée, ou morte comme *preuve* |
| **PIÉGÉE** | Équivalence correcte, pas plus facile que RH |
| **BLOQUÉE** | Programme sérieux, obstacle structurel identifié |
| **OUVERTE** | Encore vivante ; partial results possibles |
| **HEURISTIQUE** | Indice fort, pas une démonstration |
| **ARTEFACT** | Échec numérique de *méthode*, pas de l’énoncé |
| **FALSE_STRONG** | Plus fort que RH, connu faux (implique RH mais faux) |
| **NEEDS_VERIFICATION** | Annonce récente, audit communautaire incomplet |

## Décisions structurantes

1. **Ne pas promettre une preuve de RH.** Objectif = triage, calcul, archivage.
2. **Équivalence ≠ preuve.** Speiser, Robin, Lagarias, Li, NB, Weil, Jensen_all sont des oracles.
3. **Le fini ne tue pas l’infini.** N zéros, Robin jusqu’à X, λ_n jusqu’à N₀ ≠ RH.
4. **Enterrer vite les zombies** pour ne pas y reperdre du temps.
5. **Archiver en markdown** pistes, status, découvertes, RUN IDs.

## Convention d’IDs

| Préfixe | Sens |
|---------|------|
| `A#` | Tombe (allée A) |
| `B#` | Crypte ouverte / partielle (allée B) |
| `RUN n` | Expérience numérotée dans le journal |
