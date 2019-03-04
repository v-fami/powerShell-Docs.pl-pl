---
title: Element PropertyName SelectionCondition dla EntrySelectedBy dla elementu ListControl (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 71c3f1f6-6fe2-42f1-8260-6974d3871748
caps.latest.revision: 11
ms.openlocfilehash: f857f5944b9e971215a06d6f5c39f7c22c6cf99f
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56844919"
---
# <a name="propertyname-element-for-selectioncondition-for-entryselectedby-for-listcontrol-format"></a><span data-ttu-id="b1dee-102">PropertyName, element — SelectionCondition, EntrySelectedBy, ListControl (format)</span><span class="sxs-lookup"><span data-stu-id="b1dee-102">PropertyName Element for SelectionCondition for EntrySelectedBy for ListControl (Format)</span></span>

<span data-ttu-id="b1dee-103">Określa właściwości platformy .NET, która wyzwala warunku.</span><span class="sxs-lookup"><span data-stu-id="b1dee-103">Specifies the .NET property that triggers the condition.</span></span> <span data-ttu-id="b1dee-104">Gdy ta właściwość jest obecny, lub jeśli wynikiem jego obliczenia `true`, warunek jest spełniony, i wpis na liście jest używany.</span><span class="sxs-lookup"><span data-stu-id="b1dee-104">When this property is present or when it evaluates to `true`, the condition is met, and the list entry is used.</span></span>

<span data-ttu-id="b1dee-105">— Element (Format) ViewDefinitions — Element (Format) widoku elementu (w formacie) elementu ListControl — Element (Format) elementu ListEntries (Format) ListEntry — Element (Format) EntrySelectedBy Element konfiguracji elementu SelectionCondition ListEntry (Format) EntrySelectedBy ListEntry (Format) elementu PropertyName SelectionCondition dla EmtrySelectedBy dla ListEntry (Format)</span><span class="sxs-lookup"><span data-stu-id="b1dee-105">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) ListControl Element (Format) ListEntries Element (Format) ListEntry Element (Format) EntrySelectedBy Element for ListEntry (Format) SelectionCondition Element for EntrySelectedBy for ListEntry (Format) PropertyName Element for SelectionCondition for EmtrySelectedBy for ListEntry (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1dee-106">Składnia</span><span class="sxs-lookup"><span data-stu-id="b1dee-106">Syntax</span></span>

```xml
<PropertyName>.NetTypeProperty</PropertyName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b1dee-107">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="b1dee-107">Attributes and Elements</span></span>

<span data-ttu-id="b1dee-108">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `PropertyName` elementu.</span><span class="sxs-lookup"><span data-stu-id="b1dee-108">The following sections describe attributes, child elements, and the parent element of the `PropertyName` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="b1dee-109">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="b1dee-109">Attributes</span></span>

<span data-ttu-id="b1dee-110">Brak.</span><span class="sxs-lookup"><span data-stu-id="b1dee-110">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="b1dee-111">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="b1dee-111">Child Elements</span></span>

<span data-ttu-id="b1dee-112">Brak.</span><span class="sxs-lookup"><span data-stu-id="b1dee-112">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="b1dee-113">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="b1dee-113">Parent Elements</span></span>

|<span data-ttu-id="b1dee-114">Element</span><span class="sxs-lookup"><span data-stu-id="b1dee-114">Element</span></span>|<span data-ttu-id="b1dee-115">Opis</span><span class="sxs-lookup"><span data-stu-id="b1dee-115">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="b1dee-116">Element SelectionCondition EntrySelectedBy dla ListEntry (Format)</span><span class="sxs-lookup"><span data-stu-id="b1dee-116">SelectionCondition Element for EntrySelectedBy for ListEntry (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-listcontrol-format.md)|<span data-ttu-id="b1dee-117">Określa warunek, który musi istnieć dla tego wpisu listy ma być używany.</span><span class="sxs-lookup"><span data-stu-id="b1dee-117">Defines the condition that must exist for this list entry to be used.</span></span>|

## <a name="text-value"></a><span data-ttu-id="b1dee-118">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="b1dee-118">Text Value</span></span>

<span data-ttu-id="b1dee-119">Określ nazwę właściwości platformy .NET.</span><span class="sxs-lookup"><span data-stu-id="b1dee-119">Specify the .NET property name.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1dee-120">Uwagi</span><span class="sxs-lookup"><span data-stu-id="b1dee-120">Remarks</span></span>

<span data-ttu-id="b1dee-121">Warunek wyboru należy określić co najmniej jedną właściwość name lub blok skryptu, ale nie można określić jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="b1dee-121">The selection condition must specify at least one property name or a script block, but cannot specify both.</span></span> <span data-ttu-id="b1dee-122">Aby uzyskać więcej informacji o sposobie używania warunków wyboru, zobacz [definiujący warunki dla, gdy wpis widoku lub służy element](./defining-conditions-for-displaying-data.md).</span><span class="sxs-lookup"><span data-stu-id="b1dee-122">For more information about how to use selection conditions, see [Defining Conditions for when a View Entry or Item is Used](./defining-conditions-for-displaying-data.md).</span></span>

<span data-ttu-id="b1dee-123">Aby uzyskać więcej informacji o innych składnikach widoku listy, zobacz [tworzenia widoku listy](./creating-a-list-view.md).</span><span class="sxs-lookup"><span data-stu-id="b1dee-123">For more information about other components of a list view, see [Creating List View](./creating-a-list-view.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b1dee-124">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="b1dee-124">See Also</span></span>

[<span data-ttu-id="b1dee-125">Tworzenie widoku listy</span><span class="sxs-lookup"><span data-stu-id="b1dee-125">Creating a List View</span></span>](./creating-a-list-view.md)

[<span data-ttu-id="b1dee-126">Definiowanie warunków podczas danych jest wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="b1dee-126">Defining Conditions for When Data is Displayed</span></span>](./defining-conditions-for-displaying-data.md)

[<span data-ttu-id="b1dee-127">Element ListEntry (Format)</span><span class="sxs-lookup"><span data-stu-id="b1dee-127">ListEntry Element (Format)</span></span>](./listentry-element-for-listcontrol-format.md)

[<span data-ttu-id="b1dee-128">Element ScriptBlock SelectionCondition dla EntrySelectedBy dla ListEntry (Format)</span><span class="sxs-lookup"><span data-stu-id="b1dee-128">ScriptBlock Element for SelectionCondition for EntrySelectedBy for ListEntry (Format)</span></span>](./scriptblock-element-for-selectioncondition-for-entryselectedby-for-listcontrol-format.md)

[<span data-ttu-id="b1dee-129">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="b1dee-129">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)