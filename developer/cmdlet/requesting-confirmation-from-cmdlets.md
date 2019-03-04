---
title: Żądanie potwierdzenia z polecenia cmdlet | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- ConfirmImpact [PowerShell Programmer's Guide], described
- ShouldContinue [PowerShell Programmer's Guide], described
- user feedback [PowerShell Programmer's Guide], requesting
- ShouldProcess [PowerShell Programmer's Guide], described
- ConfirmPreference [PowerShell Programmer's Guide], described
ms.assetid: 37d6e87f-57b7-40bd-b645-392cf0b6e88e
caps.latest.revision: 13
ms.openlocfilehash: ec441831f5e3231a44c9875d1b6d2bf6280a6965
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56844989"
---
# <a name="requesting-confirmation-from-cmdlets"></a><span data-ttu-id="a6fa2-102">Żądanie potwierdzenia z poziomu poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6fa2-102">Requesting Confirmation from Cmdlets</span></span>

<span data-ttu-id="a6fa2-103">Polecenia cmdlet powinny żądania potwierdzenia, gdy chcesz wprowadzić zmiany w systemie, który znajduje się poza środowisko Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-103">Cmdlets should request confirmation when they are about to make a change to the system that is outside of the Windows PowerShell environment.</span></span> <span data-ttu-id="a6fa2-104">Na przykład jeśli polecenie cmdlet jest dodać konto użytkownika lub zatrzymywanie procesu, polecenia cmdlet powinny wymagać potwierdzenia przez użytkownika, przed przechodzi.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-104">For example, if a cmdlet is about to add a user account or stop a process, the cmdlet should require confirmation from the user before it proceeds.</span></span> <span data-ttu-id="a6fa2-105">Z kolei jeśli polecenie cmdlet ma zostać zmieniona zmienną środowiska Windows PowerShell, polecenie cmdlet nie trzeba wymaga potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-105">In contrast, if a cmdlet is about to change a Windows PowerShell variable, the cmdlet does not need to require confirmation.</span></span>

<span data-ttu-id="a6fa2-106">W celu żądania potwierdzenia, polecenia cmdlet musi wskazywać, że obsługuje ona żądania potwierdzenia i musi on wywołać metodę [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) i [ System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metody (opcjonalnie) aby wyświetlić komunikat z żądaniem potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-106">In order to make a confirmation request, the cmdlet must indicate that it supports confirmation requests, and it must call the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) and [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) (optional) methods to display a confirmation request message.</span></span>

## <a name="supporting-confirmation-requests"></a><span data-ttu-id="a6fa2-107">Obsługa żądania potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="a6fa2-107">Supporting Confirmation Requests</span></span>

<span data-ttu-id="a6fa2-108">Obsługuje żądania potwierdzenia, polecenia cmdlet należy ustawić `SupportsShouldProcess` parametru atrybutu polecenia Cmdlet `true`.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-108">To support confirmation requests, the cmdlet must set the `SupportsShouldProcess` parameter of the Cmdlet attribute to `true`.</span></span> <span data-ttu-id="a6fa2-109">Dzięki temu `Confirm` i `WhatIf` parametry polecenia cmdlet, które są dostarczane przez środowisko Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-109">This enables the `Confirm` and `WhatIf` cmdlet parameters that are provided by Windows PowerShell.</span></span> <span data-ttu-id="a6fa2-110">`Confirm` Parametr umożliwia użytkownikowi kontrolowanie, czy jest wyświetlany żądania potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-110">The `Confirm` parameter allows the user to control whether the confirmation request is displayed.</span></span> <span data-ttu-id="a6fa2-111">`WhatIf` Parametr umożliwia użytkownikowi ustalić, czy polecenia cmdlet powinny wyświetlać komunikat lub wykonać jej działaniem.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-111">The `WhatIf` parameter allows the user to determine whether the cmdlet should display a message or perform its action.</span></span> <span data-ttu-id="a6fa2-112">Nie należy ręcznie dodawać `Confirm` i `WhatIf` parametry do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-112">Do not manually add the `Confirm` and `WhatIf` parameters to a cmdlet.</span></span>

<span data-ttu-id="a6fa2-113">Poniższy przykład pokazuje deklaracji atrybutu polecenia Cmdlet, który obsługuje żądania potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-113">The following example shows a Cmdlet attribute declaration that supports confirmation requests.</span></span>

```csharp
[Cmdlet(VerbsDiagnostic.Test, "RequestConfirmationTemplate1",
        SupportsShouldProcess = true)]
```

## <a name="calling-the-confirmation-request-methods"></a><span data-ttu-id="a6fa2-114">Wywoływanie metod żądania potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="a6fa2-114">Calling the Confirmation request methods</span></span>

<span data-ttu-id="a6fa2-115">W kodzie polecenia cmdlet, należy wywołać [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) metoda przed wykonaniem operacji, która zmienia się system.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-115">In the cmdlet code, call the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) method before the operation that changes the system is performed.</span></span> <span data-ttu-id="a6fa2-116">Projektowanie polecenia cmdlet, tak że jeśli to wywołanie zwraca wartość `false`, operacja nie jest wykonywane, i polecenia cmdlet przetwarza następnej operacji.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-116">Design the cmdlet so that if the call returns a value of `false`, the operation is not performed, and the cmdlet processes the next operation.</span></span>

## <a name="calling-the-shouldcontinue-method"></a><span data-ttu-id="a6fa2-117">Wywołanie metody ShouldContinue</span><span class="sxs-lookup"><span data-stu-id="a6fa2-117">Calling the ShouldContinue Method</span></span>

<span data-ttu-id="a6fa2-118">Większość poleceń cmdlet żądania potwierdzenia przy użyciu tylko [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) metody.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-118">Most cmdlets request confirmation using only the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) method.</span></span> <span data-ttu-id="a6fa2-119">Jednak w niektórych przypadkach mogą wymagać dodatkowe potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-119">However, some cases might require additional confirmation.</span></span> <span data-ttu-id="a6fa2-120">W takich przypadkach należy uzupełnić [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) wywołanie wywołaniem [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metody.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-120">For these cases, supplement the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) call with a call to the [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) method.</span></span> <span data-ttu-id="a6fa2-121">Pozwala to polecenie cmdlet lub dostawcę, aby bardziej precyzyjne kontrolowanie zakresu **tak na wszystko** odpowiedzi na monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-121">This allows the cmdlet or provider to more finely control the scope of the **Yes to all** response to the confirmation prompt.</span></span>

<span data-ttu-id="a6fa2-122">Jeśli wywołuje polecenie cmdlet [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metody, polecenia cmdlet należy również podać `Force` parametr przełącznika.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-122">If a cmdlet calls the [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) method, the cmdlet must also provide a `Force` switch parameter.</span></span> <span data-ttu-id="a6fa2-123">Jeśli użytkownik określi `Force` po użytkownik wywołuje polecenie cmdlet, polecenie cmdlet nadal powinny wywoływać [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess), należy pominąć, wywołanie metody, ale [ System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue).</span><span class="sxs-lookup"><span data-stu-id="a6fa2-123">If the user specifies `Force` when the user invokes the cmdlet, the cmdlet should still call [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess), but it should bypass the call to [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue).</span></span>

<span data-ttu-id="a6fa2-124">[System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) spowoduje zgłoszenie wyjątku, gdy jest wywoływana przy użyciu środowiska nieinterakcyjnych których użytkownik nie można wyświetlić monitu.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-124">[System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) will throw an exception when it is called from a non-interactive environment where the user cannot be prompted.</span></span> <span data-ttu-id="a6fa2-125">Dodawanie `Force` parametru gwarantuje, że można nadal można wykonać polecenia wywołana w środowisku nieinterakcyjnych.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-125">Adding a `Force` parameter ensures that the command can still be performed when it is invoked in a non-interactive environment.</span></span>

<span data-ttu-id="a6fa2-126">Poniższy przykład pokazuje sposób wywoływania [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) i [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue).</span><span class="sxs-lookup"><span data-stu-id="a6fa2-126">The following example shows how to call [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) and [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue).</span></span>

```csharp
if (ShouldProcess (...) )
{
  if (Force || ShouldContinue(...))
  {
     // Add code that performs the operation.
  }
}
```

<span data-ttu-id="a6fa2-127">Zachowanie [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) wywołania mogą się różnić w zależności od środowiska, w którym jest wywoływana polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-127">The behavior of a [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) call can vary depending on the environment in which the cmdlet is invoked.</span></span> <span data-ttu-id="a6fa2-128">Za pomocą wytycznych poprzedniego pomoże zapewnić spójne działania polecenia cmdlet z innymi poleceniami cmdlet, niezależnie od tego, w środowisku hosta.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-128">Using the previous guidelines will help ensure that the cmdlet behaves consistently with other cmdlets, regardless of the host environment.</span></span>

<span data-ttu-id="a6fa2-129">Na przykład wywołanie [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) metody, zobacz [jak żądania potwierdzenia](./how-to-request-confirmations.md).</span><span class="sxs-lookup"><span data-stu-id="a6fa2-129">For an example of calling the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) method, see [How to Request Confirmations](./how-to-request-confirmations.md).</span></span>

## <a name="specify-the-impact-level"></a><span data-ttu-id="a6fa2-130">Określ poziom wpływu</span><span class="sxs-lookup"><span data-stu-id="a6fa2-130">Specify the Impact Level</span></span>

<span data-ttu-id="a6fa2-131">Podczas tworzenia polecenia cmdlet, należy określić poziom wpływu (ważność) zmiany.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-131">When you create the cmdlet, specify the impact level (the severity) of the change.</span></span> <span data-ttu-id="a6fa2-132">Aby to zrobić, ustaw wartość `ConfirmImpact` parametru atrybutu polecenia Cmdlet na wysoki, średni lub niski.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-132">To do this, set the value of the `ConfirmImpact` parameter of the Cmdlet attribute to High, Medium, or Low.</span></span> <span data-ttu-id="a6fa2-133">Można określić wartość dla `ConfirmImpact` tylko gdy określasz również `SupportsShouldProcess` parametr polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-133">You can specify a value for `ConfirmImpact` only when you also specify the `SupportsShouldProcess` parameter for the cmdlet.</span></span>

<span data-ttu-id="a6fa2-134">Dla większości poleceń cmdlet, nie trzeba jawnie określić `ConfirmImpact`.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-134">For most cmdlets, you do not have to explicitly specify `ConfirmImpact`.</span></span>  <span data-ttu-id="a6fa2-135">Zamiast tego użyj ustawienia domyślnego parametru, która jest.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-135">Instead, use the default setting of the parameter, which is Medium.</span></span> <span data-ttu-id="a6fa2-136">Jeśli ustawisz `ConfirmImpact` na wysoki, operacja zostanie potwierdzone domyślnie.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-136">If you set `ConfirmImpact` to High, the operation will be confirmed by default.</span></span> <span data-ttu-id="a6fa2-137">Zarezerwuj to ustawienie dla bardzo uciążliwe akcje, takie jak ponowne formatowanie woluminu dysku twardego.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-137">Reserve this setting for highly disruptive actions, such as reformatting a hard-disk volume.</span></span>

## <a name="calling-non-confirmation-methods"></a><span data-ttu-id="a6fa2-138">Wywoływanie metod bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="a6fa2-138">Calling Non-Confirmation Methods</span></span>

<span data-ttu-id="a6fa2-139">Jeśli polecenia cmdlet lub dostawca musi wysłać wiadomość, ale nie żądania potwierdzenia, wywołując następujących trzech metod.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-139">If the cmdlet or provider must send a message but not request confirmation, it can call the following three methods.</span></span> <span data-ttu-id="a6fa2-140">Unikaj używania [System.Management.Automation.Cmdlet.Writeobject\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteObject) metodę, aby wysyłać komunikaty z tych typów, ponieważ [System.Management.Automation.Cmdlet.Writeobject\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteObject) to są dane wyjściowe zwykłe dane wyjściowe polecenia cmdlet lub dostawcy, który sprawia, że pisanie skryptów trudne.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-140">Avoid using the [System.Management.Automation.Cmdlet.Writeobject\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteObject) method to send messages of these types because [System.Management.Automation.Cmdlet.Writeobject\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteObject) output is intermingled with the normal output of your cmdlet or provider, which makes script writing difficult.</span></span>

- <span data-ttu-id="a6fa2-141">Uwaga użytkownika i kontynuować wykonywanie operacji, można wywołać polecenia cmdlet lub dostawca [System.Management.Automation.Cmdlet.Writewarning\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteWarning) metody.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-141">To caution the user and continue with the operation, the cmdlet or provider can call the [System.Management.Automation.Cmdlet.Writewarning\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteWarning) method.</span></span>

- <span data-ttu-id="a6fa2-142">Dodatkowe informacje, które użytkownik może pobrać za pomocą `Verbose` parametru polecenia cmdlet i dostawcy może wywołać [System.Management.Automation.Cmdlet.Writeverbose\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteVerbose) metody.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-142">To provide additional information that the user can retrieve using the `Verbose` parameter, the cmdlet or provider can call the [System.Management.Automation.Cmdlet.Writeverbose\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteVerbose) method.</span></span>

- <span data-ttu-id="a6fa2-143">Aby podać szczegóły na poziomie debugowania innym deweloperom lub pomocy technicznej, można wywołać polecenia cmdlet lub dostawca [System.Management.Automation.Cmdlet.Writedebug\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteDebug) metody.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-143">To provide debugging-level detail for other developers or for product support, the cmdlet or provider can call the [System.Management.Automation.Cmdlet.Writedebug\*](/dotnet/api/System.Management.Automation.Cmdlet.WriteDebug) method.</span></span> <span data-ttu-id="a6fa2-144">Użytkownik może pobrać te informacje przy użyciu `Debug` parametru.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-144">The user can retrieve this information using the `Debug` parameter.</span></span>

<span data-ttu-id="a6fa2-145">Polecenia cmdlet i dostawców należy najpierw wywołać następujące metody umożliwiające żądania potwierdzenia przed ich podjął próbę wykonania operacji, która zmienia systemu poza programu Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a6fa2-145">Cmdlets and providers first call the following methods to request confirmation before they attempt to perform an operation that changes a system outside of Windows PowerShell:</span></span>

- [<span data-ttu-id="a6fa2-146">System.Management.Automation.Cmdlet.Shouldprocess</span><span class="sxs-lookup"><span data-stu-id="a6fa2-146">System.Management.Automation.Cmdlet.Shouldprocess</span></span>](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess)

- [<span data-ttu-id="a6fa2-147">System.Management.Automation.Provider.Cmdletprovider.Shouldprocess</span><span class="sxs-lookup"><span data-stu-id="a6fa2-147">System.Management.Automation.Provider.Cmdletprovider.Shouldprocess</span></span>](/dotnet/api/System.Management.Automation.Provider.CmdletProvider.ShouldProcess)

<span data-ttu-id="a6fa2-148">Mogą to zrobić, wywołując [System.Management.Automation.Cmdlet.Shouldprocess](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) metody, która wyświetli monit o potwierdzenie operacji, w oparciu o sposób użytkownik wywołał polecenie.</span><span class="sxs-lookup"><span data-stu-id="a6fa2-148">They do so by calling the [System.Management.Automation.Cmdlet.Shouldprocess](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) method, which prompts the user to confirm the operation based on how the user invoked the command.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6fa2-149">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="a6fa2-149">See Also</span></span>

[<span data-ttu-id="a6fa2-150">Zapisywanie polecenia Cmdlet programu Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6fa2-150">Writing a Windows PowerShell Cmdlet</span></span>](./writing-a-windows-powershell-cmdlet.md)