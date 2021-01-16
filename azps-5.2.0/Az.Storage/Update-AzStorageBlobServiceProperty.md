---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282188"
---
# <span data-ttu-id="cfb38-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfb38-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="cfb38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfb38-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb38-103">修改 Azure 儲存區 Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb38-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="cfb38-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfb38-104">SYNTAX</span></span>

### <span data-ttu-id="cfb38-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="cfb38-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfb38-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cfb38-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfb38-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb38-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfb38-108">說明</span><span class="sxs-lookup"><span data-stu-id="cfb38-108">DESCRIPTION</span></span>
<span data-ttu-id="cfb38-109">**AzStorageBlobServiceProperty** Cmdlet 會修改 Azure Storage Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb38-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="cfb38-110">示例</span><span class="sxs-lookup"><span data-stu-id="cfb38-110">EXAMPLES</span></span>

### <span data-ttu-id="cfb38-111">範例1：將 Blob 服務 DefaultServiceVersion 設定為2018-03-28</span><span class="sxs-lookup"><span data-stu-id="cfb38-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="cfb38-112">這個命令會將 Blob 服務的 DefaultServiceVersion 設定為2018-03-28。</span><span class="sxs-lookup"><span data-stu-id="cfb38-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="cfb38-113">範例2：在儲存空間帳戶的 Blob 服務上啟用 Changefeed</span><span class="sxs-lookup"><span data-stu-id="cfb38-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="cfb38-114">這個命令可讓 Changefeed 在儲存帳戶的 Blob 服務上變更 [Azure Blob 儲存空間] 中的摘要支援，方法是透過偵聽任何 Blob 層級建立、修改或刪除事件的 GPv2 或 Blob 儲存空間帳戶來運作。</span><span class="sxs-lookup"><span data-stu-id="cfb38-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="cfb38-115">接著，它會針對儲存在儲存空間帳戶內 $blobchangefeed 容器中的 blob 輸出已排序的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="cfb38-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="cfb38-116">序列化的變更會保留為 Apache Avro 檔案，而且可以以非同步和增量方式進行處理。</span><span class="sxs-lookup"><span data-stu-id="cfb38-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="cfb38-117">範例3：在儲存空間帳戶的 Blob 服務上啟用版本設定</span><span class="sxs-lookup"><span data-stu-id="cfb38-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="cfb38-118">這個命令可在儲存空間帳戶的 Blob 服務上啟用版本設定</span><span class="sxs-lookup"><span data-stu-id="cfb38-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="cfb38-119">參數</span><span class="sxs-lookup"><span data-stu-id="cfb38-119">PARAMETERS</span></span>

### <span data-ttu-id="cfb38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb38-120">-DefaultProfile</span></span>
<span data-ttu-id="cfb38-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfb38-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb38-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="cfb38-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="cfb38-123">要設定的預設服務版本</span><span class="sxs-lookup"><span data-stu-id="cfb38-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="cfb38-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="cfb38-124">-EnableChangeFeed</span></span>
<span data-ttu-id="cfb38-125">[啟用變更儲存空間的摘要記錄] 設定為 [$true]，停用將摘要記錄設為 [$false]。</span><span class="sxs-lookup"><span data-stu-id="cfb38-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="cfb38-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="cfb38-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="cfb38-127">如果設為 true，則會啟用或設定版本設定。</span><span class="sxs-lookup"><span data-stu-id="cfb38-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="cfb38-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfb38-128">-ResourceGroupName</span></span>
<span data-ttu-id="cfb38-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cfb38-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="cfb38-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb38-130">-ResourceId</span></span>
<span data-ttu-id="cfb38-131">輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="cfb38-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="cfb38-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfb38-132">-StorageAccount</span></span>
<span data-ttu-id="cfb38-133">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="cfb38-133">Storage account object</span></span>

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

### <span data-ttu-id="cfb38-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cfb38-134">-StorageAccountName</span></span>
<span data-ttu-id="cfb38-135">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cfb38-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="cfb38-136">-確認</span><span class="sxs-lookup"><span data-stu-id="cfb38-136">-Confirm</span></span>
<span data-ttu-id="cfb38-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cfb38-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfb38-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfb38-138">-WhatIf</span></span>
<span data-ttu-id="cfb38-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cfb38-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfb38-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cfb38-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfb38-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb38-141">CommonParameters</span></span>
<span data-ttu-id="cfb38-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfb38-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb38-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cfb38-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb38-144">輸入</span><span class="sxs-lookup"><span data-stu-id="cfb38-144">INPUTS</span></span>

### <span data-ttu-id="cfb38-145">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="cfb38-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cfb38-146">System.object</span><span class="sxs-lookup"><span data-stu-id="cfb38-146">System.String</span></span>

## <span data-ttu-id="cfb38-147">輸出</span><span class="sxs-lookup"><span data-stu-id="cfb38-147">OUTPUTS</span></span>

### <span data-ttu-id="cfb38-148">PSBlobServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="cfb38-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="cfb38-149">筆記</span><span class="sxs-lookup"><span data-stu-id="cfb38-149">NOTES</span></span>

## <span data-ttu-id="cfb38-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfb38-150">RELATED LINKS</span></span>
