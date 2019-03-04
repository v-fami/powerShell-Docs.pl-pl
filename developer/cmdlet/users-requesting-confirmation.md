---
title: Użytkownicy z żądaniem potwierdzenia | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6f337498-c534-40ed-968a-09d4d9ca3849
caps.latest.revision: 8
ms.openlocfilehash: e4abbb14b31406b845d9b6af6b6372338fb0d926
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56846977"
---
# <a name="users-requesting-confirmation"></a><span data-ttu-id="6657b-102">Użytkownicy żądający potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="6657b-102">Users Requesting Confirmation</span></span>

<span data-ttu-id="6657b-103">Po określeniu wartości `true` dla `SupportsShouldProcess` parametru deklaracji atrybutu polecenia Cmdlet, użytkownicy mogą określić `Confirm` parametr w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="6657b-103">When you specify a value of `true` for the `SupportsShouldProcess` parameter of the Cmdlet attribute declaration, users can specify the `Confirm` parameter at the command prompt.</span></span>

<span data-ttu-id="6657b-104">W środowisku domyślnym użytkownicy mogą określić `Confirm` parametru lub `"-Confirm:$true` tak, aby żądania potwierdzenia podczas [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) metoda jest wywoływana.</span><span class="sxs-lookup"><span data-stu-id="6657b-104">In the default environment, users can specify the `Confirm` parameter or `"-Confirm:$true` so that confirmation is requested when the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) method is called.</span></span> <span data-ttu-id="6657b-105">To pomija [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) żądania potwierdzenia, nawet w przypadku operacji o dużym znaczeniu.</span><span class="sxs-lookup"><span data-stu-id="6657b-105">This bypasses [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) confirmation requests, even for high-impact operations.</span></span>

<span data-ttu-id="6657b-106">Jeśli `Confirm` nie zostanie określony, [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) wywołanie zażąda potwierdzenia, jeśli `$ConfirmPreference` zmiennej preferencji jest równa lub większa niż `ConfirmImpact` ustawienie polecenia cmdlet lub dostawcy.</span><span class="sxs-lookup"><span data-stu-id="6657b-106">If `Confirm` is not specified, the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) call requests confirmation if the `$ConfirmPreference` preference variable is equal to or greater than the `ConfirmImpact` setting of the cmdlet or provider.</span></span> <span data-ttu-id="6657b-107">Domyślne ustawienie `$ConfirmPreference` jest wysoki.</span><span class="sxs-lookup"><span data-stu-id="6657b-107">The default setting of `$ConfirmPreference` is High.</span></span> <span data-ttu-id="6657b-108">W związku z tym w środowisku domyślnym tylko polecenia cmdlet i dostawców, które określają akcji o dużym znaczeniu żądania potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="6657b-108">Therefore, in the default environment, only cmdlets and providers that specify a high-impact action request confirmation.</span></span>

<span data-ttu-id="6657b-109">Jeśli `Confirm` ma wartość false lub jeśli `"-Confirm:$false` jest określony, [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) wywołanie zażąda potwierdzenia przez użytkownika i `$ConfirmPreference` zmiennej powłoki jest ignorowana.</span><span class="sxs-lookup"><span data-stu-id="6657b-109">If `Confirm` is false or if `"-Confirm:$false` is specified, the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) call requests confirmation from the user, and the `$ConfirmPreference` shell variable is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="6657b-110">Uwagi</span><span class="sxs-lookup"><span data-stu-id="6657b-110">Remarks</span></span>

- <span data-ttu-id="6657b-111">Dla poleceń cmdlet i dostawców, które określają `SupportsShouldProcess`, ale nie `ConfirmImpact`te akcje są obsługiwane jako akcje "średni wpływ" i nie będzie monitował domyślnie.</span><span class="sxs-lookup"><span data-stu-id="6657b-111">For cmdlets and providers that specify `SupportsShouldProcess`, but not `ConfirmImpact`, those actions are handled as "medium impact" actions, and they will not prompt by default.</span></span> <span data-ttu-id="6657b-112">Ich poziom wpływu jest niższy niż domyślne ustawienie `$ConfirmPreference` zmiennej preferencji.</span><span class="sxs-lookup"><span data-stu-id="6657b-112">Their impact level is less than the default setting of the `$ConfirmPreference` preference variable.</span></span>

- <span data-ttu-id="6657b-113">Jeśli użytkownik określi `Verbose` parametru, zostanie powiadomiony, operacji nawet jeśli nie są monitowani o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6657b-113">If the user specifies the `Verbose` parameter, they will be notified of the operation even if they are not prompted for confirmation.</span></span>

## <a name="see-also"></a><span data-ttu-id="6657b-114">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="6657b-114">See Also</span></span>

[<span data-ttu-id="6657b-115">Zapisywanie polecenia Cmdlet programu Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6657b-115">Writing a Windows PowerShell Cmdlet</span></span>](./writing-a-windows-powershell-cmdlet.md)