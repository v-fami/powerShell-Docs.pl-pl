---
ms.date: 06/12/2017
keywords: DSC, powershell, konfiguracja, ustawienia
title: Metoda ResourceSet klasy MSFT_DSCLocalConfigurationManager
ms.openlocfilehash: 2712b7ff0a19e643c1f343d436c084f8970c9dd4
ms.sourcegitcommit: e04292a9c10de9a8391d529b7f7aa3753b362dbe
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/04/2019
ms.locfileid: "54048446"
---
# <a name="resourceset-method-of-the-msftdsclocalconfigurationmanager-class"></a>Metoda ResourceSet klasy MSFT_DSCLocalConfigurationManager

Bezpośrednio wywołuje **ustaw** metod zasobów DSC.

## <a name="syntax"></a>Składnia

```mof
uint32 ResourceSet(
  [in]  string  ResourceType,
  [in]  string  ModuleName,
  [in]  uint8   resourceProperty[],
  [out] boolean RebootRequired
);
```

## <a name="parameters"></a>Parametry

*Typ zasobu* \[w\] nazwę zasobu do wywołania.

*ModuleName* \[w\] nazwę modułu, który zawiera zasób do wywołania.

*resourceProperty* \[w\] Określa nazwę właściwości zasobów i jego wartość w tabeli wyznaczania wartości skrótu jako klucza i wartości, odpowiednio. Użyj [Get-DscResource](/powershell/module/PSDesiredStateConfiguration/Get-DscResource) polecenia cmdlet, aby odnaleźć właściwości zasobów i ich typy.

*RebootRequired* \[się\] przy powrocie, właściwość ta jest równa **true** Jeśli węzeł docelowy musi zostać przeprowadzony ponowny rozruch.

## <a name="return-value"></a>Wartość zwracana

Zwraca wartość zero w przypadku powodzenia; w przeciwnym razie zwraca kod błędu.

## <a name="remarks"></a>Uwagi

Jest to metoda statyczna.

## <a name="requirements"></a>Wymagania

**PLIK MOF:** DscCore.mof

**Namespace**: Root\Microsoft\Windows\DesiredStateConfiguration

## <a name="see-also"></a>Zobacz też

[**MSFT_DSCLocalConfigurationManager**](msft-dsclocalconfigurationmanager.md)