---
ms.date: 06/12/2017
contributor: manikb
keywords: Galeria, programu powershell, polecenie cmdlet, psget
title: Rozwiązywanie problemów z poleceń cmdlet
ms.openlocfilehash: f5cd9c0cc23fef5891bf02c10b6541ab0f9d418a
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "55686551"
---
# <a name="troubleshooting-cmdlets"></a>Rozwiązywanie problemów z poleceń cmdlet

## <a name="how-to-resolve-warning-package-your-package-name-failed-to-download-issue"></a>Jak rozwiązać problem "ostrzeżenia: Nie można pobrać pakietu "nazwą pakietu" "problem

Zostanie zgłoszone, `Install-Module` lub `Update-Module` czasami kończy się niepowodzeniem na niektórych komputerach.
Na podstawie badania, jest coś, co można zrobić za pomocą połączenia sieci.
Ostatnio Zaktualizowaliśmy dostawcy NuGet, aby je niezawodnie umożliwia pobranie pakietów.
Możesz postępuj zgodnie z poniższymi instrukcjami, aby zainstalować najnowszą wersję programu dostawcy NuGet i następnie instalowanie lub aktualizowanie modułu.
Na przykład poniżej użyjemy modułu "Azure".

```powershell
Install-PackageProvider NuGet -MinimumVersion 2.8.5.206 -Force
Launch new PowerShell Console
Update-Module Azure -Verbose
```
