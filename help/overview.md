---
title: Outils Adobe CX Enterprise Agentic
description: Connectez les agents IA et les outils de développement aux fonctionnalités Adobe CX Enterprise à l’aide de serveurs MCP, d’Agent Skills et d’API.
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 6%
---

# Outils Adobe CX Enterprise Agentic

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491244/?captions=fre_fr&learn=on&enablevpops)

Laissez AI devenir votre collaborateur pour Adobe CX Enterprise. Connectez votre plateforme d’IA aux campagnes, aux audiences, aux parcours et au contenu. Interagissez avec eux en langage clair à partir de n’importe quel outil que vous utilisez déjà. Pas de nouvelles interfaces, pas de changement de contexte, pas de codage requis pour commencer.

>[!TIP]
>**Commencer avec Adobe CX Enterprise Coworker.** Il est compatible avec vos applications CX Enterprise, aucune configuration de serveur ou de plateforme d’IA n’étant requise. [Essayer Un Collègue](https://experienceleague.adobe.com/fr/docs/cx-enterprise-coworker/content/home)
>
>Vous préférez rester dans Claude, ChatGPT, Microsoft 365 Copilot, ou une autre plateforme d&#39;IA ? Utilisez [Adobe CX Enterprise Coworker pour les plateformes d’IA](tools/mcp-servers.md#connect-to-your-ai-platform). Si aucun d’eux ne fonctionne pour vous, connectez votre plateforme d’IA aux [serveurs MCP de produit](tools/mcp-servers.md#connect-to-your-ai-platform).

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI platform to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
  {cta = Explore MCP Servers}
  {image = assets/mcp-servers-card.png}

* tools/agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflows that guide agents through CX Enterprise tasks. Domain expertise encoded once, applied consistently.}
  {cta = Explore Agent Skills}
  {image = assets/agent-skills-card.png}

* tools/apis.md
  {title = APIs for Builders}
  {description = Build custom Adobe CX Enterprise applications using agentic coding tools like Claude Code and Cursor.}
  {cta = Explore APIs for Builders}
  {image = assets/apis-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="Serveurs MCP">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="Serveurs MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" title="Serveurs MCP">Serveurs MCP</a>
                    </p>
                    <p class="is-size-6">Connectez n’importe quelle plateforme d’IA compatible MCP aux workflows Adobe CX Enterprise. Interroger des données, analyser des campagnes et accéder à des audiences sans quitter votre outil d’IA.</p>
                </div>
                <a href="tools/mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorer les serveurs MCP</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="Compétences de l’agent">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="Compétences de l’agent"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" title="Compétences de l’agent">Compétences De L’Agent</a>
                    </p>
                    <p class="is-size-6">Workflows traités par Adobe qui guident les agents tout au long des tâches de CX Enterprise. Expertise du domaine encodée une fois, appliquée de manière cohérente.</p>
                </div>
                <a href="tools/agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorer les compétences de l’agent</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="API pour les créateurs">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="API pour les créateurs"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/apis.md" title="API pour les créateurs">API pour Builders</a>
                    </p>
                    <p class="is-size-6">Créez des applications Adobe CX Enterprise personnalisées à l’aide d’outils de codage agentiques tels que Claude Code et Cursor.</p>
                </div>
                <a href="tools/apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Explorer les API pour les créateurs</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Des outils agentiques pour chaque équipe

>[!BEGINTABS]

>[!TAB Serveurs MCP]

Utilisez n’importe quelle plateforme d’IA compatible pour accéder aux applications CX Enterprise en langage clair. Aucun codage requis. Commencez avec Coworker pour obtenir le chemin le plus rapide entre les applications. Pour rester sur votre propre plateforme d’IA, utilisez Coworker pour les plateformes d’IA. Si aucun de ces protocoles ne fonctionne, connectez-vous directement à AJO, CJA, AEM et d’autres applications avec leur propre serveur MCP.

- Connectez-vous en quelques minutes depuis Claude, Cursor, ChatGPT et d&#39;autres plateformes d&#39;IA compatibles avec MCP
- Interrogation des campagnes, des audiences et des données de parcours à l’aide du langage naturel
- Aucune nouvelle interface ou formation requise

[Prise en main des serveurs MCP](tools/mcp-servers.md)

>[!TAB Compétences De L’Agent]

Les compétences de l’agent codent l’expertise du domaine Adobe en tant qu’instructions que votre plateforme d’IA peut suivre. Au lieu d’improviser, l’agent sait exactement ce qu’il doit faire, de manière fiable, répétée et alignée sur les bonnes pratiques Adobe.

- Résultats cohérents pour les workflows CX Enterprise répétables
- Nul besoin d’expliquer Adobe à l’agent : la compétence s’en charge
- Fonctionne sur les plateformes d’IA qui prennent en charge les compétences des agents

[Explorer les compétences de l’agent](tools/agent-skills.md)

>[!TAB API pour Builders]

Accès direct et par programmation aux mêmes API que celles qui alimentent les produits Adobe. Créez des applications et des intégrations personnalisées qui donnent à votre équipe un accès ciblé et régi à des workflows CX Enterprise spécifiques.

- Créer une seule fois, déployer dans l’ensemble de l’organisation
- Ajoutez des mécanismes de sécurisation, des approbations et une logique personnalisée dont votre équipe a besoin
- Utilisez le code Claude, le curseur et d&#39;autres outils de codage pour créer plus rapidement

[Explorer les API pour Builders](tools/apis.md)

>[!ENDTABS]

## Outils agentiques en action

Découvrez à quoi ressemblent les outils agentiques de Adobe CX Enterprise dans la pratique. Chaque présentation couvre un scénario commercial réel, de la configuration au résultat, montrant exactement comment commencer à utiliser Coworker ou votre plateforme d’IA, ce qu’il faut demander et ce que vous obtenez en retour.

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="Informations sur la campagne sans rapports">
                        <img class="is-bordered-r-small" src="assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Informations sur la campagne sans rapports"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" title="Informations sur la campagne sans rapports">Informations de campagne sans rapports</a>
                    </p>
                    <p class="is-size-6">Posez des questions sur les performances en langage clair et obtenez des réponses de Customer Journey Analytics, sans créer de rapport unique.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Informations sur la campagne de surface</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="Expédition plus rapide des mises à jour de contenu">
                        <img class="is-bordered-r-small" src="assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Expédition plus rapide des mises à jour de contenu"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" title="Expédition plus rapide des mises à jour de contenu">Expédier les mises à jour de contenu plus rapidement</a>
                    </p>
                    <p class="is-size-6">Recherchez, mettez à jour et publiez plus rapidement des pages et des fragments de contenu AEM, sans passer par l’interface d’AEM.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Expédier le contenu plus rapidement</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

**[Voir toutes les procédures pas à pas](use-cases/overview.md)**

## Ressources Adobe

| Ressource | Ce que vous trouverez |
| --- | --- |
| [Registre Adobe AI](https://developer.adobe.com/ai-registry/?type=mcp) | Connecteurs gérés et détails du serveur pour certains serveurs MCP Adobe |
| [Compétences De L’Agent Adobe](https://github.com/adobe/skills) | Compétences en agent traitées par Adobe pour les workflows CX Enterprise |
| [Catalogue des API Adobe](https://developer.adobe.com/apis) | Référence complète de l’API Adobe CX Enterprise |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | Configuration et authentification du projet d’API |
| [Adobe Admin Console](https://adminconsole.adobe.com) | Gestion de l’accès aux utilisateurs et aux produits |
| [Experience League](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/home) | Documentation et tutoriels complets sur l’application Adobe |
