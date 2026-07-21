## Préparation Jury — HMW — Diisoo

### HMW Définitif

"Comment pourrions-nous offrir aux jeunes Sénégalais comme Awa un espace d'écoute anonyme et techniquement sécurisé, au ton culturellement familier, pour qu'ils osent exprimer leur détresse sans attendre que leur entourage soit prêt à les comprendre — tout en les orientant vers une aide humaine en cas de besoin réel ?"

### Les 5 Questions Probables

#### Question 1

**Le jury demande :** "Comment garantissez-vous réellement l'anonymat, techniquement ? Un simple 'pas de compte' ne suffit pas à le prouver."

**Ce qu'il teste :** La rigueur technique derrière une promesse marketing

**Votre réponse :** "C'est notre Contrainte 1 dans contraintes-mvp.md : aucune conversation n'est associée à un numéro, un compte ou un historique persistant. Concrètement, chaque session génère un identifiant temporaire non rattaché à une identité, et aucun log de contenu n'est conservé côté serveur au-delà de la session active."

**Fichier à ouvrir :** documents/contraintes-mvp.md — Contrainte 1

#### Question 2

**Le jury demande :** "Comment votre agent distingue-t-il un simple stress passager d'une vraie urgence suicidaire ? N'est-ce pas dangereux de laisser une IA en juger ?"

**Ce qu'il teste :** La responsabilité éthique et la robustesse du garde-fou central

**Votre réponse :** "C'est notre Hypothèse C2 dans hypotheses-validation.md, notre point de validation le plus critique. Nous testons l'agent sur des scénarios scriptés couvrant différents niveaux de détresse, avec un objectif de 100% de redirection vers une aide humaine sur les cas à risque élevé — tolérance zéro, documentée aussi dans l'Alerte A2 de metriques-succes.md. L'agent n'a jamais vocation à juger seul ; il redirige, il ne traite pas."

**Fichier à ouvrir :** documents/hypotheses-validation.md — Hypothèse C2

#### Question 3

**Le jury demande :** "Pourquoi cibler spécifiquement les jeunes femmes ? N'excluez-vous pas les jeunes hommes, tout aussi concernés par la santé mentale ?"

**Ce qu'il teste :** La connaissance du persona et la conscience des limites du MVP

**Votre réponse :** "Notre persona Awa est né d'une interview approfondie, mais nous avons documenté ce risque nous-mêmes dans hmw-definitif.md — section 'Ce que ce HMW exclut explicitement'. Le ton badiane est une hypothèse à valider pour les jeunes hommes, pas une certitude. C'est précisément notre Hypothèse I1 dans hypotheses-validation.md, testée avec un panel mixte."

**Fichier à ouvrir :** documents/hmw-definitif.md — section 'Ce que ce HMW exclut'

#### Question 4

**Le jury demande :** "En quoi votre solution diffère-t-elle d'un chatbot de bien-être générique déjà existant à l'international ?"

**Ce qu'il teste :** Le positionnement et la connaissance du marché

**Votre réponse :** "Les solutions internationales de bien-être ne répondent pas à notre insight central identifié en interview : même la confidence à une amie proche est effacée par peur d'exposition. Notre différenciateur documenté dans vpc-connections.md est un anonymat total — y compris envers l'entourage de confiance — combiné à un registre culturel spécifique, la badiane, qui n'existe dans aucune solution générique."

**Fichier à ouvrir :** documents/vpc-connections.md — section Profil Client, Pain "peur que la démarche soit découverte"

#### Question 5

**Le jury demande :** "Comment saurez-vous, concrètement, que votre MVP a un impact réel sur Awa et pas seulement un usage superficiel ?"

**Ce qu'il teste :** La rigueur de mesure d'impact, au-delà du simple usage

**Votre réponse :** "Notre Métrique Nord dans metriques-succes.md ne mesure pas juste l'usage, mais la complétude de l'échange — 70% des conversations initiées doivent aller jusqu'au bout. Et notre Métrique P2 va plus loin en demandant directement à l'utilisatrice si l'échange l'a aidée, en fin de session, de façon anonyme."

**Fichier à ouvrir :** documents/metriques-succes.md — Métrique Nord et Métrique P2

### Les 2 Questions Pièges

#### Piège 1

**Le jury demande :** "Si votre agent rate un cas réel de détresse suicidaire et que quelque chose de grave arrive, qui est responsable ?"

**Pourquoi c'est un piège :** Le jury teste si l'équipe minimise le risque ou le fuit par un optimisme technologique déplacé

**Stratégie de réponse :** Ne jamais promettre une fiabilité à 100% dans l'absolu — reconnaître la limite réelle d'un MVP académique, insister sur le fait que l'agent est un point d'entrée vers l'aide humaine et non un substitut, et que cette limite est justement documentée comme risque prioritaire dans notre propre travail.

**Phrase d'ouverture :** "C'est exactement le risque que nous avons identifié nous-mêmes comme prioritaire dans notre Chapeau Noir — voici comment nous le traitons et voici ses limites actuelles, en toute transparence."

#### Piège 2

**Le jury demande :** "Votre MVP repose sur un persona unique construit par vous-mêmes. Comment savez-vous que ce n'est pas juste votre propre biais, sans vraie validation terrain ?"

**Pourquoi c'est un piège :** Le jury teste l'honnêteté méthodologique de l'équipe sur la solidité réelle de ses données

**Stratégie de réponse :** Reconnaître ouvertement que la version initiale (v1) reposait sur des hypothèses, montrer explicitement la progression vers une v2 avec verbatims documentés, et pointer vers les hypothèses encore non validées comme un travail en cours assumé plutôt que caché.

**Phrase d'ouverture :** "Vous avez raison de le souligner — c'est pour ça que notre carte-empathie.md existe en deux versions, et que hypotheses-validation.md liste précisément ce qui reste à confirmer sur le terrain."

### Réflexe en soutenance

Si vous ne savez pas répondre : "Bonne question — laissez-moi ouvrir le fichier correspondant dans notre dépôt GitHub pour vous montrer comment on a documenté ça."
