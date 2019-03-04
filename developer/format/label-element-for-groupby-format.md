---
title: Etykieta elementu dla grupowania (w formacie) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 3351d237-e8c2-4ec5-9500-4eceadb407c2
caps.latest.revision: 11
ms.openlocfilehash: e7158711c60d13c745bbdfab9b1b9fc7d98b34e2
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56851289"
---
# <a name="label-element-for-groupby-format"></a><span data-ttu-id="68832-102">Label, element — GroupBy (format)</span><span class="sxs-lookup"><span data-stu-id="68832-102">Label Element for GroupBy (Format)</span></span>

<span data-ttu-id="68832-103">Określa etykietę, która jest wyświetlana, gdy zostanie osiągnięty nowej grupy.</span><span class="sxs-lookup"><span data-stu-id="68832-103">Specifies a label that is displayed when a new group is encountered.</span></span>

<span data-ttu-id="68832-104">— Element (Format) elementu ViewDefinitions (Format) widoku elementu (w formacie) GroupBy Element konfiguracji dla elementu Label widoku (w formacie) dla grupowania (w formacie)</span><span class="sxs-lookup"><span data-stu-id="68832-104">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) GroupBy Element for View (Format) Label Element for GroupBy (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="68832-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="68832-105">Syntax</span></span>

```xml
<Label>DisplayedLabel</Label>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="68832-106">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="68832-106">Attributes and Elements</span></span>

<span data-ttu-id="68832-107">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `Label` elementu.</span><span class="sxs-lookup"><span data-stu-id="68832-107">The following sections describe the attributes, child elements, and parent element of the `Label` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="68832-108">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="68832-108">Attributes</span></span>

<span data-ttu-id="68832-109">Brak.</span><span class="sxs-lookup"><span data-stu-id="68832-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="68832-110">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="68832-110">Child Elements</span></span>

<span data-ttu-id="68832-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="68832-111">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="68832-112">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="68832-112">Parent Elements</span></span>

|<span data-ttu-id="68832-113">Element</span><span class="sxs-lookup"><span data-stu-id="68832-113">Element</span></span>|<span data-ttu-id="68832-114">Opis</span><span class="sxs-lookup"><span data-stu-id="68832-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="68832-115">GroupBy — Element dla widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="68832-115">GroupBy Element for View (Format)</span></span>](./groupby-element-for-view-format.md)|<span data-ttu-id="68832-116">Definiuje sposób wyświetlania nowej grupy obiektów.</span><span class="sxs-lookup"><span data-stu-id="68832-116">Defines how a new group of objects is displayed.</span></span>|

## <a name="text-value"></a><span data-ttu-id="68832-117">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="68832-117">Text Value</span></span>

<span data-ttu-id="68832-118">Podaj tekst, który jest wyświetlany zawsze wtedy, gdy napotka programu Windows PowerShell, nową właściwość lub wartość skryptu.</span><span class="sxs-lookup"><span data-stu-id="68832-118">Specify the text that is displayed whenever Windows PowerShell encounters a new property or script value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68832-119">Uwagi</span><span class="sxs-lookup"><span data-stu-id="68832-119">Remarks</span></span>

<span data-ttu-id="68832-120">Oprócz tekstu określonego przez ten element programu Windows PowerShell Wyświetla nową wartość, która rozpoczyna się w grupie, a następnie dodaje pusty wiersz, przed i po niej.</span><span class="sxs-lookup"><span data-stu-id="68832-120">In addition to the text specified by this element, Windows PowerShell displays the new value that starts the group, and adds a blank line before and after the group.</span></span>

## <a name="example"></a><span data-ttu-id="68832-121">Przykład</span><span class="sxs-lookup"><span data-stu-id="68832-121">Example</span></span>

<span data-ttu-id="68832-122">Poniższy przykład przedstawia etykietę dla nowej grupy.</span><span class="sxs-lookup"><span data-stu-id="68832-122">The following example shows the label for a new group.</span></span> <span data-ttu-id="68832-123">Wyświetlanej etykiety powinien wyglądać mniej więcej tak: `Service Type: NewValueofProperty`</span><span class="sxs-lookup"><span data-stu-id="68832-123">The displayed label would look similar to this: `Service Type: NewValueofProperty`</span></span>

```xml
<GroupBy>
  <Label>Service Type</Label>
  <PropertyName>ServiceType</PropertyName>
</GroupBy>

```

<span data-ttu-id="68832-124">Na przykład kompletny plik formatowania, który zawiera ten element zobacz [szerokie (grupowania)](./wide-view-groupby.md).</span><span class="sxs-lookup"><span data-stu-id="68832-124">For an example of a complete formatting file that includes this element, see [Wide View (GroupBy)](./wide-view-groupby.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="68832-125">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="68832-125">See Also</span></span>

[<span data-ttu-id="68832-126">GroupBy — Element dla widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="68832-126">GroupBy Element for View (Format)</span></span>](./groupby-element-for-view-format.md)

[<span data-ttu-id="68832-127">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="68832-127">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)