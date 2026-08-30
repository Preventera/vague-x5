<div align="center">

<img src="assets/logo.png" alt="AgenticX5" width="110">

# vague-x5

**Registre L0-L4 et protocoles pré-enregistrés**

![statut](https://img.shields.io/badge/statut-d%C3%A9monstration-orange) ![gouvernance](https://img.shields.io/badge/gouvernance-HITL-blue) ![licence](https://img.shields.io/badge/licence-%C3%A0%20d%C3%A9terminer-lightgrey)

[🇬🇧 English](README.en.md)

</div>

---

> [!WARNING]
> **Démonstration architecturale.** Ce dépôt n'est pas un produit livré. Rien ici ne
> constitue un avis actuariel, médical ou juridique. Aucune mise en service réelle
> sans calibration sur données québécoises, validation par un tiers, entente Loi 25
> et gouvernance humaine dans la boucle.

## Contenu

Le dispositif qui permet à un déploiement de mesures SST de **produire une
preuve** au lieu d'un simple constat d'exécution.

Principe : la comparaison vient du calendrier, pas d'une privation. Personne ne
renonce à une mesure de sécurité — le témoin est celui qui n'est **pas encore**
équipé. Tout le monde finit équipé.

## Les cinq principes

1. On ne prouve rien sans comparer.
2. La comparaison vient du calendrier, pas d'une privation.
3. On mesure l'usage, pas la possession.
4. On écrit ce qu'on cherche avant de le chercher.
5. On commence par le cas où la donnée existe déjà.

## Architecture en couches

| Couche | Contenu | Régime |
|:---:|---|---|
| **L0** | Registre — entités, contexte, calendrier | Versionné, jamais écrasé |
| **L1** | Sceau — protocole figé | Écriture seule, horodaté |
| **L2** | Observation — déploiement, dose, outcome | Provenance obligatoire |
| **L3** | Analyse — exécution du protocole scellé | Ne lit L1 qu'en entier |
| **L4** | Preuve — fiches PreuveX5 | Conditionnée à un sceau valide |

### Règles de flux

> [!CAUTION]
> **On ne remonte pas.** L3 ne modifie pas L1. L4 ne modifie pas L3.
> Si un résultat déplaît, on ne réécrit pas le protocole — on lance une nouvelle
> vague avec un nouveau sceau.

Une analyse non déclarée dans L1 sort étiquetée **exploratoire** et ne peut jamais
alimenter L4. Aucun coefficient dans `trajectoire-x5` sans `sceau_id`.

Ces règles sont à faire respecter par les protections de branche, pas seulement
par la discipline : `l1-sceaux/` ne devrait jamais recevoir de commit modifiant un
fichier existant.

## Le champ qu'on oublie

`definition_non_concluant`, **distinct de « pas d'effet »**. Sans lui, un manque
de puissance se lit comme une absence d'effet. C'est le champ qui coûte le plus
cher à omettre.

## Premier sceau — VX5-001

**Assignation temporaire.** Choisie parce que la donnée existe déjà (dossiers
administratifs), l'événement est fréquent, aucun capteur n'est requis, et un
résultat est atteignable en 18 mois. Voir [`l1-sceaux/VX5-001.md`](l1-sceaux/VX5-001.md).

> [!IMPORTANT]
> **Réserve éthique.** Une réduction de la durée d'indemnisation peut refléter un
> meilleur retour au travail — ou une pression sur le travailleur. Le protocole
> inclut un outcome de contrepoids : taux de récidive et taux de contestation.
> Une baisse de durée accompagnée d'une hausse de récidive n'est pas un succès.

## Points de vigilance

**Le risque principal est L2, pas L3.** La tentation sera de nettoyer les doses.
Chaque geste est défendable isolément ; cumulés, ils rendent le résultat
indéfendable.

**La population sera volontaire.** Les établissements qui n'adoptent rien —
souvent les plus à risque — resteront invisibles. Il faut le dire dans chaque fiche.

**Conflit d'intérêts.** Produire de la preuve sur ses propres outils exige un
tiers analytique. Le pré-enregistrement public et une validation externe ne sont
pas des ornements : ce sont les conditions pour que le résultat soit lu.

## Vocabulaire externe

En interne : vague, dose, sceau. Vers un organisme public, une mutuelle ou un
institut de recherche, traduire — *déploiement échelonné*, *taux d'utilisation
effectif*, *protocole pré-enregistré*. Ces termes passent sans explication.

---

<div align="center">

**AgenticX5 · NordicX5** — Montréal, Québec
[team@agenticx5.com](mailto:team@agenticx5.com)

*Sources liées, jamais reproduites. L'IA propose, l'humain décide.*

</div>
