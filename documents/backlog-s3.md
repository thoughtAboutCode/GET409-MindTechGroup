## Backlog S3 — Diisoo

### HMW Définitif

"Comment pourrions-nous offrir aux jeunes Sénégalais comme Awa un espace d'écoute anonyme et techniquement sécurisé, au ton culturellement familier, pour qu'ils osent exprimer leur détresse sans attendre que leur entourage soit prêt à les comprendre — tout en les orientant vers une aide humaine en cas de besoin réel ?"

### User Stories MUST

*(À construire obligatoirement en S3)*

#### US-01

**Story :** En tant qu'Awa, je veux que SamaBadiane détecte les signaux de détresse sérieuse dans mes messages afin d'être orientée vers une aide humaine avant tout risque grave

**Priorité :** MUST

**Outil :** Dify (prompt système + règles de détection)

**Effort :** moyen

**Adresse :** Contrainte non négociable #3 (contraintes-mvp.md) — orientation vers l'aide humaine en cas de détresse

**Critère d'acceptation :** sur 15 messages scriptés simulant différents niveaux de détresse, l'agent redirige vers une ressource humaine dans 100% des cas à risque élevé

#### US-02

**Story :** En tant qu'Awa, je veux démarrer une conversation avec SamaBadiane sans créer de compte ni fournir mon numéro de téléphone afin de garantir mon anonymat total

**Priorité :** MUST

**Outil :** Dify (session sans authentification) + interface web légère (Bolt.new)

**Effort :** moyen

**Adresse :** Pain Reliever #1 (vpc.md) — aucune identification requise

**Critère d'acceptation :** un utilisateur peut ouvrir une conversation complète sans jamais saisir d'information identifiable (nom, numéro, email)

#### US-03

**Story :** En tant qu'Awa, je veux que SamaBadiane me parle avec un ton chaleureux et familier, en français et en wolof, afin de me sentir comprise sans vocabulaire médical

**Priorité :** MUST

**Outil :** Dify (prompt système, ton et registre de langue)

**Effort :** faible

**Adresse :** Pain Reliever #2 (vpc.md) — ton culturellement ancré

**Critère d'acceptation :** au moins 3 utilisateurs sur 5 testés décrivent le ton comme "naturel" ou "proche" en debrief, aucun ne mentionne de vocabulaire clinique

### User Stories SHOULD

*(À construire si le temps le permet)*

#### US-04

**Story :** En tant qu'Awa, je veux recevoir une question de clôture en fin de conversation afin que l'équipe puisse mesurer si l'échange m'a aidée

**Priorité :** SHOULD

**Outil :** Dify (message de clôture standardisé)

**Effort :** faible

**Adresse :** Métrique P2 (metriques-succes.md) — % de retours positifs

**Critère d'acceptation :** la question de clôture s'affiche systématiquement en fin d'échange, réponse agrégée sans contenu identifiable

### User Stories COULD

*(Roadmap post-MVP)*

#### US-05

**Story :** En tant qu'Awa, je veux que SamaBadiane me propose une phrase d'ouverture pour parler à un proche quand je m'en sens prête afin d'être progressivement moins isolée

**Priorité :** COULD

**Outil :** Dify (fonctionnalité optionnelle)

**Effort :** élevé

**Adresse :** Gain Creator #3 (vpc.md) — famille plus soutenante à terme

#### US-06

**Story :** En tant qu'Awa, je veux un mode vocal éphémère où rien n'est enregistré afin de m'exprimer à voix haute sans laisser de trace

**Priorité :** COULD

**Outil :** À définir — non tracé dans les 6 Chapeaux (vpc-connections.md), à valider en interview S3

**Effort :** élevé

**Adresse :** idée Chapeau Vert non encore confirmée sur le terrain

### Sprint S3

**Semaine 1 :** US-01 (détection de détresse) + US-02 (anonymat technique) — les deux fondations non négociables du service

**Semaine 2 :** US-03 (ton et registre) + tests terrain sur le panel utilisateur

**Démo S6 :** US-01 et US-02 démontrées en live — une conversation anonyme complète avec redirection simulée en cas de détresse
