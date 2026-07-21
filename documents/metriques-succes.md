## Métriques de Succès — Diisoo

### MVP

SamaBadiane est un agent conversationnel anonyme, accessible par chat, qui écoute les jeunes en détresse psychologique dans un registre familier et culturellement ancré, et les oriente vers une aide humaine en cas de besoin réel.

### ⭐ Métrique Nord

**Indicateur :** % de conversations où l'utilisateur va jusqu'au bout d'un échange complet (au moins 3 messages échangés) sans abandonner dès l'écran d'accueil

**Valeur cible à 30 jours :** 70% des conversations initiées vont jusqu'au bout

**Comment mesurer :** Compteur simple côté agent Dify (nombre de messages par session), sans stockage d'aucun contenu de conversation

### 📈 Métriques de Progression

#### Métrique P1

**Indicateur :** Nombre d'utilisateurs distincts (sessions anonymes) ayant initié une conversation avec SamaBadiane

**Valeur cible à 30 jours :** 30 sessions distinctes

**Comment mesurer :** Compteur de sessions anonymisées côté agent, sans identifiant personnel

#### Métrique P2

**Indicateur :** % de sessions où l'utilisateur exprime explicitement se sentir "écouté" ou "soulagé" en fin d'échange (via une question de clôture simple posée par l'agent)

**Valeur cible à 30 jours :** 60% de retours positifs à la question de clôture

**Comment mesurer :** Question standardisée posée par SamaBadiane en fin de conversation ("Est-ce que ça t'a aidé de m'en parler ?"), réponse agrégée sans contenu identifiable

#### Métrique P3

**Indicateur :** % de sessions à risque détecté où l'agent propose effectivement une ressource d'aide humaine

**Valeur cible à 30 jours :** 100% des sessions à risque élevé détecté

**Comment mesurer :** Test de scénarios scriptés + revue manuelle des logs de redirection (sans contenu de conversation, uniquement le déclenchement de la redirection)

### 🚨 Métriques d'Alerte

#### Alerte A1

**Signal :** Taux d'abandon supérieur à 50% dès le premier message

**Seuil :** Plus de la moitié des sessions s'arrêtent après 1 seul message

**Action corrective :** Revoir le message d'accueil de SamaBadiane — probable manque de clarté sur l'anonymat ou ton perçu comme peu naturel ; retester avec le panel utilisateur

#### Alerte A2

**Signal :** Une session à risque élevé détectée où l'agent ne propose PAS de redirection vers une aide humaine

**Seuil :** Un seul cas suffit à déclencher l'alerte — tolérance zéro sur ce point

**Action corrective :** Suspendre le déploiement du prototype jusqu'à correction du prompt système et nouveau test complet des scénarios de détresse

### Tableau de Bord S6

À la démo S6, nous présenterons ces 3 chiffres :

1. Métrique Nord — % de conversations complètes (réel vs cible 70%)
2. Métrique P1 — Nombre de sessions distinctes testées (réel vs cible 30)
3. Alerte A2 — déclenchée ou non (tolérance zéro)
