---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc15650b9a3cf16b1448b5e971669fbd37733b94
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441984"
---
# <span data-ttu-id="3b7e5-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="3b7e5-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="3b7e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7e5-103">從頁面 blob 快照開始增量複製作業至指定的目的地頁面 blob。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="3b7e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b7e5-104">SYNTAX</span></span>

### <span data-ttu-id="3b7e5-105">ContainerInstance (預設) </span><span class="sxs-lookup"><span data-stu-id="3b7e5-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b7e5-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="3b7e5-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b7e5-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3b7e5-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b7e5-108">容器</span><span class="sxs-lookup"><span data-stu-id="3b7e5-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b7e5-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="3b7e5-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3b7e5-110">說明</span><span class="sxs-lookup"><span data-stu-id="3b7e5-110">DESCRIPTION</span></span>
<span data-ttu-id="3b7e5-111">從頁面 blob 快照開始增量複製作業至指定的目的地頁面 blob。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="3b7e5-112">如需更多有關功能的詳細資訊，請參閱 https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob 。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="3b7e5-113">示例</span><span class="sxs-lookup"><span data-stu-id="3b7e5-113">EXAMPLES</span></span>

### <span data-ttu-id="3b7e5-114">範例1：根據 blob 名稱和快照時間來啟動增量複製操作</span><span class="sxs-lookup"><span data-stu-id="3b7e5-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="3b7e5-115">這個命令會依 blob 名稱和快照時間啟動增量複製操作</span><span class="sxs-lookup"><span data-stu-id="3b7e5-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="3b7e5-116">範例2：使用來源 uri 開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="3b7e5-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="3b7e5-117">這個命令會使用來源 uri 開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="3b7e5-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="3b7e5-118">範例3：使用容器管線從 GetAzureStorageContainer 開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="3b7e5-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="3b7e5-119">這個命令從 GetAzureStorageContainer 使用容器管線開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="3b7e5-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="3b7e5-120">範例4：從 CloudPageBlob 物件開始增量複製作業至含 blob 名稱的目標 blob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="3b7e5-121">這個命令從 CloudPageBlob 物件開始增量複製作業至含 blob 名稱的目標 blob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="3b7e5-122">參數</span><span class="sxs-lookup"><span data-stu-id="3b7e5-122">PARAMETERS</span></span>

### <span data-ttu-id="3b7e5-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="3b7e5-123">-AbsoluteUri</span></span>
<span data-ttu-id="3b7e5-124">來源的絕對 Uri。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-124">Absolute Uri to the source.</span></span>
<span data-ttu-id="3b7e5-125">請注意，如果來源需要的話，必須在 Uri 中提供認證。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b7e5-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3b7e5-127">用戶端每個要求的最大執行時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-127">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-128">-CloudBlob</span></span>
<span data-ttu-id="3b7e5-129">從 Azure 存儲用戶端文件庫 CloudBlob 物件。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-129">CloudBlob object from Azure Storage Client library.</span></span>
<span data-ttu-id="3b7e5-130">您可以建立它或使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3b7e5-131">-CloudBlobContainer</span></span>
<span data-ttu-id="3b7e5-132">從 Azure 存儲用戶端文件庫 CloudBlobContainer 物件。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-132">CloudBlobContainer object from Azure Storage Client library.</span></span>
<span data-ttu-id="3b7e5-133">您可以建立它或使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3b7e5-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3b7e5-135">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="3b7e5-136">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-136">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-137">-內容</span><span class="sxs-lookup"><span data-stu-id="3b7e5-137">-Context</span></span>
<span data-ttu-id="3b7e5-138">來源 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-138">Source Azure Storage Context.</span></span>
<span data-ttu-id="3b7e5-139">您可以 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-140">-DestBlob</span></span>
<span data-ttu-id="3b7e5-141">目的地 blob 名稱</span><span class="sxs-lookup"><span data-stu-id="3b7e5-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-142">-DestCloudBlob</span></span>
<span data-ttu-id="3b7e5-143">目的地 CloudBlob 物件</span><span class="sxs-lookup"><span data-stu-id="3b7e5-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="3b7e5-144">-DestContainer</span></span>
<span data-ttu-id="3b7e5-145">目的地容器名稱</span><span class="sxs-lookup"><span data-stu-id="3b7e5-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-146">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="3b7e5-146">-DestContext</span></span>
<span data-ttu-id="3b7e5-147">[目的地 Azure 儲存區] 內容。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-147">Destination Azure Storage Context.</span></span>
<span data-ttu-id="3b7e5-148">您可以 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b7e5-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3b7e5-150">伺服器針對每個要求的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-150">The server time out for each request in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-151">-SrcBlob</span></span>
<span data-ttu-id="3b7e5-152">來源頁面 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3b7e5-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="3b7e5-154">來源頁面 blob 快照時間。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="3b7e5-155">-SrcContainer</span></span>
<span data-ttu-id="3b7e5-156">來源容器名稱</span><span class="sxs-lookup"><span data-stu-id="3b7e5-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-157">-確認</span><span class="sxs-lookup"><span data-stu-id="3b7e5-157">-Confirm</span></span>
<span data-ttu-id="3b7e5-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7e5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b7e5-159">-WhatIf</span></span>
<span data-ttu-id="3b7e5-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b7e5-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="3b7e5-162">輸入</span><span class="sxs-lookup"><span data-stu-id="3b7e5-162">INPUTS</span></span>

### <span data-ttu-id="3b7e5-163">[WindowsAzure] CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="3b7e5-163">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="3b7e5-164">WindowsAzure. CloudBlobContainer. WindowsAzure.. 常見... AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3b7e5-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="3b7e5-165">輸出</span><span class="sxs-lookup"><span data-stu-id="3b7e5-165">OUTPUTS</span></span>

### <span data-ttu-id="3b7e5-166">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="3b7e5-166">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="3b7e5-167">筆記</span><span class="sxs-lookup"><span data-stu-id="3b7e5-167">NOTES</span></span>

## <span data-ttu-id="3b7e5-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b7e5-168">RELATED LINKS</span></span>

