---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967990"
---
# <span data-ttu-id="b5798-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="b5798-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="b5798-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5798-102">SYNOPSIS</span></span>
<span data-ttu-id="b5798-103">取得虛擬機器之最新可用擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5798-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="b5798-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5798-104">SYNTAX</span></span>

### <span data-ttu-id="b5798-105">ListLatestExtensions (預設) </span><span class="sxs-lookup"><span data-stu-id="b5798-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5798-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="b5798-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5798-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="b5798-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5798-108">說明</span><span class="sxs-lookup"><span data-stu-id="b5798-108">DESCRIPTION</span></span>
<span data-ttu-id="b5798-109">AzureVMAvailableExtension Cmdlet 會取得虛擬機器最新可用擴充 **功能** 的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5798-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="b5798-110">示例</span><span class="sxs-lookup"><span data-stu-id="b5798-110">EXAMPLES</span></span>

### <span data-ttu-id="b5798-111">範例1：取得最新可用延伸的資訊</span><span class="sxs-lookup"><span data-stu-id="b5798-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="b5798-112">這個命令會取得所有虛擬機器的最新可用擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5798-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="b5798-113">範例2：從指定的副檔名取得資訊</span><span class="sxs-lookup"><span data-stu-id="b5798-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="b5798-114">這個命令會從名為 VMAccessAgent 及名為 Microsoft. 電腦的發行商的所有版本中取得資訊。</span><span class="sxs-lookup"><span data-stu-id="b5798-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="b5798-115">範例3：透過版本號碼從特定的虛擬機器延伸取得資訊</span><span class="sxs-lookup"><span data-stu-id="b5798-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="b5798-116">這個命令會取得名為 VMAccessAgent 和名為 Microsoft. 延伸版本1.0.3 的副檔名的資訊。</span><span class="sxs-lookup"><span data-stu-id="b5798-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="b5798-117">參數</span><span class="sxs-lookup"><span data-stu-id="b5798-117">PARAMETERS</span></span>

### <span data-ttu-id="b5798-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="b5798-118">-AllVersions</span></span>
<span data-ttu-id="b5798-119">表示此 Cmdlet 列出延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="b5798-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b5798-120">-ExtensionName</span></span>
<span data-ttu-id="b5798-121">指定可用副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5798-121">Specifies the name of the available extension.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5798-122">-InformationAction</span></span>
<span data-ttu-id="b5798-123">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b5798-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5798-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b5798-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5798-125">持續</span><span class="sxs-lookup"><span data-stu-id="b5798-125">Continue</span></span>
- <span data-ttu-id="b5798-126">理會</span><span class="sxs-lookup"><span data-stu-id="b5798-126">Ignore</span></span>
- <span data-ttu-id="b5798-127">看</span><span class="sxs-lookup"><span data-stu-id="b5798-127">Inquire</span></span>
- <span data-ttu-id="b5798-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5798-128">SilentlyContinue</span></span>
- <span data-ttu-id="b5798-129">停止</span><span class="sxs-lookup"><span data-stu-id="b5798-129">Stop</span></span>
- <span data-ttu-id="b5798-130">封存</span><span class="sxs-lookup"><span data-stu-id="b5798-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5798-131">-InformationVariable</span></span>
<span data-ttu-id="b5798-132">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b5798-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b5798-133">-Profile</span></span>
<span data-ttu-id="b5798-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b5798-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5798-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b5798-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b5798-136">-Publisher</span></span>
<span data-ttu-id="b5798-137">指定副檔名的發行者。</span><span class="sxs-lookup"><span data-stu-id="b5798-137">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-138">-版本</span><span class="sxs-lookup"><span data-stu-id="b5798-138">-Version</span></span>
<span data-ttu-id="b5798-139">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="b5798-139">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5798-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5798-140">CommonParameters</span></span>
<span data-ttu-id="b5798-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5798-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5798-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5798-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5798-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b5798-143">INPUTS</span></span>

## <span data-ttu-id="b5798-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b5798-144">OUTPUTS</span></span>

## <span data-ttu-id="b5798-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b5798-145">NOTES</span></span>

## <span data-ttu-id="b5798-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5798-146">RELATED LINKS</span></span>

