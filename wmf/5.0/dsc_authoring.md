---
ms.date: 06/12/2017
keywords: wmf,powershell,setup
ms.openlocfilehash: ec4ae8e4b2ef0ec226cb75607f7aaf34b48f6b76
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "55688763"
---
# <a name="authoring-improvements-using-powershell-ise"></a>Ulepszenia tworzenia przy użyciu środowiska PowerShell ISE

Tworzenie konfiguracji DSC w środowisku Windows PowerShell ISE jest znacznie łatwiejsze, dziękuję do następujące ulepszenia:

- Wyświetla listę wszystkich zasobów DSC w ramach **konfiguracji** bloku lub **węzła** bloku, wprowadzając **Ctrl + spacja** w pustym wierszu znajdujący się w nim.
- Automatyczne uzupełnianie na właściwościach zasobów, które są **wyliczenie** typu.
- Automatyczne uzupełnianie na **DependsOn** własności zasobów DSC, w oparciu o innych wystąpień zasobów w konfiguracji.
- Lepsze uzupełniania po naciśnięciu tabulatora wartości właściwości zasobu.

**Uwaga:** Pusty ciąg wartości właściwości zasobu musi mieć, zanim użyjesz Ctrl + spacja, aby wyświetlić listę opcji. Naciśnięcie klawisza **kartę** cykle za pomocą opcji.
