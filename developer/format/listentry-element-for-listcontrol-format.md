---
title: Element ListEntry dla elementu ListControl (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6d16bca8-d025-432d-aa84-8b607b8af3ae
caps.latest.revision: 12
ms.openlocfilehash: 1a3bafd4ca94aee70e869c699f7a4ef8befc5511
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56851184"
---
# <a name="listentry-element-for-listcontrol-format"></a><span data-ttu-id="e7a07-102">ListEntry, element — ListControl (format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-102">ListEntry Element for ListControl (Format)</span></span>

<span data-ttu-id="e7a07-103">Zawiera definicję widoku listy.</span><span class="sxs-lookup"><span data-stu-id="e7a07-103">Provides a definition of the list view.</span></span>

<span data-ttu-id="e7a07-104">Konfiguracji elementu (w formacie) Element ViewDefinitions (Format) widoku elementu (w formacie) elementu ListControl — Element (Format) elementu ListEntries (Format) ListEntry elemencie (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-104">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) ListControl Element (Format) ListEntries Element (Format) ListEntry Element (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a07-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="e7a07-105">Syntax</span></span>

```xml
<ListEntry>
  <EntrySelectedBy>...</EntrySelectedBy>
  <ListItems>...</ListItems>
</ListEntry>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e7a07-106">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="e7a07-106">Attributes and Elements</span></span>

<span data-ttu-id="e7a07-107">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `ListEntry` elementu.</span><span class="sxs-lookup"><span data-stu-id="e7a07-107">The following sections describe the attributes, child elements, and the parent element of the `ListEntry` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="e7a07-108">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="e7a07-108">Attributes</span></span>

<span data-ttu-id="e7a07-109">Brak.</span><span class="sxs-lookup"><span data-stu-id="e7a07-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="e7a07-110">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="e7a07-110">Child Elements</span></span>

|<span data-ttu-id="e7a07-111">Element</span><span class="sxs-lookup"><span data-stu-id="e7a07-111">Element</span></span>|<span data-ttu-id="e7a07-112">Opis</span><span class="sxs-lookup"><span data-stu-id="e7a07-112">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="e7a07-113">Element EntrySelectedBy ListEntry (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-113">EntrySelectedBy Element for ListEntry (Format)</span></span>](./entryselectedby-element-for-listentry-for-listcontrol-format.md)|<span data-ttu-id="e7a07-114">Element opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e7a07-114">Optional element.</span></span><br /><br /> <span data-ttu-id="e7a07-115">Definiuje obiekty .NET, korzystające z tej listy definicji widoku lub warunek, który musi istnieć, aby ta definicja ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e7a07-115">Defines the .NET objects that use this list view definition or the condition that must exist for this definition to be used.</span></span>|
|[<span data-ttu-id="e7a07-116">Element ListItems (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-116">ListItems Element (Format)</span></span>](./listitems-element-for-listentry-for-listcontrol-format.md)|<span data-ttu-id="e7a07-117">Element wymagany.</span><span class="sxs-lookup"><span data-stu-id="e7a07-117">Required element.</span></span><br /><br /> <span data-ttu-id="e7a07-118">Definiuje właściwości i skrypty, których wartości są wyświetlane w widoku listy.</span><span class="sxs-lookup"><span data-stu-id="e7a07-118">Defines the properties and scripts whose values are displayed by the list view.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="e7a07-119">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="e7a07-119">Parent Elements</span></span>

|<span data-ttu-id="e7a07-120">Element</span><span class="sxs-lookup"><span data-stu-id="e7a07-120">Element</span></span>|<span data-ttu-id="e7a07-121">Opis</span><span class="sxs-lookup"><span data-stu-id="e7a07-121">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="e7a07-122">Element ListEntries (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-122">ListEntries Element (Format)</span></span>](./listentries-element-for-listcontrol-format.md)|<span data-ttu-id="e7a07-123">Zawiera definicje w widoku listy.</span><span class="sxs-lookup"><span data-stu-id="e7a07-123">Provides the definitions of the list view.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e7a07-124">Uwagi</span><span class="sxs-lookup"><span data-stu-id="e7a07-124">Remarks</span></span>

<span data-ttu-id="e7a07-125">Widok listy jest format listy, która wyświetla wartości właściwości lub wartości skryptu dla każdego obiektu.</span><span class="sxs-lookup"><span data-stu-id="e7a07-125">A list view is a list format that displays property values or script values for each object.</span></span> <span data-ttu-id="e7a07-126">Aby uzyskać więcej informacji na temat widoki list zobacz [tworzenia widoku listy](./creating-a-list-view.md).</span><span class="sxs-lookup"><span data-stu-id="e7a07-126">For more information about list views, see [Creating a List View](./creating-a-list-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="e7a07-127">Przykład</span><span class="sxs-lookup"><span data-stu-id="e7a07-127">Example</span></span>

<span data-ttu-id="e7a07-128">Elementy XML, które określają widok listy w tym przykładzie [System.Serviceprocess.Servicecontroller](/dotnet/api/System.ServiceProcess.ServiceController) obiektu.</span><span class="sxs-lookup"><span data-stu-id="e7a07-128">This example shows the XML elements that define the list view for the [System.Serviceprocess.Servicecontroller](/dotnet/api/System.ServiceProcess.ServiceController) object.</span></span>

```xml
<View>
  <Name>System.ServiceProcess.ServiceController</Name>
  <ViewSelectedBy>
    <TypeName>System.ServiceProcess.ServiceController</TypeName>
  </ViewSelectedBy>
  <ListControl>
    <ListEntries>
      <ListEntry>
        <ListItems>...</ListItems>
      </ListEntry>
    </ListEntries>
  </ListControl>
</View>
```

## <a name="see-also"></a><span data-ttu-id="e7a07-129">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="e7a07-129">See Also</span></span>

[<span data-ttu-id="e7a07-130">Tworzenie widoku listy</span><span class="sxs-lookup"><span data-stu-id="e7a07-130">Creating a List View</span></span>](./creating-a-list-view.md)

[<span data-ttu-id="e7a07-131">Element EntrySelectedBy ListEntry (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-131">EntrySelectedBy Element for ListEntry (Format)</span></span>](./entryselectedby-element-for-listentry-for-listcontrol-format.md)

[<span data-ttu-id="e7a07-132">Element ListEntries (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-132">ListEntries Element (Format)</span></span>](./listentries-element-for-listcontrol-format.md)

[<span data-ttu-id="e7a07-133">Element ListItems (Format)</span><span class="sxs-lookup"><span data-stu-id="e7a07-133">ListItems Element (Format)</span></span>](./listitems-element-for-listentry-for-listcontrol-format.md)

[<span data-ttu-id="e7a07-134">Pisanie programu Windows PowerShell, formatowania i typy plików</span><span class="sxs-lookup"><span data-stu-id="e7a07-134">Writing a Windows PowerShell Formatting and Types File</span></span>](./writing-a-powershell-formatting-file.md)