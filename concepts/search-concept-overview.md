---
title: "Search API overview (preview)"
description: "Learn about using the Microsoft Search API to index content and add search across your Office & indexed content into your apps."
localization_priority: Priority
ms.prod: "search"
author: "snlraju-msft"
scenarios: "getting-started"
---

# Overview for extending the Microsoft Search experience for apps on Microsoft Graph (preview)

Microsoft Search is an enterprise search engine that delivers productivity gains and relevant search results for your organization. It harnesses the collective knowledge and productivity of an organization, and surfaces relevant content to keep end users up to date. Microsoft Search is available in various experiences including Office, SharePoint, Delve, Windows, and Bing.

[!INCLUDE [search-api-preview-signup](../includes/search-api-preview-signup.md)]

<!-- markdownlint-disable MD026 -->
## Why use the Microsoft Search API?

### One unified search endpoint for Microsoft cloud data

The Microsoft Search API provides one unified search endpoint to let developers [query](/graph/api/search-query?view=graph-rest-beta) data in the Microsoft cloud - messages and events in Outlook mailboxes, and files on OneDrive and SharePoint - data that Microsoft Search already indexes.

### Include custom external data in search experience

Customers who want to include data outside of the Microsoft cloud in their search experience can use [connectors](/microsoftsearch/connectors-overview) to connect to a specific data source such as an organization's human resources database or product catalog, and use the Microsoft Search API to seamlessly [query](/graph/api/search-query?view=graph-rest-beta) the external data source. The [Microsoft Graph connectors gallery](/microsoftsearch/connectors-gallery) lists a number of ready-to-use connectors. Alternatively, customers can [build connectors](/graph/api/resources/indexing-api-overview?view=graph-rest-beta#common-use-cases), index external custom items and files, and query specific external data sources as well.

### Consistent, up-to-date search experience

Using the Microsoft Search API, customers benefit from getting more personalized relevant results powered by Microsoft Graph. This also makes search in your apps return results consistent with search in Office applications.

## What data can I add or access by using these APIs?

Microsoft Search supports searching content in the Microsoft cloud:

- Outlook [message](/graph/api/resources/message?view=graph-rest-beta) and [event](/graph/api/resources/event?view=graph-rest-beta) objects
- SharePoint and OneDrive [driveItem](/graph/api/resources/driveitem?view=graph-rest-beta) file objects

In addition, you can index and search external content:

- [externalItem](/graph/api/resources/externalitem?view=graph-rest-beta) objects which are of custom types
- [externalFile](/graph/api/resources/externalfile?view=graph-rest-beta) objects which are of well-known types

## API reference

Looking for the API reference for this service?

- [Use the Microsoft Search API to query data](/graph/api/resources/search-api-overview?view=graph-rest-beta)
- [Use the Microsoft Search API to index data](/graph/api/resources/indexing-api-overview?view=graph-rest-beta)

## Next steps

- Learn more about [Microsoft Search](/microsoftsearch/).
- Learn more about a few key use cases:
  - [Search Outlook messages](search-concept-messages.md)
  - [Search calendar events](search-concept-events.md)
  - [Manage connections to index external content](search-index-manage-connections.md)
  - [Index external content](search-index-manage-items.md)
  - [Search custom types (externalItem)](search-concept-custom-types.md)
  - [Search files (including externalFile)](search-concept-files.md)
- Explore the search APIs in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).
- Download the [sample search connector](https://github.com/microsoftgraph/msgraph-search-connector-sample) from GitHub.

## See also

Engage with the community:

- [Discuss on StackOverflow](https://stackoverflow.com/questions/tagged/microsoft-search)
