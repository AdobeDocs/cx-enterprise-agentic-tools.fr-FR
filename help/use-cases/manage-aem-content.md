---
title: Tenez le contenu à jour et envoyez les mises à jour plus rapidement
description: Utilisez le serveur MCP AEM pour rechercher, réviser, mettre à jour et publier du contenu AEM sans passer d’un outil à l’autre.
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 7%
---

# Tenez le contenu à jour et envoyez les mises à jour plus rapidement

<!-- last-modified: 2026-05-22 -->

![La plateforme d’IA qui confirme la publication de la page renvoie l’URL active](../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

Maintenir le contenu du site à jour est une pression opérationnelle constante. Cette présentation explique comment les équipes de contenu peuvent rechercher, réviser, mettre à jour et publier des pages et des fragments de contenu AEM par le biais d’une plateforme d’IA, à l’aide du serveur MCP AEM pour réduire le temps entre une décision de contenu et une mise à jour en direct.

| Détails du scénario | |
| --- | --- |
| Applications CX Enterprise | [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/overview/introduction) |
| Outils agentiques | [Adobe CX Enterprise Coworker](https://experienceleague.adobe.com/fr/docs/cx-enterprise-coworker/content/home), [Adobe CX Enterprise Coworker pour les plateformes d’IA](../tools/mcp-servers.md#connect-to-your-ai-platform) ou [AEM MCP Server](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/ai/mcp-servers/overview) |
| Audience | Gestionnaires de contenu, équipes marketing |
| Prérequis | Accès à AEM as a Cloud Service, plus Coworker, une plateforme d’IA avec Coworker pour les plateformes d’IA ou une plateforme d’IA compatible avec MCP |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. Une section **Plus que vous pouvez accomplir** suit pour une exploration supplémentaire dans la même session.

## Avant de commencer

>[!BEGINTABS]

>[!TAB Coworker]

Le moyen le plus rapide d’y parvenir est Coworker, qui ne nécessite aucune configuration de serveur ou de plateforme d’IA. [Essayer Un Collègue](https://experienceleague.adobe.com/fr/docs/cx-enterprise-coworker/content/home)

Si vous ne pouvez pas ou ne souhaitez pas utiliser directement Coworker, utilisez-le plutôt à partir de votre propre plateforme d’IA. Consultez l’onglet **Collègues pour les plateformes d’IA**. Si cela ne fonctionne pas non plus pour vous, connectez directement votre plateforme d’IA au serveur MCP AEM à l’aide des onglets restants.

>[!TAB Collègue pour les plateformes d’IA]

Vous pouvez également effectuer cette présentation avec Coworker pour les plateformes d’IA à partir de votre propre plateforme d’IA. [Configuration de Coworker pour les plateformes d’IA](../tools/mcp-servers.md#connect-to-your-ai-platform) | [Documentation Adobe](https://experienceleague.adobe.com/fr/docs/coworker/content/ai-platforms#set-up-coworker)

>[!TAB Claude.ai]

Connectez le serveur AEM MCP en tant que connecteur personnalisé.

1. Accédez à **Paramètres > Intégrations** dans Claude.ai.
2. Sélectionnez **Ajouter un connecteur personnalisé** et saisissez l’URL du serveur : `https://mcp.adobeaemcloud.com/adobe/mcp/aem`
3. Sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.

Configuration complète : [Documentation sur les connecteurs personnalisés Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Connectez le serveur AEM MCP à l’aide du mode Développeur ChatGPT (Pro, Plus, Business, Enterprise ou Education plan requis).

1. Activez le **mode Développeur** dans les **paramètres ChatGPT**.
2. Accédez à **Paramètres > Intégrations** et sélectionnez **Ajouter un connecteur personnalisé > Serveur MCP distant**.
3. Saisissez l&#39;URL du serveur : `https://mcp.adobeaemcloud.com/adobe/mcp/aem`
4. Sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.

Configuration complète : [Documentation du MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Autres plateformes d’IA]

Utiliser Gemini, Microsoft Copilot, Cursor, Claude Code ou un autre environnement compatible avec MCP ? Connectez-vous au serveur AEM MCP à l’aide de ce point d’entrée :

```
https://mcp.adobeaemcloud.com/adobe/mcp/aem
```

Instructions de configuration complètes pour toutes les plateformes d’IA prises en charge : [Connexion à votre plateforme d’IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à votre environnement AEM as a Cloud Service. Les autorisations sont appliquées au niveau d’AEM. Votre plateforme d’IA peut uniquement effectuer des opérations pour lesquelles votre compte est autorisé.
>
>Lors de la première connexion, votre plateforme d’IA peut vous demander de confirmer votre organisation ou l’environnement AEM. Une fois ce contexte défini, le serveur MCP l’utilise pour le reste de la session.
>
>Certains outils vous demandent votre approbation avant de s’exécuter. Examinez la mesure proposée et approuvez ou refusez. Aucune modification n’est apportée sans votre confirmation.

## Étape 1 : recherche de contenu dans l’ensemble de votre environnement AEM

Commencez par demander à votre plateforme d’IA de découvrir vos environnements AEM et de rechercher du contenu. Vous pouvez effectuer des recherches par sujet, mot-clé ou type de contenu sans connaître les chemins exacts.

```
From WKND Dev environment, find all ski related content.
```

+++Voir un exemple de réponse

![Plateforme d’IA affichant les résultats de recherche de contenu de ski de l’environnement WKND Dev AEM](../assets/use-cases/manage-aem-content/manage-aem-content-step1-find-ski.png){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


## Étape 2 : vérifier une page spécifique

Une fois que vous avez localisé le contenu pertinent, demandez à votre plateforme d’IA de vous afficher une page spécifique. Vous pouvez faire référence aux pages par leur nom ou leur chemin d’accès. Le serveur MCP résout la référence et renvoie la structure du contenu.

```
Show me the US English Home Page.
```

+++Voir un exemple de réponse

![Plateforme d’IA affichant la structure de contenu de la page d’accueil en anglais américain d’AEM](../assets/use-cases/manage-aem-content/manage-aem-content-step2-home-page.png){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


## Étape 3 : améliorer le contenu

Une fois le contenu de la page affiché, demandez à votre plateforme d’IA de suggérer ou d’appliquer des améliorations. L’IA peut proposer des modifications de copie basées sur ce que la page dit actuellement et demander une confirmation avant d’écrire quoi que ce soit.

```
Improve the Hero CTAs.
```

+++Voir un exemple de réponse

![Plateforme d’IA proposant une copie améliorée de CTA Hero avec une invite de confirmation avant d’appliquer les modifications](../assets/use-cases/manage-aem-content/manage-aem-content-step3.gif){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


>[!CAUTION]
>
>Confirmez chaque modification lorsque vous y êtes invité. AEM MCP Server peut créer, mettre à jour et supprimer du contenu. Examinez la modification proposée avant l’approbation, en particulier sur les pages actives.

## Étape 4 : publier et partager

Après avoir confirmé la mise à jour, publiez la page et récupérez une URL partageable, le tout dans la même conversation.

```
Publish the changes and share the URL.
```

+++Voir un exemple de réponse

![La plateforme d’IA qui confirme la publication de la page renvoie l’URL active](../assets/use-cases/manage-aem-content/manage-aem-content-step4.gif){zoomable="yes"}

*Sélectionner pour effectuer un zoom.*

+++


## Ce que vous avez accompli

Vous avez utilisé le serveur MCP AEM pour rechercher du contenu, passer en revue une page active, apporter des améliorations suggérées par l’IA et publier le résultat, sans ouvrir l’interface d’AEM. En associant la découverte, la modification et la publication de contenu dans une seule session d’IA, les équipes de contenu peuvent passer de l’identification d’un écart à l’envoi et à la mise à jour plus rapidement et avec moins de changements de contexte. Le même workflow se met à l’échelle à plusieurs pages, fragments de contenu et lancements de campagne coordonnés.

## Plus de choses à accomplir

Le serveur AEM MCP gère bien plus que les couvertures de présentation. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer dans la même session.

+++Anticiper la révision ou la relance d’un site

Les audits de contenu prennent du temps lorsqu’ils sont effectués manuellement. Ces invites vous permettent de faire rapidement apparaître le contenu obsolète, les brouillons qui n&#39;ont jamais été envoyés et les trous qui doivent être corrigés avant une notification push majeure.

**Invites**

```
Show me everything updated in the last two weeks.
```

```
What content is sitting in draft and hasn't been published yet?
```

```
Find pages that haven't been touched in over a year.
```

```
Which pages are missing their description field?
```

```
We're reorganizing the taxonomy. Find all articles missing tags or categories.
```

+++

+++Correction des problèmes d’optimisation pour les moteurs de recherche et d’accessibilité à grande échelle

Les écarts d’optimisation pour les moteurs de recherche et d’accessibilité se multiplient rapidement sur les sites volumineux. Ces invites vous aident à trouver et à classer par priorité les problèmes les plus importants avant un audit ou un lancement.

**Invites**

```
Pull a list of all pages with an empty meta description.
```

```
Which pages have thin content that's likely to underperform for SEO?
```

```
Find all images missing alt text.
```

```
Our CTAs aren't consistent. Scan the site and flag anywhere the call-to-action wording differs from "Book now."
```

```
The homepage was updated yesterday. Show me what changed compared to the version before.
```

+++

+++Gardez votre bibliothèque de ressources organisée et prête

Les références de ressources endommagées et les chargements non traités ralentissent la production de contenu. Ces invites vous aident à rechercher et à gérer les ressources avant de bloquer une mise à jour de page ou une campagne.

**Invites**

```
We're building a biking content series. What image assets do we already have?
```

```
Can you upload a placeholder asset from https://placehold.co/800x450/png to the wknd folder and save it as placeholder.png?
```

```
That asset was just uploaded. Is it processed and ready to use in a page?
```

```
I need to replace the hero image across the site. Which fragments are currently using it?
```

+++

+++Coordination du lancement d’un contenu sur plusieurs pages

Le lancement d’une campagne implique souvent la coordination des modifications entre plusieurs fragments de contenu et pages. Ces invites vous aident à regrouper les mises à jour, à les examiner avant de les promouvoir et à les expédier proprement.

**Invites**

```
I need to update the surfing adventure. Show me its content and all its fields.
```

```
Create an EMEA market variation of the ski adventure fragment.
```

```
Bundle everything we changed in this session into a launch called May Updates.
```

```
What launches are open right now, and which ones are ready to promote?
```

```
Before I promote, show me exactly what changed between May Updates and what is currently live.
```

```
Promote the May Updates launch to production.
```

+++


## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Documentation du serveur AEM MCP](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/ai/mcp-servers/overview){target="_blank"} | Liste des outils et disponibilité |
| [Documentation d’AEM as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service){target="_blank"} | Documentation complète de l’application AEM |
