---
title: Przykłady obszarem działania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c92a6d3d-8d34-4a76-bdc3-dea923d9858e
caps.latest.revision: 17
ms.openlocfilehash: e24d40746da91f60aaf2af655ddcadc88ab6a4db
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56847747"
---
# <a name="runspace-samples"></a><span data-ttu-id="9b43b-102">Przykłady obszarów działania</span><span class="sxs-lookup"><span data-stu-id="9b43b-102">Runspace Samples</span></span>

<span data-ttu-id="9b43b-103">Ta sekcja zawiera przykładowy kod, który ilustruje sposób używania różnych rodzajów obszary działania do uruchamiania poleceń, synchronicznie i asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="9b43b-103">This section includes sample code that shows how to use different types of runspaces to run commands synchronously and asynchronously.</span></span> <span data-ttu-id="9b43b-104">Microsoft Visual Studio umożliwia tworzenie aplikacji konsolowej, a następnie skopiować kod z tematy w tej sekcji, w aplikacji hosta.</span><span class="sxs-lookup"><span data-stu-id="9b43b-104">You can use Microsoft Visual Studio to create a console application and then copy the code from the topics in this section into your host application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b43b-105">W tej sekcji</span><span class="sxs-lookup"><span data-stu-id="9b43b-105">In This Section</span></span>

> [!NOTE]
> <span data-ttu-id="9b43b-106">Aby uzyskać przykłady aplikacji hosta, które tworzą interfejsy niestandardowego hosta, zobacz [niestandardowego hosta przykłady](./custom-host-samples.md).</span><span class="sxs-lookup"><span data-stu-id="9b43b-106">For samples of host applications that create custom host interfaces, see [Custom Host Samples](./custom-host-samples.md).</span></span>

 <span data-ttu-id="9b43b-107">[Przykładowe Runspace01](./runspace01-sample.md) w tym przykładzie pokazano, jak [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) klasy, aby uruchomić [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) polecenia cmdlet synchronicznie i wyświetlić dane wyjściowe w konsoli programu okno.</span><span class="sxs-lookup"><span data-stu-id="9b43b-107">[Runspace01 Sample](./runspace01-sample.md) This sample shows how to use the [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) class to run the [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) cmdlet synchronously and display its output in a console window.</span></span>

 <span data-ttu-id="9b43b-108">[Przykładowe Runspace02](./runspace02-sample.md) w tym przykładzie pokazano, jak [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) klasy, aby uruchomić [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) i [Sort-Object](/powershell/module/Microsoft.PowerShell.Utility/Sort-Object) polecenia cmdlet synchronicznie.</span><span class="sxs-lookup"><span data-stu-id="9b43b-108">[Runspace02 Sample](./runspace02-sample.md) This sample shows how to use the [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) class to run the [Get-Process](/powershell/module/Microsoft.PowerShell.Management/Get-Process) and [Sort-Object](/powershell/module/Microsoft.PowerShell.Utility/Sort-Object) cmdlets synchronously.</span></span> <span data-ttu-id="9b43b-109">Wyniki tych poleceń jest wyświetlana przy użyciu [System.Windows.Forms.Datagridview](/dotnet/api/System.Windows.Forms.DataGridView) kontroli.</span><span class="sxs-lookup"><span data-stu-id="9b43b-109">The results of these commands is displayed by using a [System.Windows.Forms.Datagridview](/dotnet/api/System.Windows.Forms.DataGridView) control.</span></span>

 <span data-ttu-id="9b43b-110">[Przykładowe Runspace03](./runspace03-sample.md) w tym przykładzie pokazano, jak [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) klasy, aby uruchomić skrypt synchronicznie i sposób obsługi błędy niepowodujące.</span><span class="sxs-lookup"><span data-stu-id="9b43b-110">[Runspace03 Sample](./runspace03-sample.md) This sample shows how to use the [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) class to run a script synchronously, and how to handle non-terminating errors.</span></span> <span data-ttu-id="9b43b-111">Skrypt otrzymuje listę nazw procesu, a następnie pobierze te procesy.</span><span class="sxs-lookup"><span data-stu-id="9b43b-111">The script receives a list of process names and then retrieves those processes.</span></span> <span data-ttu-id="9b43b-112">Wyniki skryptu, między innymi niepowodujące błędy, które zostały wygenerowane podczas uruchamiania skryptu, są wyświetlane w oknie konsoli.</span><span class="sxs-lookup"><span data-stu-id="9b43b-112">The results of the script, including any non-terminating errors that were generated when running the script, are displayed in a console window.</span></span>

 <span data-ttu-id="9b43b-113">[Przykładowe Runspace04](./runspace04-sample.md) w tym przykładzie pokazano, jak [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) klasy do uruchamiania poleceń oraz jak catch kończący błędów, które są zgłaszane w przypadku uruchamiania polecenia.</span><span class="sxs-lookup"><span data-stu-id="9b43b-113">[Runspace04 Sample](./runspace04-sample.md) This sample shows how to use the [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) class to run commands, and how to catch terminating errors that are thrown when running the commands.</span></span> <span data-ttu-id="9b43b-114">Dwa polecenia są uruchamiane, a ostatnie polecenie jest przekazany argument parametru, który jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="9b43b-114">Two commands are run, and the last command is passed a parameter argument that is not valid.</span></span> <span data-ttu-id="9b43b-115">W rezultacie obiekty nie są zwracane i generowany jest błąd powodujący zakończenie.</span><span class="sxs-lookup"><span data-stu-id="9b43b-115">As a result no objects are returned and a terminating error is thrown.</span></span>

 <span data-ttu-id="9b43b-116">[Przykładowe Runspace05](./runspace05-sample.md) w tym przykładzie przedstawiono sposób dodawania przystawki do [System.Management.Automation.Runspaces.Initialsessionstate](/dotnet/api/System.Management.Automation.Runspaces.InitialSessionState) obiekt cmdlet przystawki jest dostępne po otwarciu obszaru działania.</span><span class="sxs-lookup"><span data-stu-id="9b43b-116">[Runspace05 Sample](./runspace05-sample.md) This sample shows how to add a snap-in to an [System.Management.Automation.Runspaces.Initialsessionstate](/dotnet/api/System.Management.Automation.Runspaces.InitialSessionState) object so that the cmdlet of the snap-in is available when the runspace is opened.</span></span> <span data-ttu-id="9b43b-117">Ta przystawka udostępnia polecenia cmdlet Get-Proc (zdefiniowane przez [przykładowe GetProcessSample01](../cmdlet/getprocesssample01-sample.md)) uruchamiane synchronicznie przy użyciu [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) obiektu.</span><span class="sxs-lookup"><span data-stu-id="9b43b-117">The snap-in provides a Get-Proc cmdlet (defined by the [GetProcessSample01 Sample](../cmdlet/getprocesssample01-sample.md)) that is run synchronously using a [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) object.</span></span>

 <span data-ttu-id="9b43b-118">[Przykładowe Runspace06](./runspace06-sample.md) w tym przykładzie przedstawiono sposób dodawania modułu, aby [System.Management.Automation.Runspaces.Initialsessionstate](/dotnet/api/System.Management.Automation.Runspaces.InitialSessionState) obiekt moduł jest załadowany po otwarciu obszaru działania.</span><span class="sxs-lookup"><span data-stu-id="9b43b-118">[Runspace06 Sample](./runspace06-sample.md) This sample shows how to add a module to an [System.Management.Automation.Runspaces.Initialsessionstate](/dotnet/api/System.Management.Automation.Runspaces.InitialSessionState) object so that the module is loaded when the runspace is opened.</span></span> <span data-ttu-id="9b43b-119">Moduł zawiera polecenia cmdlet Get-Proc (zdefiniowany przez [przykładowe GetProcessSample02](../cmdlet/getprocesssample02-sample.md)) uruchamiane synchronicznie przy użyciu [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) obiektu.</span><span class="sxs-lookup"><span data-stu-id="9b43b-119">The module provides a Get-Proc cmdlet (defined by the [GetProcessSample02 Sample](../cmdlet/getprocesssample02-sample.md)) that is run synchronously using a [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) object.</span></span>

 <span data-ttu-id="9b43b-120">[Przykładowe Runspace07](./runspace07-sample.md) w tym przykładzie pokazano, jak utworzyć obszar działania, a następnie użyj tego obszaru działania na dwa polecenia cmdlet były uruchamiane synchronicznie przy użyciu [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) obiektu.</span><span class="sxs-lookup"><span data-stu-id="9b43b-120">[Runspace07 Sample](./runspace07-sample.md) This sample shows how to create a runspace, and then use that runspace to run two cmdlets synchronously by using a [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) object.</span></span>

 <span data-ttu-id="9b43b-121">[Przykładowe Runspace08](./runspace08-sample.md) w tym przykładzie przedstawiono sposób dodawania polecenia i argumentów do potoku [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) obiektu i jak polecenia były uruchamiane synchronicznie.</span><span class="sxs-lookup"><span data-stu-id="9b43b-121">[Runspace08 Sample](./runspace08-sample.md) This sample shows how to add commands and arguments to the pipeline of a [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) object and how to run the commands synchronously.</span></span>

 <span data-ttu-id="9b43b-122">[Przykładowe Runspace09](./runspace09-sample.md) w tym przykładzie pokazano, jak dodać skrypt do potoku [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) obiektu oraz sposobu uruchamiania skryptu asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="9b43b-122">[Runspace09 Sample](./runspace09-sample.md) This sample shows how to add a script to the pipeline of a [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) object and how to run the script asynchronously.</span></span> <span data-ttu-id="9b43b-123">Zdarzenia są używane do obsługi danych wyjściowych skryptu.</span><span class="sxs-lookup"><span data-stu-id="9b43b-123">Events are used to handle the output of the script.</span></span>

 <span data-ttu-id="9b43b-124">[Przykładowe Runspace10](./runspace10-sample.md) w tym przykładzie pokazano, jak utworzyć domyślny początkowy stan sesji, jak dodać polecenia cmdlet, aby [System.Management.Automation.Runspaces.Initialsessionstate](/dotnet/api/System.Management.Automation.Runspaces.InitialSessionState), jak utworzyć obszar działania, który używa Stan sesji początkowej oraz sposobu uruchamiania polecenia przy użyciu [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) obiektu.</span><span class="sxs-lookup"><span data-stu-id="9b43b-124">[Runspace10 Sample](./runspace10-sample.md) This sample shows how to create a default initial session state, how to add a cmdlet to the [System.Management.Automation.Runspaces.Initialsessionstate](/dotnet/api/System.Management.Automation.Runspaces.InitialSessionState), how to create a runspace that uses the initial session state, and how to run the command by using a [System.Management.Automation.Powershell](/dotnet/api/system.management.automation.powershell) object.</span></span>

 <span data-ttu-id="9b43b-125">[Przykładowe Runspace11](./runspace11-sample.md) to pokazuje, jak używać [System.Management.Automation.Proxycommand](/dotnet/api/System.Management.Automation.ProxyCommand) klasy, aby utworzyć polecenie proxy, który wywołuje istniejące polecenia cmdlet, ale ogranicza zestaw dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="9b43b-125">[Runspace11 Sample](./runspace11-sample.md) This shows how to use the [System.Management.Automation.Proxycommand](/dotnet/api/System.Management.Automation.ProxyCommand) class to create a proxy command that calls an existing cmdlet, but restricts the set of available parameters.</span></span> <span data-ttu-id="9b43b-126">Polecenie proxy jest dodawane do stanu sesji początkowej, która służy do tworzenia ograniczonego obszaru działania.</span><span class="sxs-lookup"><span data-stu-id="9b43b-126">The proxy command is then added to an initial session state that is used to create a constrained runspace.</span></span> <span data-ttu-id="9b43b-127">Oznacza to, że użytkownik ma dostęp funkcjonalność polecenia cmdlet tylko za pomocą polecenia proxy.</span><span class="sxs-lookup"><span data-stu-id="9b43b-127">This means that the user can access the functionality of the cmdlet only through the proxy command.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b43b-128">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="9b43b-128">See Also</span></span>