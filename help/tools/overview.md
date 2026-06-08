---
title: Outils Agentic
description: Comparez les serveurs MCP, les compétences des agents et les API pour Builders et choisissez l’outil agentique approprié pour vos workflows Adobe CX Enterprise.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 2%

---


# Outils Agentic

<!-- last-modified: 2026-05-08 -->

Toutes les méthodes d’outillage des agences ne répondent pas au même besoin. Les serveurs MCP vous permettent d’accéder immédiatement aux données Adobe en langage naturel à partir de n’importe quel client d’IA compatible, sans codage requis. Les compétences des agents codent l’expertise du domaine Adobe en workflows d’agent répétables afin que les tâches s’exécutent de manière cohérente à chaque fois. Les API offrent aux développeurs un contrôle programmatique complet pour créer des applications et des intégrations personnalisées. Cette page décrit les compromis à effectuer pour choisir le bon point de départ pour votre situation.

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->

## Comparer les outils agentiques

| | Serveurs MCP | Compétences de l’agent | API pour les créateurs |
| --- | --- | --- | --- |
| Idéal pour | Utilisateurs de clients d’IA | Tous les utilisateurs | Développeurs |
| Nécessite un codage | Non | Non | Oui |
| Heure de configuration | Minutes | Minutes | Heures en jours |
| Ce que vous obtenez | Accès à Adobe à partir de votre outil d’IA | Workflows guidés et reproductibles | Contrôle programmatique complet |
| Client d’IA nécessaire | Oui | Oui | Facultatif |

## Vous ne savez pas par où commencer ?

- Pour utiliser l’IA afin d’interagir avec les applications d’entreprise Adobe CX (prendre des mesures, interroger des données et laisser l’IA découvrir ce qu’il doit faire ensuite par le biais d’une conversation naturelle), les [serveurs MCP](mcp-servers.md) constituent le point de départ le plus flexible.
- Pour que les agents suivent de manière cohérente les workflows natifs d’Adobe sans improvisation, [les compétences des agents](agent-skills.md) codent cette expertise de domaine dans des instructions réutilisables.
- Pour créer une application ciblée qui simplifie ou automatise un workflow Adobe spécifique pour vos utilisateurs, les [API pour les créateurs](apis.md) vous permettent de contrôler directement et par programmation ce qui se passe exactement.

>[!BEGINTABS]

>[!TAB  Serveurs MCP ]

Considérez les serveurs MCP comme un lien en direct entre votre outil d’IA et Adobe. Connectez-vous une seule fois et votre IA peut interroger les campagnes, extraire les audiences, vérifier le statut du parcours, etc. Le tout en langage clair, sans code.

**Utiliser des serveurs MCP quand :**

- Vous souhaitez que les données Adobe se trouvent dans l’outil d’IA que vous utilisez déjà
- Vous effectuez une analyse exploratoire ou une récupération de données ad hoc
- Vous souhaitez obtenir des résultats rapidement, sans démarrer de projet

**Faites un essai :** demandez à Claude de résumer vos parcours actifs. Extrayez les tailles d’audience Real-Time CDP à partir du ChatGPT. Examinez les mesures de campagne CJA sans ouvrir de tableau de bord.

[Explorer les serveurs MCP](mcp-servers.md)

>[!TAB Compétences agent]

Les compétences de l’agent sont des compétences de domaine Adobe, encodées en instructions que votre agent peut suivre. Au lieu d&#39;espérer que votre agent comprenne les bonnes étapes, une compétence lui dit exactement ce qu&#39;il doit faire. Fiable, répétable et déjà adapté aux workflows Adobe.

**Utiliser les compétences de l’agent lorsque :**

- Vous souhaitez que la même tâche soit effectuée de la même manière à chaque fois
- Vous exécutez des workflows de production de contenu ou de médias répétables.
- Vous voulez un agent qui connaît Adobe sans avoir à l’expliquer

**Essayez-le :** Modifier par lots un ensemble de photos pour obtenir un aspect cohérent. Générez des variantes de réseaux sociaux prêts pour la plateforme à partir d’une ressource source. Concevez à partir d’un modèle Adobe Express en quelques invites.

[Explorer les compétences de l’agent](agent-skills.md)

>[!TAB API pour Builders]

Les API sont les blocs de création. Ils permettent aux développeurs d’accéder directement et par programmation aux données et aux opérations d’Adobe, en utilisant les mêmes API que celles qui alimentent leurs propres produits Adobe. Utilisez-les pour créer quelque chose qui s’exécute selon votre planning, vos conditions et votre pile.

**Utiliser des API quand :**

- Vous créez une application ou un tableau de bord personnalisé
- Vous devez intégrer des données Adobe dans un autre système
- Vous utilisez Claude Code ou Cursor pour générer une application complète
- Un contrôle complet de création, de mise à jour ou de suppression est nécessaire

**Essayer :** créer un tableau de bord de campagne personnalisé. Automatisez un pipeline de données. Générez une application avec du code Claude qui lit et écrit dans Adobe Experience Platform.

[Explorer les API pour Builders](apis.md)

>[!ENDTABS]

## Les utiliser ensemble

Les serveurs MCP, les compétences des agents et les API sont complémentaires. De nombreux workflows combinent les trois :

- Une compétence d’agent définit le workflow et guide l’agent
- Les serveurs MCP permettent à l’agent d’accéder en lecture aux données d’Adobe en cours de workflow
- Les API gèrent les actions qui nécessitent des écritures système directes ou une logique d’application personnalisée
