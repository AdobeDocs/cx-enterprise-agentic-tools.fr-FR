---
title: Effectuez un déploiement sur AEM as a Cloud Service en toute confiance
description: Vérifiez l’intégrité de l’environnement, consultez l’historique des pipelines et déclenchez ou gérez les déploiements sans quitter votre client d’IA.
last-substantial-update: 2026-06-10T00:00:00Z
source-git-commit: 40d93f878ba9f48c9daffd3beccb4bf829113a36
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 2%

---


# Effectuez un déploiement sur AEM as a Cloud Service en toute confiance

<!-- last-modified: 2026-05-21 -->

>[!VIDEO](https://video.tv.adobe.com/v/3480340/?learn=on&enablevpops)

Le déploiement est plus sûr si vous savez que votre environnement est sain avant d’effectuer des notifications push. Cette présentation explique comment vérifier le statut de l’environnement AEM, consulter l’historique des pipelines et déclencher des déploiements à partir d’un client d’IA à l’aide du serveur MCP AEM Cloud Manager, de sorte que les équipes puissent se déplacer rapidement sans perdre de visibilité.

| Détails du scénario | |
| --- | --- |
| Applications d’entreprise CX | [Adobe Experience Manager Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/introduction-to-cloud-manager) |
| Outils agentiques | [Serveur AEM Cloud Manager MCP](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) |
| Audience | Développeurs, opérations de développement, équipes opérationnelles |
| Prérequis | Client d’IA compatible avec MCP, accès à AEM Cloud Manager |

Chaque étape affiche une invite représentative et un exemple de réponse de l’IA. Une section **Plus d’invites pour essayer** suit pour une exploration supplémentaire dans la même session.

## Avant de commencer

>[!BEGINTABS]

>[!TAB Code Claude]

Accédez d’abord au répertoire de votre projet, puis ajoutez le serveur Cloud Manager MCP à l’aide de l’interface de ligne de commande :

```bash
claude mcp add --transport http adobe-cloud-manager https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

Vous pouvez également l’ajouter manuellement à `.mcp.json` dans la racine de votre projet :

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Redémarrez Claude Code. Les outils de Cloud Manager seront disponibles lors de votre prochaine session.

Configuration complète : [documentation Claude Code MCP](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Curseur]

Ajoutez le serveur Cloud Manager MCP à `~/.cursor/mcp.json` (global) ou `.cursor/mcp.json` dans la racine de votre projet :

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Ouvrez **Paramètres > MCP**, sélectionnez **Se connecter** en regard du serveur et connectez-vous avec votre Adobe ID.

Configuration complète : [documentation Cursor MCP](https://cursor.com/docs/mcp)

>[!TAB  Copilote GitHub ]

Ajoutez le serveur MCP Cloud Manager à `.vscode/mcp.json` dans la racine de votre projet :

```json
{
  "servers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Note : VS Code utilise `"servers"` comme clé de niveau supérieur, et non `"mcpServers"`.

Ouvrez le panneau **Conversation copilote GitHub**, passez en **mode Agent**, puis sélectionnez **Se connecter** en regard du serveur. Les outils MCP ne sont disponibles qu’en mode Agent.

Configuration complète : documentation sur les serveurs MCP [VS Code](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)

>[!TAB Autres clients d’IA]

Vous utilisez un autre environnement compatible avec MCP ? Connectez-vous au serveur Cloud Manager MCP à l’aide de ce point d’entrée :

```
https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

Instructions de configuration complètes pour tous les clients pris en charge : [Connexion à votre client IA](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Connectez-vous avec votre Adobe ID lorsque vous y êtes invité et sélectionnez l’organisation IMS liée à votre programme AEM as a Cloud Service. Les autorisations sont appliquées au niveau du Cloud Manager. Votre client d’IA peut uniquement effectuer des opérations pour lesquelles votre compte est autorisé.
>
>Lors de la première connexion, votre client d’IA peut vous demander de confirmer votre organisation ou votre programme AEM. Une fois ce contexte défini, le serveur MCP l’utilise pour le reste de la session.
>
>Certains outils vous demandent votre approbation avant de s’exécuter. Examinez la mesure proposée et approuvez ou refusez. Aucune action n’est entreprise sans votre confirmation.

## Étape 1 : vérifier le statut de l’environnement

Avant de lancer une version, vérifiez que vos environnements sont sains et que rien n’est en cours d’exécution.

```
What is the status of the production environment?
```

+++Voir un exemple de réponse

Client ![AI affichant le statut de l’environnement de production à partir de Cloud Manager](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step1-01-ai.png)

+++


## Étape 2 : vérifier les exécutions de pipeline

Consultez l’historique récent des pipelines pour comprendre les modèles de déploiement et intercepter les échecs avant qu’ils ne bloquent votre prochaine version.

```
Show me the last five pipeline runs for the production pipeline.
```

+++Voir un exemple de réponse

Client ![AI affichant les cinq dernières exécutions de pipeline pour le pipeline de production](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step2-01-ai.png)

+++


## Étape 3 : déclencher un pipeline

Démarrer un pipeline directement à partir de votre client d’IA. Le serveur confirme l’environnement cible et demande une validation avant de démarrer.

```
Run the Fullstack pipeline against dev environment of WKND sandbox program.
```

+++Voir un exemple de réponse

Client ![AI affichant la confirmation du déclenchement du pipeline et l’interface utilisateur de Cloud Manager reflétant le pipeline en cours d’exécution](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step3.gif)

+++


>[!CAUTION]
>
>Le client d’IA vous demandera de confirmer le nom du pipeline avant de déclencher une exécution. Saisissez le nom exact du pipeline pour continuer. Examinez attentivement l’environnement cible avant de confirmer, en particulier pour les pipelines qui se déploient en production.

## Étape 4 : vérifier le statut du pipeline

Après le déclenchement d’une exécution, demandez à votre client d’IA une mise à jour de statut sans passer à l’interface de Cloud Manager.

```
What is the status of the triggered pipeline?
```

+++Voir un exemple de réponse

Client ![AI affichant le statut de l’exécution du pipeline déclenché](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step4-01-ai.png)

+++


## Ce que vous avez accompli

Vous avez utilisé AEM Cloud Manager MCP Server pour vérifier l’intégrité de l’environnement, consulter l’historique des pipelines, déclencher un déploiement et vérifier son statut, sans ouvrir l’interface de Cloud Manager. En combinant la visibilité de l’environnement et le contrôle du déploiement dans une seule session d’IA, les équipes de développement et d’exploitation peuvent répondre plus rapidement aux problèmes et conserver leur workflow au sein des outils qu’elles utilisent déjà.

## Plus de choses à accomplir

Le serveur Cloud Manager MCP gère bien plus que ce que couvre la présentation ci-dessus. Développez un scénario ci-dessous pour afficher les invites que vous pouvez essayer dans la même session.

+++Détecter les problèmes avant qu’une version ne soit lancée

Les déploiements échouent souvent pour des raisons qui étaient visibles avant l’exécution du pipeline. Ces invites vous aident à confirmer l&#39;intégrité de l&#39;environnement, à rechercher les exécutions en conflit et à vérifier l&#39;alignement des versions entre les environnements avant de valider une version.

**Invites**

```
We're about to kick off a production release. Give me a full status check on all environments first.
```

```
Is there anything currently running in the staging pipeline? I don't want to queue on top of an active run.
```

```
Before I promote main branch to production, confirm main was deployed to Dev and all environments are on the same AEM version.
```

```
What repositories are connected to the WKND program?
```

+++

+++Cours-corriger un déploiement qui est déjà en cours

Un déclencheur accidentel ou un point de contrôle d’approbation bloqué peut se traduire en cascade par un pipeline bloqué ou un déploiement indésirable. Ces invites vous permettent d&#39;annuler ou d&#39;avancer un pipeline en cours d&#39;exécution sans passer à l&#39;interface Cloud Manager.

**Invites**

```
The staging pipeline kicked off by mistake. Cancel it before it deploys.
```

```
The release pipeline is waiting at the approval gate. Advance it to continue the deployment.
```

+++

+++Comprendre l’historique de votre déploiement

Savoir quand les choses ont réussi pour la dernière fois, combien de temps les pipelines fonctionnent et si les modèles changent vous aide à planifier les publications et à capturer une dégradation lente avant qu’elle ne devienne un incident. Utilisez ces invites pour extraire cet historique à la demande.

**Invites**

```
What is the status of the last production pipeline execution? If it failed, explain why.
```

```
When was the last successful deployment to the staging environment?
```

```
Our pipeline times are creeping up. What's the longest run we've had in the last 30 days?
```

+++

+++Remettre une version endommagée sur la bonne voie

Lorsqu’un pipeline échoue, le chemin le plus rapide vers la résolution est de comprendre exactement où et pourquoi il s’est rompu. Ces invites indiquent les détails des échecs de surface, l&#39;historique des modifications et les problèmes de point de contrôle qualité afin que votre équipe puisse diagnostiquer et corriger sans fouiller manuellement dans les journaux.

**Invites**

```
We're seeing a regression on the live site. What changed in production over the last week?
```

```
Which pipelines have failed in the last 7 days, and at what stage did they fail?
```

```
The last pipeline failed at the code quality step. What specific issues need to be fixed before I can retry?
```

```
Pull the step logs for the last failed run. I need to see exactly what the quality gate flagged.
```

+++


## Informations supplémentaires

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Documentation d’AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service){target="_blank"} | Documentation complète de l’application AEM |
