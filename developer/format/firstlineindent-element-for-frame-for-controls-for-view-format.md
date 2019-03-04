---
title: Element FirstLineIndent ramki dla formantów widoku (Format) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ec63f4f9-8858-4529-8646-ffbbc278f83e
caps.latest.revision: 7
ms.openlocfilehash: 694c5baaa5e90a772257276ba139d90acf7ec0e3
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56845633"
---
# <a name="firstlineindent-element-for-frame-for-controls-for-view-format"></a><span data-ttu-id="b4244-102">FirstLineIndent, element — Frame, Controls, View (format)</span><span class="sxs-lookup"><span data-stu-id="b4244-102">FirstLineIndent Element for Frame for Controls for View (Format)</span></span>

<span data-ttu-id="b4244-103">Określa liczbę znaków w pierwszym wierszu danych jest przesuwany w prawo.</span><span class="sxs-lookup"><span data-stu-id="b4244-103">Specifies how many characters the first line of data is shifted to the right.</span></span> <span data-ttu-id="b4244-104">Ten element jest używany podczas definiowania formantów, które mogą być używane przez widok.</span><span class="sxs-lookup"><span data-stu-id="b4244-104">This element is used when defining controls that can be used by a view.</span></span>

<span data-ttu-id="b4244-105">— Element (Format) ViewDefinitions — Element (w formacie) widoku elementu (w formacie) kontrolki elementu (w formacie) kontroli Element konfiguracji dla formantów dla elementu formant niestandardowy widok (w formacie) dla formantu dla formantów elementu CustomEntries widoku (Format) Formant niestandardowy widok (w formacie) elementu CustomEntry CustomEntries dla formantów widoku (Format) elementu CustomItem CustomEntry dla formantów widoku (Format) elementu ramki CustomItem dla formantów dla elementu FirstLineIndent widoku (Format) ramki formantów widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="b4244-105">Configuration Element (Format) ViewDefinitions Element (Format) View Element (Format) Controls Element (Format) Control Element for Controls for View (Format) CustomControl Element for Control for Controls for View (Format) CustomEntries Element for CustomControl for View (Format) CustomEntry Element for CustomEntries for Controls for View (Format) CustomItem Element for CustomEntry for Controls for View (Format) Frame Element for CustomItem for Controls for View (Format) FirstLineIndent Element of Frame of Controls of View (Format)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4244-106">Składnia</span><span class="sxs-lookup"><span data-stu-id="b4244-106">Syntax</span></span>

```xml
<FirstLineIndent>NumberOfCharactersToShift</FirstLineIndent>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b4244-107">Atrybuty i elementy</span><span class="sxs-lookup"><span data-stu-id="b4244-107">Attributes and Elements</span></span>

<span data-ttu-id="b4244-108">W poniższych sekcjach opisano atrybuty, elementy podrzędne i element nadrzędny `FirstLineIndent` elementu.</span><span class="sxs-lookup"><span data-stu-id="b4244-108">The following sections describe attributes, child elements, and parent element of the `FirstLineIndent` element.</span></span>

### <a name="attributes"></a><span data-ttu-id="b4244-109">Atrybuty</span><span class="sxs-lookup"><span data-stu-id="b4244-109">Attributes</span></span>

<span data-ttu-id="b4244-110">Brak.</span><span class="sxs-lookup"><span data-stu-id="b4244-110">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="b4244-111">Elementy podrzędne</span><span class="sxs-lookup"><span data-stu-id="b4244-111">Child Elements</span></span>

<span data-ttu-id="b4244-112">Brak.</span><span class="sxs-lookup"><span data-stu-id="b4244-112">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="b4244-113">Elementy nadrzędne</span><span class="sxs-lookup"><span data-stu-id="b4244-113">Parent Elements</span></span>

|<span data-ttu-id="b4244-114">Element</span><span class="sxs-lookup"><span data-stu-id="b4244-114">Element</span></span>|<span data-ttu-id="b4244-115">Opis</span><span class="sxs-lookup"><span data-stu-id="b4244-115">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="b4244-116">Element ramki dla CustomItem dla formantów widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="b4244-116">Frame Element for CustomItem for Controls for View (Format)</span></span>](./frame-element-for-customitem-for-controls-for-view-format.md)|<span data-ttu-id="b4244-117">Definiuje sposób wyświetlania danych, takie jak przesunięcie danych do lewej lub prawej strony.</span><span class="sxs-lookup"><span data-stu-id="b4244-117">Defines how the data is displayed, such as shifting the data to the left or right.</span></span>|

## <a name="text-value"></a><span data-ttu-id="b4244-118">Wartość tekstowa</span><span class="sxs-lookup"><span data-stu-id="b4244-118">Text Value</span></span>

<span data-ttu-id="b4244-119">Określ liczbę znaków, które mają zostać przesunięte na pierwszy wiersz danych.</span><span class="sxs-lookup"><span data-stu-id="b4244-119">Specify the number of characters that you want to shift the first line of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4244-120">Uwagi</span><span class="sxs-lookup"><span data-stu-id="b4244-120">Remarks</span></span>

<span data-ttu-id="b4244-121">Jeśli ten element jest określony, nie można określić [FirstLineHanging](./firstlinehanging-element-for-frame-for-controls-for-view-format.md) elementu.</span><span class="sxs-lookup"><span data-stu-id="b4244-121">If this element is specified, you cannot specify the [FirstLineHanging](./firstlinehanging-element-for-frame-for-controls-for-view-format.md) element.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4244-122">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="b4244-122">See Also</span></span>

[<span data-ttu-id="b4244-123">Element FirstLineHanging ramki dla formantów widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="b4244-123">FirstLineHanging Element for Frame for Controls for View (Format)</span></span>](./firstlinehanging-element-for-frame-for-controls-for-view-format.md)

[<span data-ttu-id="b4244-124">Element ramki dla CustomItem dla formantów widoku (Format)</span><span class="sxs-lookup"><span data-stu-id="b4244-124">Frame Element for CustomItem for Controls for View (Format)</span></span>](./frame-element-for-customitem-for-controls-for-view-format.md)

[<span data-ttu-id="b4244-125">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="b4244-125">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)