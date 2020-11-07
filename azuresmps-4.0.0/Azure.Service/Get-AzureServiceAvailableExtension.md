---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967052"
---
# <span data-ttu-id="3b8b4-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="3b8b4-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="3b8b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8b4-103">取得託管服務可用擴充功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="3b8b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b8b4-104">SYNTAX</span></span>

### <span data-ttu-id="3b8b4-105">ListLatestExtensions (預設) </span><span class="sxs-lookup"><span data-stu-id="3b8b4-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8b4-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="3b8b4-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8b4-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="3b8b4-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b8b4-108">說明</span><span class="sxs-lookup"><span data-stu-id="3b8b4-108">DESCRIPTION</span></span>
<span data-ttu-id="3b8b4-109">**AzureServiceAvailableExtension** Cmdlet 會取得託管服務最新可用延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="3b8b4-110">示例</span><span class="sxs-lookup"><span data-stu-id="3b8b4-110">EXAMPLES</span></span>

### <span data-ttu-id="3b8b4-111">範例1：取得可用的延伸</span><span class="sxs-lookup"><span data-stu-id="3b8b4-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="3b8b4-112">這個命令會取得所有可用的延伸。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="3b8b4-113">範例2：取得指定命名空間中的延伸</span><span class="sxs-lookup"><span data-stu-id="3b8b4-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="3b8b4-114">這個命令會在指定的命名空間中取得指定名稱的延伸。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="3b8b4-115">範例3：取得特定的延伸版本</span><span class="sxs-lookup"><span data-stu-id="3b8b4-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="3b8b4-116">此命令會取得特定副檔名版本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="3b8b4-117">參數</span><span class="sxs-lookup"><span data-stu-id="3b8b4-117">PARAMETERS</span></span>

### <span data-ttu-id="3b8b4-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="3b8b4-118">-AllVersions</span></span>
<span data-ttu-id="3b8b4-119">表示此 Cmdlet 會取得副檔名的所有版本。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

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

### <span data-ttu-id="3b8b4-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="3b8b4-120">-ExtensionName</span></span>
<span data-ttu-id="3b8b4-121">指定副檔名。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-121">Specifies the extension name.</span></span>

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

### <span data-ttu-id="3b8b4-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3b8b4-122">-InformationAction</span></span>
<span data-ttu-id="3b8b4-123">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b8b4-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3b8b4-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b8b4-125">持續</span><span class="sxs-lookup"><span data-stu-id="3b8b4-125">Continue</span></span>
- <span data-ttu-id="3b8b4-126">理會</span><span class="sxs-lookup"><span data-stu-id="3b8b4-126">Ignore</span></span>
- <span data-ttu-id="3b8b4-127">看</span><span class="sxs-lookup"><span data-stu-id="3b8b4-127">Inquire</span></span>
- <span data-ttu-id="3b8b4-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b8b4-128">SilentlyContinue</span></span>
- <span data-ttu-id="3b8b4-129">停止</span><span class="sxs-lookup"><span data-stu-id="3b8b4-129">Stop</span></span>
- <span data-ttu-id="3b8b4-130">封存</span><span class="sxs-lookup"><span data-stu-id="3b8b4-130">Suspend</span></span>

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

### <span data-ttu-id="3b8b4-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b8b4-131">-InformationVariable</span></span>
<span data-ttu-id="3b8b4-132">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3b8b4-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3b8b4-133">-Profile</span></span>
<span data-ttu-id="3b8b4-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b8b4-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b8b4-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3b8b4-136">-ProviderNamespace</span></span>
<span data-ttu-id="3b8b4-137">指定延伸提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-137">Specifies the extension provider namespace.</span></span>

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

### <span data-ttu-id="3b8b4-138">-版本</span><span class="sxs-lookup"><span data-stu-id="3b8b4-138">-Version</span></span>
<span data-ttu-id="3b8b4-139">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-139">Specifies the extension version.</span></span>

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

### <span data-ttu-id="3b8b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8b4-140">CommonParameters</span></span>
<span data-ttu-id="3b8b4-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8b4-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b8b4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8b4-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3b8b4-143">INPUTS</span></span>

## <span data-ttu-id="3b8b4-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3b8b4-144">OUTPUTS</span></span>

## <span data-ttu-id="3b8b4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3b8b4-145">NOTES</span></span>

## <span data-ttu-id="3b8b4-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b8b4-146">RELATED LINKS</span></span>

[<span data-ttu-id="3b8b4-147">AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="3b8b4-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


