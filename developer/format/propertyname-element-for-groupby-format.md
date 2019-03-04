---
title: Element PropertyName GroupBy (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ddcecc46-ac75-43fa-b03a-802a68524ec3
caps.latest.revision: 10
ms.openlocfilehash: da6ac5abe7acbbee8f57b3e81529664f81800b86
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56851898"
---
# <a name="propertyname-element-for-groupby-format"></a><span data-ttu-id="8afd2-102">PropertyName, element — GroupBy (format)</span><span class="sxs-lookup"><span data-stu-id="8afd2-102">PropertyName Element for GroupBy (Format)</span></span>

<span data-ttu-id="8afd2-103">Określa właściwości platformy .NET, który uruchamia nową grupę, zmianie wartości.</span><span class="sxs-lookup"><span data-stu-id="8afd2-103">Specifies the .NET property that starts a new group whenever its value changes.</span></span>

<span data-ttu-id="8afd2-104">— Element (Format) ViewDefinitions — Element (Format) widoku elementu (w formacie) GroupBy Element konfiguracji dla elementu PropertyName widoku (w formacie) dla grupowania (w formacie)</span><span class="sxs-lookup"><span data-stu-id="8afd2-104">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) GroupBy Element for View (Format) PropertyName Element for GroupBy (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="8afd2-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="8afd2-105">Syntax</span></span>

```xml
<PropertyName>.NetTypeProperty</PropertyName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8afd2-106">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="8afd2-106">Attributes and Elements</span></span>

<span data-ttu-id="8afd2-107">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `PropertyName` elementu.</span><span class="sxs-lookup"><span data-stu-id="8afd2-107">The following sections describe attributes, child elements, and the parent element of the `PropertyName` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="8afd2-108">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="8afd2-108">Attributes</span></span>

<span data-ttu-id="8afd2-109">Brak.</span><span class="sxs-lookup"><span data-stu-id="8afd2-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="8afd2-110">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="8afd2-110">Child Elements</span></span>

<span data-ttu-id="8afd2-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="8afd2-111">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="8afd2-112">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="8afd2-112">Parent Elements</span></span>

|<span data-ttu-id="8afd2-113">Element</span><span class="sxs-lookup"><span data-stu-id="8afd2-113">Element</span></span>|<span data-ttu-id="8afd2-114">Opis</span><span class="sxs-lookup"><span data-stu-id="8afd2-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="8afd2-115">GroupBy — Element dla widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="8afd2-115">GroupBy Element for View (Format)</span></span>](./groupby-element-for-view-format.md)|<span data-ttu-id="8afd2-116">Definiuje sposób wyświetlania grupy obiektów platformy .NET.</span><span class="sxs-lookup"><span data-stu-id="8afd2-116">Defines how a group of .NET objects is displayed.</span></span>|

## <a name="text-value"></a><span data-ttu-id="8afd2-117">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="8afd2-117">Text Value</span></span>

<span data-ttu-id="8afd2-118">Określ nazwę właściwości platformy .NET.</span><span class="sxs-lookup"><span data-stu-id="8afd2-118">Specify the .NET property name.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afd2-119">Uwagi</span><span class="sxs-lookup"><span data-stu-id="8afd2-119">Remarks</span></span>

<span data-ttu-id="8afd2-120">Rozpoczyna się nowej grupy programu Windows PowerShell, zawsze wtedy, gdy zmieni się wartość tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="8afd2-120">Windows PowerShell starts a new group whenever the value of this property changes.</span></span>

<span data-ttu-id="8afd2-121">Gdy ten element jest określony, nie można określić [ScriptBlock](./scriptblock-element-for-groupby-format.md) element, aby rozpocząć nową grupę.</span><span class="sxs-lookup"><span data-stu-id="8afd2-121">When this element is specified, you cannot specify the [ScriptBlock](./scriptblock-element-for-groupby-format.md) element to start a new group.</span></span>

## <a name="example"></a><span data-ttu-id="8afd2-122">Przykład</span><span class="sxs-lookup"><span data-stu-id="8afd2-122">Example</span></span>

<span data-ttu-id="8afd2-123">Poniższy przykład pokazuje, jak uruchomić nową grupę, po zmianie wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="8afd2-123">The following example shows how to start a new group when the value of a property changes.</span></span>

```xml
<GroupBy>
  <Label>Service Type</Label>
  <PropertyName>ServiceType</PropertyName>
</GroupBy>

```

<span data-ttu-id="8afd2-124">Na przykład kompletny plik formatowania, który zawiera ten element zobacz [szerokie (grupowania)](./wide-view-groupby.md).</span><span class="sxs-lookup"><span data-stu-id="8afd2-124">For an example of a complete formatting file that includes this element, see [Wide View (GroupBy)](./wide-view-groupby.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8afd2-125">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="8afd2-125">See Also</span></span>

[<span data-ttu-id="8afd2-126">GroupBy — Element dla widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="8afd2-126">GroupBy Element for View (Format)</span></span>](./groupby-element-for-view-format.md)

[<span data-ttu-id="8afd2-127">Element ScriptBlock GroupBy (Format)</span><span class="sxs-lookup"><span data-stu-id="8afd2-127">ScriptBlock Element for GroupBy (Format)</span></span>](./scriptblock-element-for-groupby-format.md)

[<span data-ttu-id="8afd2-128">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="8afd2-128">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)