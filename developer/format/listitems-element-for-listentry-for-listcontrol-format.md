---
title: Element ListItems ListEntry dla elementu ListControl (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: d2c1da6d-acc7-4fe8-9e7d-6dcddc2787cd
caps.latest.revision: 9
ms.openlocfilehash: c25f18489d9c7abd8889758499dbbacd6ee29304
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56848622"
---
# <a name="listitems-element-for-listentry-for-listcontrol-format"></a><span data-ttu-id="a7156-102">ListItems, element — ListEntry, ListControl (format)</span><span class="sxs-lookup"><span data-stu-id="a7156-102">ListItems Element for ListEntry for ListControl (Format)</span></span>

<span data-ttu-id="a7156-103">Definiuje właściwości i skrypty, których wartości są wyświetlane w wierszach widoku listy.</span><span class="sxs-lookup"><span data-stu-id="a7156-103">Defines the properties and scripts whose values are displayed in the rows of the list view.</span></span>

<span data-ttu-id="a7156-104">— Element (w formacie) elementu ViewDefinitions (Format) widoku elementu (w formacie) elementu ListControl — Element (Format) ListEntries Element konfiguracji dla elementu ListEntry List kontroli (w formacie) dla elementu ListItems elementu ListControl (w formacie) dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="a7156-104">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) ListControl Element (Format) ListEntries Element for List Control (Format) ListEntry Element for ListControl (Format) ListItems Element for ListControl (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7156-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="a7156-105">Syntax</span></span>

```xml
<ListItems>
  <ListItem>...</ListItem>
</ListItems>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a7156-106">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="a7156-106">Attributes and Elements</span></span>

<span data-ttu-id="a7156-107">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `ListItems` elementu.</span><span class="sxs-lookup"><span data-stu-id="a7156-107">The following sections describe the attributes, child elements, and parent element of the `ListItems` element.</span></span> <span data-ttu-id="a7156-108">Nie ma żadnego limitu liczby elementów podrzędnych, które można określić.</span><span class="sxs-lookup"><span data-stu-id="a7156-108">There is no limit to the number of child elements that can be specified.</span></span> <span data-ttu-id="a7156-109">Kolejność elementów podrzędnych definiuje kolejność wyświetlania wartości w widoku listy.</span><span class="sxs-lookup"><span data-stu-id="a7156-109">The order of the child elements defines the order that values are displayed in the list view.</span></span>

### <a name="attributes"></a><span data-ttu-id="a7156-110">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="a7156-110">Attributes</span></span>

<span data-ttu-id="a7156-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="a7156-111">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="a7156-112">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="a7156-112">Child Elements</span></span>

|<span data-ttu-id="a7156-113">Element</span><span class="sxs-lookup"><span data-stu-id="a7156-113">Element</span></span>|<span data-ttu-id="a7156-114">Opis</span><span class="sxs-lookup"><span data-stu-id="a7156-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="a7156-115">Element ListItem dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="a7156-115">ListItem Element for ListControl (Format)</span></span>](./listitem-element-for-listitems-for-listcontrol-format.md)|<span data-ttu-id="a7156-116">Element wymagany.</span><span class="sxs-lookup"><span data-stu-id="a7156-116">Required element.</span></span><br /><br /> <span data-ttu-id="a7156-117">Definiuje właściwości lub skryptu, którego wartość jest wyświetlana w widoku listy.</span><span class="sxs-lookup"><span data-stu-id="a7156-117">Defines the property or script whose value is displayed by the list view.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="a7156-118">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="a7156-118">Parent Elements</span></span>

|<span data-ttu-id="a7156-119">Element</span><span class="sxs-lookup"><span data-stu-id="a7156-119">Element</span></span>|<span data-ttu-id="a7156-120">Opis</span><span class="sxs-lookup"><span data-stu-id="a7156-120">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="a7156-121">Element ListEntry dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="a7156-121">ListEntry Element for ListControl (Format)</span></span>](./listentry-element-for-listcontrol-format.md)|<span data-ttu-id="a7156-122">Zawiera definicję widoku listy.</span><span class="sxs-lookup"><span data-stu-id="a7156-122">Provides a definition of the list view.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a7156-123">Uwagi</span><span class="sxs-lookup"><span data-stu-id="a7156-123">Remarks</span></span>

<span data-ttu-id="a7156-124">Aby uzyskać więcej informacji na temat tego typu widoku, zobacz [tworzenia widoku listy](./creating-a-list-view.md).</span><span class="sxs-lookup"><span data-stu-id="a7156-124">For more information about this type of view, see [Creating a List View](./creating-a-list-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="a7156-125">Przykład</span><span class="sxs-lookup"><span data-stu-id="a7156-125">Example</span></span>

<span data-ttu-id="a7156-126">Ten przykład pokazuje elementy XML, które określają trzy wiersze w widoku listy.</span><span class="sxs-lookup"><span data-stu-id="a7156-126">This example shows the XML elements that define three rows of the list view.</span></span>

```xml
<ListEntry>
    <ListItems>
      <ListItem>
        <Label>Property1: </Label>
        <PropertyName>.NetTypeProperty1</PropertyName>
      </ListItem>
      <ListItem>
        <PropertyName>.NetTypeProperty2</PropertyName>
      </ListItem>
      <ListItem>
        <ScriptBlock>$_.ProcessName + ":" $_.Id</ScriptBlock>
      </ListItem>
  </ListEntry>
```

## <a name="see-also"></a><span data-ttu-id="a7156-127">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="a7156-127">See Also</span></span>

[<span data-ttu-id="a7156-128">Element ListEntry dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="a7156-128">ListEntry Element for ListControl (Format)</span></span>](./listentry-element-for-listcontrol-format.md)

[<span data-ttu-id="a7156-129">Element ListItem dla elementu ListControl (Format)</span><span class="sxs-lookup"><span data-stu-id="a7156-129">ListItem Element for ListControl (Format)</span></span>](./listitem-element-for-listitems-for-listcontrol-format.md)

[<span data-ttu-id="a7156-130">Tworzenie widoku listy</span><span class="sxs-lookup"><span data-stu-id="a7156-130">Creating a List View</span></span>](./creating-a-list-view.md)

[<span data-ttu-id="a7156-131">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="a7156-131">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)