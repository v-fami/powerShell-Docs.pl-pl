---
title: Widok (Basic) listy | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 918f381c-43e6-4594-a468-a40bfa8a16d6
caps.latest.revision: 7
ms.openlocfilehash: 1c683693c331ccfaf7355a0dd51801ed6fd39b3b
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56844926"
---
# <a name="list-view-basic"></a><span data-ttu-id="3d7ef-102">Widok listy (podstawowy)</span><span class="sxs-lookup"><span data-stu-id="3d7ef-102">List View (Basic)</span></span>

<span data-ttu-id="3d7ef-103">W tym przykładzie pokazano, jak zaimplementować wyświetlony widok listy podstawowe [System.Serviceprocess.Servicecontroller? Displayproperty = imię i nazwisko](/dotnet/api/System.ServiceProcess.ServiceController) obiektów zwróconych przez [Get-Service](/powershell/module/microsoft.powershell.management/get-service) polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-103">This example shows how to implement a basic list view that displays the [System.Serviceprocess.Servicecontroller?Displayproperty=Fullname](/dotnet/api/System.ServiceProcess.ServiceController) objects returned by the [Get-Service](/powershell/module/microsoft.powershell.management/get-service) cmdlet.</span></span> <span data-ttu-id="3d7ef-104">Aby uzyskać więcej informacji o składnikach w widoku listy, zobacz [tworzenia widoku listy](./creating-a-list-view.md).</span><span class="sxs-lookup"><span data-stu-id="3d7ef-104">For more information about the components of a list view, see [Creating a List View](./creating-a-list-view.md).</span></span>
<span data-ttu-id="3d7ef-105">W tym przykładzie pokazano, jak zaimplementować wyświetlony widok listy podstawowe [System.Serviceprocess.Servicecontroller? Displayproperty = imię i nazwisko](/dotnet/api/System.ServiceProcess.ServiceController) obiektów zwróconych przez [Get-Service](/powershell/module/microsoft.powershell.management/get-service) polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-105">This example shows how to implement a basic list view that displays the [System.Serviceprocess.Servicecontroller?Displayproperty=Fullname](/dotnet/api/System.ServiceProcess.ServiceController) objects returned by the [Get-Service](/powershell/module/microsoft.powershell.management/get-service) cmdlet.</span></span> <span data-ttu-id="3d7ef-106">Aby uzyskać więcej informacji o składnikach w widoku listy, zobacz [tworzenia widoku listy](./creating-a-list-view.md).</span><span class="sxs-lookup"><span data-stu-id="3d7ef-106">For more information about the components of a list view, see [Creating a List View](./creating-a-list-view.md).</span></span>

### <a name="to-load-this-formatting-file"></a><span data-ttu-id="3d7ef-107">Aby załadować ten plik formatowania</span><span class="sxs-lookup"><span data-stu-id="3d7ef-107">To load this formatting file</span></span>

1. <span data-ttu-id="3d7ef-108">Skopiuj plik XML z sekcji przykład tego tematu do pliku tekstowego.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-108">Copy the XML from the Example section of this topic into a text file.</span></span>

2. <span data-ttu-id="3d7ef-109">Zapisz plik tekstowy.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-109">Save the text file.</span></span> <span data-ttu-id="3d7ef-110">Pamiętaj dodać `format.ps1xml` rozszerzenie pliku, aby zidentyfikować go jako plik formatowania.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-110">Be sure to add the `format.ps1xml` extension to the file to identify it as a formatting file.</span></span>

3. <span data-ttu-id="3d7ef-111">Otwórz program Windows PowerShell i uruchom następujące polecenie, aby załadować plik formatowania do bieżącej sesji: `Update-formatdata -prependpath PathToFormattingFile`.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-111">Open Windows PowerShell, and run the following command to load the formatting file into the current session: `Update-formatdata -prependpath PathToFormattingFile`.</span></span>

   > [!WARNING]
   > <span data-ttu-id="3d7ef-112">Ten plik formatowania definiuje wyświetlanie obiektu, który jest już zdefiniowana w pliku formatowania programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-112">This formatting file defines the display of an object that is already defined by a Windows PowerShell formatting file.</span></span> <span data-ttu-id="3d7ef-113">Należy użyć `prependPath` parametru po uruchomieniu polecenia cmdlet, a nie można załadować to formatowanie pliku jako moduł.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-113">You must use the `prependPath` parameter when you run the cmdlet, and you cannot load this formatting file as a module.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="3d7ef-114">Przedstawiono</span><span class="sxs-lookup"><span data-stu-id="3d7ef-114">Demonstrates</span></span>

<span data-ttu-id="3d7ef-115">Ten plik formatowania pokazuje następujące elementy XML:</span><span class="sxs-lookup"><span data-stu-id="3d7ef-115">This formatting file demonstrates the following XML elements:</span></span>

- <span data-ttu-id="3d7ef-116">[Nazwa](./name-element-for-view-format.md) elementu widoku.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-116">The [Name](./name-element-for-view-format.md) element for the view.</span></span>

- <span data-ttu-id="3d7ef-117">[ViewSelectedBy](./viewselectedby-element-format.md) element, który definiuje, jakie obiekty są wyświetlane w widoku.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-117">The [ViewSelectedBy](./viewselectedby-element-format.md) element that defines what objects are displayed by the view.</span></span>

- <span data-ttu-id="3d7ef-118">[Elementu ListControl](./listcontrol-element-format.md) element, który definiuje, jakie właściwości jest wyświetlany w widoku.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-118">The [ListControl](./listcontrol-element-format.md) element that defines what property is displayed by the view.</span></span>

- <span data-ttu-id="3d7ef-119">[ListItem](./listitem-element-for-listitems-for-listcontrol-format.md) element, który definiuje, co jest wyświetlane w wierszu w widoku listy.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-119">The [ListItem](./listitem-element-for-listitems-for-listcontrol-format.md) element that defines what is displayed in a row of the list view.</span></span>

- <span data-ttu-id="3d7ef-120">[PropertyName](./propertyname-element-for-listitem-for-listcontrol-format.md) element, który definiuje, w którym właściwość jest wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-120">The [PropertyName](./propertyname-element-for-listitem-for-listcontrol-format.md) element that defines which property is displayed.</span></span>

## <a name="example"></a><span data-ttu-id="3d7ef-121">Przykład</span><span class="sxs-lookup"><span data-stu-id="3d7ef-121">Example</span></span>

<span data-ttu-id="3d7ef-122">Następujący kod XML definiuje widok listy zostaną wyświetlone cztery właściwości [System.Serviceprocess.Servicecontroller? Displayproperty = imię i nazwisko](/dotnet/api/System.ServiceProcess.ServiceController) obiektu.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-122">The following XML defines a list view that displays four properties of the [System.Serviceprocess.Servicecontroller?Displayproperty=Fullname](/dotnet/api/System.ServiceProcess.ServiceController) object.</span></span> <span data-ttu-id="3d7ef-123">W każdym wierszu jest wyświetlana nazwa właściwości, następuje wartość właściwości.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-123">In each row, the name of the property is displayed followed by the value of the property.</span></span>

```xml
<Configuration>
  <View>
    <Name>System.ServiceProcess.ServiceController</Name>
    <ViewSelectedBy>
      <TypeName>System.ServiceProcess.ServiceController</TypeName>
    </ViewSelectedBy>
    <ListControl>
      <ListEntries>
        <ListEntry>
          <ListItems>
            <ListItem>
              <PropertyName>Name</PropertyName>
            </ListItem>
            <ListItem>
              <PropertyName>DisplayName</PropertyName>
            </ListItem>
            <ListItem>
              <PropertyName>Status</PropertyName>
            </ListItem>
            <ListItem>
              <PropertyName>ServiceType</PropertyName>
            </ListItem>
          </ListItems>
        </ListEntry>
      </ListEntries>
    </ListControl>
  </View>
</Configuration>
```

<span data-ttu-id="3d7ef-124">W poniższym przykładzie przedstawiono sposób wyświetlania środowiska Windows PowerShell [System.Serviceprocess.Servicecontroller? Displayproperty = imię i nazwisko](/dotnet/api/System.ServiceProcess.ServiceController) obiektów po załadowaniu tego formatu pliku.</span><span class="sxs-lookup"><span data-stu-id="3d7ef-124">The following example shows how Windows PowerShell displays the [System.Serviceprocess.Servicecontroller?Displayproperty=Fullname](/dotnet/api/System.ServiceProcess.ServiceController) objects after this format file is loaded.</span></span>

```powershell
Get-Service f*
```

```output
Name        : Fax
DisplayName : Fax
Status      : Stopped
ServiceType : Win32OwnProcess

Name        : FCSAM
DisplayName : Microsoft Antimalware Service
Status      : Running
ServiceType : Win32OwnProcess

Name        : fdPHost
DisplayName : Function Discovery Provider Host
Status      : Stopped
ServiceType : Win32ShareProcess

Name        : FDResPub
DisplayName : Function Discovery Resource Publication
Status      : Running
ServiceType : Win32ShareProcess

Name        : FontCache
DisplayName : Windows Font Cache Service
Status      : Running
ServiceType : Win32ShareProcess

Name        : FontCache3.0.0.0
DisplayName : Windows Presentation Foundation Font Cache 3.0.0.0
Status      : Stopped
ServiceType : Win32OwnProcess

Name        : FSysAgent
DisplayName : Microsoft Forefront System Agent
Status      : Running
ServiceType : Win32OwnProcess

Name        : FwcAgent
DisplayName : Firewall Client Agent
Status      : Running
ServiceType : Win32OwnProcess
```

## <a name="see-also"></a><span data-ttu-id="3d7ef-125">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="3d7ef-125">See Also</span></span>

[<span data-ttu-id="3d7ef-126">Przykłady formatowania plików</span><span class="sxs-lookup"><span data-stu-id="3d7ef-126">Examples of Formatting Files</span></span>](./examples-of-formatting-files.md)

[<span data-ttu-id="3d7ef-127">Pisanie programu PowerShell, formatowanie pliku</span><span class="sxs-lookup"><span data-stu-id="3d7ef-127">Writing a PowerShell Formatting File</span></span>](./writing-a-powershell-formatting-file.md)