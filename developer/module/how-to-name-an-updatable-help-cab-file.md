---
title: Jak nazwać plik CAB aktualizowalnej pomocy | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/12/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: de302da0-c17a-4d31-a8ef-14a626738993
caps.latest.revision: 7
ms.openlocfilehash: 23303489372cfe7e036fdea842ae75f7e47503c8
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56850512"
---
# <a name="how-to-name-an-updatable-help-cab-file"></a><span data-ttu-id="72e15-102">Jak nazwać plik CAB aktualizowalnej pomocy</span><span class="sxs-lookup"><span data-stu-id="72e15-102">How to Name an Updatable Help CAB File</span></span>

<span data-ttu-id="72e15-103">W tym temacie opisano wymaganą nazwą format pliku cabinet aktualizowalnej pomocy (. Pliki CAB).</span><span class="sxs-lookup"><span data-stu-id="72e15-103">This topic explains the required name format for the Updatable Help cabinet (.CAB) files.</span></span>

## <a name="how-to-name-an-updatable-help-cab-file"></a><span data-ttu-id="72e15-104">Jak nazwać plik CAB aktualizowalnej pomocy</span><span class="sxs-lookup"><span data-stu-id="72e15-104">How to Name an Updatable Help CAB File</span></span>

<span data-ttu-id="72e15-105">Można zaktualizować pliku cabinet (. Plik CAB) musi mieć nazwę w następującym formacie.</span><span class="sxs-lookup"><span data-stu-id="72e15-105">A Updatable cabinet (.CAB) file must have a name with the following format.</span></span>

`<ModuleName>_<ModuleGUID>_<UICulture>_HelpContent.cab`

<span data-ttu-id="72e15-106">Dostępne są następujące elementy o tej nazwie.</span><span class="sxs-lookup"><span data-stu-id="72e15-106">The elements of the name are as follows.</span></span>

<span data-ttu-id="72e15-107">Modulename: wartość z **nazwa** właściwość **ModuleInfo** obiekt [Get-Module](/powershell/module/Microsoft.PowerShell.Core/Get-Module) polecenie cmdlet zwraca.</span><span class="sxs-lookup"><span data-stu-id="72e15-107">ModuleName The value of the **Name** property of the **ModuleInfo** object that the [Get-Module](/powershell/module/Microsoft.PowerShell.Core/Get-Module) cmdlet returns.</span></span>
<span data-ttu-id="72e15-108">Wartość **nazwa** właściwość **ModuleInfo** obiekt [Get-Module](/powershell/module/Microsoft.PowerShell.Core/Get-Module) polecenie cmdlet zwraca.</span><span class="sxs-lookup"><span data-stu-id="72e15-108">The value of the **Name** property of the **ModuleInfo** object that the [Get-Module](/powershell/module/Microsoft.PowerShell.Core/Get-Module) cmdlet returns.</span></span>

<span data-ttu-id="72e15-109">ModuleGUID wartość z **GUID** klucza w manifeście modułu.</span><span class="sxs-lookup"><span data-stu-id="72e15-109">ModuleGUID The value of the **GUID** key in the module manifest.</span></span>

<span data-ttu-id="72e15-110">Kultura interfejsu użytkownika UICulture pliki pomocy w pliku CAB.</span><span class="sxs-lookup"><span data-stu-id="72e15-110">UICulture The UI culture of the help files in the CAB file.</span></span> <span data-ttu-id="72e15-111">Ta wartość musi odpowiadać wartości jednego z **UICulture** elementy w pliku HelpInfo XML dla modułu.</span><span class="sxs-lookup"><span data-stu-id="72e15-111">This value must match the value of one of the **UICulture** elements in the HelpInfo XML file for the module.</span></span>

<span data-ttu-id="72e15-112">Na przykład jeśli nazwa modułu jest "TestModule", moduł identyfikator GUID jest 9cabb9ad-f2ac-4914-a46b-bfc1bebf07f9 i kultura interfejsu użytkownika jest "en US", nazwa pliku CAB:</span><span class="sxs-lookup"><span data-stu-id="72e15-112">For example, if the module name is "TestModule," the module GUID is 9cabb9ad-f2ac-4914-a46b-bfc1bebf07f9, and the UI culture is "en-US", the name of the CAB file would be:</span></span>

`TestModule_9cabb9ad-f2ac-4914-a46b-bfc1bebf07f9_en-US_HelpContent.cab`