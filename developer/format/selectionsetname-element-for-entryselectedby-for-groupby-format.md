---
title: Element SelectionSetName EntrySelectedBy dla grupowania (w formacie) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: d569c623-2277-49e3-933e-c26262b91cd5
caps.latest.revision: 6
ms.openlocfilehash: 69cd113c444b4e3c5dceabcdfddb439cd1376f6b
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56848811"
---
# <a name="selectionsetname-element-for-entryselectedby-for-groupby-format"></a><span data-ttu-id="93990-102">SelectionSetName, element — EntrySelectedBy, GroupBy (format)</span><span class="sxs-lookup"><span data-stu-id="93990-102">SelectionSetName Element for EntrySelectedBy for GroupBy (Format)</span></span>

<span data-ttu-id="93990-103">Określa zestaw obiektów platformy .NET dla wpisu listy.</span><span class="sxs-lookup"><span data-stu-id="93990-103">Specifies a set of .NET objects for the list entry.</span></span> <span data-ttu-id="93990-104">Nie ma żadnego limitu liczby zestawów wybór, które można określić dla wpisu.</span><span class="sxs-lookup"><span data-stu-id="93990-104">There is no limit to the number of selection sets that can be specified for an entry.</span></span> <span data-ttu-id="93990-105">Ten element jest używany podczas definiowania sposobu wyświetlania nowej grupy obiektów.</span><span class="sxs-lookup"><span data-stu-id="93990-105">This element is used when defining how a new group of objects is displayed.</span></span>

<span data-ttu-id="93990-106">— Element (w formacie) elementu ViewDefinitions (Format) widoku elementu (w formacie) GroupBy Element konfiguracji dla elementu formant niestandardowy widok (w formacie) dla elementu CustomEntries GroupBy (Format), formant niestandardowy elementu CustomEntry GroupBy (Format) Formant niestandardowy GroupBy (Format) elementu EntrySelectedBy CustomEntry GroupBy (Format) elementu SelectionSetName EntrySelectedBy dla grupowania (w formacie)</span><span class="sxs-lookup"><span data-stu-id="93990-106">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) GroupBy Element for View (Format) CustomControl Element for GroupBy (Format) CustomEntries Element for CustomControl for GroupBy (Format) CustomEntry Element for CustomControl for GroupBy (Format) EntrySelectedBy Element for CustomEntry for GroupBy (Format) SelectionSetName Element for EntrySelectedBy for GroupBy (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="93990-107">Składnia</span><span class="sxs-lookup"><span data-stu-id="93990-107">Syntax</span></span>

```xml
<SelectionSetName>NameofSelectionSet</SelectionSetName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="93990-108">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="93990-108">Attributes and Elements</span></span>

<span data-ttu-id="93990-109">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `SelectionSetName` elementu.</span><span class="sxs-lookup"><span data-stu-id="93990-109">The following sections describe attributes, child elements, and the parent element of the `SelectionSetName` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="93990-110">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="93990-110">Attributes</span></span>

<span data-ttu-id="93990-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="93990-111">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="93990-112">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="93990-112">Child Elements</span></span>

<span data-ttu-id="93990-113">Brak.</span><span class="sxs-lookup"><span data-stu-id="93990-113">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="93990-114">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="93990-114">Parent Elements</span></span>

|<span data-ttu-id="93990-115">Element</span><span class="sxs-lookup"><span data-stu-id="93990-115">Element</span></span>|<span data-ttu-id="93990-116">Opis</span><span class="sxs-lookup"><span data-stu-id="93990-116">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="93990-117">Element EntrySelectedBy CustomEntry dla grupowania (w formacie)</span><span class="sxs-lookup"><span data-stu-id="93990-117">EntrySelectedBy Element for CustomEntry for GroupBy (Format)</span></span>](./entryselectedby-element-for-customentry-for-groupby-format.md)|<span data-ttu-id="93990-118">Definiuje typy .NET, korzystające z tego wpisu niestandardowych lub warunek, który musi istnieć dla tego wpisu do użycia.</span><span class="sxs-lookup"><span data-stu-id="93990-118">Defines the .NET types that use this custom entry or the condition that must exist for this entry to be used.</span></span>|

## <a name="text-value"></a><span data-ttu-id="93990-119">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="93990-119">Text Value</span></span>

<span data-ttu-id="93990-120">Określ nazwę zestawu wyboru.</span><span class="sxs-lookup"><span data-stu-id="93990-120">Specify the name of the selection set.</span></span>

## <a name="remarks"></a><span data-ttu-id="93990-121">Uwagi</span><span class="sxs-lookup"><span data-stu-id="93990-121">Remarks</span></span>

<span data-ttu-id="93990-122">Każda definicja kontrolka niestandardowa musi mieć co najmniej jedną nazwę typu, wybór zestawu lub warunek wyboru.</span><span class="sxs-lookup"><span data-stu-id="93990-122">Each custom control definition must have at least one type name, selection set, or selection condition defined.</span></span>

<span data-ttu-id="93990-123">Wybór zestawy są zwykle używane zdefiniować grupy obiektów, które są używane w wielu widoków.</span><span class="sxs-lookup"><span data-stu-id="93990-123">Selection sets are typically used when you want to define a group of objects that are used in multiple views.</span></span> <span data-ttu-id="93990-124">Na przykład można utworzyć widoku tabeli i widok listy, aby uzyskać ten sam zestaw obiektów.</span><span class="sxs-lookup"><span data-stu-id="93990-124">For example, you may want to create a table view and a list view for the same set of objects.</span></span> <span data-ttu-id="93990-125">Aby uzyskać więcej informacji na temat definiowania zestawów wybór zobacz [Definiowanie ustawia wybór](./defining-selection-sets.md).</span><span class="sxs-lookup"><span data-stu-id="93990-125">For more information about defining selection sets, see [Defining Selection Sets](./defining-selection-sets.md).</span></span>

<span data-ttu-id="93990-126">Aby uzyskać więcej informacji o składnikach widoku kontrolki niestandardowej, zobacz [Tworzenie niestandardowych formantów](./creating-custom-controls.md).</span><span class="sxs-lookup"><span data-stu-id="93990-126">For more information about the components of a custom control view, see [Creating Custom Controls](./creating-custom-controls.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="93990-127">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="93990-127">See Also</span></span>

[<span data-ttu-id="93990-128">Element EntrySelectedBy CustomEntry dla grupowania (w formacie)</span><span class="sxs-lookup"><span data-stu-id="93990-128">EntrySelectedBy Element for CustomEntry for GroupBy (Format)</span></span>](./entryselectedby-element-for-customentry-for-groupby-format.md)

[<span data-ttu-id="93990-129">Tworzenie niestandardowych formantów</span><span class="sxs-lookup"><span data-stu-id="93990-129">Creating Custom Controls</span></span>](./creating-custom-controls.md)

[<span data-ttu-id="93990-130">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="93990-130">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)