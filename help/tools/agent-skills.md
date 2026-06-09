---
title: Compétences de l’agent
description: Workflows et instructions traités par Adobe qui guident les agents d’IA de manière cohérente tout au long des tâches d’entreprise CX.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: a130fc470e97f2316e2ea72ebda47b9fc4ad9b33
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---


# Compétences de l’agent

<!-- last-modified: 2026-05-19 -->

![Compétences agent pour Adobe CX Enterprise](../assets/hero-agent-skills.png)

Les compétences des agents sont des workflows traités par Adobe qui fournissent aux agents d’IA des instructions détaillées pour exécuter de manière fiable les tâches d’Adobe CX Enterprise. Chaque compétence d’agent encode l’expertise du domaine et les bonnes pratiques afin que les agents produisent des résultats cohérents et validés sans avoir à improviser. Les compétences d’agent ont un sens lorsque vous souhaitez un comportement guidé et reproductible tout au long des conversations, en particulier pour les tâches qui nécessiteraient autrement une invite détaillée à chaque fois. Ils complètent les serveurs MCP et les API : les compétences des agents définissent le fonctionnement d’un agent. Les serveurs MCP et les API fournissent l’accès sous-jacent.

## Compétences de l’agent d’entreprise Adobe CX

Sélectionnez une zone de fonctionnalité ci-dessous pour explorer les compétences de ce workflow.

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

Compétences d’agent pour le développement, le contenu, la conception et la gestion de projet Experience Manager dans AEM as a Cloud Service, Edge Delivery Services et AEM 6.5 LTS.

[Afficher les compétences de l’agent](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

Compétences de l’agent pour la surveillance des KPI, l’analyse funnel et les workflows de reporting exécutif dans Adobe Analytics.

[Afficher les compétences de l’agent](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

Compétences de l’agent pour la comparaison des performances, l’analyse des dimensions et la création d’espaces de travail dans Customer Journey Analytics.

[Afficher les compétences de l’agent](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

Compétences en agent pour la génération de modèles automatique, le test et le déploiement d’applications personnalisées avec Adobe App Builder.

[Afficher les compétences de l’agent](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Tab]

Compétences d’agent pour la modification de photos par lots, la conception à partir de modèles, la modification vidéo et les variantes de médias sociaux avec Creative Cloud.

[Afficher les compétences de l’agent](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## Add Agent Skills

![Fonctionnement des compétences d’agent](../assets/hero-connect-agent-skills.gif)

Une compétence d’agent est un ensemble d’instructions qui indique à un agent d’IA comment effectuer une tâche à l’aide d’outils d’agent Adobe. Lorsqu’un agent charge une compétence, il suit ce workflow plutôt que d’improviser.

### Installer les compétences de l’agent

Les compétences de l’agent sont installées en fonction du client d’IA que vous utilisez. Certains clients prennent en charge l’installation directe à partir de la ligne de commande :

- **Code Claude** : `/plugin install adobe/skills`
- **Environnements de nœud** : `npx skills add adobe/skills`
- **GitHub CLI** : `gh upskill adobe/skills`

Pour les autres clients, vous devez télécharger et ajouter directement les fichiers de compétences à votre client d’IA. Consultez le [LISEZ-MOI des compétences Adobe sur GitHub](https://github.com/adobe/skills#installation) pour obtenir des instructions d’installation complètes par client.

### Recherche de compétences d’agent

Parcourez la liste complète des compétences disponibles dans le référentiel GitHub [Compétences &#x200B;](https://github.com/adobe/skills). Chaque compétence d’agent comprend un fichier `SKILL.md` avec des conseils détaillés, des références et des exemples.

Après avoir installé ou ajouté le package `adobe/skills`, certains clients d’IA vous permettent de répertorier directement toutes les compétences disponibles :

- **Code Claude** : `claude /plugin list`
- **Environnements de nœud** : `npx skills list`
- **GitHub CLI** : `gh upskill list`
