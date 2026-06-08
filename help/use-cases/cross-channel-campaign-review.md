---
title: Exécuter une révision de campagne cross-canal
description: Utilisez la passerelle MCP Entreprise CX dans une seule session d’IA pour obtenir une vue unifiée de l’intégrité des campagnes AJO, CJA et Real-Time CDP sur l’ensemble des parcours, des audiences et des performances.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 4%

---


# Exécuter une révision de campagne cross-canal

<!-- last-modified: 2026-05-21 -->

![Exécution d’une révision de campagne cross-canal](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review)

Une image complète de l’intégrité de la campagne nécessite des données provenant de plusieurs systèmes : les parcours actifs d’AJO, le statut d’activation de l’audience de Real-Time CDP et les mesures de performances de CJA. Cette présentation montre comment connecter les trois en une seule session d’IA, afin que vous puissiez passer de l’état du parcours à l’intégrité de l’audience et suivre les tendances de performances dans une seule conversation plutôt que dans trois outils distincts.

| | |
| --- | --- |
| Applications d’entreprise CX | Adobe Journey Optimizer, Customer Journey Analytics, Real-Time CDP |
| Outils agentiques | Passerelle MCP Entreprise CX |
| Audience | Chargés d&#39;opération, opérations marketing |
| Prérequis | Client d’IA compatible avec MCP, accès à AJO, CJA et Real-Time CDP |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. La section **Plus que vous pouvez accomplir** suit pour une exploration supplémentaire au cours de la même session.

## Avant de commencer

>[!BEGINTABS]

>[!TAB Claude.ai]

Connectez la passerelle MCP Entreprise CX en tant que connecteur personnalisé. Une connexion vous donne accès aux outils AJO, CJA et Real-Time CDP.

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
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à vos environnements AJO, CJA et Real-Time CDP. Choisir la mauvaise organisation est la source la plus courante d’erreurs d’authentification.
>
>Lors de la première connexion, votre client d’IA peut vous demander de sélectionner une organisation IMS ou de spécifier un sandbox. Une fois ce contexte défini, le serveur MCP l’utilise pour le reste de la session.
>
>Certains outils vous demandent votre approbation avant de s’exécuter. Examinez la demande et approuvez ou refusez — aucune action n&#39;est entreprise sans votre confirmation.

## Étape 1 : passer en revue les parcours et campagnes actifs

Commencez avec AJO pour établir ce qui est en cours d’exécution. Le fait de savoir quels parcours sont en ligne et ont été récemment modifiés constitue la base du reste de la révision.

```
What journeys are currently active in AJO?
```

+++Voir un exemple de réponse

8 parcours actifs ont été trouvés dans votre organisation AJO :

| Parcours | Canal(s) | Last modified |
| --- | --- | --- |
| Série de bienvenue — Nouveaux membres | E-mail, notification push | 18 Mai 2026 |
| Suivi après achat | E-mail, SMS | 14 Mai 2026 |
| Réengagement de la fidélité | Email | 20 Mai 2026 |
| Panier abandonné - 24 heures | E-mail, SMS | 10 Mai 2026 |
| Promotion du printemps | E-mail, notification push | 19 Mai 2026 |
| Reconquête — 90 Jours Inactifs | E-mail | 28 Avril 2026 |
| Récompense d&#39;anniversaire | Email | 15 Avril 2026 |
| Réengagement - Opt-Out Push | SMS | 12 Mai 2026 |

3 parcours ont été modifiés ces 7 derniers jours. Voulez-vous des détails sur l&#39;un d&#39;entre eux ?

+++

## Étape 2 : vérifier le statut d’activation de l’audience

Une fois les parcours affichés, vérifiez que les audiences qui alimentent ces campagnes alimentent correctement leurs destinations.

```
Show me the activation status for the high-value loyalty segment.
```

+++Voir un exemple de réponse

**Segment de fidélité à valeur élevée** — statut d’activation sur plusieurs destinations :

| Destination | Statut | Dernière exécution réussie | Taille de l’audience |
| --- | --- | --- | --- |
| Google Ads | Actif | 21 mai 2026 02:14 AM | 48,320 |
| Meta Ads | Actif | 21 mai 2026 01:58 | 48,295 |
| Salesforce Marketing Cloud | Actif | 20 mai 2026 11:30 PM | 47,940 |
| Adobe Target | Actif | 21 mai 2026 12:00 | 48,320 |

Aucune erreur de flux de données détectée. Toutes les activations se sont terminées au cours des 3 dernières heures.

+++

## Étape 3 : extraire les mesures de performances de CJA

Une fois le contexte du parcours et de l’audience établi, utilisez CJA pour évaluer comment ces campagnes sont converties et où l’engagement chute.

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++Voir un exemple de réponse

**Loyalty Re-engagement Campaign** — Du 21 avril au 21 mai 2026 :

| Canal | Envois | CTR | de conversions | Conv. Taux |
| --- | --- | --- | --- | --- |
| Email | 48,320 | 8.4% | 1,973 | 4.1% |
| Notification push | 31,200 | 12.1% | 987 | 3.2% |

Taux de conversion combiné : 3,8 %. Le taux de clics des e-mails a augmenté de 1,2 % par rapport à la période de 30 jours précédente. Les conversions push sont aplaties.

+++

## Étape 4 : synthétiser un résumé de l&#39;intégrité de la campagne

Demandez à votre client d’IA de rassembler l’image sur les trois sources et de faire apparaître tout ce qui nécessite une attention particulière.

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++Voir un exemple de réponse

Voici votre résumé de l’intégrité actuelle de la campagne dans AJO, Real-Time CDP et CJA :

parcours actifs :**8 en ligne, 3 modifiés cette semaine.** Le parcours de réengagement de la fidélité est le plus récemment mis à jour.

**Activation de l’audience :** tous les segments circulent correctement vers 4 destinations. Aucune erreur de flux de données détectée.

**Performances :** le taux de clics des e-mails est élevé dans les campagnes de fidélité. La conversion push est plate. Aucun canal n’est en déclin significatif.

**Indicateurs pour l’attention :**

- Le parcours de reconquête (90 jours inactif) a été modifié pour la dernière fois il y a 23 jours et n’a pas été examiné récemment.
- Le taux de conversion des notifications push stagne depuis 3 périodes consécutives. Il vaut la peine de passer en revue les messages ou le timing.

Aucun problème critique détecté. Deux éléments ci-dessus méritent d’être examinés avant le prochain lancement de campagne.

+++

C’est là que l’approche multi-serveur s’avère payante : votre client d’IA raisonne sur la configuration du parcours, le statut de l’audience et les données de performances dans une seule conversation.

## Étape 5 : Agir sur ce que vous avez trouvé

La révision a fait apparaître deux éléments. Demandez à votre client d’IA de vous aider à prioriser et à acheminer chacun d’eux.

```
For each flag you identified, what should I do and where should I go to do it?
```

+++Voir un exemple de réponse

Voici un plan d’action hiérarchisé pour les deux indicateurs :

**1. Parcours de reconquête : passez en revue les conditions de reprise (MCP AJO, puis application AJO si des modifications sont nécessaires)**

Le parcours Win-Back n&#39;a pas été modifié depuis 23 jours. Me demander de passer en revue ses conditions de rentrée actuelles et sa logique de sortie. Si les conditions semblent obsolètes ou incorrectes, les modifications structurelles du flux du parcours nécessitent l’ouverture d’AJO. Les mises à jour de la limite de fréquence et de l’audience peuvent être effectuées ici.

**2. Conversion push plate pendant 3 périodes — mettre à jour la messagerie ou tester une variante**

La conversion plate signale généralement une fatigue des messages ou une incohérence entre l’offre et l’audience. Deux chemins :

- **Mettre à jour le contenu push maintenant (AEM MCP) :** si les notifications push pointent vers une page de destination, ajoutez le serveur AEM Content MCP et mettez à jour la copie de page ou le CTA sans changer d’outil.
- **Exécution d’un test A/B push (application AJO) :** créez une variante au niveau de la campagne avec des messages différents pour déterminer s’il s’agit de contenu ou de ciblage. Cela nécessite d’accéder directement à AJO.

Par quoi souhaiteriez-vous commencer ?

+++

## Ce que vous avez accompli

Vous avez exécuté une révision de l’intégrité des campagnes cross-canal en connectant AJO, Real-Time CDP et CJA à une seule session d’IA. Plutôt que d’ouvrir trois applications et d’assembler manuellement une image, vous avez parcouru le statut du parcours, l’activation de l’audience et les données de performances en une seule conversation. Le résumé donne aux responsables de campagne un moyen plus rapide d’identifier ce qui fonctionne, ce qui doit être ajusté et sur quoi se concentrer ensuite.

## Plus de choses à accomplir

Avec AJO, CJA et Real-Time CDP connectés au cours de la même session, vous pouvez aller bien au-delà de la présentation. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer.

+++Savoir exactement ce qui s’exécute avant de lancer quelque chose de nouveau.

Les parcours qui se chevauchent, les campagnes récemment modifiées et les canaux que vous n’avez pas examinés peuvent tous affecter un nouveau lancement. Ces invites vous donnent une idée précise de l&#39;état actuel avant d&#39;ajouter quoi que ce soit.

**Invites**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++Assurez-vous que les audiences atteignent les bonnes destinations

Les problèmes d’activation restent silencieux : un segment cesse de circuler et votre campagne l’envoie vers une liste plus petite sans avertissement. Ces invites font apparaître les écarts et les erreurs avant d&#39;affecter les résultats.

**Invites**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++Comprendre ce qui fonctionne et sur quoi se concentrer ensuite

Les tendances des performances sur l’ensemble des canaux vous indiquent où investir et ce qu’il faut retirer. Ces invites vous aident à identifier ce qui génère des résultats et où l&#39;attention du prochain trimestre doit être portée.

**Invites**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++

## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Documentation ](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/ajo-home) | Documentation complète de l’application AJO |
| [Documentation MCP Analytics](https://developer.adobe.com/analytics-mcp/docs/) | Configuration de CJA MCP et référence des outils |
| [Documentation Real-Time CDP MCP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | Guide de configuration de RTCDP MCP |
| [Serveur AJO MCP dans le registre IA](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) | Disponibilité et outils du serveur AJO MCP |
| [Serveur CJA MCP dans le registre IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | Disponibilité et outils du serveur CJA MCP |
| [ Serveurs MCP ](../tools/mcp-servers.md) | Connexion d’un client d’IA aux serveurs MCP Adobe |
