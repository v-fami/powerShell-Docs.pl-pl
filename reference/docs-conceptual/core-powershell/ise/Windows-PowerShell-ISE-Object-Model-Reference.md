---
ms.date: 2017-06-05
keywords: polecenia cmdlet programu PowerShell
title: "Dokumentacja dotycząca modelu obiektów środowiska Windows PowerShell ISE"
ms.assetid: e1a9e7d1-0fd5-47de-8d9b-f1be1ed13b0c
ms.openlocfilehash: 624ddca3895ba3e24bf52a27babdb07e8714baae
ms.sourcegitcommit: 18e3bfae83ffe282d3fd1a45f5386f3b7250f0c0
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/08/2018
---
# <a name="windows-powershell-ise-object-model-reference"></a><span data-ttu-id="da1f9-103">Dokumentacja dotycząca modelu obiektów środowiska Windows PowerShell ISE</span><span class="sxs-lookup"><span data-stu-id="da1f9-103">Windows PowerShell ISE Object Model Reference</span></span>
  
## <a name="object-model-reference"></a><span data-ttu-id="da1f9-104">Odwołanie do obiektu modelu</span><span class="sxs-lookup"><span data-stu-id="da1f9-104">Object Model Reference</span></span>
 <span data-ttu-id="da1f9-105">Ta sekcja zawiera odwołanie na klasy podstawowej, które definiują różne inWindows obiektów PowerShell® Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="da1f9-105">This section provides a reference on the underlying classes that define the various objects inWindows PowerShell® Integrated Scripting Environment (ISE).</span></span> <span data-ttu-id="da1f9-106">Aby wyświetlić obiekty zorganizowane w hierarchii, zobacz [hierarchii modelu obiektu ISE](The-ISE-Object-Model-Hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="da1f9-106">To see the objects organized in their hierarchy, see [The ISE Object Model Hierarchy](The-ISE-Object-Model-Hierarchy.md).</span></span>

 <span data-ttu-id="da1f9-107">[Obiekt ISEAddOnTool](The-ISEAddOnTool-Object.md) przykłady: $psISE.CurrentVisibleHorizontalTool, $psISE.CurrentVisibleVerticalTool.</span><span class="sxs-lookup"><span data-stu-id="da1f9-107">[The ISEAddOnTool Object](The-ISEAddOnTool-Object.md) Examples: $psISE.CurrentVisibleHorizontalTool, $psISE.CurrentVisibleVerticalTool.</span></span>

 <span data-ttu-id="da1f9-108">[Obiekt ISEAddOnTool](The-ISEAddOnTool-Object.md) [obiektu ISEEditor](The-ISEEditor-Object.md) przykłady: $psISE.CurrentFile.Editor, $psISE.CurrentPowerShellTab.Output, $psISE.CurrentPowerShellTab.CommandPane.</span><span class="sxs-lookup"><span data-stu-id="da1f9-108">[The ISEAddOnTool Object](The-ISEAddOnTool-Object.md) [The ISEEditor Object](The-ISEEditor-Object.md) Examples: $psISE.CurrentFile.Editor, $psISE.CurrentPowerShellTab.Output, $psISE.CurrentPowerShellTab.CommandPane.</span></span>

 <span data-ttu-id="da1f9-109">[Obiekt ISEFile](The-ISEFile-Object.md) przykłady: $psISE.CurrentFile, $psISE.PowerShellTabs.Files\[0\].</span><span class="sxs-lookup"><span data-stu-id="da1f9-109">[The ISEFile Object](The-ISEFile-Object.md) Examples: $psISE.CurrentFile, $psISE.PowerShellTabs.Files\[0\].</span></span>

 <span data-ttu-id="da1f9-110">[Obiekt ISEFileCollection](The-ISEFileCollection-Object.md) przykłady: $psISE.PowerShellTabs.Files.</span><span class="sxs-lookup"><span data-stu-id="da1f9-110">[The ISEFileCollection Object](The-ISEFileCollection-Object.md) Examples: $psISE.PowerShellTabs.Files.</span></span>

 <span data-ttu-id="da1f9-111">[Obiekt ISEMenuItem](The-ISEMenuItem-Object.md) przykłady: $psISE.CurrentPowerShellTab.AddOnsMenu, $psISE.CurrentPowerShellTab.AddOnsMenu.Submenus\[0\].</span><span class="sxs-lookup"><span data-stu-id="da1f9-111">[The ISEMenuItem Object](The-ISEMenuItem-Object.md) Examples: $psISE.CurrentPowerShellTab.AddOnsMenu , $psISE.CurrentPowerShellTab.AddOnsMenu.Submenus\[0\].</span></span>

 <span data-ttu-id="da1f9-112">[Obiekt ISEMenuItemCollection](The-ISEMenuItemCollection-Object.md) przykład: $psISE.CurrentPowerShellTab.AddOnsMenu.Submenus.</span><span class="sxs-lookup"><span data-stu-id="da1f9-112">[The ISEMenuItemCollection Object](The-ISEMenuItemCollection-Object.md) Example: $psISE.CurrentPowerShellTab.AddOnsMenu.Submenus.</span></span>

 <span data-ttu-id="da1f9-113">[Obiekt ISEOptions](The-ISEOptions-Object.md) przykłady: $psISE.Options, $psISE.Options.DefaultOptions.</span><span class="sxs-lookup"><span data-stu-id="da1f9-113">[The ISEOptions Object](The-ISEOptions-Object.md) Examples: $psISE.Options, $psISE.Options.DefaultOptions.</span></span>

 <span data-ttu-id="da1f9-114">[Obiekt ObjectModelRoot](The-ObjectModelRoot-Object.md) przykład: obiekt główny $psISE.</span><span class="sxs-lookup"><span data-stu-id="da1f9-114">[The ObjectModelRoot Object](The-ObjectModelRoot-Object.md) Example: The root $psISE object.</span></span>

 <span data-ttu-id="da1f9-115">[Obiekt PowerShellTab](The-PowerShellTab-Object.md) przykłady: $psISE.CurrentPowerShellTab, $psISE.PowerShellTabs\[0\].</span><span class="sxs-lookup"><span data-stu-id="da1f9-115">[The PowerShellTab Object](The-PowerShellTab-Object.md) Examples: $psISE.CurrentPowerShellTab, $psISE.PowerShellTabs\[0\].</span></span>

 <span data-ttu-id="da1f9-116">[Obiekt PowerShellTabCollection](The-PowerShellTabCollection-Object.md) przykład: $psISE.PowerShellTabs.</span><span class="sxs-lookup"><span data-stu-id="da1f9-116">[The PowerShellTabCollection Object](The-PowerShellTabCollection-Object.md) Example: $psISE.PowerShellTabs.</span></span>

## <a name="see-also"></a><span data-ttu-id="da1f9-117">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="da1f9-117">See Also</span></span>
- [<span data-ttu-id="da1f9-118">Windows PowerShell ISE skryptów modelu obiektów</span><span class="sxs-lookup"><span data-stu-id="da1f9-118">The Windows PowerShell ISE Scripting Object Model</span></span>](The-Windows-PowerShell-ISE-Scripting-Object-Model.md)