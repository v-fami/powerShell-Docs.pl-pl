---
title: Przykładowy kod RunSpace07 | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8ad306d9-45c2-4d55-8e64-fdcba43402c5
caps.latest.revision: 6
ms.openlocfilehash: 064e7d7ea2ee173bbcdd75a9f3a6c12582afe17b
ms.sourcegitcommit: 69abc5ad16e5dd29ddfb1853e266a4bfd1d59d59
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/05/2019
ms.locfileid: "57429645"
---
# <a name="runspace07-code-sample"></a>Przykładowy kod RunSpace07

Poniżej przedstawiono kod źródłowy dla przykładowych Runspace07 opisanego w [tworzenia aplikacji, dodaje poleceń konsoli dla potoku](http://msdn.microsoft.com/en-us/01eb7808-e97b-4905-80be-9e2fa38c262e). Ta przykładowa aplikacja tworzy obszar działania, tworzy potok, dodaje dwa polecenia do potoku i następnie uruchamia potok. Polecenia dodane do potoku znajdują się `Get-Process` i `Measure-Object` polecenia cmdlet.

> [!NOTE]
> Możesz pobrać C# pliku źródłowego (runspace07.cs) przy użyciu programu Microsoft Windows oprogramowania Development Kit dla Windows Vista i programu Microsoft .NET Framework 3.0 Runtime składników. Aby uzyskać instrukcje pobierania, zobacz [jak instalowanie programu Windows PowerShell i pobierania zestawu SDK programu Windows PowerShell](/powershell/developer/installing-the-windows-powershell-sdk).
>
> Pliki pobrane źródło są dostępne w  **\<przykłady programu PowerShell >** katalogu.

## <a name="code-sample"></a>Przykładowy kod

[!code-csharp[Runspace07.cs](../../powershell-sdk-samples/SDK-2.0/csharp/Runspace07/Runspace07.cs#L11-L108 "Runspace07.cs")]

## <a name="see-also"></a>Zobacz też

[Windows PowerShell przewodnik](./windows-powershell-programmer-s-guide.md)

[Zestaw SDK programu Windows PowerShell](../windows-powershell-reference.md)