---
title: "Erstellen, entwickelt und versionsverwaltung Microservice APIs und Verträge"
description: ".NET Microservices Architektur für Datenvolumes .NET-Anwendungen | Erstellen, entwickelt und versionsverwaltung Microservice APIs und Verträge"
keywords: Docker, Microservices, ASP.NET, Container
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 433711c3479eafd52bf9f5d53faf8e5707c6c624
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2017
---
# <a name="creating-evolving-and-versioning-microservice-apis-and-contracts"></a><span data-ttu-id="1c997-104">Erstellen, entwickelt und versionsverwaltung Microservice APIs und Verträge</span><span class="sxs-lookup"><span data-stu-id="1c997-104">Creating, evolving, and versioning microservice APIs and contracts</span></span>

<span data-ttu-id="1c997-105">Ein Microservice-API ist ein Vertrag zwischen dem Dienst und seinen Clients.</span><span class="sxs-lookup"><span data-stu-id="1c997-105">A microservice API is a contract between the service and its clients.</span></span> <span data-ttu-id="1c997-106">Sie können werden ein Microservice eigenständig nur, wenn Sie keine API-Vertrag, beschädigen daher der Vertrag so wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="1c997-106">You will be able to evolve a microservice independently only if you do not break its API contract, which is why the contract is so important.</span></span> <span data-ttu-id="1c997-107">Wenn Sie den Vertrag ändern, wirkt sie Ihre Clientanwendungen angewendet oder Ihr API-Gateway.</span><span class="sxs-lookup"><span data-stu-id="1c997-107">If you change the contract, it will impact your client applications or your API Gateway.</span></span>

<span data-ttu-id="1c997-108">Die Art der API-Definition abhängig ist, auf welches Protokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c997-108">The nature of the API definition depends on which protocol you are using.</span></span> <span data-ttu-id="1c997-109">Für die Instanz, wenn Sie messaging verwenden (z. B. [AMQP](https://www.amqp.org/)), die API besteht aus den Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="1c997-109">For instance, if you are using messaging (like [AMQP](https://www.amqp.org/)), the API consists of the message types.</span></span> <span data-ttu-id="1c997-110">Wenn Sie HTTP und RESTful-Dienste verwenden, besteht die API die URLs und die Anforderung und Antwort JSON-Formate.</span><span class="sxs-lookup"><span data-stu-id="1c997-110">If you are using HTTP and RESTful services, the API consists of the URLs and the request and response JSON formats.</span></span>

<span data-ttu-id="1c997-111">Allerdings auch, wenn Sie Informationen zu den ersten Vertrag durchdachtes sind, müssen eine Dienst-API im Laufe der Zeit ändern.</span><span class="sxs-lookup"><span data-stu-id="1c997-111">However, even if you are thoughtful about your initial contract, a service API will need to change over time.</span></span> <span data-ttu-id="1c997-112">Wann dies geschieht – und insbesondere dann, wenn Ihre API eine öffentliche API von mehreren Clientanwendungen genutzt werden – Sie in der Regel können nicht erzwingen, dass alle Clients so aktualisieren Sie auf die neue API-Vertrags.</span><span class="sxs-lookup"><span data-stu-id="1c997-112">When that happens—and especially if your API is a public API consumed by multiple client applications—you typically cannot force all clients to upgrade to your new API contract.</span></span> <span data-ttu-id="1c997-113">Sie müssen in der Regel inkrementell auf neue Versionen eines Diensts auf eine Weise bereitstellen, die alte und neue Versionen eines Dienstvertrags gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1c997-113">You usually need to incrementally deploy new versions of a service in a way that both old and new versions of a service contract are running simultaneously.</span></span> <span data-ttu-id="1c997-114">Aus diesem Grund ist es wichtig, dass eine Strategie für die dienstversionsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="1c997-114">Therefore, it is important to have a strategy for your service versioning.</span></span>

<span data-ttu-id="1c997-115">Wenn die API-Änderungen "klein" sind, z. B., wenn Sie Attribute oder Parameter auf Ihre API hinzufügen, sollten Clients, bei denen eine ältere API wechseln und Arbeiten mit der neuen Version des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1c997-115">When the API changes are small, like if you add attributes or parameters to your API, clients that use an older API should switch and work with the new version of the service.</span></span> <span data-ttu-id="1c997-116">Möglicherweise Standardwerte für alle fehlenden Attribute bereitzustellen, die erforderlich sind, und die Clients können möglicherweise keine zusätzliche Antwort Attribute ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c997-116">You might be able to provide default values for any missing attributes that are required, and the clients might be able to ignore any extra response attributes.</span></span>

<span data-ttu-id="1c997-117">Allerdings müssen gelegentlich Sie Haupt- und nicht kompatible Änderungen an einer Dienst-API vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1c997-117">However, sometimes you need to make major and incompatible changes to a service API.</span></span> <span data-ttu-id="1c997-118">Da möglicherweise nicht zum Erzwingen von Clientanwendungen oder Diensten, sofort auf die neue Version aktualisiert werden können, muss ein Dienst ältere Versionen der API für einen gewissen Zeitraum unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1c997-118">Because you might not be able to force client applications or services to upgrade immediately to the new version, a service must support older versions of the API for some period.</span></span> <span data-ttu-id="1c997-119">Wenn Sie einen HTTP-basierte Mechanismus wie REST verwenden, ist ein Ansatz besteht darin, die API-Versionsnummer in der URL oder in einen HTTP-Header einzubetten.</span><span class="sxs-lookup"><span data-stu-id="1c997-119">If you are using an HTTP-based mechanism such as REST, one approach is to embed the API version number in the URL or into a HTTP header.</span></span> <span data-ttu-id="1c997-120">Sie können dann entscheiden, zwischen beide Versionen des Diensts gleichzeitig innerhalb der gleichen Dienstinstanz implementieren oder die Bereitstellung von anderen Instanzen, jeweils eine Version der API behandeln.</span><span class="sxs-lookup"><span data-stu-id="1c997-120">Then you can decide between implementing both versions of the service simultaneously within the same service instance, or deploying different instances that each handle a version of the API.</span></span> <span data-ttu-id="1c997-121">Ist ein guter Ansatz für diesen die [Vermittler Muster](https://en.wikipedia.org/wiki/Mediator_pattern) (z. B. [MediatR Bibliothek](https://github.com/jbogard/MediatR)), die andere Implementierung Versionen in unabhängigen Handler zu entkoppeln.</span><span class="sxs-lookup"><span data-stu-id="1c997-121">A good approach for this is the [Mediator pattern](https://en.wikipedia.org/wiki/Mediator_pattern) (for example, [MediatR library](https://github.com/jbogard/MediatR)) to decouple the different implementation versions into independent handlers.</span></span>

<span data-ttu-id="1c997-122">Abschließend, wenn Sie eine REST-Architektur verwenden [Hypermedia](https://www.infoq.com/articles/mark-baker-hypermedia) besteht die beste Lösung für die versionsverwaltung Ihrer Dienste und evolvable APIs ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1c997-122">Finally, if you are using a REST architecture, [Hypermedia](https://www.infoq.com/articles/mark-baker-hypermedia) is the best solution for versioning your services and allowing evolvable APIs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c997-123">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1c997-123">Additional resources</span></span>

-   <span data-ttu-id="1c997-124">**Scott Hanselman. ASP.NET Core RESTful-Web-API-versionsverwaltung lassen sich einfach**
    <http://www.hanselman.com/blog/ASPNETCoreRESTfulWebAPIVersioningMadeEasy.aspx></span><span class="sxs-lookup"><span data-stu-id="1c997-124">**Scott Hanselman. ASP.NET Core RESTful Web API versioning made easy**
<http://www.hanselman.com/blog/ASPNETCoreRESTfulWebAPIVersioningMadeEasy.aspx></span></span>

-   <span data-ttu-id="1c997-125">**Eine RESTful-Web-API-versionsverwaltung**
    [*https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api*](https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api)</span><span class="sxs-lookup"><span data-stu-id="1c997-125">**Versioning a RESTful web API**
[*https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api*](https://docs.microsoft.com/azure/architecture/best-practices/api-design#versioning-a-restful-web-api)</span></span>

-   <span data-ttu-id="1c997-126">**Roy Fielding. Versionsverwaltung, Hypermedia und REST**
    <https://www.infoq.com/articles/roy-fielding-on-versioning></span><span class="sxs-lookup"><span data-stu-id="1c997-126">**Roy Fielding. Versioning, Hypermedia, and REST**
<https://www.infoq.com/articles/roy-fielding-on-versioning></span></span>


>[!div class="step-by-step"]
<span data-ttu-id="1c997-127">[Vorherigen] (asynchrone-Nachricht-Basis-communication.md) [weiter] (Microservices-Adressierbarkeit-Service-registry.md)</span><span class="sxs-lookup"><span data-stu-id="1c997-127">[Previous] (asynchronous-message-based-communication.md) [Next] (microservices-addressability-service-registry.md)</span></span>