---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274943"
---
# <span data-ttu-id="efa3c-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="efa3c-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="efa3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efa3c-102">SYNOPSIS</span></span>
<span data-ttu-id="efa3c-103">從頁面 blob 快照開始增量複製作業至指定的目的地頁面 blob。</span><span class="sxs-lookup"><span data-stu-id="efa3c-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="efa3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="efa3c-104">SYNTAX</span></span>

### <span data-ttu-id="efa3c-105">ContainerInstance (預設) </span><span class="sxs-lookup"><span data-stu-id="efa3c-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa3c-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="efa3c-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa3c-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="efa3c-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa3c-108">容器</span><span class="sxs-lookup"><span data-stu-id="efa3c-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa3c-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="efa3c-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa3c-110">說明</span><span class="sxs-lookup"><span data-stu-id="efa3c-110">DESCRIPTION</span></span>
<span data-ttu-id="efa3c-111">從頁面 blob 快照開始增量複製作業至指定的目的地頁面 blob。</span><span class="sxs-lookup"><span data-stu-id="efa3c-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="efa3c-112">如需更多有關功能的詳細資訊，請參閱 https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob 。</span><span class="sxs-lookup"><span data-stu-id="efa3c-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="efa3c-113">示例</span><span class="sxs-lookup"><span data-stu-id="efa3c-113">EXAMPLES</span></span>

### <span data-ttu-id="efa3c-114">範例1：根據 blob 名稱和快照時間來啟動增量複製操作</span><span class="sxs-lookup"><span data-stu-id="efa3c-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="efa3c-115">這個命令會依 blob 名稱和快照時間啟動增量複製操作</span><span class="sxs-lookup"><span data-stu-id="efa3c-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="efa3c-116">範例2：使用來源 uri 開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="efa3c-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="efa3c-117">這個命令會使用來源 uri 開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="efa3c-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="efa3c-118">範例3：使用容器管線從 GetAzureStorageContainer 開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="efa3c-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="efa3c-119">這個命令從 GetAzureStorageContainer 使用容器管線開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="efa3c-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="efa3c-120">範例4：從 CloudPageBlob 物件開始增量複製作業至含 blob 名稱的目標 blob</span><span class="sxs-lookup"><span data-stu-id="efa3c-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="efa3c-121">這個命令從 CloudPageBlob 物件開始增量複製作業至含 blob 名稱的目標 blob</span><span class="sxs-lookup"><span data-stu-id="efa3c-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="efa3c-122">參數</span><span class="sxs-lookup"><span data-stu-id="efa3c-122">PARAMETERS</span></span>

### <span data-ttu-id="efa3c-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="efa3c-123">-AbsoluteUri</span></span>
<span data-ttu-id="efa3c-124">來源的絕對 Uri。</span><span class="sxs-lookup"><span data-stu-id="efa3c-124">Absolute Uri to the source.</span></span> <span data-ttu-id="efa3c-125">請注意，如果來源需要的話，必須在 Uri 中提供認證。</span><span class="sxs-lookup"><span data-stu-id="efa3c-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efa3c-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="efa3c-127">用戶端每個要求的最大執行時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="efa3c-127">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="efa3c-128">-CloudBlob</span></span>
<span data-ttu-id="efa3c-129">從 Azure 存儲用戶端文件庫 CloudBlob 物件。</span><span class="sxs-lookup"><span data-stu-id="efa3c-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="efa3c-130">您可以建立它或使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efa3c-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="efa3c-131">-CloudBlobContainer</span></span>
<span data-ttu-id="efa3c-132">從 Azure 存儲用戶端文件庫 CloudBlobContainer 物件。</span><span class="sxs-lookup"><span data-stu-id="efa3c-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="efa3c-133">您可以建立它或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efa3c-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="efa3c-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="efa3c-135">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="efa3c-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="efa3c-136">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="efa3c-136">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-137">-內容</span><span class="sxs-lookup"><span data-stu-id="efa3c-137">-Context</span></span>
<span data-ttu-id="efa3c-138">來源 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="efa3c-138">Source Azure Storage Context.</span></span> <span data-ttu-id="efa3c-139">您可以 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="efa3c-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa3c-140">-DefaultProfile</span></span>
<span data-ttu-id="efa3c-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efa3c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="efa3c-142">-DestBlob</span></span>
<span data-ttu-id="efa3c-143">目的地 blob 名稱</span><span class="sxs-lookup"><span data-stu-id="efa3c-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="efa3c-144">-DestCloudBlob</span></span>
<span data-ttu-id="efa3c-145">目的地 CloudBlob 物件</span><span class="sxs-lookup"><span data-stu-id="efa3c-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="efa3c-146">-DestContainer</span></span>
<span data-ttu-id="efa3c-147">目的地容器名稱</span><span class="sxs-lookup"><span data-stu-id="efa3c-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-148">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="efa3c-148">-DestContext</span></span>
<span data-ttu-id="efa3c-149">[目的地 Azure 儲存區] 內容。</span><span class="sxs-lookup"><span data-stu-id="efa3c-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="efa3c-150">您可以 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="efa3c-150">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efa3c-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="efa3c-152">伺服器針對每個要求的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="efa3c-152">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="efa3c-153">-SrcBlob</span></span>
<span data-ttu-id="efa3c-154">來源頁面 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="efa3c-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="efa3c-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="efa3c-156">來源頁面 blob 快照時間。</span><span class="sxs-lookup"><span data-stu-id="efa3c-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="efa3c-157">-SrcContainer</span></span>
<span data-ttu-id="efa3c-158">來源容器名稱</span><span class="sxs-lookup"><span data-stu-id="efa3c-158">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa3c-159">-確認</span><span class="sxs-lookup"><span data-stu-id="efa3c-159">-Confirm</span></span>
<span data-ttu-id="efa3c-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efa3c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa3c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa3c-161">-WhatIf</span></span>
<span data-ttu-id="efa3c-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efa3c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa3c-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efa3c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa3c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa3c-164">CommonParameters</span></span>
<span data-ttu-id="efa3c-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efa3c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa3c-166">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efa3c-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa3c-167">輸入</span><span class="sxs-lookup"><span data-stu-id="efa3c-167">INPUTS</span></span>

### <span data-ttu-id="efa3c-168">[CloudPageBlob]。</span><span class="sxs-lookup"><span data-stu-id="efa3c-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="efa3c-169">[CloudBlobContainer]。</span><span class="sxs-lookup"><span data-stu-id="efa3c-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="efa3c-170">System.object</span><span class="sxs-lookup"><span data-stu-id="efa3c-170">System.String</span></span>

### <span data-ttu-id="efa3c-171">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="efa3c-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="efa3c-172">輸出</span><span class="sxs-lookup"><span data-stu-id="efa3c-172">OUTPUTS</span></span>

### <span data-ttu-id="efa3c-173">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="efa3c-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="efa3c-174">筆記</span><span class="sxs-lookup"><span data-stu-id="efa3c-174">NOTES</span></span>

## <span data-ttu-id="efa3c-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="efa3c-175">RELATED LINKS</span></span>
