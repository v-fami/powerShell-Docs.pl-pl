---
title: Element ScriptBlock SelectionCondition dla EntrySelectedBy dla EnumerableExpansion (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4126b799-c43d-4175-8513-6d761c65437e
caps.latest.revision: 9
ms.openlocfilehash: a51d8d22fa8b0c7f303a5e8f37edcc5e57724063
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56845969"
---
# <a name="scriptblock-element-for-selectioncondition-for-entryselectedby-for-enumerableexpansion-format"></a><span data-ttu-id="35ab0-102">ScriptBlock, element — SelectionCondition, EntrySelectedBy, EnumerableExpansion (format)</span><span class="sxs-lookup"><span data-stu-id="35ab0-102">ScriptBlock Element for SelectionCondition for EntrySelectedBy for EnumerableExpansion (Format)</span></span>

<span data-ttu-id="35ab0-103">Określa skrypt, który wyzwala warunku.</span><span class="sxs-lookup"><span data-stu-id="35ab0-103">Specifies the script that triggers the condition.</span></span>

<span data-ttu-id="35ab0-104">— Element (w formacie) DefaultSettings — Element (Format) EnumerableExpansions — Element (Format) EnumerableExpansion — Element (Format) EntrySelectedBy Element konfiguracji elementu SelectionCondition EnumerableExpansion (Format) EntrySelectedBy dla Element ScriptBlock EnumerableExpansion (w formacie) dla SelectionCondition dla EntrySelectedBy dla EnumerableExpansion (Format)</span><span class="sxs-lookup"><span data-stu-id="35ab0-104">Configuration Element (Format) DefaultSettings Element (Format) EnumerableExpansions Element (Format) EnumerableExpansion Element (Format) EntrySelectedBy Element for EnumerableExpansion (Format) SelectionCondition Element for EntrySelectedBy for EnumerableExpansion (Format) ScriptBlock Element for SelectionCondition for EntrySelectedBy for EnumerableExpansion (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="35ab0-105">Składnia</span><span class="sxs-lookup"><span data-stu-id="35ab0-105">Syntax</span></span>

```xml
<ScriptBlock>ScriptToEvaluate</ScriptBlock>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="35ab0-106">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="35ab0-106">Attributes and Elements</span></span>

<span data-ttu-id="35ab0-107">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `ScriptBlock` elementu.</span><span class="sxs-lookup"><span data-stu-id="35ab0-107">The following sections describe attributes, child elements, and the parent element of the `ScriptBlock` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="35ab0-108">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="35ab0-108">Attributes</span></span>

<span data-ttu-id="35ab0-109">Brak.</span><span class="sxs-lookup"><span data-stu-id="35ab0-109">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="35ab0-110">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="35ab0-110">Child Elements</span></span>

<span data-ttu-id="35ab0-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="35ab0-111">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="35ab0-112">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="35ab0-112">Parent Elements</span></span>

|<span data-ttu-id="35ab0-113">Element</span><span class="sxs-lookup"><span data-stu-id="35ab0-113">Element</span></span>|<span data-ttu-id="35ab0-114">Opis</span><span class="sxs-lookup"><span data-stu-id="35ab0-114">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="35ab0-115">Element SelectionCondition EntrySelectedBy dla EnumerableExpansion (Format)</span><span class="sxs-lookup"><span data-stu-id="35ab0-115">SelectionCondition Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-enumerableexpansion-format.md)|<span data-ttu-id="35ab0-116">Określa warunek, który musi istnieć, aby rozwinąć kolekcji obiektów tej definicji.</span><span class="sxs-lookup"><span data-stu-id="35ab0-116">Defines the condition that must exist to expand the collection objects of this definition.</span></span>|

## <a name="text-value"></a><span data-ttu-id="35ab0-117">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="35ab0-117">Text Value</span></span>

<span data-ttu-id="35ab0-118">Określ skrypt, który jest oceniany.</span><span class="sxs-lookup"><span data-stu-id="35ab0-118">Specify the script that is evaluated.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ab0-119">Uwagi</span><span class="sxs-lookup"><span data-stu-id="35ab0-119">Remarks</span></span>

<span data-ttu-id="35ab0-120">Warunek wyboru należy określić co najmniej jedną nazwę skryptu lub właściwości do oceny, ale nie można podać obydwie wartości.</span><span class="sxs-lookup"><span data-stu-id="35ab0-120">The selection condition must specify at least one script or property name to evaluate, but cannot specify both.</span></span> <span data-ttu-id="35ab0-121">Aby uzyskać więcej informacji o sposobie używania warunków wyboru, zobacz [warunki określające gdy dane są wyświetlane](./defining-conditions-for-displaying-data.md).</span><span class="sxs-lookup"><span data-stu-id="35ab0-121">For more information about how to use selection conditions, see [Defining Conditions for when Data is Displayed](./defining-conditions-for-displaying-data.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="35ab0-122">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="35ab0-122">See Also</span></span>

[<span data-ttu-id="35ab0-123">Definiowanie warunków, gdy dane są wyświetlane</span><span class="sxs-lookup"><span data-stu-id="35ab0-123">Defining Conditions for When Data Is Displayed</span></span>](./defining-conditions-for-displaying-data.md)

[<span data-ttu-id="35ab0-124">Element PropertyName SelectionCondition dla EntrySelectedBy dla EnumerableExpansion (Format)</span><span class="sxs-lookup"><span data-stu-id="35ab0-124">PropertyName Element for SelectionCondition for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./propertyname-element-for-selectioncondition-for-entryselectedby-for-enumerableexpansion-format.md)

[<span data-ttu-id="35ab0-125">Element SelectionCondition EntrySelectedBy dla EnumerableExpansion (Format)</span><span class="sxs-lookup"><span data-stu-id="35ab0-125">SelectionCondition Element for EntrySelectedBy for EnumerableExpansion (Format)</span></span>](./selectioncondition-element-for-entryselectedby-for-enumerableexpansion-format.md)

[<span data-ttu-id="35ab0-126">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="35ab0-126">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)