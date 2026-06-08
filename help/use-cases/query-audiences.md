---
title: Découvrez vos audiences et où elles sont activées
description: Utilisez la passerelle MCP Entreprise CX pour surveiller le statut d’activation des audiences, vérifier l’intégrité de la destination et les problèmes de surface avant qu’ils n’affectent vos campagnes.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 2%

---


# Découvrez vos audiences et où elles sont activées

<!-- last-modified: 2026-06-04 -->

![Requête sur les audiences avec le langage naturel](https://placehold.co/1600x900?text=Query+Audiences)

Comprendre quelles audiences sont activées, où elles circulent et si les destinations sont saines implique généralement l’ouverture de Real-Time CDP et la navigation sur plusieurs écrans. Cette présentation explique comment obtenir les mêmes réponses par le biais d’un client d’IA, à l’aide du serveur RTCDP MCP pour faire apparaître la configuration de destination, le statut d’activation et l’intégrité du flux de données au moyen de questions en langage clair.

| | |
| --- | --- |
| Applications d’entreprise CX | Real-Time Customer Data Platform (Real-Time CDP) |
| Outils agentiques | Passerelle MCP Entreprise CX |
| Audience | Marketeurs, analystes, opérateurs |
| Prérequis | Client d’IA compatible avec MCP, accès à Real-Time CDP |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. La section **Plus que vous pouvez accomplir** suit pour une exploration supplémentaire au cours de la même session.

## Avant de commencer

>[!BEGINTABS]

>[!TAB Claude.ai]

Connectez la passerelle MCP d’entreprise CX en tant que connecteur personnalisé pour accéder aux outils Real-Time CDP.

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
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à votre instance Real-Time CDP. Choisir la mauvaise organisation est la source la plus courante d’erreurs d’authentification.

## Étape 1 : Découvrir vos audiences et ce qu&#39;elles représentent

Commencez par demander un inventaire des audiences disponibles et des comportements des clients qu’elles capturent. Vous obtenez ainsi le paysage complet avant d’effectuer un forage dans un segment spécifique.

```
What audiences are currently available and what customer behaviors do they represent?
```

+++Voir un exemple de réponse

![Client IA répertoriant les audiences disponibles et les comportements des clients qu’elles représentent](../assets/use-cases/query-audiences/query-audiences-step1-audience-list.png)

+++

## Étape 2 : Identifier vos segments les plus précieux

Avec le paysage de l’audience en vue, demandez-vous quels segments sont les plus grands et ce qui les rend stratégiquement précieux.

```
Which audiences are the largest and what makes them valuable?
```

+++Voir un exemple de réponse

Client ![AI identifiant les audiences les plus importantes et expliquant ce qui les rend précieuses](../assets/use-cases/query-audiences/query-audiences-step2.gif)

+++

## Étape 3 : vérifier l’activation et les destinations

Demandez à vos audiences où elles circulent actuellement et vers quelles destinations elles sont activées.

```
Where are our audiences currently being activated and to which destinations?
```

+++Voir un exemple de réponse

Client ![AI affichant le statut d’activation de l’audience et le mappage de destination](../assets/use-cases/query-audiences/query-audiences-step3.gif)

+++

## Étape 4 : obtenez des recommandations stratégiques

Les outils RTCDP de la passerelle CX Enterprise MCP sont en lecture seule : ils affichent le statut d’activation, l’intégrité de la destination et les données de flux de données, mais ne modifient pas la configuration. Une fois que vous avez identifié un problème, le correctif se produit dans l’application.

```
If you were our audience strategist, what would you prioritize next and why?
```

+++Voir un exemple de réponse

![Client AI donnant des recommandations prioritaires en matière de stratégie d’audience](../assets/use-cases/query-audiences/query-audiences-step4.gif)

+++

>[!NOTE]
>
>Les outils RTCDP de la passerelle CX Enterprise MCP font apparaître les données de destination et d’activation, mais ne peuvent pas modifier la configuration de destination, les définitions de segment ou les paramètres de flux de données. Les étapes de correction se produisent dans l’application Real-Time CDP.

## Ce que vous avez accompli

Vous avez connecté un client d’IA à Real-Time CDP et dressé un portrait stratégique de votre portefeuille d’audiences en quatre invites. Vous avez mappé les audiences disponibles aux comportements de client qu’elles capturent, identifié vos segments les plus volumineux et les plus précieux, confirmé où chaque audience se dirige et vers quelles destinations, et reçu des recommandations prioritaires sur votre prochaine activation. Vous pouvez ainsi parcourir plusieurs écrans de Real-Time CDP plutôt que d’avoir une conversation stratégique directe.

## Plus de choses à accomplir

Les outils Real-Time CDP de la passerelle CX Enterprise MCP prennent en charge un large éventail de requêtes d’audience et d’activation. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer dans la même session.

+++Savoir exactement ce qui coule où avant l’envoi d’une campagne

Les échecs d’activation restent silencieux. Les audiences ne circulent plus sans avertissement et les campagnes sont envoyées à des listes obsolètes. Ces invites vous donnent une idée claire des segments qui atteignent quelles destinations et quand.

**Invites**

```
Which audiences are activated to Google Ads?
```

```
Show me the activation history for the [audience name] audience.
```

```
What is the last refresh time for the [audience name] audience?
```

+++

+++Résoudre les problèmes d’activation avant qu’ils n’affectent une campagne

Une destination qui a manqué une exécution ou un segment sans destination active signifie que votre campagne atteint peut-être moins de personnes que prévu. Ces invites font apparaître ces lacunes de manière proactive.

**Invites**

```
Are there any audiences with no active destinations?
```

```
Are any destination dataflows showing errors right now?
```

```
Which audiences have not been updated in the last 30 days?
```

+++

+++Contrôler et comprendre le paysage de votre audience

Lorsque la taille de l’audience change ou que de nouveaux segments sont créés, un inventaire clair vous aide à planifier et à éviter d’activer la mauvaise liste. Ces invites vous donnent cette visibilité à la demande.

**Invites**

```
How many profiles are in the [segment name] segment?
```

```
Show me all audiences created in the last 30 days.
```

```
Which audience has grown the most in the last 60 days?
```

```
How many total profiles are in my Real-Time CDP instance?
```

+++

+++Comprendre l’identité et la qualité des données

Les espaces de noms d’identité et les politiques de fusion affectent directement les profils inclus dans une audience et leur résolution. Ces invites fournissent des détails de configuration de surface pouvant expliquer des tailles d’audience inattendues ou des chevauchements de profils.

**Invites**

```
What identity namespaces are configured and which are most commonly used?
```

```
What merge policies are defined and which audiences use each one?
```

```
Are there any audiences using a non-default merge policy that could cause profile overlap?
```

+++

## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Documentation Real-Time CDP MCP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | Configuration du serveur MCP et référence des outils |
| [Registre ](https://developer.adobe.com/ai-registry/?type=mcp) | Métadonnées et disponibilité du serveur MCP |
| [Documentation ](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/home) | Documentation complète de l’application Real-Time CDP |
| [Documentation sur les destinations ](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/home) | Référence des destinations complètes |
