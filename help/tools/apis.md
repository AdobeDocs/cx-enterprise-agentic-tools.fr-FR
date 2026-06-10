---
title: API pour les créateurs
description: Créez des applications et des intégrations personnalisées à l’aide des API d’entreprise Adobe CX.
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: f7ace53bd5988b5902659c89c6da16448398e0c0
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 10%

---


# API pour les créateurs

<!-- last-modified: 2026-06-02 -->

![API Adobe CX Enterprise](../assets/hero-apis.png)

Les API d’entreprise Adobe CX donnent aux développeurs et aux outils de codage assistés par l’IA un accès direct aux données et aux workflows d’Adobe. Utilisez-les pour créer des applications personnalisées, automatiser les intégrations et incorporer les fonctionnalités d’Adobe dans vos propres systèmes. Les API sont le bon choix lorsque vous avez besoin d’un contrôle programmatique complet sur une intégration système ou que vous créez une application sur les données d’Adobe. Pour un accès conversationnel piloté par un agent aux workflows Adobe, reportez-vous à la section [Serveurs MCP](mcp-servers.md).

## API d’entreprise Adobe CX

>[!BEGINTABS]

>[!TAB Adobe Analytics]

Rapports, flux de données, mesures calculées et gestion des segments.

[Explorer l’API](https://developer.adobe.com/analytics-apis/docs/2.0/)

>[!TAB Adobe Commerce]

API REST et GraphQL pour le catalogue, le panier, les commandes, les clients et les promotions.

[Explorer l’API](https://developer.adobe.com/commerce/webapi/)

>[!TAB Adobe Experience Platform]

Opérations CRUD pour les jeux de données, les schémas, les profils, les identités, les requêtes et la segmentation.

[Explorer l’API](https://developer.adobe.com/experience-platform-apis/)

>[!TAB Adobe Journey Optimizer]

orchestration des parcours, gestion des campagnes, modèles de contenu et Offer Decisioning.

[Explorer l’API](https://developer.adobe.com/journey-optimizer-apis/)

>[!TAB AEM as a Cloud Service]

API de gestion de contenu, de ressources et de workflows pour Adobe Experience Manager.

[Explorer l’API](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions)

>[!TAB Audience Manager]

Workflows d’activation et de gestion des audiences.

[Explorer l’API](https://developer.adobe.com/audience-manager/)

>[!TAB SDK client]

SDK mobiles, SDK Edge et messagerie in-app.

[Explorer l’API](https://developer.adobe.com/client-sdks/home/)

>[!TAB Customer Journey Analytics]

Workflows d’accès aux données, de création de rapports et d’informations CJA.

[Explorer l’API](https://developer.adobe.com/cja-apis/docs/)

>[!TAB Collecte de données]

Ingestion des données Edge Network, collecte d’événements en temps réel et diffusion de données en continu.

[Explorer l’API](https://developer.adobe.com/data-collection-apis/docs/)

>[!TAB Tab]

Configuration du projet API, authentification et gestion des informations d’identification.

[Explorer l’API](https://developer.adobe.com/developer-console/docs/guides/)

>[!TAB Événements]

Intégrations basées sur des événements, webhooks et triggers d’automatisation.

[Explorer l’API](https://developer.adobe.com/events/docs/)

>[!TAB Confidentialité]

Workflows de confidentialité, gouvernance des données et requêtes des titulaires de données.

[Explorer l’API](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/home)

>[!TAB Gestion des utilisateurs]

Gestion des utilisateurs, administration des identités et automatisation des comptes d’entreprise.

[Explorer l’API](https://developer.adobe.com/umapi/)

>[!ENDTABS]

## Créer avec des API

![Un IDE se connectant aux API d’entreprise Adobe CX](../assets/hero-connect-apis.gif)

Les agents de codage tels que Claude Code, Cursor et OpenAI Codex sont adaptés à la création avec les API d’entreprise Adobe CX. Ajoutez une spécification OpenAPI à votre projet pour que l’agent puisse découvrir les points d’entrée, créer des requêtes et donner une raison sur le comportement de l’API sans câblage manuel. Pour commencer, deux éléments sont nécessaires : les informations d’identification authentifiées de Adobe Developer Console et l’ajout de la documentation de l’API à votre projet.

### Configuration des informations d’identification d’API dans Adobe Developer Console

Tout accès à l’API d’entreprise Adobe CX est géré via [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/). Créez un projet, ajoutez les API dont votre application a besoin et générez des informations d’identification.

1. Connectez-vous et [créez un projet](https://developer.adobe.com/developer-console/docs/guides/projects/) dans Adobe Developer Console.
2. [Ajoutez l’API](https://developer.adobe.com/developer-console/docs/guides/services/) pour l’application Adobe CX Enterprise dont vous avez besoin.
3. Choisissez un [type d’authentification](https://developer.adobe.com/developer-console/docs/guides/authentication/). Utilisez **OAuth de serveur à serveur** pour les workflows automatisés ou **OAuth Web App** pour les applications orientées utilisateur.
4. Générez vos informations d’identification. Notez l’ID client, le secret client et le point d’entrée du jeton à utiliser dans votre application.

La plupart des API d’entreprise Adobe CX nécessitent une licence d’application. Si une API n’est pas disponible dans votre projet Developer Console, contactez votre représentant Adobe.

### Ajouter le contexte de l’API Adobe à votre projet

Les agents de codage de l’IA peuvent découvrir et utiliser de manière fiable les API Adobe lorsque vous ajoutez le matériel de référence approprié à votre projet. Cela fonctionne pour toute API d’entreprise Adobe CX qui publie une spécification OpenAPI.

**1. Recherchez la spécification d’API**

Parcourez les [API Adobe CX Enterprise](#adobe-cx-enterprise-apis) répertoriées ci-dessus ou accédez directement au [catalogue d’API Adobe Developer](https://developer.adobe.com/apis).

**2. Téléchargez la spécification OpenAPI**

Créez un répertoire `/specs` dans votre projet. Téléchargez le YAML OpenAPI à partir de la page des références d’API sur [developer.adobe.com](https://developer.adobe.com/apis) et enregistrez-le. Ajoutez un `README.md` qui enregistre l’URL source et la date de téléchargement.

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>Un instantané archivé donne à votre agent de codage un comportement stable et reproductible et rend les modifications d’API visibles dans votre historique Git.

**3. Générez un index API**

Collez cette invite dans votre agent de codage, en remplaçant `<API-SPEC-FILE>` par votre nom de fichier :

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. Générez les instructions de l’agent**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. Vérifier**

Demandez à votre agent de codage d’effectuer une tâche simple en utilisant uniquement les fichiers générés :

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

Si l’agent l’effectue correctement sans inventer de comportement, la configuration est terminée.

**Structure de projet recommandée**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**Actualisation des spécifications**

Lorsqu’Adobe publie une nouvelle version d’API : téléchargez un nouvel instantané dans `/specs`, mettez à jour la date dans `README.md`, puis régénérez l’index et le `AGENTS.md`.

## Les API en action

Les API offrent aux équipes de développement un contrôle programmatique complet pour créer des applications ciblées qui automatisent des workflows CX Enterprise spécifiques. Ces procédures pas à pas présentent des intégrations réelles créées de bout en bout, de la configuration des informations d’identification au code de travail que votre entreprise peut envoyer.

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="Appeler des API AEM à partir d’une application web" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="Appeler des API AEM à partir d’une application web"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="Appeler des API AEM à partir d’une application web">Appeler des API AEM à partir d’une application web</a>
                    </p>
                    <p class="is-size-6">Créez une application web qui authentifie les utilisateurs et appelle les OpenAPI d’AEM à l’aide d’OAuth pour fournir un accès gouverné et programmatique.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Essayer avec les API</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
