---
title: Optimiser le contenu en fonction des données de performance
description: Utilisez les serveurs MCP CJA et AEM ensemble pour identifier le contenu peu performant et le mettre à jour, sans changer d’outil.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# Optimiser le contenu en fonction des données de performance

<!-- last-modified: 2026-05-21 -->

![Optimisation du contenu en fonction des données de performances](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

Pour boucler la boucle entre les données de performances du contenu et les mises à jour de contenu, basculez normalement entre les analyses et votre CMS. Cette présentation montre comment connecter Customer Journey Analytics et AEM dans la même session d’IA, afin que vous puissiez faire apparaître les pages peu performantes et les mettre à jour sans quitter votre conversation.

| | |
| --- | --- |
| Applications d’entreprise CX | Customer Journey Analytics, Adobe Experience Manager as a Cloud Service |
| Outils agentiques | Passerelle MCP Entreprise CX, serveur MCP de contenu AEM |
| Audience | Responsables de campagne, stratèges de contenu, opérations marketing |
| Prérequis | Client d’IA compatible MCP, accès CJA, accès AEM as a Cloud Service |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. La section **Plus que vous pouvez accomplir** suit pour une exploration supplémentaire au cours de la même session.

## Avant de commencer

>[!BEGINTABS]

>[!TAB Claude.ai]

Connectez les deux serveurs MCP en tant que connecteurs personnalisés. Ajoutez chacun séparément.

1. Accédez à **Paramètres > Intégrations** dans Claude.ai.
2. Sélectionnez **Ajouter un connecteur personnalisé**, saisissez une URL de serveur, puis sélectionnez **Se connecter**.
3. Connectez-vous avec votre Adobe ID, puis répétez l’opération pour le deuxième serveur.

| Serveur | Point d’entrée |
| --- | --- |
| Passerelle MCP Entreprise CX | `https://cx-enterprise.adobe.io/mcp` |
| Serveur AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configuration complète : [documentation des connecteurs personnalisés Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Connectez les deux serveurs MCP en mode Développeur ChatGPT (Pro, Plus, Business, Enterprise ou Education plan requis). Ajoutez chaque serveur séparément.

1. Activez le **mode Développeur** dans **Paramètres ChatGPT**.
2. Accédez à **Paramètres > Intégrations** et sélectionnez **Ajouter un connecteur personnalisé > Serveur MCP distant**.
3. Saisissez une URL de serveur, sélectionnez **Connexion** et connectez-vous avec votre Adobe ID.
4. Répétez l’opération pour le deuxième serveur.

| Serveur | Point d’entrée |
| --- | --- |
| Passerelle MCP Entreprise CX | `https://cx-enterprise.adobe.io/mcp` |
| Serveur AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configuration complète : [documentation MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Autres clients d’IA]

Utiliser Gemini, Microsoft Copilot, Cursor, Claude Code ou un autre environnement compatible avec MCP ? Connectez-vous aux deux serveurs MCP à l’aide des points d’entrée suivants :

| Serveur | Point d’entrée |
| --- | --- |
| Passerelle MCP Entreprise CX | `https://cx-enterprise.adobe.io/mcp` |
| Serveur AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Instructions de configuration complètes pour tous les clients pris en charge : [Connexion à votre client IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à vos environnements CJA et AEM. Choisir la mauvaise organisation est la source la plus courante d’erreurs d’authentification.
>
>Lors de la première connexion, votre client d’IA peut vous demander de sélectionner une organisation IMS ou de spécifier un sandbox. Une fois ce contexte défini, le serveur MCP l’utilise pour le reste de la session.
>
>Certains outils vous demandent votre approbation avant de s’exécuter. Examinez la demande et approuvez ou refusez — aucune action n&#39;est entreprise sans votre confirmation.

## Étape 1 : identifier le contenu peu performant

Utilisez la passerelle CX Enterprise MCP pour classer les pages par mesures d’engagement et de conversion dans Customer Journey Analytics. L’objectif est d’obtenir une liste claire et hiérarchisée des contenus auxquels il faut prêter attention.

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++Voir un exemple de réponse

Pages d’engagement les plus basses (du 22 mars au 21 mai 2026) :

| Classer | Page | Taux d’engagement | Taux de rebond | Moy. temps passé sur la page |
| --- | --- | --- | --- | --- |
| 1 | /fr/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /fr/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /fr/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12,3-14,1 % | 63-67 % | :35-1:10 |

Le taux d’engagement moyen de votre site est de 34,7 %. Ces pages sont 2 à 4 fois inférieures à la moyenne.

+++

## Étape 2 : consulter le contenu dans AEM

Sans quitter votre session d’IA, extrayez l’état actuel de ces pages d’AEM. Comprendre le contenu est la première étape pour savoir ce qui doit être modifié.

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++Voir un exemple de réponse

**Page:** `/en/products/analytics`
**Dernière modification :** 30 avril 2026 par T. MacMillan
**Statut :** Publié

**Section Hero :**
Titre : « Décisions basées sur les données pour chaque équipe »
Sous-titre : « Adobe Analytics fournit à votre organisation les informations nécessaires pour agir ».
CTA : « Demander une démonstration » → /contact/demo

**Corps :** 3 blocs de fonctionnalités suivis d’une bande de logo du client et d’un CTA secondaire. Aucun élément vidéo ou interactif. La page n’a pas été mise à jour depuis 21 jours.

**Description Meta :** « Adobe Analytics : rapports en temps réel et informations d’IA pour les équipes d’entreprise ».

+++

## Étape 3 : effectuer des mises à jour ciblées

Avec les données de performances et le contenu actuel en vue, effectuez des mises à jour basées sur ce que les données ont révélé.

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++Voir un exemple de réponse

**Modification proposée :**

| Champ | Valeur actuelle | Nouvelle valeur |
| --- | --- | --- |
| Titre du héros | Décisions axées sur les données pour chaque équipe | Prendre des décisions plus rapides grâce aux analyses optimisées par l’IA |

Page : `/en/products/analytics`

Confirmer cette modification ? Si vous répondez « oui », la mise à jour sera enregistrée dans AEM. La page reste publiée dans son état actuel jusqu’à ce que vous la republiiez explicitement.

+++

>[!CAUTION]
>
>Confirmez chaque modification de contenu lorsque vous y êtes invité. Examinez la comparaison complète avant d’approuver les mises à jour des pages actives.

## Étape 4 : valider et publier

Fermez la boucle en confirmant toutes les modifications et en promouvant le contenu lorsque vous êtes satisfait(e) des mises à jour.

```
Show me a summary of all changes made in this session.
```

+++Voir un exemple de réponse

**Résumé de la session — 21 mai 2026:**

| Page | Changement | Statut |
| --- | --- | --- |
| /fr/products/analytics | Titre du héros mis à jour | Enregistré, dépublié |

1 page mise à jour. Prêt à publier une fois confirmé.

**Restant de votre liste à faible engagement :** 9 pages n’ont pas été mises à jour au cours de cette session. Voulez-vous passer à la page suivante ou créer un lancement pour la révision par lots avant la publication ?

+++

## Ce que vous avez accompli

Vous avez connecté Customer Journey Analytics et AEM en une seule session d’IA et utilisé les données de performances pour informer directement les modifications de contenu. En passant de la mesure à la mise à jour sans changer d’outil, vous avez raccourci la boucle des commentaires entre Analytics insight et le contenu publié. C’est à l’échelle d’une campagne que cela importe le plus, car des dizaines de pages peuvent nécessiter une attention particulière et les workflows manuels entre outils entraînent des retards.

## Plus de choses à accomplir

Les serveurs CJA et AEM MCP prennent en charge le cycle complet, de l’identification des problèmes aux correctifs d’expédition. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer dans la même session.

+++Recherche du contenu qui freine vos performances

Un trafic élevé avec un faible engagement signale un problème de contenu, pas un problème de trafic. Ces invites vous aident à faire apparaître les pages et les modèles spécifiques qui nécessitent une attention particulière avant qu’une échéance de campagne ne force le problème.

**Invites**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++Correction de ce que les données vous indiquent de corriger

Une fois que vous savez ce qui ne fonctionne pas, l’étape suivante consiste à apporter des modifications ciblées. Ces invites vous permettent de mettre à jour les titres, les CTA et les méta-descriptions en fonction de ce que les données de performances ont révélé.

**Invites**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++Améliorations des expéditions avant la prochaine campagne

Les modifications apportées en milieu de session peuvent s’accumuler rapidement. Ces invites vous aident à vérifier ce qui est prêt, à regrouper les mises à jour dans un lancement révisable et à effectuer une promotion propre avant qu’une campagne ne soit activée.

**Invites**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Documentation MCP Analytics](https://developer.adobe.com/analytics-mcp/docs/) | Configuration de CJA MCP et référence des outils |
| [Documentation d’AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | Documentation complète d’AEM |
| [Serveur CJA MCP dans le registre IA](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | Disponibilité et outils du serveur CJA MCP |
| [Serveur AEM Content MCP dans le registre AI](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | Disponibilité et outils du serveur AEM Content MCP |
| [ Serveurs MCP ](../tools/mcp-servers.md) | Connexion d’un client d’IA aux serveurs MCP Adobe |
