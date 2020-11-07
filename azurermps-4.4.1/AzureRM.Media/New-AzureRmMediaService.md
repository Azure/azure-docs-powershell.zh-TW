---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625146"
---
# <span data-ttu-id="042c2-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="042c2-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="042c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="042c2-102">SYNOPSIS</span></span>
<span data-ttu-id="042c2-103">如果媒體服務已存在，就會建立媒體服務，所有其屬性都會隨著提供的輸入而更新。</span><span class="sxs-lookup"><span data-stu-id="042c2-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="042c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="042c2-104">SYNTAX</span></span>

### <span data-ttu-id="042c2-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="042c2-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="042c2-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="042c2-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="042c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="042c2-107">DESCRIPTION</span></span>
<span data-ttu-id="042c2-108">**新的-AzureRmMediaService** Cmdlet 會建立媒體服務。</span><span class="sxs-lookup"><span data-stu-id="042c2-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="042c2-109">如果媒體服務已存在，此 Cmdlet 會更新其屬性。</span><span class="sxs-lookup"><span data-stu-id="042c2-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="042c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="042c2-110">EXAMPLES</span></span>

### <span data-ttu-id="042c2-111">Example1：僅使用主要儲存空間帳戶建立媒體服務</span><span class="sxs-lookup"><span data-stu-id="042c2-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="042c2-112">這個範例示範如何使用僅指定主要儲存空間帳戶來建立媒體服務。</span><span class="sxs-lookup"><span data-stu-id="042c2-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="042c2-113">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="042c2-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="042c2-114">範例2：使用多個儲存空間建立媒體服務</span><span class="sxs-lookup"><span data-stu-id="042c2-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="042c2-115">此範例說明如何使用多個儲存空間帳戶建立媒體服務。</span><span class="sxs-lookup"><span data-stu-id="042c2-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="042c2-116">此腳本會使用幾個其他的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="042c2-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="042c2-117">參數</span><span class="sxs-lookup"><span data-stu-id="042c2-117">PARAMETERS</span></span>

### <span data-ttu-id="042c2-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="042c2-118">-AccountName</span></span>
<span data-ttu-id="042c2-119">指定此 Cmdlet 所建立之媒體服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="042c2-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-120">-位置</span><span class="sxs-lookup"><span data-stu-id="042c2-120">-Location</span></span>
<span data-ttu-id="042c2-121">指定此 Cmdlet 在其中建立媒體服務的區域。</span><span class="sxs-lookup"><span data-stu-id="042c2-121">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="042c2-123">指定指派媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="042c2-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="042c2-124">-StorageAccountId</span></span>
<span data-ttu-id="042c2-125">指定與媒體服務帳戶相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="042c2-125">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="042c2-126">-StorageAccounts</span></span>
<span data-ttu-id="042c2-127">指定要與媒體服務建立關聯的儲存空間帳戶陣列。</span><span class="sxs-lookup"><span data-stu-id="042c2-127">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-128">-標記</span><span class="sxs-lookup"><span data-stu-id="042c2-128">-Tags</span></span>
<span data-ttu-id="042c2-129">指定媒體服務的標記。</span><span class="sxs-lookup"><span data-stu-id="042c2-129">Specifies tags for the media service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-130">-確認</span><span class="sxs-lookup"><span data-stu-id="042c2-130">-Confirm</span></span>
<span data-ttu-id="042c2-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="042c2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="042c2-132">-WhatIf</span></span>
<span data-ttu-id="042c2-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="042c2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="042c2-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="042c2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042c2-135">-DefaultProfile</span></span>
<span data-ttu-id="042c2-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="042c2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042c2-137">CommonParameters</span></span>
<span data-ttu-id="042c2-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="042c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042c2-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="042c2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042c2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="042c2-140">INPUTS</span></span>

## <span data-ttu-id="042c2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="042c2-141">OUTPUTS</span></span>

### <span data-ttu-id="042c2-142">PSMediaService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="042c2-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="042c2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="042c2-143">NOTES</span></span>

## <span data-ttu-id="042c2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="042c2-144">RELATED LINKS</span></span>

[<span data-ttu-id="042c2-145">AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="042c2-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="042c2-146">移除-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="042c2-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="042c2-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="042c2-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


