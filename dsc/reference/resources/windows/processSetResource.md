---
ms.date: 06/12/2017
keywords: DSC, powershell, konfiguracja, ustawienia
title: Zasób Processset DSC
ms.openlocfilehash: 91a2d5b562864addcb8e11062916d291448bbf57
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "55688840"
---
# <a name="dsc-windowsprocess-resource"></a><span data-ttu-id="55c73-103">Zasób Windowsprocess DSC</span><span class="sxs-lookup"><span data-stu-id="55c73-103">DSC WindowsProcess Resource</span></span>

<span data-ttu-id="55c73-104">_Dotyczy: Windows PowerShell 5.0_</span><span class="sxs-lookup"><span data-stu-id="55c73-104">_Applies To: Windows PowerShell 5.0_</span></span>

<span data-ttu-id="55c73-105">**ProcessSet** zasobów w Windows PowerShell Desired State Configuration (DSC) udostępnia mechanizm do konfigurowania procesów na węzeł docelowy.</span><span class="sxs-lookup"><span data-stu-id="55c73-105">The **ProcessSet** resource in Windows PowerShell Desired State Configuration (DSC) provides a mechanism to configure processes on a target node.</span></span> <span data-ttu-id="55c73-106">Ten zasób jest [złożonego zasobów](../../../resources/authoringResourceComposite.md) wywołująca [zasób windowsprocess](windowsProcessResource.md) dla każdej grupy określony w `GroupName` parametru.</span><span class="sxs-lookup"><span data-stu-id="55c73-106">This resource is a [composite resource](../../../resources/authoringResourceComposite.md) that calls the [WindowsProcess resource](windowsProcessResource.md) for each group specified in the `GroupName` parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c73-107">Składnia</span><span class="sxs-lookup"><span data-stu-id="55c73-107">Syntax</span></span>

```
WindowsProcess [string] #ResourceName
{
    Arguments = [string]
    Path = [string]
    [ Credential = [PSCredential] ]
    [ Ensure = [string] { Absent | Present }  ]
    [ StandardOutputPath = [string] ]
    [ StandardErrorPath = [string] ]
    [ StandardInputPath = [string] ]
    [ WorkingDirectory = [string] ]
    [ DependsOn = [string[]] ]
}
```

## <a name="properties"></a><span data-ttu-id="55c73-108">Właściwości</span><span class="sxs-lookup"><span data-stu-id="55c73-108">Properties</span></span>

| <span data-ttu-id="55c73-109">Właściwość</span><span class="sxs-lookup"><span data-stu-id="55c73-109">Property</span></span> | <span data-ttu-id="55c73-110">Opis</span><span class="sxs-lookup"><span data-stu-id="55c73-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="55c73-111">Argumenty</span><span class="sxs-lookup"><span data-stu-id="55c73-111">Arguments</span></span>| <span data-ttu-id="55c73-112">Ciąg, który zawiera argumenty do przekazania do procesu jako-to.</span><span class="sxs-lookup"><span data-stu-id="55c73-112">A string that contains arguments to pass to the process as-is.</span></span> <span data-ttu-id="55c73-113">Jeśli musisz przekazać argumenty kilka umieściliśmy je w tym ciągu.</span><span class="sxs-lookup"><span data-stu-id="55c73-113">If you need to pass several arguments, put them all in this string.</span></span>|
| <span data-ttu-id="55c73-114">Ścieżka</span><span class="sxs-lookup"><span data-stu-id="55c73-114">Path</span></span>| <span data-ttu-id="55c73-115">Ścieżki do plików wykonywalnych procesu.</span><span class="sxs-lookup"><span data-stu-id="55c73-115">The paths to the process executables.</span></span> <span data-ttu-id="55c73-116">Jeśli są one nazwy plików wykonywalnych (nie w pełni kwalifikowanej ścieżki), umożliwia wyszukiwanie zasobów DSC środowiska **ścieżki** zmiennej (`$env:Path`) aby znaleźć pliki.</span><span class="sxs-lookup"><span data-stu-id="55c73-116">If these are the names of the executable files (not fully qualified paths), the DSC resource will search the environment **Path** variable (`$env:Path`) to find the files.</span></span> <span data-ttu-id="55c73-117">Jeśli wartości tej właściwości to w pełni kwalifikowanej ścieżki, DSC nie będzie używać **ścieżki** zmiennej środowiskowej, aby znaleźć pliki i zgłosi błąd, jeśli ścieżki nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="55c73-117">If the values of this property are fully qualified paths, DSC will not use the **Path** environment variable to find the files, and will throw an error if any of the paths do not exist.</span></span> <span data-ttu-id="55c73-118">Ścieżki względne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="55c73-118">Relative paths are not allowed.</span></span>|
| <span data-ttu-id="55c73-119">Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="55c73-119">Credential</span></span>| <span data-ttu-id="55c73-120">Określa poświadczenia do uruchamiania procesu.</span><span class="sxs-lookup"><span data-stu-id="55c73-120">Indicates the credentials for starting the process.</span></span>|
| <span data-ttu-id="55c73-121">Upewnij się</span><span class="sxs-lookup"><span data-stu-id="55c73-121">Ensure</span></span>| <span data-ttu-id="55c73-122">Określa, czy istnieje procesów.</span><span class="sxs-lookup"><span data-stu-id="55c73-122">Specifies whether the processes exists.</span></span> <span data-ttu-id="55c73-123">Ustaw tę właściwość "Present", aby upewnić się, że istnieje proces.</span><span class="sxs-lookup"><span data-stu-id="55c73-123">Set this property to "Present" to ensure that the process exists.</span></span> <span data-ttu-id="55c73-124">W przeciwnym wypadku ustaw ją na "Brak".</span><span class="sxs-lookup"><span data-stu-id="55c73-124">Otherwise, set it to "Absent".</span></span> <span data-ttu-id="55c73-125">Wartość domyślna to "Istnieje".</span><span class="sxs-lookup"><span data-stu-id="55c73-125">The default is "Present".</span></span>|
| <span data-ttu-id="55c73-126">StandardErrorPath</span><span class="sxs-lookup"><span data-stu-id="55c73-126">StandardErrorPath</span></span>| <span data-ttu-id="55c73-127">Ścieżka, do którego procesy standardowy błąd zapisu.</span><span class="sxs-lookup"><span data-stu-id="55c73-127">The path to which the processes write standard error.</span></span> <span data-ttu-id="55c73-128">Wszystkie istniejące pliki zostaną zastąpione.</span><span class="sxs-lookup"><span data-stu-id="55c73-128">Any existing file there will be overwritten.</span></span>|
| <span data-ttu-id="55c73-129">StandardInputPath</span><span class="sxs-lookup"><span data-stu-id="55c73-129">StandardInputPath</span></span>| <span data-ttu-id="55c73-130">Strumień, z którego proces odbiera standardowe dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="55c73-130">The stream from which the process receives standard input.</span></span>|
| <span data-ttu-id="55c73-131">StandardOutputPath</span><span class="sxs-lookup"><span data-stu-id="55c73-131">StandardOutputPath</span></span>| <span data-ttu-id="55c73-132">Ścieżka pliku, w której procesy zapisuje standardowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="55c73-132">The path of the file to which the processes write standard output.</span></span> <span data-ttu-id="55c73-133">Wszystkie istniejące pliki zostaną zastąpione.</span><span class="sxs-lookup"><span data-stu-id="55c73-133">Any existing file there will be overwritten.</span></span>|
| <span data-ttu-id="55c73-134">WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="55c73-134">WorkingDirectory</span></span>| <span data-ttu-id="55c73-135">Lokalizacja używana jako bieżący katalog roboczy dla procesów.</span><span class="sxs-lookup"><span data-stu-id="55c73-135">The location used as the current working directory for the processes.</span></span>|
| <span data-ttu-id="55c73-136">DependsOn</span><span class="sxs-lookup"><span data-stu-id="55c73-136">DependsOn</span></span> | <span data-ttu-id="55c73-137">Wskazuje, że konfiguracji inny zasób, należy uruchomić przed ten zasób jest skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="55c73-137">Indicates that the configuration of another resource must run before this resource is configured.</span></span> <span data-ttu-id="55c73-138">Na przykład, jeśli identyfikator konfiguracji zasobu skryptu Blok, który chcesz uruchomić najpierw jest **ResourceName** a jej typ jest **_ResourceType**, składnia przy użyciu tej właściwości jest `DependsOn = "[ResourceType]ResourceName"` .</span><span class="sxs-lookup"><span data-stu-id="55c73-138">For example, if the ID of the resource configuration script block that you want to run first is **ResourceName** and its type is **_ResourceType**, the syntax for using this property is `DependsOn = "[ResourceType]ResourceName"` .</span></span>|