# Make it pullable!

On a un réflexe assez naturel avec le travail. Quand quelque chose doit être fait, on essaie de le faire avancer.

Une demande arrive, on cherche quelqu’un pour la prendre. Une décision doit être prise, on l’envoie à la bonne personne. Quelqu’un termine quelque chose, on lui trouve la suite. Une initiative est approuvée, on cherche où la démarrer. Ça semble parfaitement logique. Après tout, le but est bien de faire avancer les choses.

Je me demande parfois si on n’investit pas énormément d’énergie à pousser le travail à travers nos systèmes, alors qu’on pourrait en investir davantage à créer les conditions pour qu’il puisse naturellement être pris en charge par le système.

En d’autres mots: **Make it pullable.**

## Pull change le signal

Push commence généralement avec le travail. J’ai quelque chose qui doit avancer. Où est-ce que je peux l’envoyer?

Le travail existe. Il est important. Il a été planifié. Quelqu’un l’attend. On cherche donc à le faire progresser dans le système.

Pull part d’un autre signal: de la capacité vient de se libérer.

La question n’est plus simplement « quelle est la prochaine chose à démarrer? », mais plutôt: **parmi ce que le système peut prendre, qu’est-ce qui aiderait le plus le flow maintenant?**

Prenons un exemple volontairement banal. Un développeur termine quelque chose. Le réflexe naturel peut être de lui donner immédiatement la prochaine story. La capacité vient de se libérer, on la remplit. Tout le monde reste occupé.

Mais ailleurs dans le système, une review attend peut-être. Quelqu’un est bloqué. Un item pourrait terminer avec un peu d’aide. Des tests s’accumulent. Un bottleneck commence à se former.

Commencer quelque chose de nouveau est peut-être une bonne décision. Mais pas toujours.

**Starting isn’t finishing.**

Un système rempli de travail commencé n’est pas nécessairement un système qui termine beaucoup de choses. Plus on injecte de travail, plus on peut créer de queues, de dépendances, de context switches, de handoffs, d’attente et de WIP.

Pull change donc quelque chose de simple, mais important: la présence de travail ne suffit plus à créer le signal de départ. La capacité disponible et l’état réel du système comptent aussi.

Sauf que ça soulève une autre question: quand cette capacité se libère, **qu’est-ce qu’elle peut réellement pull?**

## Le bon travail doit aussi être pullable

Imaginons qu’une équipe obtienne 30 % de capacité supplémentaire. Bonne nouvelle. Qu’est-ce qu’elle peut réellement prendre?

Cette feature attend une décision. Celle-là dépend d’une autre équipe. Une autre est trop grosse pour être absorbée dans l’état actuel du système. Une quatrième nécessite une expertise indisponible. Une initiative est clairement importante, mais personne ne sait encore comment l’attaquer sans recréer plusieurs semaines de discussions, de coordination et de flou.

On vient d’ajouter de la capacité. Mais pas nécessairement beaucoup d’options utiles.

C’est là que **pullability** devient utile comme grille de lecture.

J’utilise ici le terme pour parler d’un travail qu’une capacité pertinente peut réellement prendre en charge et faire progresser sans devoir d’abord déclencher une quantité disproportionnée de préparation, de coordination ou de déblocage.

Ça ne veut pas dire qu’il sera choisi, ni même qu’il devrait l’être.

Un travail peut être parfaitement pullable et ne plus avoir assez de valeur pour mériter notre capacité. À l’inverse, notre priorité absolue peut être extrêmement importante tout en étant pratiquement impossible à absorber dans l’état actuel du système.

La valeur et la priorité nous aident à déterminer ce qui compte. La pullability pose une autre question: **si une capacité pertinente se libérait, est-ce que ce travail pourrait réellement entrer dans le flow?** Et la réponse dépend de beaucoup plus que de la qualité du ticket.

## Pullable ne veut pas simplement dire Ready

*Pullable* ne veut pas dire complètement spécifié.

Prenons un problème encore relativement incertain. La solution n’est pas définie dans tous ses détails, mais l’équipe comprend le domaine, possède suffisamment de contexte, peut accéder rapidement au feedback et dispose de l’autonomie nécessaire pour prendre les petites décisions en avançant.

Ce travail peut être très pullable. L’incertitude existe toujours, mais le système peut l’absorber.

Prenons maintenant l’inverse. Un ticket contient quinze pages de spécifications, une architecture documentée et des acceptance criteria complets. Mais avant de le terminer, il faudra obtenir une décision externe, coordonner trois équipes, trouver du temps avec un expert précis, réserver un environnement et synchroniser une release avec plusieurs autres changements.

Le ticket peut très bien avoir été déclaré `Ready`. Ça ne dit pas encore à quel point le système pourra réellement l’absorber.

**Un statut `Ready` ne suffit pas à dire si le système saura l’absorber.**

Et surtout, la pullability n’est pas uniquement une propriété du travail.

Le même item peut être pullable par une équipe et pas une autre. Il peut ne pas être pullable dans une configuration donnée, puis le devenir sans qu’une seule ligne de sa description change: une expertise devient accessible, une décision est prise, une dépendance disparaît, un environnement devient self-service.

La pullability dépend donc aussi de la capacité et du système qui doivent absorber le travail. Et ça change la façon de l’améliorer.

## Débloquer l’item ou changer le système?

Supposons qu’une décision manque. On peut trouver la bonne personne, organiser une discussion et obtenir la décision. Problème réglé. Cet item peut maintenant avancer.

Mais si le même type de décision bloque constamment du travail, une autre question devient possible: **pourquoi faut-il systématiquement pousser cette décision jusqu’à cette personne?**

Peut-être que son jugement est réellement nécessaire. Ou peut-être qu’il manque surtout un cadre explicite, un périmètre de décision clair ou suffisamment de contexte pour permettre à l’équipe de décider localement dans certaines limites.

Le premier geste rend cet item pullable. Le deuxième peut rendre ce type de travail plus pullable à l’avenir.

On retrouve le même pattern avec l’expertise. Lorsqu’une équipe a besoin d’un expert, on peut trouver du temps dans son agenda. Mais si des dizaines de demandes similaires passent continuellement par lui, on peut aussi se demander quelle partie de cette expertise pourrait être distribuée sous forme de documentation, de conventions, de tooling, de guardrails, de composants réutilisables ou simplement d’apprentissage.

L’expert reste nécessaire pour les vrais problèmes experts. Mais il cesse d’être le passage obligé de tout le reste.

Même logique avec les releases, les environnements ou les dépendances. On peut devenir très bon à coordonner chaque exception, ou réduire progressivement les raisons qui rendent cette coordination nécessaire aussi souvent.

Ce ne sont pas les mêmes investissements. Dans un cas, on fournit l’énergie nécessaire pour faire passer le travail à travers la contrainte. Dans l’autre, on modifie la contrainte.

Et un système peut devenir extrêmement efficace à faire la première chose: meetings, escalades, relances, approvals, coordination, efforts exceptionnels. Le travail finit par avancer. On peut alors conclure que le système fonctionne.

Mais peut-être qu’on est simplement devenu très bon à **pousser manuellement du travail non pullable à travers le système**.

C’est ici que *Make it pullable* devient, pour moi, plus intéressant qu’une autre façon de gérer un backlog.

Les investissements les plus utiles en pullability ne préparent pas nécessairement davantage de travail. Ils réduisent l’effort nécessaire pour rendre **le prochain travail** absorbable.

## On optimise beaucoup la capacité. Et la pullability?

Quand un système n’absorbe pas suffisamment de travail, notre réaction est souvent de chercher davantage de capacité: plus de personnes, plus d’automatisation, parfois plus de parallélisme. On espère alors terminer davantage de travail et augmenter le throughput.

Toutes ces interventions peuvent évidemment aider. Mais un pull system dépend d’au moins deux capacités différentes: **la capacité à absorber du travail pullable** et **la capacité à rendre le prochain travail pullable**. Le flow peut être limité par l’une ou par l’autre.

Reprenons ce problème à l’échelle du système. Ajoutons deux développeurs là où chaque changement important dépend toujours du même Tech Lead, des mêmes approvals, du même environnement partagé et du même release bundle.

On a augmenté la capacité à absorber du travail. Qu’est-ce que cette nouvelle capacité peut réellement pull sans d’abord se heurter aux mêmes contraintes déjà saturées?

Si la vraie contrainte est la capacité à rendre le travail pullable, augmenter seulement la capacité à l’absorber ne crée pas automatiquement plus de pull. Ça peut surtout créer plus de capacité qui attend d’être alimentée.

Et cette capacité visible peut créer une pression assez prévisible: garder tout le monde occupé, ouvrir plus de fronts, faire entrer du travail qui n’est pas encore réellement absorbable.

Deux systèmes peuvent avoir exactement le même nombre de personnes et offrir des possibilités très différentes lorsque quelqu’un termine quelque chose. Dans l’un, plusieurs chemins utiles sont ouverts. Dans l’autre, presque tout attend une décision, une expertise, une permission ou une coordination précise.

Il y a énormément de travail. Mais très peu d’options réellement absorbables.

On retrouve le même problème au niveau des initiatives.

Une initiative est approuvée, financée et importante. Le réflexe naturel est de chercher à la démarrer ASAP.

Mais si toutes les capacités pertinentes sont déjà saturées, que les dépendances sont partout et que l’initiative ne peut produire de valeur qu’en faisant avancer plusieurs morceaux couplés simultanément, la pousser dans le système ne signifie pas nécessairement que le système vient de l’absorber.

On vient peut-être simplement de créer davantage de WIP.

La question devient alors: **qu’est-ce qu’il faudrait changer pour que le système puisse réellement absorber cette initiative?**

Peut-être qu’il faut la découper autrement. Peut-être qu’une dépendance doit disparaître. Peut-être qu’une décision doit être prise. Peut-être qu’il faut terminer autre chose avant de la commencer.

Et oui, peut-être qu’il faut réellement plus de capacité. Si plusieurs options sont déjà pullables et que la capacité à les absorber est réellement saturée, l’augmenter peut être exactement la bonne intervention. Le point n’est pas de préférer une capacité à l’autre. C’est d’identifier laquelle limite le flow maintenant. Et cette contrainte peut bouger.

## Make it pullable ne veut pas dire tout préparer

Il y a évidemment un piège.

Si on conclut de tout ça qu’il faut avoir cinquante features parfaitement pullables six mois à l’avance, on vient probablement de recréer un push system upstream.

On aura dépensé énormément d’énergie à raffiner, décider, découper et préparer du travail avant même de savoir s’il sera encore pertinent lorsqu’une capacité apparaîtra.

Du travail rendu pullable trop tôt peut lui aussi devenir de l’inventory.

L’objectif n’est donc pas de rendre tout le travail pullable, ni d’éliminer toutes les dépendances. Et ce n’est pas non plus de forcer chaque problème en unités minuscules et indépendantes. Certains changements ont un couplage ou un ordre qui fait partie du problème; les découper artificiellement peut simplement déplacer le coût dans la coordination.

Certaines expertises, décisions, contraintes réglementaires ou séparations de responsabilités ont d’excellentes raisons d’exister.

Et augmenter la pullability coûte quelque chose. Créer du self-service, découpler une architecture ou distribuer de l’expertise consomme aussi de la capacité. Toutes les frictions ne méritent pas un programme de transformation.

Si une dépendance apparaît deux fois par année, la coordination manuelle est peut-être parfaitement raisonnable. Si elle bloque trente items chaque sprint, la question devient plus intéressante.

Même chose pour push. Il y aura toujours des urgences, des incidents, des engagements ou des situations où quelqu’un devra décider et faire bouger les choses immédiatement.

*Make it pullable* n’est pas une règle absolue. C’est une grille de lecture.

Dans un système pull, ce qui compte doit toujours rester clair. Mais savoir ce qui compte n’oblige pas nécessairement à prédéterminer chaque mouvement du travail.

Quelque chose doit avancer. Notre question habituelle est: **comment est-ce qu’on fait avancer ça?**

Je pense qu’une autre mérite parfois d’arriver avant: **qu’est-ce qui empêche le système de pouvoir l’absorber?**

Si la réponse est ponctuelle, débloquons l’item. Mais si nous retrouvons constamment la même décision, le même expert, la même dépendance, le même approval ou la même coordination sur le chemin, peut-être que le problème mérite d’être traité ailleurs que dans le prochain ticket.

Un peu moins d’énergie à pousser le travail jusqu’à quelqu’un qui peut lever la contrainte. Un peu plus à créer les conditions dans lesquelles le bon travail peut être absorbé lorsque la capacité existe. Peut-être qu’on démarrerait un peu moins de choses. Peut-être qu’on en terminerait davantage.

What if we pushed a little less and made things a little more pullable?

## Références

Le vocabulaire Kanban utilisé ici s’appuie notamment sur ces sources de référence:

- [The Kanban Method Glossary, Kanban University](https://kanban.university/glossary/): pull signals, pull system, push system, replenishment et pull criteria.
- [The Official Guide to the Kanban Method, Kanban University](https://kanban.university/kanban-guide/): WIP limits, capacité disponible et principe de pull.
- [Open Guide to Kanban, July 2025](https://kanbanguides.org/open-guide-to-kanban/2025.7/): contrôle du WIP, sélection du travail selon la capacité et politiques explicites de flow.
