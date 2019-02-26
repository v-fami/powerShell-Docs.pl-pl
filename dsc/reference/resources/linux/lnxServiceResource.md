---
ms.date: 06/12/2017
keywords: DSC, powershell, konfiguracja, ustawienia
title: DSC dla systemu Linux zasób nxService
ms.openlocfilehash: fe8043995205649378725f2ab0a78e19313739c9
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "55684248"
---
# <a name="dsc-for-linux-nxservice-resource"></a><span data-ttu-id="d2949-103">DSC dla systemu Linux zasób nxService</span><span class="sxs-lookup"><span data-stu-id="d2949-103">DSC for Linux nxService Resource</span></span>

<span data-ttu-id="d2949-104">**NxService** zasobów w programie PowerShell Desired State Configuration (DSC) udostępnia mechanizm do zarządzania usługami w węźle systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="d2949-104">The **nxService** resource in PowerShell Desired State Configuration (DSC) provides a mechanism to manage services on a Linux node.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2949-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="d2949-105">Syntax</span></span>

```
nxService <string> #ResourceName
{
    Name = <string>
    [ Controller = <string> { init | upstart | systemd } ]
    [ Enabled = <bool> ]
    [ State = <string> { Running | Stopped } ]
    [ DependsOn = <string[]> ]
}
```

## <a name="properties"></a><span data-ttu-id="d2949-106">Właściwości</span><span class="sxs-lookup"><span data-stu-id="d2949-106">Properties</span></span>

| <span data-ttu-id="d2949-107">Właściwość</span><span class="sxs-lookup"><span data-stu-id="d2949-107">Property</span></span> | <span data-ttu-id="d2949-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d2949-108">Description</span></span> |
|---|---|
| <span data-ttu-id="d2949-109">Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2949-109">Name</span></span>| <span data-ttu-id="d2949-110">Nazwa usługi/demona do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="d2949-110">The name of the service/daemon to configure.</span></span>|
| <span data-ttu-id="d2949-111">Kontroler</span><span class="sxs-lookup"><span data-stu-id="d2949-111">Controller</span></span>| <span data-ttu-id="d2949-112">Typ kontrolera usługi do użycia podczas konfigurowania usługi.</span><span class="sxs-lookup"><span data-stu-id="d2949-112">The type of service controller to use when configuring the service.</span></span>|
| <span data-ttu-id="d2949-113">Enabled</span><span class="sxs-lookup"><span data-stu-id="d2949-113">Enabled</span></span>| <span data-ttu-id="d2949-114">Wskazuje, czy usługa jest uruchamiana podczas rozruchu.</span><span class="sxs-lookup"><span data-stu-id="d2949-114">Indicates whether the service starts on boot.</span></span>|
| <span data-ttu-id="d2949-115">Stan</span><span class="sxs-lookup"><span data-stu-id="d2949-115">State</span></span>| <span data-ttu-id="d2949-116">Wskazuje, czy usługa jest uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="d2949-116">Indicates whether the service is running.</span></span> <span data-ttu-id="d2949-117">Ustaw wartość "Stopped", aby upewnić się, że usługa nie jest uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="d2949-117">Set this property to "Stopped" to ensure that the service is not running.</span></span> <span data-ttu-id="d2949-118">Ustaw ją na "Uruchomiona", aby upewnić się, że usługa nie jest uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="d2949-118">Set it to "Running" to ensure that the service is not running.</span></span>|
| <span data-ttu-id="d2949-119">DependsOn</span><span class="sxs-lookup"><span data-stu-id="d2949-119">DependsOn</span></span> | <span data-ttu-id="d2949-120">Wskazuje, że konfiguracji inny zasób, należy uruchomić przed ten zasób jest skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="d2949-120">Indicates that the configuration of another resource must run before this resource is configured.</span></span> <span data-ttu-id="d2949-121">Na przykład jeśli **identyfikator** zasobu jest najpierw blok skryptu konfiguracji, który chcesz uruchomić **ResourceName** a jej typ jest **ResourceType**, składnia za pomocą tego Właściwość jest `DependsOn = "[ResourceType]ResourceName"`.</span><span class="sxs-lookup"><span data-stu-id="d2949-121">For example, if the **ID** of the resource configuration script block that you want to run first is **ResourceName** and its type is **ResourceType**, the syntax for using this property is `DependsOn = "[ResourceType]ResourceName"`.</span></span>|

## <a name="additional-information"></a><span data-ttu-id="d2949-122">Dodatkowe informacje</span><span class="sxs-lookup"><span data-stu-id="d2949-122">Additional Information</span></span>

<span data-ttu-id="d2949-123">**NxService** zasobu nie utworzy definicji usługi lub skryptu dla usługi, gdy nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="d2949-123">The **nxService** resource will not create a service definition or script for the service if it does not exist.</span></span> <span data-ttu-id="d2949-124">Możesz użyć programu PowerShell Desired State Configuration **nxFile** zasobów zasobów do zarządzania istnienie lub zawartości pliku definicji usługi lub skryptu.</span><span class="sxs-lookup"><span data-stu-id="d2949-124">You can use the PowerShell Desired State Configuration **nxFile** Resource resource to manage the existence or contents of the service definition file or script.</span></span>

## <a name="example"></a><span data-ttu-id="d2949-125">Przykład</span><span class="sxs-lookup"><span data-stu-id="d2949-125">Example</span></span>

<span data-ttu-id="d2949-126">W poniższym przykładzie pokazano konfigurację usługi "host z wieloma adresami" (w przypadku Apache HTTP Server), zarejestrowane w usłudze **SystemD** kontrolera usług.</span><span class="sxs-lookup"><span data-stu-id="d2949-126">The following example shows configuration of the 'httpd' service (for Apache HTTP Server), registered with the **SystemD** service controller.</span></span>

```powershell
Import-DSCResource -Module nx

Node $node {
    #Apache Service
    nxService ApacheService {
        Name = 'httpd'
        State = 'running'
        Enabled = $true
        Controller = 'systemd'
    }
}
```