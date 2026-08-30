# L0 — Établissement

| Champ | Type | Note |
|---|---|---|
| `etab_id` | identifiant | pseudonymisé |
| `scian` | code | 4 chiffres si disponible |
| `effectif` | entier | dénominateur de base |
| `version_date` | date | nouvelle ligne à chaque changement, **jamais d'écrasement** |
| `ctx_supervision` | ordinal | présence de supervision terrain |
| `ctx_ratio_charge` | ratio | soignant/patient, opérateur/machine selon secteur |
| `ctx_roulement` | % annuel | perte de formation |
| `ctx_taille` | catégorie | PME / moyenne / grande |

Trois à cinq variables de contexte, pas dix. Les quatre `ctx_*` ci-dessus se
lisent dans des données administratives déjà disponibles.

Le contexte n'est pas un champ descriptif : c'est un jeu de variables déclarées à
l'avance, sur lesquelles on stratifie les vagues et on découpe les résultats.
