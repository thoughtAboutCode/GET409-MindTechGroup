## Contraintes MVP — Diisoo

### Persona

Awa · 23 ans · Étudiante en licence + petit commerce en ligne · Pikine, Dakar · Smartphone Android d'entrée de gamme, data limitée

### Contraintes Non Négociables

#### Contrainte 1

**Critère :** Le MVP DOIT garantir qu'aucune conversation n'est associée à un numéro de téléphone, un compte identifiable ou un historique persistant

**Origine :** Chapeau Rouge / Noir (Awa efface systématiquement toute trace de ses recherches d'aide et de ses confidences, même envers sa meilleure amie)

**Élimine :** Création de compte obligatoire, authentification par numéro de téléphone, historique de conversation sauvegardé par défaut

#### Contrainte 2

**Critère :** Le MVP DOIT fonctionner sur une connexion data faible et via un canal déjà installé sur le téléphone d'Awa (WhatsApp ou web app légère)

**Origine :** Chapeau Blanc (Awa possède un smartphone Android d'entrée de gamme avec une data limitée)

**Élimine :** Application native à télécharger, fonctionnalités vidéo ou audio haute résolution, dépendance à une connexion stable

#### Contrainte 3

**Critère :** Le MVP NE DOIT PAS se substituer à une prise en charge professionnelle — il DOIT détecter les signaux de détresse sérieuse et orienter vers une aide humaine

**Origine :** Chapeau Noir (un agent IA mal calibré pourrait donner l'illusion d'un vrai soutien professionnel et retarder une prise en charge nécessaire)

**Élimine :** Toute formulation de diagnostic, tout conseil médical ou posologique, toute promesse de traitement de fond

#### Contrainte 4

**Critère :** Le MVP DOIT s'exprimer dans un ton familier et culturellement ancré (registre "badiane"), en français et en wolof, sans vocabulaire médical ou clinique

**Origine :** Chapeau Rouge / Noir (le vocabulaire médical fait peur et stigmatise ; un ton artificiel ou infantilisant réduirait l'adoption)

**Élimine :** Interface en anglais uniquement, ton clinique ou institutionnel, jargon psychologique non vulgarisé

### Fonctionnalités Éliminées

- Application mobile native → éliminée car Awa n'installera pas une appli visible sur son téléphone, cela crée un risque d'exposition (icône visible, notifications)
- Compte utilisateur avec profil et historique → éliminé car il contredit directement le besoin d'anonymat total identifié en interview
- Diagnostic ou évaluation clinique automatisée → éliminé car hors du rôle d'un agent IA non professionnel, risque réel pour l'utilisatrice
- Notifications push ou rappels programmés → éliminés car ils pourraient exposer l'usage de l'appli à l'entourage d'Awa

### Critère de Validation Final

Le MVP est valide si Awa peut ouvrir une conversation avec SamaBadiane, s'exprimer librement sur son stress, et recevoir une réponse bienveillante et culturellement adaptée — sans qu'aucune trace identifiable ne subsiste après la conversation, et sans qu'aucun proche ne puisse détecter qu'elle a utilisé le service.
