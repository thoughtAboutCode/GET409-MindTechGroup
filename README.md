# GET409-MindTechGroup

---
# 🤍 Diisoo — un espace pour souffler, en toute discrétion
 
> *La discrétion d'un secret bien gardé, la chaleur d'une tante qui écoute.*
 
**Diisoo** est un espace d'écoute anonyme destiné aux jeunes Sénégalais en détresse psychologique, porté par **SamaBadiane**, un agent conversationnel au ton de badiane — cette tante à qui, dans la culture sénégalaise, on confie ce qu'on ne peut dire à personne d'autre.
---
🔗 **MVP en ligne :** [https://app.diisoo.workers.dev/]
---

## Notre équipe

| Prénom Nom | Rôle | GitHub |
|---|---|---|
| Agnes Paulette SARR | Chef de Produit (PM) | @AgnesPaulette |
| Mamadou Said WADE | Responsable Impact | @masaidwade-oss |
| Sègla Gildas Armel FAGBEDJI | Dev UI (No-Code) | @thoughtAboutCode |
| Khadidiatou YADE | Responsable Impact | @khadidiatou444 |
| Nadine E. GABA SAGBO | Master Prompt Engineer | @Gena-Sag|
| Aminata DIAW | Chef de Produit (PM) | @DiawAminata |

---

## Notre défi

**Secteur :** Santé & télémédecine — santé mentale des jeunes au Sénégal
 
**Problème :** Les jeunes Sénégalais en détresse psychologique n'osent pas chercher de l'aide par peur de la stigmatisation, y compris auprès de leurs proches les plus fiables, et ne connaissent ni les services existants ni leur coût.
 
**Énoncé HMW :**
> Comment pourrions-nous offrir aux jeunes Sénégalais comme Awa un espace d'écoute anonyme et techniquement sécurisé, au ton culturellement familier, pour qu'ils osent exprimer leur détresse sans attendre que leur entourage soit prêt à les comprendre — tout en les orientant vers une aide humaine en cas de besoin réel ?

---

## L'insight qui a tout déterminé
 
Notre persona, **Awa** (23 ans, étudiante à Pikine), n'efface pas seulement ses recherches Google sur le stress. Elle supprime aussi les messages vocaux envoyés à sa meilleure amie.
 
> *« J'avais honte de m'entendre comme ça, aussi faible. »*
> *« C'est le regard des gens, le plus dur. Pas l'argent, pas de trouver où aller — c'est que quelqu'un l'apprenne. »*
 
Le frein n'est donc ni l'accès ni le coût : c'est **l'exposition sociale**. D'où notre exigence centrale — un anonymat **total**, y compris vis-à-vis de l'entourage de confiance. Cette exigence se retrouve dans chaque décision technique du projet : aucun compte, aucun numéro demandé, aucune persistance, un bouton de sortie rapide.

---

## Architecture
 
```
Interface React (Lovable → VSCode)
        │  webhook POST
        ▼
Dify — workflow SamaBadiane
        │
   ANALYSTE (temp 0) ──► détresse ? ──► TEMPLATE_ALERTE (texte figé)
        │
        └─► RAG (fiches bien-être) ──► SAMABADIANE ──► demande de contact ?
                                                            └─► TEMPLATE_ANNUAIRE
```

### Le principe de conception : un LLM n'écrit jamais un chiffre
 
Tous nos incidents de développement (numéro inventé, mauvais centre associé au mauvais numéro, ressource proposée hors contexte) avaient la même cause : le modèle était autorisé à **reformuler des données factuelles**.
 
Aucun prompt ne corrige durablement ce risque. Notre réponse est architecturale : **les contacts d'urgence sortent de nœuds Template figés**, écrits et vérifiés à la main, jamais générés. La base de connaissances ne contient plus aucun numéro — uniquement des fiches de bien-être, où une reformulation approximative est sans danger.

---

## Documentation
 
### Découverte & cadrage — S1
| Fichier | Contenu |
|---|---|
| [`docs/fiche-equipe.md`](documents/fiche-equipe.md) | Équipe, rôles, secteur |
| [`docs/guide-interview.md`](documents/guide-interview.md) | Guide d'entretien d'empathie |
| [`docs/carte-empathie.md`](documents/carte-empathie.md) | Carte d'empathie v1 (hypothèses) |
| [`docs/carte-empathie-v2.md`](documents/carte-empathie-v2.md) | Carte v2 — enrichie par verbatims |
 
### Idéation & priorisation — S2
| Fichier | Contenu |
|---|---|
| [`docs/chapeaux-bono.md`](documents/chapeaux-bono.md) | 6 Chapeaux de Bono |
| [`docs/contraintes-mvp.md`](documents/contraintes-mvp.md) | Contraintes non négociables |
| [`docs/hypotheses-validation.md`](documents/hypotheses-validation.md) | Hypothèses critiques à tester |
| [`docs/metriques-succes.md`](documents/metriques-succes.md) | Métrique Nord, progression, alertes |
| [`docs/vpc.md`](documents/vpc.md) | Value Proposition Canvas |
| [`docs/vpc-connections.md`](documents/vpc-connections.md) | Traçabilité 6 Chapeaux → VPC |
| [`docs/backlog-s3.md`](documents/backlog-s3.md) | User stories MUST / SHOULD / COULD |
| [`docs/pitch-vpc-draft.md`](documents/pitch-vpc-draft.md) | Bloc pitch proposition de valeur |
| [`docs/hmw-definitif.md`](documents/hmw-definitif.md) | HMW validé contre 6 critères |
| [`docs/hmw-alignement.md`](documents/hmw-alignement.md) | Scoring backlog vs HMW |
| [`docs/hmw-demo.md`](documents/hmw-demo.md) | Script de démonstration |
| [`docs/hmw-jury.md`](documents/hmw-jury.md) | Préparation aux questions du jury |
 
### Construction — S3 à S5
| Fichier | Contenu |
|---|---|
| [`docs/workflow-dify.md`](documents/workflow-dify.md) | Workflow complet, nœud par nœud, + suite de tests |
| [`data/ressources_aide_diisoo_v2.csv`](data/ressources_aide_diisoo_v2.csv) | 19 ressources d'aide vérifiées |
| [`data/fiches_psychoeducation_diisoo_v2.txt`](data/fiches_psychoeducation_diisoo_v2.txt) | 33 fiches de bien-être |

---

## Traçabilité — comment nous répondons au jury
 
> *« Pourquoi cette fonctionnalité et pas une autre ? »*
 
`backlog-s3.md` → US-02 adresse le Pain Reliever n°1
→ `vpc.md` → ce Pain Reliever répond au Pain n°1 d'Awa
→ `vpc-connections.md` → ce Pain vient du Chapeau Noir
→ `chapeaux-bono.md` → *« Awa efface systématiquement toute trace de ses recherches d'aide »*
 
**Quatre fichiers. Une réponse. Dix secondes.**
 
---
 
## Sources des données
 
| Donnée | Source |
|---|---|
| Numéros d'urgence (1515, 17, 18) | Ministère de la Santé + sources concordantes |
| Structures de santé mentale | Brochure officielle de la Division de la Santé Mentale, sante.gouv.sn |
| Fiches de bien-être | Rédigées par l'équipe, inspirées des principes de gestion du stress de l'OMS |
| Contexte socio-anthropologique | Diagne, P. M. (2016), *Soigner les malades mentaux errants dans l'agglomération dakaroise*, Anthropologie & Santé, 13 |
 
---
 
## ⚠️ Limites assumées
 
Diisoo **n'est pas un service médical d'urgence** et SamaBadiane **n'est pas un professionnel de santé**. L'agent n'établit aucun diagnostic, ne prescrit rien, et ne remplace pas une consultation.
 
Notre architecture garantit que les informations critiques ne transitent jamais par la génération — mais aucun système automatisé ne détecte une détresse avec une fiabilité absolue. C'est pourquoi l'orientation vers une aide humaine est déclenchée au moindre doute, et pourquoi ce projet est conçu comme **une première porte, pas comme une solution**.
 
**En cas d'urgence au Sénégal : 1515 (SAMU, gratuit, 24h/24).**
 
---
