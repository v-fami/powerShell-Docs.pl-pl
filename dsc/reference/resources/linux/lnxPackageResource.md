---
ms.date: 06/12/2017
keywords: DSC, powershell, konfiguracja, ustawienia
title: DSC dla systemu Linux zasób nxPackage
ms.openlocfilehash: 64bb89a95bd6cbaea4e74b8a9979de52428fef3f
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "55685683"
---
# <a name="dsc-for-linux-nxpackage-resource"></a><span data-ttu-id="e3c84-103">DSC dla systemu Linux zasób nxPackage</span><span class="sxs-lookup"><span data-stu-id="e3c84-103">DSC for Linux nxPackage Resource</span></span>

<span data-ttu-id="e3c84-104">**NxPackage** zasobów w programie PowerShell Desired State Configuration (DSC) udostępnia mechanizm do zarządzania pakietami w węźle systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="e3c84-104">The **nxPackage** resource in PowerShell Desired State Configuration (DSC) provides a mechanism to manage packages on a Linux node.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c84-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="e3c84-105">Syntax</span></span>

```
nxPackage <string> #ResourceName
{
    Name = <string>
    [ Ensure = <string> { Absent | Present }  ]
    [ PackageManager = <string> { Yum | Apt | Zypper } ]
    [ PackageGroup = <bool>]
    [ Arguments = <string> ]
    [ ReturnCode = <uint32> ]
    [ LogPath = <string> ]
    [ DependsOn = <string[]> ]

}
```

## <a name="properties"></a><span data-ttu-id="e3c84-106">Właściwości</span><span class="sxs-lookup"><span data-stu-id="e3c84-106">Properties</span></span>

|  <span data-ttu-id="e3c84-107">Właściwość</span><span class="sxs-lookup"><span data-stu-id="e3c84-107">Property</span></span> |  <span data-ttu-id="e3c84-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e3c84-108">Description</span></span> |
|---|---|
| <span data-ttu-id="e3c84-109">Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3c84-109">Name</span></span>| <span data-ttu-id="e3c84-110">Nazwa pakietu, dla którego chcesz zapewnić określonego stanu.</span><span class="sxs-lookup"><span data-stu-id="e3c84-110">The name of the package for which you want to ensure a specific state.</span></span>|
| <span data-ttu-id="e3c84-111">Upewnij się</span><span class="sxs-lookup"><span data-stu-id="e3c84-111">Ensure</span></span>| <span data-ttu-id="e3c84-112">Określa, czy należy sprawdzić, czy istnieje pakiet.</span><span class="sxs-lookup"><span data-stu-id="e3c84-112">Determines whether to check if the package exists.</span></span> <span data-ttu-id="e3c84-113">Ustaw tę właściwość "Present", aby upewnić się, że pakiet istnieje.</span><span class="sxs-lookup"><span data-stu-id="e3c84-113">Set this property to "Present" to ensure the package exists.</span></span> <span data-ttu-id="e3c84-114">Ustaw ją na "Brak", aby upewnić się, że pakiet nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="e3c84-114">Set it to "Absent" to ensure the package does not exist.</span></span> <span data-ttu-id="e3c84-115">Wartość domyślna to "Istnieje".</span><span class="sxs-lookup"><span data-stu-id="e3c84-115">The default value is "Present".</span></span>|
| <span data-ttu-id="e3c84-116">PackageManager</span><span class="sxs-lookup"><span data-stu-id="e3c84-116">PackageManager</span></span>| <span data-ttu-id="e3c84-117">Obsługiwane wartości to "yum", "apt" i "zypper".</span><span class="sxs-lookup"><span data-stu-id="e3c84-117">Supported values are "yum", "apt", and "zypper".</span></span> <span data-ttu-id="e3c84-118">Określa Menedżera pakietów do użycia podczas instalowania pakietów.</span><span class="sxs-lookup"><span data-stu-id="e3c84-118">Specifies the package manager to use when installing packages.</span></span> <span data-ttu-id="e3c84-119">Jeśli **FilePath** jest określony, podana ścieżka będzie służyć do zainstalowania pakietu.</span><span class="sxs-lookup"><span data-stu-id="e3c84-119">If **FilePath** is specified, the provided path will be used to install the package.</span></span> <span data-ttu-id="e3c84-120">W przeciwnym razie Menedżera pakietów będzie służyć do zainstalowania pakietu ze wstępnie skonfigurowanym repozytorium.</span><span class="sxs-lookup"><span data-stu-id="e3c84-120">Otherwise, a Package Manager will be used to install the package from a pre-configured repository.</span></span> <span data-ttu-id="e3c84-121">Jeśli żadna **PackageManager** ani **FilePath** są dostarczane, domyślnego menedżera pakietów dla systemu, który będzie używany.</span><span class="sxs-lookup"><span data-stu-id="e3c84-121">If neither **PackageManager** nor **FilePath** are provided, the default package manager for the system will be used.</span></span>|
| <span data-ttu-id="e3c84-122">FilePath</span><span class="sxs-lookup"><span data-stu-id="e3c84-122">FilePath</span></span>| <span data-ttu-id="e3c84-123">Ścieżka pliku, w którym znajduje się pakiet</span><span class="sxs-lookup"><span data-stu-id="e3c84-123">The file path where the package resides</span></span>|
| <span data-ttu-id="e3c84-124">PackageGroup</span><span class="sxs-lookup"><span data-stu-id="e3c84-124">PackageGroup</span></span>| <span data-ttu-id="e3c84-125">Jeśli **$true**, **nazwa** powinna być nazwa grupy pakietu do użytku z programem **PackageManager**.</span><span class="sxs-lookup"><span data-stu-id="e3c84-125">If **$true**, the **Name** is expected to be the name of a package group for use with a **PackageManager**.</span></span> <span data-ttu-id="e3c84-126">**PacakgeGroup** jest nieprawidłowa, podczas dostarczania **FilePath**.</span><span class="sxs-lookup"><span data-stu-id="e3c84-126">**PacakgeGroup** is not valid when providing a **FilePath**.</span></span>|
| <span data-ttu-id="e3c84-127">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e3c84-127">Arguments</span></span>| <span data-ttu-id="e3c84-128">Ciąg argumenty, które zostaną przekazane do pakietu dokładnie zgodnie z postanowieniami.</span><span class="sxs-lookup"><span data-stu-id="e3c84-128">A string of arguments that will be passed to the package exactly as provided.</span></span>|
| <span data-ttu-id="e3c84-129">Kod zwrotny</span><span class="sxs-lookup"><span data-stu-id="e3c84-129">ReturnCode</span></span>| <span data-ttu-id="e3c84-130">Oczekiwany kod powrotny.</span><span class="sxs-lookup"><span data-stu-id="e3c84-130">The expected return code.</span></span> <span data-ttu-id="e3c84-131">Jeśli rzeczywiste zwróci kod nie odpowiada oczekiwanej wartości zostanie podany tutaj, konfiguracja zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="e3c84-131">If the actual return code does not match the expected value provided here, the configuration will return an error.</span></span>|
| <span data-ttu-id="e3c84-132">DependsOn</span><span class="sxs-lookup"><span data-stu-id="e3c84-132">DependsOn</span></span> | <span data-ttu-id="e3c84-133">Wskazuje, że konfiguracji inny zasób, należy uruchomić przed ten zasób jest skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="e3c84-133">Indicates that the configuration of another resource must run before this resource is configured.</span></span> <span data-ttu-id="e3c84-134">Na przykład jeśli **identyfikator** zasobu jest najpierw blok skryptu konfiguracji, który chcesz uruchomić **ResourceName** a jej typ jest **ResourceType**, składnia za pomocą tego Właściwość jest `DependsOn = "[ResourceType]ResourceName"`.</span><span class="sxs-lookup"><span data-stu-id="e3c84-134">For example, if the **ID** of the resource configuration script block that you want to run first is **ResourceName** and its type is **ResourceType**, the syntax for using this property is `DependsOn = "[ResourceType]ResourceName"`.</span></span>|

## <a name="example"></a><span data-ttu-id="e3c84-135">Przykład</span><span class="sxs-lookup"><span data-stu-id="e3c84-135">Example</span></span>

<span data-ttu-id="e3c84-136">Poniższy przykład gwarantuje, że na komputerze z systemem Linux, przy użyciu Menedżera pakietów "Yum" zainstalowano pakiet o nazwie "host z wieloma adresami".</span><span class="sxs-lookup"><span data-stu-id="e3c84-136">The following example ensures that the package named "httpd" is installed on a Linux computer, using the “Yum” package manager.</span></span>

```
Import-DSCResource -Module nx

Node $node {
nxPackage httpd
{
    Name = "httpd"
    Ensure = "Present"
    PackageManager = "Yum"
}
}
```