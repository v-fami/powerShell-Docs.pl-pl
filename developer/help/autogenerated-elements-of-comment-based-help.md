---
title: Wygenerowany automatycznie elementy Pomoc oparta na komentarzach | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/12/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 2a7098fe-0854-4fbb-83e9-073c20b299c7
caps.latest.revision: 4
ms.openlocfilehash: 572a80c72efd29b5c6117b1ea16bf75998b3c700
ms.sourcegitcommit: 5990f04b8042ef2d8e571bec6d5b051e64c9921c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/12/2019
ms.locfileid: "57794369"
---
# <a name="autogenerated-elements-of-comment-based-help"></a>Automatycznie generowane elementy pomocy opartej na komentarzach

`Get-Help` Polecenia cmdlet automatycznie generuje wiele elementów oparta na komentarzach tematu. Te elementy wygenerowany automatycznie wprowadzić oparta na komentarzach pomocy wyglądać bardzo podobnie pomocy, który jest generowany na podstawie plików XML.

## <a name="autogenerated-elements"></a>Wygenerowany automatycznie elementów

`Get-Help` Polecenia cmdlet automatycznie generuje następujące elementy tematu Pomocy. Nie można edytować tych elementów bezpośrednio, ale w wielu przypadkach można zmienić wyniki, zmieniając źródła tego elementu.

**Nazwa** sekcji nazwę tematu pomocy funkcji jest pobierana z nazwą funkcji w definicji funkcji. Nazwa tematu Pomocy skryptu jest pobierana z nazwę pliku skryptu. Aby zmienić nazwę lub jej wielkość liter, Zmień definicję funkcji lub nazwę pliku skryptu.

**Składnia** składni części tematu Pomocy jest generowany na podstawie listę parametrów dla instrukcji Param funkcji lub skryptu. Aby dodać szczegóły do składni tematu pomocy, takich jak .NET Framework typu parametru, należy dodać szczegóły do listy parametrów. Jeśli nie określisz typ parametru typu "Object" jest wstawiany jako wartość domyślną.

**Lista parametrów** parametrów na części tematu Pomocy jest generowana z listę parametrów dla funkcji lub skrypcie i opisy, które możesz dodać za pomocą `.Parameters` — słowo kluczowe lub komentarze na liście parametrów.

Parametry są wyświetlane w sekcji parametrów w tej samej kolejności, które pojawiają się na liście parametrów. Pisownię i wielkość liter nazwy parametrów, również jest pobierana z listy parametrów; nie ma wpływu określonej przez nazwę parametru `.Parameter` — słowo kluczowe.

**Wspólne parametry** wspólne parametry są dodawane do składni i listą parametrów tematu pomocy, nawet jeśli nie mają wpływu. Aby uzyskać więcej informacji o typowych parametrach, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

**Tabela atrybutów parametr** 
 `Get-Help` generuje tabeli atrybuty parametru, który pojawia się podczas korzystania z parametru pełnej lub parametr o `Get-Help`. Wymagane wartości, położenie i domyślne wartości atrybutów jest pobierana z Składnia funkcji lub skrypcie.

**Uwagi** sekcji uwag tematu Pomocy jest generowana automatycznie na podstawie nazwy funkcji lub skrypcie. Nie można zmienić lub mają wpływ na jego zawartości.
