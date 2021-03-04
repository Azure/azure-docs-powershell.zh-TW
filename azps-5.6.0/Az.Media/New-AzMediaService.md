---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: 9ad314046ec9a1f1769042a2e36c64ddb0af0666
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916109"
---
# <span data-ttu-id="0f6b7-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0f6b7-101">New-AzMediaService</span></span>

## <span data-ttu-id="0f6b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6b7-103">如果媒體服務已存在，會建立媒體服務，其所有屬性會隨著提供的輸入更新。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="0f6b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f6b7-104">SYNTAX</span></span>

### <span data-ttu-id="0f6b7-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="0f6b7-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6b7-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="0f6b7-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6b7-107">描述</span><span class="sxs-lookup"><span data-stu-id="0f6b7-107">DESCRIPTION</span></span>
<span data-ttu-id="0f6b7-108">**New-AzMediaService** Cmdlet 會建立媒體服務。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="0f6b7-109">如果媒體服務已存在，此 Cmdlet 會更新其屬性。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="0f6b7-110">例子</span><span class="sxs-lookup"><span data-stu-id="0f6b7-110">EXAMPLES</span></span>

### <span data-ttu-id="0f6b7-111">範例1：僅使用主要儲存空間帳戶建立媒體服務</span><span class="sxs-lookup"><span data-stu-id="0f6b7-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="0f6b7-112">此範例顯示如何建立只指定主要儲存空間帳戶的媒體服務。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="0f6b7-113">此腳本使用數個其他 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="0f6b7-114">範例 2：建立具有多個儲存空間的媒體服務</span><span class="sxs-lookup"><span data-stu-id="0f6b7-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="0f6b7-115">此範例顯示如何使用多個儲存空間帳戶建立媒體服務。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="0f6b7-116">此腳本使用數個其他 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="0f6b7-117">參數</span><span class="sxs-lookup"><span data-stu-id="0f6b7-117">PARAMETERS</span></span>

### <span data-ttu-id="0f6b7-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f6b7-118">-AccountName</span></span>
<span data-ttu-id="0f6b7-119">指定此 Cmdlet 所建立之媒體服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0f6b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6b7-120">-DefaultProfile</span></span>
<span data-ttu-id="0f6b7-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0f6b7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6b7-122">-位置</span><span class="sxs-lookup"><span data-stu-id="0f6b7-122">-Location</span></span>
<span data-ttu-id="0f6b7-123">指定此 Cmdlet 建立媒體服務的區域。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="0f6b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f6b7-125">指定媒體服務指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="0f6b7-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0f6b7-126">-StorageAccountId</span></span>
<span data-ttu-id="0f6b7-127">指定與媒體服務帳戶相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-127">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="0f6b7-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="0f6b7-128">-StorageAccounts</span></span>
<span data-ttu-id="0f6b7-129">指定要與媒體服務建立關聯的儲存空間帳戶陣列。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-129">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="0f6b7-130">-標記</span><span class="sxs-lookup"><span data-stu-id="0f6b7-130">-Tag</span></span>
<span data-ttu-id="0f6b7-131">與媒體服務帳戶相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="0f6b7-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0f6b7-132">-Confirm</span></span>
<span data-ttu-id="0f6b7-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6b7-134">-WhatIf</span></span>
<span data-ttu-id="0f6b7-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f6b7-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6b7-137">CommonParameters</span></span>
<span data-ttu-id="0f6b7-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6b7-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0f6b7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6b7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0f6b7-140">INPUTS</span></span>

### <span data-ttu-id="0f6b7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0f6b7-141">System.String</span></span>

### <span data-ttu-id="0f6b7-142">Microsoft.Azure.Commands.Media.models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="0f6b7-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="0f6b7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0f6b7-143">OUTPUTS</span></span>

### <span data-ttu-id="0f6b7-144">Microsoft.Azure.Commands.Media.models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="0f6b7-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="0f6b7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0f6b7-145">NOTES</span></span>

## <span data-ttu-id="0f6b7-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f6b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="0f6b7-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0f6b7-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="0f6b7-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0f6b7-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="0f6b7-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0f6b7-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


