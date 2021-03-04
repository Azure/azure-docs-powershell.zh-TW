---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 46fff0df9eddc417f823aa7b0243824befb974e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907242"
---
# <span data-ttu-id="58906-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="58906-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="58906-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58906-102">SYNOPSIS</span></span>
<span data-ttu-id="58906-103">修改 Azure 儲存體 Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="58906-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="58906-104">語法</span><span class="sxs-lookup"><span data-stu-id="58906-104">SYNTAX</span></span>

### <span data-ttu-id="58906-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="58906-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58906-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="58906-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58906-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="58906-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58906-108">描述</span><span class="sxs-lookup"><span data-stu-id="58906-108">DESCRIPTION</span></span>
<span data-ttu-id="58906-109">**Update-AzStorageBlobServiceProperty Cmdlet** 會修改 Azure 儲存體 Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="58906-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="58906-110">例子</span><span class="sxs-lookup"><span data-stu-id="58906-110">EXAMPLES</span></span>

### <span data-ttu-id="58906-111">範例 1：將 Blob 服務 DefaultServiceVersion 設定為 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="58906-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="58906-112">此命令將 DefaultServiceVersion Blob 服務設定為 2018-03-28。</span><span class="sxs-lookup"><span data-stu-id="58906-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="58906-113">範例 2：在儲存帳戶的 Blob 服務上啟用 Changefeed</span><span class="sxs-lookup"><span data-stu-id="58906-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="58906-114">此命令可讓 Azure Blob 儲存體中的儲存帳戶變更進紙支援之 Blob 服務上的 Changefeed 運作方式為聆聽 GPv2 或 Blob 儲存帳戶的任何 Blob 層級建立、修改或刪除事件。</span><span class="sxs-lookup"><span data-stu-id="58906-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="58906-115">接著，它會針對儲存在儲存帳戶內$blobchangefeed容器的 Blob，輸出已排序的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="58906-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="58906-116">序列化變更會以 Apache Avro 檔案的方式保留，而且可以非同步且增量地處理。</span><span class="sxs-lookup"><span data-stu-id="58906-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="58906-117">範例 3：啟用儲存帳戶的 Blob 服務版本</span><span class="sxs-lookup"><span data-stu-id="58906-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="58906-118">此命令可啟用儲存空間帳戶的 Blob 服務版本</span><span class="sxs-lookup"><span data-stu-id="58906-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="58906-119">參數</span><span class="sxs-lookup"><span data-stu-id="58906-119">PARAMETERS</span></span>

### <span data-ttu-id="58906-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58906-120">-DefaultProfile</span></span>
<span data-ttu-id="58906-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58906-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58906-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="58906-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="58906-123">要設定的預設服務版本</span><span class="sxs-lookup"><span data-stu-id="58906-123">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="58906-124">-EnableChangeFeed</span></span>
<span data-ttu-id="58906-125">設定為 $true 以啟用儲存帳戶的變更資料$false。</span><span class="sxs-lookup"><span data-stu-id="58906-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="58906-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="58906-127">如果設為 True，則啟用或設定版本設定。</span><span class="sxs-lookup"><span data-stu-id="58906-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58906-128">-ResourceGroupName</span></span>
<span data-ttu-id="58906-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="58906-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58906-130">-ResourceId</span></span>
<span data-ttu-id="58906-131">輸入儲存帳戶資源識別碼或 Blob 服務屬性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="58906-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58906-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="58906-132">-StorageAccount</span></span>
<span data-ttu-id="58906-133">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="58906-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58906-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="58906-134">-StorageAccountName</span></span>
<span data-ttu-id="58906-135">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="58906-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-136">-確認</span><span class="sxs-lookup"><span data-stu-id="58906-136">-Confirm</span></span>
<span data-ttu-id="58906-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58906-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58906-138">-WhatIf</span></span>
<span data-ttu-id="58906-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58906-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58906-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58906-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58906-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58906-141">CommonParameters</span></span>
<span data-ttu-id="58906-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58906-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58906-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="58906-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58906-144">輸入</span><span class="sxs-lookup"><span data-stu-id="58906-144">INPUTS</span></span>

### <span data-ttu-id="58906-145">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58906-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="58906-146">System.String</span><span class="sxs-lookup"><span data-stu-id="58906-146">System.String</span></span>

## <span data-ttu-id="58906-147">輸出</span><span class="sxs-lookup"><span data-stu-id="58906-147">OUTPUTS</span></span>

### <span data-ttu-id="58906-148">Microsoft.Azure.Commands.management.storage.models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="58906-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="58906-149">筆記</span><span class="sxs-lookup"><span data-stu-id="58906-149">NOTES</span></span>

## <span data-ttu-id="58906-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="58906-150">RELATED LINKS</span></span>
