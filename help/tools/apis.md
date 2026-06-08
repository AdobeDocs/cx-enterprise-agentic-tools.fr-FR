---
title: API pour les créateurs
description: Créez des applications et des intégrations personnalisées à l’aide des API d’entreprise Adobe CX.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 4%

---


# API pour les créateurs

<!-- last-modified: 2026-06-02 -->

![API Adobe CX Enterprise](../assets/hero-apis.png)

Les API d’entreprise Adobe CX donnent aux développeurs et aux outils de codage assistés par l’IA un accès direct aux données et aux workflows d’Adobe. Utilisez-les pour créer des applications personnalisées, automatiser les intégrations et incorporer les fonctionnalités d’Adobe dans vos propres systèmes. Les API sont le bon choix lorsque vous avez besoin d’un contrôle programmatique complet sur une intégration système ou que vous créez une application sur les données d’Adobe. Pour un accès conversationnel piloté par un agent aux workflows Adobe, reportez-vous à la section [Serveurs MCP](mcp-servers.md).

## API d’entreprise Adobe CX

Les API d’entreprise Adobe CX exposent les données et opérations de base qui alimentent des produits tels que Adobe Experience Platform, Journey Optimizer et Customer Journey Analytics. Chaque API suit une conception API-first, donnant aux développeurs et aux outils d’agence de codage assistés par l’IA un accès direct et programmable aux mêmes fonctionnalités qu’Adobe utilise en interne. Utilisez-les pour créer des applications personnalisées, automatiser les workflows et intégrer les données Adobe dans vos propres systèmes.

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->

## API pour Builders et serveurs MCP

Utilisez les API lorsque vous avez besoin d’un contrôle total de l’intégration du système ou que vous créez une application personnalisée. Utilisez les serveurs MCP lorsque vous souhaitez qu’un agent d’IA travaille directement avec les workflows Adobe.

| | API | Serveurs MCP |
| --- | --- | --- |
| Intégration directe du système | Oui | Parfois |
| Orchestration conviviale pour les agents | Limité | Oui |
| Accès aux données brutes | Oui | Généralement abstrait |
| Développement d’applications personnalisées | Cas d’utilisation du Principal | Secondaire |
| Workflows assistés par l’IA | Pris en charge | Cas d’utilisation du Principal |

## Prise en main des API pour Builders

![Un IDE se connectant aux API d’entreprise Adobe CX](../assets/hero-connect-apis.gif)

Avant de pouvoir créer des API d’entreprise Adobe CX, deux éléments sont nécessaires : des informations d’identification authentifiées de Adobe Developer Console et l’ajout d’une documentation d’API à votre projet afin que votre agent de codage puisse travailler avec les API d’Adobe de manière fiable.

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
