---
title: Dokumentacja programu Windows PowerShell | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Windows PowerShell SDK
ms.assetid: cbba4879-bcac-484a-9906-4bbe2cd1eb33
caps.latest.revision: 11
ms.openlocfilehash: dfda6cb68b089a30a156760345420ee80d1d3ae9
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56851086"
---
# <a name="windows-powershell-reference"></a><span data-ttu-id="dd7a9-102">Dokumentacja programu Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd7a9-102">Windows PowerShell Reference</span></span>

<span data-ttu-id="dd7a9-103">Programu Windows PowerShell jest przeznaczony do automatyzacji administracyjne programu Microsoft .NET Framework — connected environment.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-103">Windows PowerShell is a Microsoft .NET Framework-connected environment designed for administrative automation.</span></span> <span data-ttu-id="dd7a9-104">Windows PowerShell udostępnia nowe podejście do tworzenia poleceń, tworzenie rozwiązań i tworzenia graficznego narzędzia do zarządzania oparte na interfejsie.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-104">Windows PowerShell provides a new approach to building commands, composing solutions, and creating graphical user interface-based management tools.</span></span>

<span data-ttu-id="dd7a9-105">Program Windows PowerShell umożliwia administratorowi systemu można zautomatyzować administracji zasobów systemowych przez wykonywanie poleceń bezpośrednio lub za pomocą skryptów.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-105">Windows PowerShell enables a system administrator to automate the administration of system resources by the execution of commands either directly or through scripts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dd7a9-106">Docelowa grupa deweloperów</span><span class="sxs-lookup"><span data-stu-id="dd7a9-106">Developer Audience</span></span>

<span data-ttu-id="dd7a9-107">Windows PowerShell Software Development Kit (SDK) jest przeznaczony dla polecenia deweloperów, którzy potrzebują informacji referencyjnych na temat interfejsów API udostępnionych przez środowisko Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-107">The Windows PowerShell Software Development Kit (SDK) is written for command developers who require reference information about the APIs provided by Windows PowerShell.</span></span> <span data-ttu-id="dd7a9-108">Polecenie deweloperzy używać środowiska Windows PowerShell do tworzenia poleceń i dostawców, które rozszerzają zadania, które mogą być wykonywane przez środowisko Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-108">Command developers use Windows PowerShell to create both commands and providers that extend the tasks that can be performed by Windows PowerShell.</span></span>

## <a name="windows-powershell-resources"></a><span data-ttu-id="dd7a9-109">Windows PowerShell zasobów</span><span class="sxs-lookup"><span data-stu-id="dd7a9-109">Windows PowerShell Resources</span></span>

<span data-ttu-id="dd7a9-110">Oprócz zestawu SDK Windows PowerShell poniższe zasoby przedstawiają więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-110">In addition to the Windows PowerShell SDK, the following resources provide more information.</span></span>

<span data-ttu-id="dd7a9-111">[Wprowadzenie do programu Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell) zawiera wprowadzenie do programu Windows PowerShell: języka, poleceń cmdlet, dostawców i obiektów.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-111">[Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell) Provides an introduction to Windows PowerShell: the language, the cmdlets, the providers, and the use of objects.</span></span>

<span data-ttu-id="dd7a9-112">[Pisanie modułu programu Windows PowerShell](./module/writing-a-windows-powershell-module.md) zawiera informacje i przykłady dla administratorów, deweloperzy skryptu i polecenia cmdlet deweloperów, którzy potrzebują pakować i rozpowszechniać swoje rozwiązania programu Windows PowerShell przy użyciu modułów programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-112">[Writing a Windows PowerShell Module](./module/writing-a-windows-powershell-module.md) Provides information and examples for administrators, script developers, and cmdlet developers who need to package and distribute their Windows PowerShell solutions using Windows PowerShell modules.</span></span>

<span data-ttu-id="dd7a9-113">[Zapisywanie polecenia Cmdlet programu Windows PowerShell](./cmdlet/writing-a-windows-powershell-cmdlet.md) zapewnia informacje i przykłady kodów kierownikom programów, którzy projektowania poleceń cmdlet oraz dla deweloperów, którzy wdrażają kodzie polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-113">[Writing a Windows PowerShell Cmdlet](./cmdlet/writing-a-windows-powershell-cmdlet.md) Provides information and code examples for program managers who are designing cmdlets and for developers who are implementing cmdlet code.</span></span>

<span data-ttu-id="dd7a9-114">[Blog zespołu programu Windows PowerShell](https://blogs.msdn.microsoft.com/PowerShell/) zostanie najlepszy zasób wiedzy i współpracować z innymi użytkownikami programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-114">[Windows PowerShell Team Blog](https://blogs.msdn.microsoft.com/PowerShell/) The best resource for learning from and collaborating with other Windows PowerShell users.</span></span> <span data-ttu-id="dd7a9-115">Przeczytaj wpis w blogu zespołu programu Windows PowerShell, a następnie dołącz do Forum użytkowników programu Windows PowerShell (microsoft.public.windows.powershell).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-115">Read the Windows PowerShell Team blog, and then join the Windows PowerShell User Forum (microsoft.public.windows.powershell).</span></span> <span data-ttu-id="dd7a9-116">Użyj usługi Windows Live Search, aby znaleźć inne środowiska Windows PowerShell, blogi i zasoby.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-116">Use Windows Live Search to find other Windows PowerShell blogs and resources.</span></span> <span data-ttu-id="dd7a9-117">Następnie podczas opracowywania wiedzę na temat swobodnie współtworzyć zawartość swoje pomysły.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-117">Then, as you develop your expertise, freely contribute your ideas.</span></span>

<span data-ttu-id="dd7a9-118">[Przeglądarka modułów programu PowerShell](/powershell/module/) zawiera najnowsze wersje wiersza polecenia Tematy pomocy.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-118">[PowerShell module browser](/powershell/module/) Provides the latest versions of the command-line Help topics.</span></span>

## <a name="class-libraries"></a><span data-ttu-id="dd7a9-119">Biblioteki klas</span><span class="sxs-lookup"><span data-stu-id="dd7a9-119">Class Libraries</span></span>

<span data-ttu-id="dd7a9-120">[System.Management.Automation](/dotnet/api/System.Management.Automation) ta przestrzeń nazw jest przestrzeń nazw korzenia dla środowiska Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-120">[System.Management.Automation](/dotnet/api/System.Management.Automation) This namespace is the root namespace for Windows PowerShell.</span></span> <span data-ttu-id="dd7a9-121">Zawiera on klas, wyliczeń i interfejsy, które trzeba do zaimplementowania niestandardowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-121">It contains the classes, enumerations, and interfaces required to implement custom cmdlets.</span></span> <span data-ttu-id="dd7a9-122">W szczególności [System.Management.Automation.Cmdlet](/dotnet/api/System.Management.Automation.Cmdlet) klasa to klasa bazowa, z których wszystkie polecenia cmdlet klasy musi pochodzić.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-122">In particular, the [System.Management.Automation.Cmdlet](/dotnet/api/System.Management.Automation.Cmdlet) class is the base class from which all cmdlet classes must be derived.</span></span> <span data-ttu-id="dd7a9-123">Aby uzyskać więcej informacji na temat poleceń cmdlet Zobacz.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-123">For more information about cmdlets, see.</span></span>

<span data-ttu-id="dd7a9-124">[System.Management.Automation.Provider](/dotnet/api/System.Management.Automation.Provider) ta przestrzeń nazw zawiera klasy, wyliczenia i połączeń wymaganych do implementowania dostawcy środowiska Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-124">[System.Management.Automation.Provider](/dotnet/api/System.Management.Automation.Provider) This namespace contains the classes, enumerations, and interfaces required to implement a Windows PowerShell provider.</span></span> <span data-ttu-id="dd7a9-125">W szczególności [System.Management.Automation.Provider.Cmdletprovider](/dotnet/api/System.Management.Automation.Provider.CmdletProvider) klasa to klasa bazowa, z których wszystkie środowiska Windows PowerShell musi pochodzić klasy dostawcy.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-125">In particular, the [System.Management.Automation.Provider.Cmdletprovider](/dotnet/api/System.Management.Automation.Provider.CmdletProvider) class is the base class from which all Windows PowerShell provider classes must be derived.</span></span>

<span data-ttu-id="dd7a9-126">[Microsoft.Powershell.Commands](/dotnet/api/Microsoft.PowerShell.Commands) ta przestrzeń nazw zawiera klasy dla poleceń cmdlet i dostawców implementowane przez środowisko Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-126">[Microsoft.Powershell.Commands](/dotnet/api/Microsoft.PowerShell.Commands) This namespace contains the classes for the cmdlets and providers implemented by Windows PowerShell.</span></span> <span data-ttu-id="dd7a9-127">Podobnie, zalecane jest, że utworzono *twojanazwa*. Polecenia te polecenia cmdlet, które należy zaimplementować w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-127">Similarly, it is recommended that you create a *YourName*.Commands namespace for those cmdlets that you implement.</span></span>

<span data-ttu-id="dd7a9-128">[System.Management.Automation.Host](/dotnet/api/System.Management.Automation.Host) ta przestrzeń nazw zawiera klasy, wyliczenia i interfejsy, które używa polecenia cmdlet w celu zdefiniowania interakcji między użytkownikiem i programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-128">[System.Management.Automation.Host](/dotnet/api/System.Management.Automation.Host) This namespace contains the classes, enumerations, and interfaces that the cmdlet uses to define the interaction between the user and Windows PowerShell.</span></span>

<span data-ttu-id="dd7a9-129">[System.Management.Automation.Internal](/dotnet/api/System.Management.Automation.Internal) ta przestrzeń nazw zawiera klasy bazowe, używane przez inne klasy w przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-129">[System.Management.Automation.Internal](/dotnet/api/System.Management.Automation.Internal) This namespace contains the base classes used by other namespace classes.</span></span> <span data-ttu-id="dd7a9-130">Na przykład [System.Management.Automation.Internal.Cmdletmetadataattribute](/dotnet/api/System.Management.Automation.Internal.CmdletMetadataAttribute) klasa jest klasą bazową dla [System.Management.Automation.Cmdletattribute](/dotnet/api/System.Management.Automation.CmdletAttribute) klasy.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-130">For example, the [System.Management.Automation.Internal.Cmdletmetadataattribute](/dotnet/api/System.Management.Automation.Internal.CmdletMetadataAttribute) class is the base class for the [System.Management.Automation.Cmdletattribute](/dotnet/api/System.Management.Automation.CmdletAttribute) class.</span></span>

<span data-ttu-id="dd7a9-131">[System.Management.Automation.Runspaces](/dotnet/api/System.Management.Automation.Runspaces) ta przestrzeń nazw zawiera klasy, wyliczenia i interfejsy, używany do tworzenia działania programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-131">[System.Management.Automation.Runspaces](/dotnet/api/System.Management.Automation.Runspaces) This namespace contains the classes, enumerations, and interfaces used to create a Windows PowerShell runspace.</span></span> <span data-ttu-id="dd7a9-132">W tym kontekście obszaru działania programu Windows PowerShell jest kontekst, w którym jeden lub wiele potoków programu Windows PowerShell wywoływanie polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-132">In this context, the Windows PowerShell runspace is the context in which one or more Windows PowerShell pipelines invoke cmdlets.</span></span> <span data-ttu-id="dd7a9-133">Oznacza to, że polecenia cmdlet działają w kontekście działania programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-133">That is, cmdlets work within the context of a Windows PowerShell runspace.</span></span> <span data-ttu-id="dd7a9-134">Aby uzyskać więcej informacji o aboutWindows obszary działania programu PowerShell, zobacz [obszary działania programu Windows PowerShell](http://msdn.microsoft.com/en-us/a1582cfe-f06d-4aff-adc6-71f49a860ce9).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-134">For more information aboutWindows PowerShell runspaces, see [Windows PowerShell Runspaces](http://msdn.microsoft.com/en-us/a1582cfe-f06d-4aff-adc6-71f49a860ce9).</span></span>