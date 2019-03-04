---
title: Etykieta elementu dla TableColumnHeader dla tablecontrol — (w formacie) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 7196f039-2f6a-41fd-b252-5b1623ebb9f9
caps.latest.revision: 11
ms.openlocfilehash: 59dfd40b95d5088a711eb89cf101eb31a4b159f5
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56846872"
---
# <a name="label-element-for-tablecolumnheader-for-tablecontrol-format"></a><span data-ttu-id="631bb-102">Label, element — TableColumnHeader, TableControl (format)</span><span class="sxs-lookup"><span data-stu-id="631bb-102">Label Element for TableColumnHeader for TableControl (Format)</span></span>

<span data-ttu-id="631bb-103">Definiuje etykietę, która jest wyświetlana w górnej części kolumny.</span><span class="sxs-lookup"><span data-stu-id="631bb-103">Defines the label that is displayed at the top of a column.</span></span> <span data-ttu-id="631bb-104">Ten element jest używany podczas definiowania widoku tabeli.</span><span class="sxs-lookup"><span data-stu-id="631bb-104">This element is used when defining a table view.</span></span>

<span data-ttu-id="631bb-105">— Element (w formacie) ViewDefinitions — Element (Format) widoku elementu (w formacie) tablecontrol — Element (Format) TableHeaders Element konfiguracji tablecontrol — (w formacie) elementu TableColumnHeader TableHeaders tablecontrol — (w formacie) etykiety elementu TableColumnHeader dla TablControl (Format)</span><span class="sxs-lookup"><span data-stu-id="631bb-105">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) TableControl Element (Format) TableHeaders Element for TableControl (Format) TableColumnHeader Element for TableHeaders for TableControl (Format) Label Element  for TableColumnHeader for TablControl (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="631bb-106">Składnia</span><span class="sxs-lookup"><span data-stu-id="631bb-106">Syntax</span></span>

```xml
<Label>DisplayedLabel</Label>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="631bb-107">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="631bb-107">Attributes and Elements</span></span>

<span data-ttu-id="631bb-108">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `Label` elementu.</span><span class="sxs-lookup"><span data-stu-id="631bb-108">The following sections describe the attributes, child elements, and the parent element of the `Label` element.</span></span> <span data-ttu-id="631bb-109">Tylko jedna etykieta jest dozwolony dla każdej kolumny.</span><span class="sxs-lookup"><span data-stu-id="631bb-109">Only one label is allowed for each column.</span></span>

### <a name="attributes"></a><span data-ttu-id="631bb-110">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="631bb-110">Attributes</span></span>

<span data-ttu-id="631bb-111">Brak.</span><span class="sxs-lookup"><span data-stu-id="631bb-111">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="631bb-112">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="631bb-112">Child Elements</span></span>

<span data-ttu-id="631bb-113">Brak.</span><span class="sxs-lookup"><span data-stu-id="631bb-113">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="631bb-114">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="631bb-114">Parent Elements</span></span>

|<span data-ttu-id="631bb-115">Element</span><span class="sxs-lookup"><span data-stu-id="631bb-115">Element</span></span>|<span data-ttu-id="631bb-116">Opis</span><span class="sxs-lookup"><span data-stu-id="631bb-116">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="631bb-117">Element TableColumnHeader TableHeaders dla tablecontrol — (w formacie)</span><span class="sxs-lookup"><span data-stu-id="631bb-117">TableColumnHeader Element for TableHeaders for TableControl  (Format)</span></span>](./tablecolumnheader-element-format.md)|<span data-ttu-id="631bb-118">Definiuje etykietę, szerokości i wyrównania danych dla kolumny tabeli.</span><span class="sxs-lookup"><span data-stu-id="631bb-118">Defines a label, the width, and the alignment of the data for a column of the table.</span></span>|

## <a name="text-value"></a><span data-ttu-id="631bb-119">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="631bb-119">Text Value</span></span>

<span data-ttu-id="631bb-120">Podaj tekst, który jest wyświetlany w górnej części kolumny tabeli.</span><span class="sxs-lookup"><span data-stu-id="631bb-120">Specify the text that is displayed at the top of the column of the table.</span></span> <span data-ttu-id="631bb-121">Nie istnieją żadne znaki w etykiecie kolumny.</span><span class="sxs-lookup"><span data-stu-id="631bb-121">There are no restricted characters for the column label.</span></span>

## <a name="remarks"></a><span data-ttu-id="631bb-122">Uwagi</span><span class="sxs-lookup"><span data-stu-id="631bb-122">Remarks</span></span>

<span data-ttu-id="631bb-123">Jeśli żadna etykieta nie zostanie określona, jest używana nazwa właściwości, którego wartość jest wyświetlana w wierszach.</span><span class="sxs-lookup"><span data-stu-id="631bb-123">If no label is specified, the name of the property whose value is displayed in the rows is used.</span></span>

<span data-ttu-id="631bb-124">Aby uzyskać więcej informacji o składnikach w widoku tabeli, zobacz [tworzenia widoku tabeli](./creating-a-table-view.md).</span><span class="sxs-lookup"><span data-stu-id="631bb-124">For more information about the components of a table view, see [Creating a Table View](./creating-a-table-view.md).</span></span>

## <a name="example"></a><span data-ttu-id="631bb-125">Przykład</span><span class="sxs-lookup"><span data-stu-id="631bb-125">Example</span></span>

<span data-ttu-id="631bb-126">W tym przykładzie `TableColumnHeader` elementu, którego etykieta jest "Kolumna 1".</span><span class="sxs-lookup"><span data-stu-id="631bb-126">This example shows a `TableColumnHeader` element whose label is "Column 1".</span></span>

```xml
<TableColumnHeader>
  <Label>Column 1</Label)
  <Width>16</Width>
  <Alignment>Left</Alignment>
</TableColumnHeader>
```

## <a name="see-also"></a><span data-ttu-id="631bb-127">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="631bb-127">See Also</span></span>

[<span data-ttu-id="631bb-128">Tworzenie widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="631bb-128">Creating a Table View</span></span>](./creating-a-table-view.md)

[<span data-ttu-id="631bb-129">Element TableColumnHeader (Format)</span><span class="sxs-lookup"><span data-stu-id="631bb-129">TableColumnHeader Element (Format)</span></span>](./tablecolumnheader-element-format.md)

[<span data-ttu-id="631bb-130">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="631bb-130">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)