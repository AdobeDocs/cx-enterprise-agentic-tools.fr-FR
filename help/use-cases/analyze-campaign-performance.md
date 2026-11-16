---
title: Affichage des informations sur les campagnes sans création de rapports
description: Utilisez le serveur MCP Customer Journey Analytics pour poser des questions sur les performances en langage clair et obtenir des réponses sans avoir à naviguer dans les Report Builders.
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 4%
---

# Affichage des informations sur les campagnes sans création de rapports

<!-- last-modified: 2026-06-02 -->

![Plateforme d’IA indiquant les étapes suivantes recommandées pour améliorer les performances de la campagne](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

L’analyse des campagnes qui nécessitait autrefois la création de rapports dans un outil distinct est désormais une conversation. Cette présentation explique comment utiliser Coworker, ou votre propre plateforme d’IA, avec Customer Journey Analytics (CJA) et poser des questions sur les performances en langage clair. Le temps d’accès à insight est ainsi plus rapide et aucune création de rapports manuelle n’est nécessaire.

| Détails du scénario | |
| --- | --- |
| Applications CX Enterprise | [Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-overview/cja-overview) |
| Outils agentiques | [Adobe CX Enterprise Coworker](https://experienceleague.adobe.com/fr/docs/cx-enterprise-coworker/content/home), [Adobe CX Enterprise Coworker pour les plateformes d’IA](../tools/mcp-servers.md#connect-to-your-ai-platform) ou [Customer Journey Analytics MCP Server](../tools/mcp-servers.md) |
| Audience | Analystes, responsables de campagne |
| Prérequis | Un accès à CJA, plus Coworker, une plateforme d’IA avec Coworker pour les plateformes d’IA ou une plateforme d’IA compatible avec MCP |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. Une section **Plus que vous pouvez accomplir** suit pour une exploration supplémentaire dans la même session.

## Avant de commencer

>[!BEGINTABS]

>[!TAB Coworker]

Le moyen le plus rapide d’obtenir ces réponses est Coworker, qui ne nécessite aucune configuration de serveur ou de plateforme d’IA. [Essayer Un Collègue](https://experienceleague.adobe.com/fr/docs/cx-enterprise-coworker/content/home)

Si vous ne pouvez pas ou ne souhaitez pas utiliser directement Coworker, utilisez-le plutôt à partir de votre propre plateforme d’IA. Consultez l’onglet **Collègues pour les plateformes d’IA**. Si cela ne fonctionne pas non plus pour vous, connectez directement votre plateforme d’IA au serveur Customer Journey Analytics MCP à l’aide des onglets restants.

>[!TAB Collègue pour les plateformes d’IA]

Vous pouvez également effectuer cette présentation avec Coworker pour les plateformes d’IA à partir de votre propre plateforme d’IA. [Configuration de Coworker pour les plateformes d’IA](../tools/mcp-servers.md#connect-to-your-ai-platform) | [Documentation Adobe](https://experienceleague.adobe.com/fr/docs/coworker/content/ai-platforms#set-up-coworker)

>[!TAB Claude.ai]

Connectez le serveur Customer Journey Analytics MCP en tant que connecteur personnalisé.

1. Accédez à **Paramètres > Intégrations** dans Claude.ai.
2. Sélectionnez **Ajouter un connecteur personnalisé** et saisissez l’URL du serveur : `https://cja-mcp.adobe.io/mcp`
3. Sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.

Configuration complète : [Documentation sur les connecteurs personnalisés Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Connectez le serveur Customer Journey Analytics MCP à l&#39;aide du mode Développeur ChatGPT (Pro, Plus, Business, Enterprise ou Education plan requis).

1. Activez le **mode Développeur** dans les **paramètres ChatGPT**.
2. Accédez à **Paramètres > Intégrations** et sélectionnez **Ajouter un connecteur personnalisé > Serveur MCP distant**.
3. Saisissez l&#39;URL du serveur : `https://cja-mcp.adobe.io/mcp`
4. Sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.

Configuration complète : [Documentation du MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Autres plateformes d’IA]

Utiliser Gemini, Microsoft Copilot, Cursor, Claude Code ou un autre environnement compatible avec MCP ? Connectez-vous au serveur Customer Journey Analytics MCP à l’aide de ce point d’entrée :

```
https://cja-mcp.adobe.io/mcp
```

Instructions de configuration complètes pour toutes les plateformes d’IA prises en charge : [Connexion à votre plateforme d’IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à vos vues de données CJA. Choisir la mauvaise organisation est la source la plus courante d’erreurs d’authentification.
>
>Lors de la première connexion, votre plateforme d’IA peut vous demander de sélectionner une organisation IMS ou de spécifier un sandbox. Une fois ce contexte défini, le serveur MCP l’utilise pour le reste de la session.
>
>Certains outils vous demandent votre approbation avant de s’exécuter. Examinez la demande et approuvez ou refusez. Aucune action n’est entreprise sans votre confirmation.

## Étape 1 : découvrir les vues de données disponibles

Commencez par demander à votre plateforme d’IA de répertorier les vues de données disponibles dans votre compte CJA. Il indique les jeux de données que vous pouvez interroger avant d’exécuter des rapports.

```
What data views are available in my CJA account?
```

+++Voir un exemple de réponse

![Plateforme d’IA répertoriant les vues de données CJA disponibles](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step1-data-views.png){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


## Étape 2 : extraire les données de performances de la campagne

Une fois la vue de données identifiée, demandez les performances de la campagne par chiffre d’affaires et taux de conversion. L’IA résout les noms des mesures et des dimensions à partir de la vue de données sans nécessiter d’identifiants techniques.

```
For '[data view name]', show me the top campaigns by revenue and conversion rate for the last 30 days.
```

+++Voir un exemple de réponse

![Plateforme d’IA affichant les principales campagnes par chiffre d’affaires et taux de conversion à partir de la vue de données omnicanal - multisecteur](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step2.gif){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


>[!NOTE]
>
>Remplacez `[data view name]` par le nom de votre vue de données de l’étape 1. Vérifiez les résultats dans Analysis Workspace en utilisant la même vue de données et la même période avant de partager avec les parties prenantes.

## Étape 3 : identifier ce qui stimule les performances

Demandez à votre plateforme d’IA d’expliquer ce qui motive les différences de performances entre les groupes de campagne. Cela permet de passer des numéros de titre aux variables en dessous.

```
What factors are driving the results for these campaign groups?
```

+++Voir un exemple de réponse

![Plateforme d’IA expliquant les facteurs déterminant les performances du groupe de campagnes](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step3.gif){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


## Étape 4 : accéder à un type de campagne spécifique

Donner suite à un résultat spécifique en demandant une répartition au niveau du segment. Les types de clients qui génèrent des performances au sein d’un type de campagne apparaissent.

```
Break down Promotional Email Campaigns by Customer Segment and explain what's driving the high conversion rate.
```

+++Voir un exemple de réponse

![Plateforme d’IA répartissant les performances des campagnes promotionnelles par e-mail par segment client](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step4-segment-breakdown.png){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


## Étape 5 : Agir sur ce que vous avez trouvé

Demandez des recommandations hiérarchisées en fonction de tout ce qui a été abordé au cours de la session. Demander des estimations de valeur commerciale vous aide à décider par où agir en premier.

```
Based on these findings, recommend the highest-impact actions to increase revenue and conversion rates. Prioritize recommendations by expected business value and estimate the potential uplift.
```

+++Voir un exemple de réponse

![Plateforme d’IA recommandant des actions prioritaires avec une valeur commerciale estimée](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5.gif){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


>[!NOTE]
>
>Les outils de CJA peuvent créer des segments, des mesures calculées et des projets Workspace dans CJA au cours de la même session. Pour mettre à jour des campagnes, des parcours ou du contenu dans d’autres applications, connectez le serveur MCP approprié ou accédez directement à l’application.

## Ce que vous avez accompli

Vous avez utilisé Coworker ou votre plateforme d’IA avec Customer Journey Analytics et êtes passé de la découverte de vues de données à des recommandations commerciales prioritaires dans cinq invites. Vous avez identifié les principales campagnes par chiffre d’affaires et taux de conversion, fait apparaître les facteurs qui déterminent les performances des groupes de campagnes, exploré les détails au niveau du segment pour un type de campagne spécifique et reçu des recommandations classées avec une augmentation estimée. Cette approche remplace la création de rapports par une conversation directe, ce qui réduit le temps entre une question commerciale et un plan d’action soutenu par les données.

## Plus de choses à accomplir

Le serveur Customer Journey Analytics MCP peut afficher beaucoup plus d’informations que les couvertures de la présentation. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer dans la même session.

+++Trouver ce qui fonctionne et ce qui ne fonctionne pas

Un aperçu rapide des campagnes diffusées et de celles qui ne le sont pas vous permet de concentrer les efforts avant d’examiner les rapports détaillés. Ces invites vous donnent cette image en une seule session.

**Invites**

```
Which campaigns are driving the most revenue and conversions?
```

```
Show me the campaigns that need attention this month.
```

```
What channels are outperforming expectations?
```

```
Identify the biggest performance changes compared to last month.
```

```
Show me conversion performance by traffic source.
```

+++

+++Comprendre ce qui génère des résultats

Les mesures des titres vous disent ce qui s’est passé. Ces invites vous aident à comprendre pourquoi : quels segments, canaux et points de contact se trouvent derrière les chiffres.

**Invites**

```
What factors are driving revenue growth?
```

```
Explain why conversion rates changed this quarter.
```

```
Break down campaign performance by customer segment.
```

```
Which customer segments are growing fastest?
```

```
Which touchpoints contribute most to conversions?
```

+++

+++Découvrir les opportunités de croissance

Savoir où les performances sont fortes n&#39;est qu&#39;une partie du tableau. Ces invites vous aident à identifier les domaines dans lesquels vous pouvez investir davantage, les audiences qui disposent d&#39;une marge de manœuvre et les campagnes prêtes à être déployées.

**Invites**

```
Where should we invest more marketing budget?
```

```
Which audiences have the greatest growth potential?
```

```
Which campaigns should we scale?
```

```
What would have the biggest impact on revenue?
```

+++

+++Transformer les informations en action

Les outils CJA peuvent créer des segments, des audiences, des mesures calculées et des projets Workspace directement dans CJA sans quitter votre session d’IA. Utilisez ces invites pour agir sur ce que vous avez trouvé.

**Invites**

```
Create a segment for high-value customers.
```

```
Build an audience from recent purchasers.
```

```
Create a calculated metric for conversion efficiency.
```

```
Save this analysis as a Workspace project for executive reporting.
```

+++


## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Serveur CJA MCP dans le registre IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | Disponibilité et outils du serveur CJA MCP |
| [Documentation Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-landing){target="_blank"} | Documentation complète de l’application CJA |
