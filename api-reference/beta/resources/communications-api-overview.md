---
title: "Working with the communications API in Microsoft Graph"
description: "The Microsoft Graph communications API adds a new dimension to how your apps and services can interact with users by enabling voice and video features."
author: "VinodRavichandran"
doc_type: conceptualPageType
ms.prod: cloud-communications
localization_priority: Priority
---

# Working with the communications API in Microsoft Graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The Microsoft Graph communications API adds a new dimension to how you or your organization can interact with other users by enabling core communication capabilities and features in your apps and services. You can use this API to create and receive calls, create and retrieve meeting coordinates, and check users' presence.

You can use the communications API to build service applications (bots) that act like participants in a call, and that create and retrieve meetings on behalf of users and to check their presence availability and activity.
This API provides calling functionality as well as the ability to create and retrieve online meetings. You can use service applications (bots) with this API, where the bot can act as a participant in your VoIP calls or Microsoft Teams meetings, for example.

## Authorization

One of the following [permissions](https://docs.microsoft.com/graph/permissions-reference#calls-permissions) is required to access the communications API. These permissions need to be granted by the administrator

| Scenario                 | Permissions                                  |
|:------------------------------------|:---------------------------------------------|
| Calling                 | Calls.JoinGroupCallsasGuest.All, Calls.JoinGroupCalls.All, Calls.Initiate.All, Calls.InitiateGroupCalls.All, Calls.AccessMedia.All |
| Meetings                 | OnlineMeetings.ReadWrite.All, OnlineMeetings.Read.All |
| Presence                 | Presence.Read, Presence.Read.All |

## Common use cases

The following table lists some of the common uses for the communications API.

| Use cases                         | REST resources                                 | See also  |
|:------------------------------------|:---------------------------------------------|:----------|
| Creating and joining 1-1 and group calls   | [Call](https://docs.microsoft.com/graph/api/resources/call?view=graph-rest-beta)| [Methods for calls](https://docs.microsoft.com/graph/api/resources/call?view=graph-rest-beta#methods)| 
|IVR calls   |     | [Methods for IVR](https://docs.microsoft.com/graph/api/resources/calls-api-ivr-overview?view=graph-rest-beta)
| Call controls (participant) | [Participant](https://docs.microsoft.com/graph/api/resources/participant?view=graph-rest-beta)   ||
|Meetings|[onlineMeeting](https://docs.microsoft.com/graph/api/resources/onlinemeeting?view=graph-rest-beta)| [Methods for meetings](https://docs.microsoft.com/graph/api/resources/onlinemeeting?view=graph-rest-beta#methods)|
|Presence | [presence](/graph/api/resources/presence) | [Methods for presence](/graph/api/resources/presence#methods) |

## Common properties

| Resource                | Properties                             |
|:------------------------------------|:---------------------------------------------|
| call                               | [call properties](https://docs.microsoft.com/graph/api/resources/call?view=graph-rest-beta#properties)  |
| participant                         | [participant properties](https://docs.microsoft.com/graph/api/resources/participant?view=graph-rest-beta#properties) |
| onlineMeeting                            | [onlineMeeting properties](https://docs.microsoft.com/graph/api/resources/onlinemeeting?view=graph-rest-beta#properties)                     |
| presence | [presence properties](/graph/api/resources/presence#properties) |

## See also

- [Communications API samples](https://github.com/microsoftgraph/microsoft-graph-comms-samples/)
- [Communication Signaling SDK](https://www.nuget.org/packages/Microsoft.Graph.Communications.Calls/1.0.0-prerelease.494)
- [Communication Media SDK](https://www.nuget.org/packages/Microsoft.Graph.Communications.Calls.Media/1.0.0-prerelease.494)
