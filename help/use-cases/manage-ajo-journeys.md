---
title: Surveillez les problèmes de parcours avant qu’ils n’affectent les clients
description: Utilisez la passerelle MCP Entreprise CX pour surveiller les parcours AJO actifs, passer en revue la configuration des campagnes et faire apparaître les problèmes opérationnels avant qu’ils n’atteignent votre audience.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 093448ea6a9840d1d2027b76e177b145400a9202
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 3%

---


# Surveillez les problèmes de parcours avant qu’ils n’affectent les clients
<!-- last-modified: 2026-06-08 -->

![Vérification des Parcours AJO](https://placehold.co/1600x900?text=Review+AJO+Journeys)

Pour identifier clairement les parcours actifs, les conditions qui les pilotent et la manière dont les campagnes sont configurées normalement, ouvrez Adobe Journey Optimizer et parcourez son interface. Cette présentation explique comment obtenir cette même visibilité par le biais d’un client d’IA, à l’aide de la passerelle MCP Entreprise CX pour interroger les données de parcours et de campagne AJO au moyen de questions en langage clair.

| | |
| --- | --- |
| Applications d’entreprise CX | Adobe Journey Optimizer (AJO) |
| Outils agentiques | Passerelle MCP Entreprise CX |
| Audience | Chargés d&#39;opération, marketeurs |
| Prérequis | Client d’IA compatible avec MCP, accès à AJO |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. La section **Plus que vous pouvez accomplir** suit pour une exploration supplémentaire au cours de la même session.


## Avant de commencer

>[!BEGINTABS]

>[!TAB Claude.ai]

Connectez la passerelle MCP d’entreprise CX en tant que connecteur personnalisé pour accéder aux outils Adobe Journey Optimizer.

1. Accédez à **Paramètres > Intégrations** dans Claude.ai.
2. Sélectionnez **Ajouter un connecteur personnalisé** et saisissez l’URL du serveur : `https://cx-enterprise.adobe.io/mcp`
3. Sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.

Configuration complète : [documentation des connecteurs personnalisés Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Connectez la passerelle MCP Entreprise CX en utilisant le mode Développeur ChatGPT (Pro, Plus, Business, Enterprise ou Education plan requis).

1. Activez le **mode Développeur** dans **Paramètres ChatGPT**.
2. Accédez à **Paramètres > Intégrations** et sélectionnez **Ajouter un connecteur personnalisé > Serveur MCP distant**.
3. Saisissez l’URL du serveur : `https://cx-enterprise.adobe.io/mcp`
4. Sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.

Configuration complète : [documentation MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Autres clients d’IA]

Utiliser Gemini, Microsoft Copilot, Cursor, Claude Code ou un autre environnement compatible avec MCP ? Connectez-vous à la passerelle MCP d’entreprise CX à l’aide de ce point d’entrée :

```
https://cx-enterprise.adobe.io/mcp
```

Instructions de configuration complètes pour tous les clients pris en charge : [Connexion à votre client IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à votre environnement AJO. Choisir la mauvaise organisation est la source la plus courante d’erreurs d’authentification.
>
>Lors de la première connexion, votre client d’IA peut vous demander de sélectionner une organisation IMS ou de spécifier un sandbox. Une fois ce contexte défini, le serveur MCP l’utilise pour le reste de la session.
>
>Certains outils vous demandent votre approbation avant de s’exécuter. Examinez la demande et approuvez ou refusez — aucune action n&#39;est entreprise sans votre confirmation.


## Etape 1 : Découvrir les parcours actifs et leur finalité

Demandez tout d&#39;abord un inventaire des parcours actifs et des objectifs commerciaux qui les sous-tendent. Vous obtiendrez ainsi une vue d’ensemble avant de vous lancer dans un parcours spécifique.

```
What customer journeys are currently available and what business objectives do they support?
```

+++Voir un exemple de réponse

![client AI répertoriant les parcours client disponibles et leurs objectifs commerciaux](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step1.gif)

+++



## Étape 2 : examiner les étapes et l’expérience client d’un parcours

Une fois la liste des parcours affichée, demandez à votre client ou cliente IA de passer en revue les étapes d’un parcours spécifique et d’expliquer ce que le client ou la cliente ressent à chaque étape.

```
Walk me through the [journey name] journey and explain the customer experience.
```

+++Voir un exemple de réponse

![Client AI passant en revue les étapes du parcours Bienvenue aux nouveaux clients et l’expérience client](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step2-welcome-journey.png)

+++


>[!NOTE]
>
>Remplacez `[journey name]` par le nom d’un parcours à partir des résultats de l’étape 1.


## Étape 3 : examiner les campagnes, les audiences et les objectifs

Basculez des parcours aux campagnes. Demandez un résumé des campagnes actives, des personnes qu’elles ciblent et des résultats qu’elles sont conçues pour obtenir.

```
Show me our campaigns, the audiences they target, and the outcomes they're designed to drive.
```

+++Voir un exemple de réponse

![Client IA répertoriant les campagnes actives avec leur ciblage d’audience et les résultats escomptés](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step3.gif)

+++



## Étape 4 : comprendre comment les campagnes et les parcours se connectent

Demandez à votre client d’IA de faire le lien entre les campagnes et les parcours et d’expliquer comment ils fonctionnent ensemble pour atteindre des objectifs d’engagement partagés.

```
How do our campaigns and journeys work together to improve customer engagement?
```

+++Voir un exemple de réponse

![Client AI expliquant la relation entre les campagnes et les parcours &#x200B;](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step4-connection.png)

+++



## Étape 5 : obtenez des recommandations hiérarchisées

Demandez des recommandations hiérarchisées sur les priorités à adopter, présentées du point de vue d’un responsable marketing du cycle de vie. Cela permet de faire ressortir les lacunes et les opportunités les plus importantes de tout ce qui a été examiné au cours de la session.

```
If you were our lifecycle marketing manager, what would you prioritize next and why?
```

+++Voir un exemple de réponse

Client ![AI donnant des recommandations marketing prioritaires relatives au cycle de vie](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5.gif)

+++


>[!NOTE]
>
>Le serveur MCP AJO surfacie les informations de parcours et de campagne, mais ne peut pas modifier les parcours, les campagnes ni le contenu. Pour implémenter les recommandations, accédez directement à l’application AJO ou connectez-vous au serveur AEM Content MCP pour voir les modifications de contenu dans la même session.


## Ce que vous avez accompli

Vous avez connecté un client d’IA à Adobe Journey Optimizer et créé une vue d’ensemble de votre parcours et de votre portfolio de campagnes au moyen de cinq invites. Vous avez inventorié les parcours actifs et leurs objectifs commerciaux, examiné l’expérience client étape par étape pour un parcours spécifique, mappé les campagnes actives à leurs audiences et résultats prévus, compris comment les campagnes et les parcours fonctionnent ensemble et reçu des recommandations hiérarchisées sur les prochaines cibles à cibler. Cela donne une visibilité stratégique au marketing du cycle de vie et aux responsables de campagne sans ouvrir l’interface d’AJO.


## Plus de choses à accomplir

La passerelle MCP Entreprise CX peut faire apparaître un large éventail de détails de parcours et de campagne AJO. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer dans la même session.

+++Savoir ce qui se passe en direct avant de faire un changement

Il est risqué d’apporter des modifications à un parcours sans savoir ce qui fonctionne en dehors de celui-ci. Ces invites vous donnent un inventaire à jour des éléments actifs, de ce qui a été modifié récemment et de la manière dont les campagnes sont configurées.

**Invites**

```
Show me all journeys modified in the last 7 days.
```

```
Show me all journeys that use SMS as a channel.
```

```
Which campaigns are scheduled to end this week?
```

```
What loyalty challenges are currently active?
```

+++

+++Découvrir les détails d’un parcours spécifique

Lorsque vous devez réviser, approuver ou transmettre un parcours, la logique complète devant vous sans ouvrir AJO vous permet de gagner du temps. Ces invites indiquent les conditions de surface, les plannings et les règles de segment à la demande.

**Invites**

```
What is the entry condition for the [journey name] journey?
```

```
What are the exit conditions and timeout rules for the [journey name] journey?
```

```
What messages and wait conditions are in the [journey name] journey?
```

```
Which segment does the [journey name] journey target?
```

+++

+++Découvrir les détails d’une campagne spécifique

Lorsque vous devez vérifier la configuration complète d’une campagne avant de l’approuver, de la transmettre ou d’y apporter des modifications, ces invites font apparaître les règles d’audience, les paramètres du canal et les détails de planning sans ouvrir AJO.

**Invites**

```
Walk me through the full configuration of the [campaign name] campaign.
```

```
What audience does the [campaign name] campaign target and how large is that segment?
```

```
What frequency cap and send schedule apply to the [campaign name] campaign?
```

```
Are any campaigns targeting overlapping audiences?
```

```
What channel configurations are set up in our AJO environment?
```

+++



## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Serveur AJO MCP dans le registre IA](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) | Disponibilité et outils du serveur AJO MCP |
| [Documentation &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/ajo-home) | Documentation complète de l’application AJO |
| [API &#x200B;](https://developer.adobe.com/journey-optimizer-apis/) | Référence de l’API AJO pour les intégrations personnalisées |
| [Tutoriels &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/overview) | Tutoriels vidéo et parcours d’apprentissage |
