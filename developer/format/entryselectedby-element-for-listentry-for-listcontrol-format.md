---
title: Element EntrySelectedBy ListEntry dla elementu ListControl (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0f7a74e9-764d-46ce-ab8e-8b9314ce1659
caps.latest.revision: 12
ms.openlocfilehash: 723619e67612b859d0acbab37eecd82141adf923
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56846074"
---
# <a name="entryselectedby-element-for-listentry-for-listcontrol-format"></a><span data-ttu-id="d81db-102">EntrySelectedBy, element — ListEntry, ListControl (format)</span><span class="sxs-lookup"><span data-stu-id="d81db-102">EntrySelectedBy Element for ListEntry for ListControl (Format)</span></span>

<span data-ttu-id="d81db-103">Definiuje typy .NET, które używają tej definicji widoku listy lub warunek, który musi istnieć, aby ta definicja ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d81db-103">Defines the .NET types that use this list view definition or the condition that must exist for this definition to be used.</span></span> <span data-ttu-id="d81db-104">W większości przypadków tylko jedną definicję, jest wymagany dla widoku listy.</span><span class="sxs-lookup"><span data-stu-id="d81db-104">In most cases only one definition is needed for a list view.</span></span> <span data-ttu-id="d81db-105">Może jednak zapewniać wiele definicji widoku listy, jeśli chcesz użyć tego samego widoku listy do wyświetlenia różnych danych do różnych obiektów.</span><span class="sxs-lookup"><span data-stu-id="d81db-105">However, you can provide multiple definitions for the list view if you want to use the same list view to display different data for different objects.</span></span>

<span data-ttu-id="d81db-106">— Element (w formacie) elementu ViewDefinitions (Format) widoku elementu (w formacie) elementu ListControl — Element (Format) ListEntries Element konfiguracji elementu ListControl (Format) elementu ListEntry ListEntry elementu EntrySelectedBy elementu ListControl (Format) ListEntry dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-106">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) ListControl Element (Format) ListEntries Element for ListControl (Format) ListEntry Element for ListEntry for ListControl (Format) EntrySelectedBy Element for ListEntry for ListControl (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="d81db-107">Składnia</span><span class="sxs-lookup"><span data-stu-id="d81db-107">Syntax</span></span>

```xml
<EntrySelectedBy>
  <TypeName>Nameof.NetType</TypeName>
  <SelectionSetName>NameofSelectionSet</SelectionSetName>
  <SelectionCondition>...</SelectionCondition>
</EntrySelectedBy>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d81db-108">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="d81db-108">Attributes and Elements</span></span>

<span data-ttu-id="d81db-109">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `EntrySelectedBy` elementu.</span><span class="sxs-lookup"><span data-stu-id="d81db-109">The following sections describe the attributes, child elements, and the parent element of the `EntrySelectedBy` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="d81db-110">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="d81db-110">Attributes</span></span>

<span data-ttu-id="d81db-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="d81db-111">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="d81db-112">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="d81db-112">Child Elements</span></span>

|<span data-ttu-id="d81db-113">Element</span><span class="sxs-lookup"><span data-stu-id="d81db-113">Element</span></span>|<span data-ttu-id="d81db-114">Opis</span><span class="sxs-lookup"><span data-stu-id="d81db-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="d81db-115">Element SelectionCondition EntrySelectedBy dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-115">SelectionCondition Element for EntrySelectedBy for ListControl  (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-listcontrol-format.md)|<span data-ttu-id="d81db-116">Element opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d81db-116">Optional element.</span></span><br /><br /> <span data-ttu-id="d81db-117">Określa warunek, który musi istnieć dla tej definicji widoku listy ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d81db-117">Defines the condition that must exist for this list view definition to be used.</span></span>|
|[<span data-ttu-id="d81db-118">Element SelectionSetName EnrtySelectedBy dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-118">SelectionSetName Element for EnrtySelectedBy for ListControl (Format)</span></span>](./selectionsetname-element-for-entryselectedby-for-listcontrol-format.md)|<span data-ttu-id="d81db-119">Element opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d81db-119">Optional element.</span></span><br /><br /> <span data-ttu-id="d81db-120">Określa zestaw typów .NET, które używają tej definicji widoku listy.</span><span class="sxs-lookup"><span data-stu-id="d81db-120">Specifies a set of .NET types that use this list view definition.</span></span>|
|[<span data-ttu-id="d81db-121">Element TypeName dla EntrySelectedBy dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-121">TypeName Element for EntrySelectedBy for ListControl (Format)</span></span>](./typename-element-for-entryselectedby-for-listcontrol-format.md)|<span data-ttu-id="d81db-122">Element opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d81db-122">Optional element.</span></span><br /><br /> <span data-ttu-id="d81db-123">Określa typ architektury .NET, która używa tej definicji widoku listy.</span><span class="sxs-lookup"><span data-stu-id="d81db-123">Specifies a .NET type that uses this list view definition.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="d81db-124">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="d81db-124">Parent Elements</span></span>

|<span data-ttu-id="d81db-125">Element</span><span class="sxs-lookup"><span data-stu-id="d81db-125">Element</span></span>|<span data-ttu-id="d81db-126">Opis</span><span class="sxs-lookup"><span data-stu-id="d81db-126">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="d81db-127">Element ListEntry dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-127">ListEntry Element for ListControl (Format)</span></span>](./listentry-element-for-listcontrol-format.md)|<span data-ttu-id="d81db-128">Definiuje sposób wyświetlania wierszy listy.</span><span class="sxs-lookup"><span data-stu-id="d81db-128">Defines how the rows of the list are displayed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d81db-129">Uwagi</span><span class="sxs-lookup"><span data-stu-id="d81db-129">Remarks</span></span>

<span data-ttu-id="d81db-130">Należy określić co najmniej jeden typ, wybór zestawu lub warunek wyboru definicji widoku listy.</span><span class="sxs-lookup"><span data-stu-id="d81db-130">You must specify at least one type, selection set, or selection condition for a list view definition.</span></span> <span data-ttu-id="d81db-131">Jest nieograniczona maksymalną liczbę elementów podrzędnych, które są dostępne.</span><span class="sxs-lookup"><span data-stu-id="d81db-131">There is no maximum limit to the number of child elements that you can use.</span></span>

<span data-ttu-id="d81db-132">Wybór warunki są używane do definiowania warunek, który musi istnieć dla definicji, który ma być używany, na przykład jeśli obiekt ma określoną właściwość lub wartość określoną właściwość lub skrypt daje w wyniku `true`.</span><span class="sxs-lookup"><span data-stu-id="d81db-132">Selection conditions are used to define a condition that must exist for the definition to be used, such as when an object has a specific property or that a specific property value or script evaluates to `true`.</span></span> <span data-ttu-id="d81db-133">Aby uzyskać więcej informacji o warunkach wyboru, zobacz [warunki określające gdy dane są wyświetlane](./defining-conditions-for-displaying-data.md).</span><span class="sxs-lookup"><span data-stu-id="d81db-133">For more information about selection conditions, see [Defining Conditions for when Data is displayed](./defining-conditions-for-displaying-data.md).</span></span>

<span data-ttu-id="d81db-134">Aby uzyskać więcej informacji o składnikach w widoku listy, zobacz [tworzenia widoku listy](./creating-a-list-view.md).</span><span class="sxs-lookup"><span data-stu-id="d81db-134">For more information about the components of a list view, see [Creating a List View](./creating-a-list-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="d81db-135">Przykład</span><span class="sxs-lookup"><span data-stu-id="d81db-135">Example</span></span>

<span data-ttu-id="d81db-136">Poniższy przykład pokazuje jak zdefiniować obiektów w celu wyświetlenia listy za pomocą nazwy typu platformy .NET.</span><span class="sxs-lookup"><span data-stu-id="d81db-136">The following example shows how to define the objects for a list view using their .NET type name.</span></span>

```xml
<ListEntry>
  <EntrySelectedBy>
    <TypeName>NameofDotNetType</TypeName>>
  </EntrySelectedBy>
</ListEntry>
```

## <a name="see-also"></a><span data-ttu-id="d81db-137">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="d81db-137">See Also</span></span>

[<span data-ttu-id="d81db-138">Element ListEntry dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-138">ListEntry Element for ListControl (Format)</span></span>](./listentry-element-for-listcontrol-format.md)

[<span data-ttu-id="d81db-139">Element SelectionCondition EntrySelectedBy dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-139">SelectionCondition Element for EntrySelectedBy for ListControl (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-listcontrol-format.md)

[<span data-ttu-id="d81db-140">Element SelectionSetName EnrtySelectedBy dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-140">SelectionSetName Element for EnrtySelectedBy for ListControl (Format)</span></span>](./selectionsetname-element-for-entryselectedby-for-listcontrol-format.md)

[<span data-ttu-id="d81db-141">Element TypeName dla EntrySelectedBy dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="d81db-141">TypeName Element for EntrySelectedBy for ListControl (Format)</span></span>](./typename-element-for-entryselectedby-for-listcontrol-format.md)

[<span data-ttu-id="d81db-142">Tworzenie widoku listy</span><span class="sxs-lookup"><span data-stu-id="d81db-142">Creating a List View</span></span>](./creating-a-list-view.md)

[<span data-ttu-id="d81db-143">Definiowanie warunków, gdy dane są wyświetlane</span><span class="sxs-lookup"><span data-stu-id="d81db-143">Defining Conditions for when Data is Displayed</span></span>](./defining-conditions-for-displaying-data.md)

[<span data-ttu-id="d81db-144">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="d81db-144">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)