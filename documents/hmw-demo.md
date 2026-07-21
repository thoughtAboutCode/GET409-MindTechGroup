## Script de Démonstration S6 — Diisoo

### HMW à prouver

"Comment pourrions-nous offrir aux jeunes Sénégalais comme Awa un espace d'écoute anonyme et techniquement sécurisé, au ton culturellement familier, pour qu'ils osent exprimer leur détresse sans attendre que leur entourage soit prêt à les comprendre — tout en les orientant vers une aide humaine en cas de besoin réel ?"

### MVP construit

Un agent conversationnel Dify nommé SamaBadiane, accessible via une interface web légère sans compte ni numéro de téléphone. Il répond en français et en wolof dans un ton familier, et redirige vers une ressource humaine dès qu'un signal de détresse sérieuse est détecté.

**Outils utilisés :** Dify (agent + logique de détection) + Bolt.new (interface web) + GitHub

**Durée de la démo :** 5 minutes

---

### Minute 0:00 — 0:45 — Situation avant le MVP

**Le présentateur dit :** "Awa a 23 ans, elle est étudiante à Pikine. La semaine dernière, avant un examen, elle a fait une crise d'angoisse. Elle a envoyé un vocal à sa meilleure amie — puis elle l'a supprimé, par honte. Elle n'a jamais osé consulter qui que ce soit."

**Le présentateur montre :** Un slide simple avec la citation d'Awa : *"J'avais honte de m'entendre comme ça, aussi faible."*

**Le jury voit :** Le contexte humain avant toute technologie — pas de démo, juste le problème.

---

### Minute 0:45 — 3:00 — Le MVP en action (démo live)

**Le présentateur dit :** "Voici SamaBadiane. Awa n'a besoin de rien créer — ni compte, ni numéro."

**Le présentateur montre :** Ouverture de l'interface web sur écran partagé. Aucun champ de connexion visible, juste une zone de conversation.

**Le jury voit :** L'écran d'accueil de SamaBadiane, message d'ouverture chaleureux en français/wolof.

**Le présentateur dit :** "Je tape un message simulant ce qu'Awa pourrait écrire : 'Je stress trop pour mes examens, j'arrive plus à respirer.'"

**Le présentateur montre :** Il tape le message en live et envoie.

**Le jury voit :** SamaBadiane répond avec un ton familier, sans vocabulaire clinique, en posant une question ouverte pour approfondir.

**Le présentateur dit :** "Maintenant je simule un signal de détresse plus sérieux : 'Je n'en peux plus, je pense que ça vaudrait mieux si je n'étais plus là.'"

**Le présentateur montre :** Il tape ce second message en live.

**Le jury voit :** SamaBadiane change immédiatement de registre et affiche une redirection claire vers une ressource humaine (numéro ou service local), sans tenter de gérer la crise seul.

**Le présentateur dit :** "C'est notre garde-fou non négociable — documenté dans notre Hypothèse C2 : l'agent ne remplace jamais un professionnel."

---

### Minute 3:00 — 4:15 — Les métriques réelles vs cibles

**Le présentateur dit :** "Voici ce qu'on a mesuré sur nos tests terrain."

**Le présentateur montre :** Le tableau de bord suivant, à l'écran :

| Métrique | Cible | Résultat réel |
|---|---|---|
| % de conversations complètes (Métrique Nord) | 70% | [À COMPLÉTER après test terrain] |
| Nombre de sessions distinctes testées (P1) | 30 | [À COMPLÉTER après test terrain] |
| Alerte A2 — redirection manquante sur cas à risque | Tolérance zéro | [À COMPLÉTER — déclenchée ou non] |

**Le jury voit :** Des chiffres réels, pas des estimations — ou une mention honnête si le test n'a pas encore atteint la cible.

---

### Minute 4:15 — 5:00 — Réponse directe au HMW

**Le présentateur dit :** "Notre HMW demandait : comment offrir un espace anonyme et sécurisé, sans attendre que l'entourage soit prêt. Ce que vous venez de voir répond aux deux moitiés de cette question : Awa peut parler sans jamais être identifiée, et si sa détresse dépasse ce qu'un agent peut gérer, elle est redirigée vers une vraie aide humaine — immédiatement, pas dans 3 jours."

**Le présentateur montre :** Le HMW à l'écran, en gras, avec un visuel simple : Awa → SamaBadiane → (si besoin) → Aide humaine.

**Le jury voit :** La boucle complète du parcours utilisateur, du problème initial à la réponse.

**Phrase de clôture :** "Diisoo ne remplace pas un psychologue. Il ouvre juste la première porte — celle qu'Awa n'osait pas pousser seule."
