## Hypothèses de Validation — Diisoo

### HMW Définitif

"Comment pourrions-nous offrir aux jeunes Sénégalais comme Awa un espace d'écoute anonyme et techniquement sécurisé, au ton culturellement familier, pour qu'ils osent exprimer leur détresse sans attendre que leur entourage soit prêt à les comprendre — tout en les orientant vers une aide humaine en cas de besoin réel ?"

### Hypothèses CRITIQUES

*(Si fausse → le MVP ne fonctionne pas)*

#### Hypothèse C1

**Affirmation :** Nous croyons que l'anonymat technique (pas de compte, pas de numéro rattaché, pas de logs identifiables) est la condition nécessaire et suffisante pour qu'Awa ose ouvrir une conversation avec SamaBadiane.

**Indicateur :** Nous le saurons si, lors du test terrain, au moins 4 utilisateurs sur 5 engagent une conversation complète (plus de 3 échanges) sans abandonner dès l'écran d'accueil.

**Méthode :** Test terrain — prototype cliquable envoyé à 5 jeunes correspondant au persona

**Qui valide :** Jeunes de 18-30 ans à Dakar/Pikine, profil proche d'Awa

**Délai S3 :** Semaine 1

#### Hypothèse C2

**Affirmation :** Nous croyons que SamaBadiane peut détecter un signal de détresse sérieuse (idées suicidaires, mise en danger) dans une conversation et orienter systématiquement vers une aide humaine, sans faux négatif.

**Indicateur :** Nous le saurons si, sur un jeu de 15 messages simulant différents niveaux de détresse, l'agent redirige vers une ressource humaine dans 100% des cas à risque élevé.

**Méthode :** Test de scénarios scriptés sur l'agent Dify

**Qui valide :** L'équipe projet, avec supervision si possible d'une personne formée (association ou professionnel)

**Délai S3 :** Semaine 1-2

### Hypothèses IMPORTANTES

*(Si fausse → expérience dégradée mais MVP utilisable)*

#### Hypothèse I1

**Affirmation :** Nous croyons que le ton "badiane" (chaleureux, familial, en wolof/français) est perçu comme rassurant et non artificiel par les jeunes utilisateurs, y compris les jeunes hommes.

**Indicateur :** Nous le saurons si au moins 3 utilisateurs sur 5 décrivent le ton de l'agent comme "naturel" ou "proche" plutôt que "bizarre" ou "robotique" en debrief post-test.

**Méthode :** Entretien de suivi post-utilisation

**Qui valide :** Panel mixte (jeunes femmes et hommes) du persona cible

**Délai S3 :** Semaine 2-3

#### Hypothèse I2

**Affirmation :** Nous croyons que WhatsApp (ou une web app légère) est un canal suffisamment discret pour qu'Awa l'utilise sans craindre d'être vue par son entourage.

**Indicateur :** Nous le saurons si aucun utilisateur testé ne mentionne spontanément une gêne liée à la visibilité de l'app/icône sur son téléphone.

**Méthode :** Observation + entretien de suivi

**Qui valide :** Panel de test terrain

**Délai S3 :** Semaine 2

### Hypothèses SECONDAIRES

*(À valider après le MVP)*

#### Hypothèse S1

**Affirmation :** Nous croyons qu'une fonctionnalité optionnelle générant une phrase d'ouverture pour parler à un proche peut, à terme, aider certains utilisateurs à sortir de l'isolement.

**Indicateur :** Nous le saurons si, après plusieurs semaines d'usage réel, une part mesurable des utilisateurs déclare avoir utilisé cette phrase avec un proche.

**Méthode :** Sondage in-app anonyme post-MVP

**Qui valide :** Utilisateurs réguliers du service, post-lancement

**Délai S3 :** Non prioritaire — après validation du MVP

### Priorité de Validation S3

La première chose à tester en S3 : envoyer le prototype conversationnel de SamaBadiane à 5 jeunes du persona cible et vérifier qu'ils engagent une conversation complète sans abandonner dès l'écran d'accueil (Hypothèse C1) — c'est la condition qui, si elle échoue, invalide tout le reste du MVP.
