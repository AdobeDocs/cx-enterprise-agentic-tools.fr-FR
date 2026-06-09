---
title: Serveurs MCP
description: Connectez n’importe quel client d’IA compatible MCP aux workflows Adobe CX Enterprise à l’aide de serveurs Model Context Protocol.
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: e37222abaf2d2502dfbc2f8588ae9ece94fffbd1
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 3%

---


# Serveurs MCP

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491324/?captions=fre_fr&learn=on&enablevpops)

Les serveurs Adobe CX Enterprise MCP donnent à tout client d’IA compatible un accès direct et régi aux données et aux workflows Adobe. Connectez-vous une seule fois et vous pourrez interroger les performances de la campagne, activer les audiences, passer en revue les parcours, gérer le contenu, etc., le tout en langage clair, sans quitter votre environnement d’IA. Les serveurs MCP se trouvant entre votre client d’IA et les systèmes sous-jacents d’Adobe, vous bénéficiez d’une flexibilité en langage naturel tandis que les contrôles d’accès et la gouvernance des données de votre entreprise restent en vigueur.

Les serveurs Adobe MCP respectent la norme ouverte [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro). Tout client d’IA compatible avec MCP se connecte à tout serveur MCP Adobe.

## Serveurs MCP d’entreprise CX

![Le CX Enterprise MCP connecte votre client IA aux outils de la suite Adobe CX Enterprise complète](../assets/mcp-gateway-hero.gif)

Sélectionnez une application pour afficher le point d’entrée et les fonctionnalités.

>[!BEGINTABS]

>[!TAB CX Enterprise MCP]

**Un point d’entrée. Plusieurs applications d’entreprise CX.**

Connectez-vous une fois et votre client AI aura accès aux applications CX Enterprise en fonction des licences de votre entreprise. Pour permettre à votre organisation de demander l’accès, envoyez un e-mail à [&#128279;](mailto:cxo-mcp-feedback@adobe.com).

```
https://cx-enterprise.adobe.io/mcp
```

| Application CX Enterprise | Ce que vous pouvez faire |
| --- | --- |
| Adobe Analytics | Découverte de suites de rapports, création de segments et création d’espaces de travail |
| Adobe Experience Platform | Découverte de jeux de données, navigation dans les schémas et gestion des sandbox |
| Adobe Journey Optimizer | Examiner les configurations des parcours, des campagnes et des canaux |
| Adobe Journey Optimizer B2B edition | Gérez les parcours B2B, les programmes de compte, les groupes d’achats et la personnalisation |
| Customer Journey Analytics | Requête sur les rapports, découverte des vues de données et création d’espaces de travail |
| Real-Time CDP | Vérifiez le statut d’activation de l’audience, l’intégrité de la destination et celle du flux de données |

>[!NOTE]
>
>L’accès à chaque application CX Enterprise dépend des droits de votre entreprise et des autorisations de votre utilisateur dans Adobe Admin Console. Pour activer CX Enterprise MCP pour votre organisation, envoyez un e-mail à [&#128279;](mailto:cxo-mcp-feedback@adobe.com).

>[!TAB Experience Manager]

Adobe Experience Manager dispose de plusieurs serveurs MCP pour différents workflows.

| Serveur MCP | Point d’entrée | Ce que vous pouvez faire |
| --- | --- | --- |
| [AEM (Mode Code)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Accès direct de l’API REST à AEM par le biais de la recherche, de la lecture, de l’écriture et de la suppression en langage naturel |
| [&#128279;](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Gestion des programmes, environnements, pipelines et référentiels |
| [Contenu &#x200B;](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Gestion des pages, des fragments de contenu, des ressources et des lancements |
| [Contenu AEM (Lecture Seule)](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Découvrir et interroger des pages, des fragments de contenu et des lancements sans accès en écriture |
| Création de documents AEM | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | Gestion des fichiers, de l’historique des versions et des références de média dans la création de documents |
| [Gouvernance de l’expérience &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Évaluer le contenu et les images par rapport aux directives et aux règles de conformité de la marque |
| [AEM Experience Production](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | Transformer et créer des pages AEM à grande échelle à l’aide de résumés de contenu pilotés par l’IA |

>[!NOTE]
>
>L’accès à chaque environnement AEM dépend des droits d’accès à AEM Cloud Service de votre entreprise et des autorisations de votre utilisateur dans cet environnement.

>[!TAB Experience Platform]

| Serveur MCP | Point d’entrée | Ce que vous pouvez faire |
| --- | --- | --- |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | Orchestrer l’analyse des audiences, les diagnostics AEP et la création de parcours B2B AJO dans les applications AEP |

>[!NOTE]
>
>L’accès dépend des droits Adobe Experience Platform de votre organisation et des autorisations de votre utilisateur.

>[!TAB Tab]

| Serveur MCP | Point d’entrée | Ce que vous pouvez faire |
| --- | --- | --- |
| [&#128279;](https://experienceleague.adobe.com/fr/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Gestion des programmes, des campagnes, des prospects, des listes dynamiques, des e-mails et des formulaires |

>[!NOTE]
>
>Marketo Engage MCP utilise les informations d’identification de service natives Marketo, et non Adobe IMS. Pour la configuration de l’authentification, consultez la documentation du serveur MCP Marketo Engage [&#128279;](https://experienceleague.adobe.com/fr/docs/marketo-developer/marketo/mcp-server). L’accès dépend de votre abonnement Marketo Engage et des autorisations de l’utilisateur de votre API.

>[!TAB Target]

Adobe Target MCP est en version bêta publique. Tous les outils actuellement disponibles sont en lecture seule. Les outils d’écriture sont prévus pour une disponibilité générale.

| Serveur MCP | Point d’entrée | Ce que vous pouvez faire |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/fr/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Examinez les activités, les offres, les audiences, les mbox et les rapports de performances |

>[!NOTE]
>
>L’accès dépend de vos droits Adobe Target et des autorisations de votre utilisateur.

>[!TAB Workfront]

| Serveur MCP | Point d’entrée | Ce que vous pouvez faire |
| --- | --- | --- |
| Adobe Workfront | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Gérer le travail, les projets, les enregistrements de planification, les informations et les approbations de contenu |

>[!NOTE]
>
>L’accès dépend de vos licences Adobe Workfront et des autorisations de votre utilisateur.

>[!ENDTABS]

## Connexion à votre client d’IA

Tous les serveurs Adobe MCP utilisent OAuth avec Adobe Identity Management Service (IMS). Sélectionnez l’organisation IMS appropriée lorsque vous y êtes invité. Le choix d’une mauvaise option est la source la plus courante d’erreurs d’authentification.

Avant de procéder à la configuration manuelle, vérifiez le registre Adobe AI [&#128279;](https://developer.adobe.com/ai-registry/?type=connector) pour trouver un connecteur géré pour votre client IA et votre application Adobe. Les connecteurs gérés gèrent automatiquement l’authentification. Si un connecteur est disponible pour votre client et votre application, utilisez-le au lieu des étapes manuelles ci-dessous.

Les étapes ci-dessous utilisent le point d’entrée CX Enterprise MCP comme exemple. Le même processus s’applique à tout serveur Adobe MCP : remplacez l’URL du point d’entrée par celle du serveur auquel vous souhaitez vous connecter.

![Un agent d’IA se connectant à un serveur MCP Adobe](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB Claude.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Recommandé"> Utiliser un connecteur géré

Accédez au registre Adobe AI [&#128279;](https://developer.adobe.com/ai-registry/?type=connector) et recherchez votre application Adobe. Si un connecteur Claude est répertorié (par exemple, le connecteur [&#128279;](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), suivez ses instructions de configuration au lieu des étapes ci-dessous.

### Se connecter à l’aide d’un connecteur personnalisé

Claude.ai prend en charge les serveurs MCP distants via des connecteurs personnalisés dans les paramètres du compte.

1. Accédez à **Paramètres > Intégrations**.
2. Cliquez sur **Ajouter un connecteur personnalisé**.
3. Saisissez le point d’entrée du serveur sous la forme d’une URL (par exemple, `https://cx-enterprise.adobe.io/mcp` pour CX Enterprise MCP) et d’un nom d’affichage de votre choix.
4. Cliquez sur **Connexion** et connectez-vous avec votre Adobe ID. Sélectionnez l’organisation IMS appropriée.

Configuration complète : [documentation des connecteurs personnalisés Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Code Claude]

### Utilisation de l’interface de ligne de commande

Exécutez `claude mcp add` pour enregistrer un serveur Adobe MCP. Remplacez le nom et l’URL du serveur par les valeurs du serveur auquel vous souhaitez vous connecter. Cet exemple utilise le MCP CX Enterprise :

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Modifier votre fichier de paramètres

Ajoutez le serveur à `~/.claude.json` (global) ou `.mcp.json` dans la racine du projet (au niveau du projet). Remplacez la clé et l’URL par les valeurs du serveur auquel vous souhaitez vous connecter :

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Les serveurs Adobe MCP utilisent OAuth. Claude Code vous invite à vous authentifier auprès de votre Adobe ID la première fois que vous appelez un outil. Sélectionnez l’organisation IMS appropriée lorsque vous y êtes invité.

Configuration complète : [documentation Claude Code MCP](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Curseur]

Ajoutez un serveur MCP Adobe à votre fichier de configuration `mcp.json` Cursor, puis connectez-vous via **Paramètres > MCP**. Remplacez la clé et l’URL par les valeurs du serveur auquel vous souhaitez vous connecter. Cet exemple utilise le MCP CX Enterprise :

- **Global (tous les projets) :** `~/.cursor/mcp.json`
- **Project-level:** `.cursor/mcp.json` dans la racine du projet

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Une fois ajoutés, les serveurs MCP apparaissent sous **Serveurs MCP installés** dans les paramètres du curseur. Sélectionnez **Se connecter** en regard de tout serveur affichant **Nécessite une authentification** et connectez-vous avec votre Adobe ID. Sélectionnez l’organisation IMS ayant accès à l’application.

![Configuration du serveur MCP de curseur affichant les serveurs MCP Adobe installés et le fichier mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configuration complète : [documentation Cursor MCP](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Recommandé"> Utiliser un connecteur géré

Accédez au registre Adobe AI [&#128279;](https://developer.adobe.com/ai-registry/?type=connector) et recherchez votre application Adobe. Si un connecteur ChatGPT est répertorié, suivez ses instructions de configuration au lieu des étapes ci-dessous.

### Se connecter à l’aide d’un serveur MCP distant

ChatGPT prend en charge les serveurs MCP distants via [mode Développeur](https://developers.openai.com/api/docs/guides/developer-mode), disponible sur les plans Pro, Plus, Business, Enterprise et Education.

1. Activez le mode Développeur dans **Paramètres ChatGPT**.
2. Accédez à **Paramètres > Intégrations**.
3. Cliquez sur **Ajouter un connecteur personnalisé** et choisissez **Serveur MCP distant**.
4. Saisissez le point d’entrée du serveur sous la forme d’une URL (par exemple, `https://cx-enterprise.adobe.io/mcp` pour CX Enterprise MCP) et d’un nom d’affichage de votre choix.
5. Définissez l’authentification sur **OAuth**.
6. Cliquez sur **Connexion** et connectez-vous avec votre Adobe ID. Sélectionnez l’organisation IMS appropriée.

Configuration complète : [documentation MCP ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI Codex CLI]

L’interface de ligne de commande OpenAI Codex prend en charge les serveurs MCP distants via la configuration TOML.

**Emplacements des fichiers de configuration :**

- **Niveau utilisateur (tous les projets) :** `~/.codex/config.toml`
- **Portée du projet :** `.codex/config.toml` dans la racine du projet

Remplacez le nom de section et l’URL par les valeurs du serveur auquel vous souhaitez vous connecter. Cet exemple utilise le MCP CX Enterprise :

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Les serveurs Adobe MCP utilisent OAuth. L’interface de ligne de commande du Codex gère automatiquement le flux OAuth lors de la première utilisation. Sélectionnez l’organisation IMS appropriée lorsque vous y êtes invité.

Configuration complète : [documentation MCP de l’interface de ligne de commande OpenAI Codex](https://developers.openai.com/codex/mcp)

>[!TAB  Copilot Studio ]

Microsoft Copilot Studio se connecte aux serveurs MCP distants à l&#39;aide de l&#39;Assistant Intégration MCP, qui crée automatiquement un connecteur personnalisé Power Platform.

1. Ouvrez votre agent dans Copilot Studio.
2. Accédez à la page **Outils**.
3. Sélectionnez **Ajouter un outil > Nouvel outil > Protocole de contexte de modèle**.
4. Dans l’Assistant d’intégration MCP, entrez les détails du serveur, par exemple, pour le MCP CX Enterprise :
   - **Nom du serveur :** `Adobe CX Enterprise`
   - **URL du serveur :** `https://cx-enterprise.adobe.io/mcp`
5. Définissez l’authentification sur **OAuth 2.0** et configurez-la avec vos URL d’autorisation et de jeton Adobe IMS.
6. Sélectionnez **Créer**, puis **Ajouter à l’agent**.

>[!NOTE]
>
>Les connexions au serveur MCP dans Copilot Studio passent par Power Platform. Les politiques de prévention des pertes de données (DLP) de votre entreprise s’appliquent.

Configuration complète : [documentation Copilot Studio MCP](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Outils agentiques en action

Reportez-vous à la section Serveurs MCP d’entreprise Adobe CX appliqués à de réels workflows métier.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Analyse des performances des campagnes" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Analyse des performances des campagnes"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analyse des performances des campagnes">Analyse des performances des campagnes</a>
                    </p>
                    <p class="is-size-6">Utilisez CX Enterprise MCP pour afficher les mesures et les informations Customer Journey Analytics de n’importe quel client IA.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Démarrer la présentation</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Requête sur les audiences" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Requête sur les audiences"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" title="Requête sur les audiences">Requête d’audiences</a>
                    </p>
                    <p class="is-size-6">Utilisez CX Enterprise MCP pour interroger les données d’audience et de destination Real-Time CDP à l’aide d’invites en langage clair.</p>
                </div>
                <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Démarrer la présentation</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Vérifier les parcours AJO" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Vérifier les parcours AJO"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="Vérifier les parcours AJO">Vérification des parcours AJO</a>
                    </p>
                    <p class="is-size-6">Utilisez CX Enterprise MCP pour accéder aux parcours AJO, au statut de la campagne et aux conditions de parcours de votre client IA.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Démarrer la présentation</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Gestion du contenu AEM avec l’IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Gestion du contenu AEM avec l’IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="Gestion du contenu AEM avec l’IA">Gérer le contenu AEM avec l’IA</a>
                    </p>
                    <p class="is-size-6">Découvrez, mettez à jour et publiez des pages et des fragments de contenu dans AEM en utilisant le langage naturel.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Démarrer la présentation</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Optimiser le contenu en fonction des données de performance" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Optimiser le contenu en fonction des données de performance"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Optimiser le contenu en fonction des données de performance">Optimiser le contenu en fonction des données de performances</a>
                    </p>
                    <p class="is-size-6">Combinez CX Enterprise MCP et AEM Content MCP Server pour identifier les contenus peu performants et les mettre à jour en une seule session.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Démarrer la présentation</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Besoin d&#39;aide supplémentaire ?

Les connexions MCP impliquent l’authentification, la sélection de l’organisation et les autorisations au niveau de l’application. Si quelque chose ne fonctionne pas comme prévu, ces étapes couvrent les causes les plus courantes.

+++Changement d’organisation dans Adobe

Si votre utilisateur Adobe appartient à plusieurs organisations IMS et que vous ne voyez pas les outils ou les données pour le bon, déconnectez le serveur MCP, déconnectez-vous de votre session Adobe dans le navigateur, puis reconnectez-vous. Vous serez invité à choisir une organisation lors de la connexion.

Un serveur Adobe CX Enterprise MCP ne peut être authentifié que sur une seule organisation IMS à la fois, même si votre compte utilisateur y a accès.

+++

+++Spécification d’un sandbox, d’une suite de rapports, d’un environnement ou d’une autre ressource de session

Certains serveurs Adobe CX Enterprise MCP nécessitent que vous spécifiiez une ressource avant de pouvoir renvoyer des résultats. Selon l’application, il peut s’agir d’un sandbox, d’un programme, d’un environnement, d’une suite de rapports ou d’une vue de données.

Si vous ne savez pas à quelles ressources vous avez accès, demandez au client d’IA. Par exemple : « Répertorier les sandbox disponibles » ou « À quelles suites de rapports ai-je accès ? » Les serveurs Adobe CX Enterprise MCP peuvent souvent renvoyer une liste complète des ressources disponibles pour votre utilisateur.

Une fois qu’une ressource de session est définie, vous pouvez la changer à tout moment en indiquant au client d’IA laquelle utiliser.

+++

+++Autorisations et erreurs d’accès

Les clients d’IA agissent au nom de votre compte utilisateur Adobe à l’aide d’OAuth. Les mêmes autorisations et contrôles d’accès que ceux qui s’appliquent lorsque vous vous connectez à une application Adobe s’appliquent lorsque vous utilisez un serveur MCP.

Si une action échoue ou ne renvoie aucun résultat, vérifiez que votre utilisateur dispose des autorisations requises dans Adobe Admin Console et dans l’application CX Enterprise appropriée. Contactez votre administrateur système Adobe si vous avez besoin d’ajuster l’accès.

+++

+++Réauthentification après une session perdue

Les serveurs Adobe CX Enterprise MCP utilisent OAuth pour authentifier votre compte utilisateur Adobe. Si l’état d’authentification est perdu, aucun autre appel d’outil ne réussira jusqu’à ce que vous vous authentifiiez à nouveau.

Pour vous réauthentifier : ouvrez la configuration du serveur MCP de votre client d’IA, sélectionnez l’entrée de serveur MCP Entreprise Adobe CX et reconnectez-vous. Vous serez invité à vous reconnecter à votre Adobe ID.

+++
