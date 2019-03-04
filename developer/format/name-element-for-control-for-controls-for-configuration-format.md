---
title: Nazwa elementu dla formantu dla formantów dla konfiguracji (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: b4371d45-49a4-4303-8384-5b54105bd0d6
caps.latest.revision: 8
ms.openlocfilehash: 2704a530e0ae269efb772ac10e531bcbb12f6eff
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56849672"
---
# <a name="name-element-for-control-for-controls-for-configuration-format"></a><span data-ttu-id="a2d1f-102">Name, element — Control, Controls, Configuration (format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-102">Name Element for Control for Controls for Configuration (Format)</span></span>

<span data-ttu-id="a2d1f-103">Określa nazwę formantu.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-103">Specifies the name of the control.</span></span> <span data-ttu-id="a2d1f-104">Ten element jest używany podczas definiowania wspólnej formant, który może być używany przez wszystkie widoki w formatowaniu pliku.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-104">This element is used when defining a common control that can be used by all the views in the formatting file.</span></span>

<span data-ttu-id="a2d1f-105">Konfiguracji elementu (w formacie) kontrolki elementu konfiguracji (Format) formantu dla formantów dla elementu nazwy konfiguracji (w formacie) dla formantu dla formantów dla konfiguracji (Format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-105">Configuration Element (Format) Controls Element of Configuration (Format) Control Element for Controls for Configuration (Format) Name Element for Control for Controls for Configuration (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d1f-106">Składnia</span><span class="sxs-lookup"><span data-stu-id="a2d1f-106">Syntax</span></span>

```xml
<Name>NameOfControl</Name>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="a2d1f-107">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="a2d1f-107">Attributes and Elements</span></span>

<span data-ttu-id="a2d1f-108">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `Name` elementu.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-108">The following sections describe attributes, child elements, and the parent element of the `Name` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="a2d1f-109">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="a2d1f-109">Attributes</span></span>

<span data-ttu-id="a2d1f-110">Brak.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-110">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="a2d1f-111">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="a2d1f-111">Child Elements</span></span>

<span data-ttu-id="a2d1f-112">Brak.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-112">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="a2d1f-113">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="a2d1f-113">Parent Elements</span></span>

|<span data-ttu-id="a2d1f-114">Element</span><span class="sxs-lookup"><span data-stu-id="a2d1f-114">Element</span></span>|<span data-ttu-id="a2d1f-115">Opis</span><span class="sxs-lookup"><span data-stu-id="a2d1f-115">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="a2d1f-116">Elementu formantu dla formantów dla konfiguracji (Format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-116">Control Element for Controls for Configuration (Format)</span></span>](./control-element-for-controls-for-configuration-format.md)|<span data-ttu-id="a2d1f-117">Definiuje typowe formant, który może być używany przez wszystkie widoki formatowania pliku i nazwę, która jest używana do odwołania kontrolki.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-117">Defines a common control that can be used by all the views of the formatting file and the name that is used to reference the control.</span></span>|

## <a name="text-value"></a><span data-ttu-id="a2d1f-118">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="a2d1f-118">Text Value</span></span>

<span data-ttu-id="a2d1f-119">Określ nazwę, która jest używana do odwoływać się do tego formantu.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-119">Specify the name that is used to reference this control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d1f-120">Uwagi</span><span class="sxs-lookup"><span data-stu-id="a2d1f-120">Remarks</span></span>

<span data-ttu-id="a2d1f-121">Nazwa określona w tym miejscu może służyć w następujących elementów można odwoływać się do tego formantu.</span><span class="sxs-lookup"><span data-stu-id="a2d1f-121">The name specified here can be used in the following elements to reference this control.</span></span>

- <span data-ttu-id="a2d1f-122">Podczas tworzenia tabeli, lista, szeroki lub niestandardowe kontrolki widoku, można określić formantu przez następujący element: [GroupBy — Element dla widoku (Format)](./groupby-element-for-view-format.md)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-122">When creating a table, list, wide or custom control view, the control can be specified by the following element: [GroupBy Element for View (Format)](./groupby-element-for-view-format.md)</span></span>

- <span data-ttu-id="a2d1f-123">Tworząc innego formantu typowego tego formantu można określić za następującego elementu: [Element ExpressionBinding CustomItem dla formantów dla konfiguracji (Format)](./expressionbinding-element-for-customitem-for-controls-for-configuration-format.md)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-123">When creating another common control, this control can be specified by the following element: [ExpressionBinding Element for CustomItem for Controls for Configuration (Format)](./expressionbinding-element-for-customitem-for-controls-for-configuration-format.md)</span></span>

- <span data-ttu-id="a2d1f-124">Podczas tworzenia formantu, który może służyć przez widok, można określić tego formantu przez następujący element: [Element ExpressionBinding CustomItem dla formantów widoku (Format)](./expressionbinding-element-for-customitem-for-controls-for-view-format.md)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-124">When creating a control that can be used by a view, this control can be specified by the following element: [ExpressionBinding Element for CustomItem for Controls for View (Format)](./expressionbinding-element-for-customitem-for-controls-for-view-format.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="a2d1f-125">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="a2d1f-125">See Also</span></span>

[<span data-ttu-id="a2d1f-126">Elementu formantu dla formantów dla konfiguracji (Format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-126">Control Element for Controls for Configuration (Format)</span></span>](./control-element-for-controls-for-configuration-format.md)

[<span data-ttu-id="a2d1f-127">Element ExpressionBinding CustomItem dla formantów dla konfiguracji (Format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-127">ExpressionBinding Element for CustomItem for Controls for Configuration (Format)</span></span>](./expressionbinding-element-for-customitem-for-controls-for-configuration-format.md)

[<span data-ttu-id="a2d1f-128">Element ExpressionBinding CustomItem dla formantów widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-128">ExpressionBinding Element for CustomItem for Controls for View (Format)</span></span>](./expressionbinding-element-for-customitem-for-controls-for-view-format.md)

[<span data-ttu-id="a2d1f-129">GroupBy — Element dla widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="a2d1f-129">GroupBy Element for View (Format)</span></span>](./groupby-element-for-view-format.md)

[<span data-ttu-id="a2d1f-130">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="a2d1f-130">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)