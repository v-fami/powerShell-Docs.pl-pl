---
title: Pisanie aplikacji hosta programu PowerShell Windows | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 81aeafad-dbc3-4712-8bb9-e6a417be260f
caps.latest.revision: 15
ms.openlocfilehash: 2039e181becd1b39fc3d6cf0cdbcf0c20e9fc206
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56851835"
---
# <a name="writing-a-windows-powershell-host-application"></a><span data-ttu-id="8a3d4-102">Pisanie aplikacji hosta programu Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a3d4-102">Writing a Windows PowerShell Host Application</span></span>

<span data-ttu-id="8a3d4-103">Program Windows PowerShell umożliwia hostowanie w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-103">You can host Windows PowerShell in your application.</span></span> <span data-ttu-id="8a3d4-104">Aplikacja hosta można zdefiniować obszar działania, w których są polecenia uruchomienia, otwórz sesji na komputerze lokalnym lub zdalnym i wywołują polecenia, albo synchronicznie lub asynchronicznie zależnie od potrzeb aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-104">The host application can define the runspace where commands are run, open sessions on a local or remote computer, and invoke the commands either synchronously or asynchronously based on the needs of the application.</span></span>

<span data-ttu-id="8a3d4-105">W poniższych tematach opisano sposób tworzenia aplikacji, który jest hostem</span><span class="sxs-lookup"><span data-stu-id="8a3d4-105">The following topics explain how to create an application that hosts</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a3d4-106">W tej sekcji</span><span class="sxs-lookup"><span data-stu-id="8a3d4-106">In This Section</span></span>

<span data-ttu-id="8a3d4-107">[Przewodnik Szybki Start programu Windows PowerShell hosta](./windows-powershell-host-quickstart.md) udostępnia instrukcje i przykłady kodu, aby ułatwić pracę, tworzenie aplikacji hosta.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-107">[Windows PowerShell Host Quickstart](./windows-powershell-host-quickstart.md) Provides instructions and code samples to get you started creating host applications.</span></span>

<span data-ttu-id="8a3d4-108">[Tworzenie obszary działania](./creating-runspaces.md) zestaw tematów, które przedstawiają sposób tworzenia obszarach działania, aby uruchomić polecenia programu Windows PowerShell w aplikacji hosta.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-108">[Creating Runspaces](./creating-runspaces.md) A set of topics that explain how to create runspaces to run Windows PowerShell command in a host application.</span></span>

<span data-ttu-id="8a3d4-109">[Dodawanie i wywoływania poleceń](./adding-and-invoking-commands.md) wyjaśnia, jak utworzyć i uruchomić potok polecenia w aplikacji hosta...</span><span class="sxs-lookup"><span data-stu-id="8a3d4-109">[Adding and invoking commands](./adding-and-invoking-commands.md) Explains how to create and run a command pipeline in your host application..</span></span>

<span data-ttu-id="8a3d4-110">[Tworzenie zdalnej obszary działania](./creating-remote-runspaces.md) Expains sposób nawiązywania połączenia z komputerem zdalnym obszaru działania.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-110">[Creating remote runspaces](./creating-remote-runspaces.md) Expains how to connect a runspace to a remote computer.</span></span>

<span data-ttu-id="8a3d4-111">[Tworzenie niestandardowego interfejsu użytkownika](./creating-a-custom-user-interface.md) użytkownika niestandardowego Introduces interfejsów i zawiera łącza do przykładów.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-111">[Creating a custom user interface](./creating-a-custom-user-interface.md) Introduces custom user interfaces and provides links to examples.</span></span>

<span data-ttu-id="8a3d4-112">[Przykłady aplikacji hosta](./host-application-samples.md) ta sekcja zawiera przykłady pełną obsługę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8a3d4-112">[Host Application Samples](./host-application-samples.md) This section includes samples of complete host applications.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a3d4-113">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="8a3d4-113">See Also</span></span>

[<span data-ttu-id="8a3d4-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a3d4-114">Windows PowerShell</span></span>](http://msdn.microsoft.com/en-us/b41a2af3-aec1-402d-8e18-c2c26be461ff)