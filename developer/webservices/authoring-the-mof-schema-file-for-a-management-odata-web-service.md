---
title: Tworzenie pliku schematu pliku MOF usługi sieci web OData zarządzania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 65fbac8b-07d0-4513-bc8d-79f1f389be0f
caps.latest.revision: 5
ms.openlocfilehash: 7aadee07b38d2e9d87c5f0c548d13a5cdad1939f
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2019
ms.locfileid: "56845913"
---
# <a name="authoring-the-mof-schema-file-for-a-management-odata-web-service"></a><span data-ttu-id="a9ff6-102">Tworzenie pliku schematu MOF na potrzeby internetowej usługi OData zarządzania</span><span class="sxs-lookup"><span data-stu-id="a9ff6-102">Authoring the MOF schema file for a Management OData web service</span></span>

<span data-ttu-id="a9ff6-103">Można zdefiniować zasoby, które uwidacznia Usługa sieci web OData zarządzania, tworząc plik MOF, który używany schemat zasób publicznego.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-103">You define the resources that your Management OData web service exposes by creating a MOF file that used the public resource schema.</span></span> <span data-ttu-id="a9ff6-104">Każdy zasób jest zdefiniowany jako klasy w pliku i właściwości są zdefiniowane jako elementy członkowskie klasy.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-104">Each resource is defined as a class in the file, and properties are defined as class members.</span></span> <span data-ttu-id="a9ff6-105">Aby uzyskać więcej informacji na temat schematów używanych w pliku MOF, zobacz [publicznych schematu zasobów](./public-resource-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a9ff6-105">For more information about the schema used in the MOF file, see [Public Resource Schema](./public-resource-schema.md).</span></span>

## <a name="example-mof-file"></a><span data-ttu-id="a9ff6-106">Przykładowy plik MOF</span><span class="sxs-lookup"><span data-stu-id="a9ff6-106">Example MOF file</span></span>

<span data-ttu-id="a9ff6-107">Następujący plik definiuje usług i zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-107">The following file defines Service and Process resources.</span></span> <span data-ttu-id="a9ff6-108">Każdy z tych zasobów odnosi się do obiektu, który może być zarządzany przez zestaw poleceń cmdlet programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-108">Each of these resources corresponds to an object that can be managed by a set of Windows PowerShell cmdlet.</span></span> <span data-ttu-id="a9ff6-109">Właściwości odpowiadają parametry używane przez te polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-109">The properties correspond to parameters used by those cmdlets.</span></span>

<span data-ttu-id="a9ff6-110">Każdy z dwóch zasobów zawiera właściwości, które są typu złożonego.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-110">Each of the two resources contains properties that are of complex type.</span></span> <span data-ttu-id="a9ff6-111">Typy złożone są zdefiniowane zgodnie z klas modyfikować za pomocą `ComplexType` kwalifikator.</span><span class="sxs-lookup"><span data-stu-id="a9ff6-111">The complex types are defined as classes modified with the `ComplexType` qualifier.</span></span>

```csharp

class PswsTest_Service
{
    [Key]      String  ServiceName;
    [Required] String  DisplayName;
    [Required] String  MachineName;
    [Required] String  ServiceType;
    [Required, EmbeddedInstance("PswsTest_DependentService")] String ServicesDependentOn [];
    [Required] Boolean CanPauseAndContinue;
    [Required] Boolean CanShutdown;
    [Required] Boolean CanStop;
    [Required, Etag] String Status;
};

class PswsTest_Process
{
    [Key] SInt32 Id;
    [Required] SInt32 BasePriority;
    [Required, EmbeddedInstance("PowerShell_PSCredential")] String Credential;
    [Required, EmbeddedInstance("PswsTest_ProcessModule")] String Modules[];
    [Required] SInt32 HandleCount;
    [Required] String MachineName;
    [Required] SInt32 MainWindowHandle;
    [Required] String MainWindowTitle;
    [Required] SInt32 NonpagedSystemMemorySize;
    [Required] SInt64 NonpagedSystemMemorySize64;
    [Required] SInt32 PagedMemorySize;
    [Required] SInt64 PagedMemorySize64;
    [Required] SInt32 PagedSystemMemorySize;
    [Required] SInt64 PagedSystemMemorySize64;
    [Required] SInt32 PeakPagedMemorySize;
    [Required] SInt64 PeakPagedMemorySize64;
    [Required] SInt32 PeakWorkingSet;
    [Required] SInt64 PeakWorkingSet64;
    [Required] SInt32 PeakVirtualMemorySize;
    [Required] SInt64 PeakVirtualMemorySize64;
    [Required] SInt32 PrivateMemorySize;
    [Required] SInt64 PrivateMemorySize64;
    [Required] String ProcessName;
    [Required] Boolean Responding;
    [Required] SInt32 SessionId;
    [Required, EmbeddedInstance("PswsTest_ProcessStartInfo")] String StartInfo;
    [Required] SInt32 VirtualMemorySize;
    [Required] SInt64 VirtualMemorySize64;
    [Required] Boolean EnableRaisingEvents;
    [Required] SInt32 WorkingSet;
    [Required] SInt64 WorkingSet64;
};

[ComplexType]
class PswsTest_DependentService
{
    String  ServiceName;
};

[ComplexType]
class PswsTest_ProcessModule
{
    String ModuleName;
    String FileName;
};

[ComplexType]
class PswsTest_ProcessStartInfo
{
    String Verb;
    String Arguments;
    Boolean CreateNoWindow;
    Boolean RedirectStandardInput;
    Boolean RedirectStandardOutput ;
    Boolean RedirectStandardError;
    [EmbeddedInstance("PswsTest_Encoding")] String StandardErrorEncoding;
    [EmbeddedInstance("PswsTest_Encoding")] String StandardOutputEncoding;
    Boolean UseShellExecute;
    String UserName ;
    [EmbeddedInstance("PswsTest_SecureString")] String Password;
    String Domain;
    Boolean LoadUserProfile;
    String FileName;
    String WorkingDirectory ;
    Boolean ErrorDialog ;
    SInt32 ErrorDialogParentHandle;
    String WindowStyle;
};

[ComplexType]
class PswsTest_FileVersionInfo
{
    String Comments;
    String CompanyName;
    SInt32 FileBuildPart;
    String FileDescription;
    sInt32 FileMajorPart;
    SInt32 FileMinorPart;
    String FileName;
    SInt32 FilePrivatePart;
    String FileVersion;
    String InternalName;
    Boolean IsDebug;
    Boolean IsPatched;
    Boolean IsPrivateBuild;
    Boolean IsPreRelease;
    Boolean IsSpecialBuild;
    String Language;
    String LegalCopyright;
    String LegalTrademarks;
    String OriginalFilename;
    String PrivateBuild;
    SInt32 ProductBuildPart;
    SInt32 ProductMajorPart;
    SInt32 ProductMinorPart;
    String ProductName;
    SInt32 ProductPrivatePart;
    String ProductVersion;
    String SpecialBuild;
};

[ComplexType]
class PswsTest_Encoding
{
    String BodyName;
    String EncodingName;
    String HeaderName;
    String WebName;
    SInt32 WindowsCodePage;
    Boolean IsBrowserDisplay;
    Boolean IsBrowserSave;
    Boolean IsMailNewsDisplay;
    Boolean IsMailNewsSave;
    Boolean IsSingleByte;
    [EmbeddedInstance("PswsTest_EncoderFallback")] String EncoderFallback;
    [EmbeddedInstance("PswsTest_DecoderFallback")] String DecoderFallback;
    Boolean IsReadOnly;
    SInt32 CodePage;
};

[ComplexType]
class PswsTest_EncoderFallback
{
    SInt32 MaxCharCount;
};

[ComplexType]
class PswsTest_DecoderFallback
{
    SInt32 MaxCharCount;
};

[ComplexType]
class PswsTest_SecureString
{
    SInt32 Length;
};

[ComplexType]
class PswsTest_ProcessThread
{
    SInt32 BasePriority;
    SInt32 CurrentPriority;
    SInt32 Id;
    SInt32 IdealProcessor;
    String PriorityLevel;
    SInt32 StartAddress;
    String ThreadState;
    String WaitReason;
    SInt32 ProcessorAffinity;
};

[ComplexType]
class PswsTest_Stream
{
    Boolean CanRead;
    Boolean CanSeek;
    Boolean CanTimeout;
    Boolean CanWrite;
    SInt64 Length;
    SInt64 Position;
    SInt32 ReadTimeout;
    SInt32 WriteTimeout;
};

```

## <a name="see-also"></a><span data-ttu-id="a9ff6-112">Zobacz też</span><span class="sxs-lookup"><span data-stu-id="a9ff6-112">See Also</span></span>

[<span data-ttu-id="a9ff6-113">Tworzenie usługi sieci Web OData zarządzania</span><span class="sxs-lookup"><span data-stu-id="a9ff6-113">Creating a Management OData Web Service</span></span>](./creating-a-management-odata-web-service.md)

[<span data-ttu-id="a9ff6-114">Zasób publicznego schematu</span><span class="sxs-lookup"><span data-stu-id="a9ff6-114">Public Resource Schema</span></span>](./public-resource-schema.md)