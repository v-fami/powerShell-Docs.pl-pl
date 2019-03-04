---
title: Jak utworzyć żądanie potwierdzenia | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f24f77d5-e224-4b62-b128-535e045d333e
caps.latest.revision: 9
ms.openlocfilehash: 8cfbcacf93733667ffba63a252c86518c0919b57
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56851996"
---
# <a name="how-to-request-confirmations"></a><span data-ttu-id="475ee-102">Jak tworzyć żądania potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="475ee-102">How to Request Confirmations</span></span>

<span data-ttu-id="475ee-103">W tym przykładzie przedstawiono sposób wywoływania [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) i [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metody żądania potwierdzenia z Użytkownik, przed wykonaniem akcji.</span><span class="sxs-lookup"><span data-stu-id="475ee-103">This example shows how to call the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) and [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) methods to request confirmations from the user before an action is taken.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="475ee-104">Aby uzyskać więcej informacji na temat tych żądań obsługi środowiska Windows PowerShell, zobacz [żądania potwierdzenia](./requesting-confirmation-from-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="475ee-104">For more information about how Windows PowerShell handles these requests, see [Requesting Confirmation](./requesting-confirmation-from-cmdlets.md).</span></span>

## <a name="to-request-confirmation"></a><span data-ttu-id="475ee-105">Aby zażądać potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="475ee-105">To request confirmation</span></span>

1. <span data-ttu-id="475ee-106">Upewnij się, że `SupportsShouldProcess` parametru polecenia Cmdlet atrybutu jest równa `true`.</span><span class="sxs-lookup"><span data-stu-id="475ee-106">Ensure that the `SupportsShouldProcess` parameter of the Cmdlet attribute is set to `true`.</span></span> <span data-ttu-id="475ee-107">(Dla funkcji jest to parametr atrybut CmdletBinding).</span><span class="sxs-lookup"><span data-stu-id="475ee-107">(For functions this is a parameter of the CmdletBinding attribute.)</span></span>

    ```csharp
    [Cmdlet(VerbsDiagnostic.Test, "RequestConfirmationTemplate1",
            SupportsShouldProcess = true)]
    ```

2. <span data-ttu-id="475ee-108">Dodaj `Force` parametru do Twojego polecenia cmdlet, aby użytkownik może zastąpić żądania potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="475ee-108">Add a `Force` parameter to your cmdlet so that the user can override a confirmation request.</span></span>

    ```csharp
    [Parameter()]
    public SwitchParameter Force
    {
      get { return force; }
      set { force = value; }
    }
    private bool force;
    ```

3. <span data-ttu-id="475ee-109">Dodaj `if` instrukcję, która używa wartość zwracaną przez [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) metodę, aby określić, czy [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metoda jest wywoływana.</span><span class="sxs-lookup"><span data-stu-id="475ee-109">Add an `if` statement that uses the return value of the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) method to determine if the [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) method is called.</span></span>

4. <span data-ttu-id="475ee-110">Dodaj drugą `if` instrukcję, która używa wartość zwracaną przez [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metody i wartości `Force` parametru, aby określić, czy operacja powinna być wykonywane.</span><span class="sxs-lookup"><span data-stu-id="475ee-110">Add a second `if` statement that uses the return value of the [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) method and the value of the `Force` parameter to determine whether the operation should be performed.</span></span>

## <a name="example"></a><span data-ttu-id="475ee-111">Przykład</span><span class="sxs-lookup"><span data-stu-id="475ee-111">Example</span></span>

<span data-ttu-id="475ee-112">W poniższym przykładzie kodu [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) i [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) metody są wywoływane z poziomu zastępowania [System.Management.Automation.Cmdlet.Processrecord\*](/dotnet/api/System.Management.Automation.Cmdlet.ProcessRecord) metody.</span><span class="sxs-lookup"><span data-stu-id="475ee-112">In the following code example, the [System.Management.Automation.Cmdlet.Shouldprocess\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldProcess) and [System.Management.Automation.Cmdlet.Shouldcontinue\*](/dotnet/api/System.Management.Automation.Cmdlet.ShouldContinue) methods are called from within the override of the [System.Management.Automation.Cmdlet.Processrecord\*](/dotnet/api/System.Management.Automation.Cmdlet.ProcessRecord) method.</span></span> <span data-ttu-id="475ee-113">Jednak te metody można również wywołać z innych danych wejściowych metody przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="475ee-113">However, you can also call these methods from the other input processing methods.</span></span>

```csharp
protected override void ProcessRecord()
{
  if (ShouldProcess("ShouldProcess target"))
  {
    if (Force || ShouldContinue("", ""))
    {
      // Add code that performs the operation.
    }
  }
}
```

## <a name="see-also"></a><span data-ttu-id="475ee-114">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="475ee-114">See Also</span></span>

[<span data-ttu-id="475ee-115">Zapisywanie polecenia Cmdlet programu Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="475ee-115">Writing a Windows PowerShell Cmdlet</span></span>](./writing-a-windows-powershell-cmdlet.md)