---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 772e97611d81362ffb3becea8875826110e822a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915010"
---
# <span data-ttu-id="92942-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="92942-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="92942-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92942-102">SYNOPSIS</span></span>
<span data-ttu-id="92942-103">啟動從頁面 Blob 快照到指定目的地頁面 Blob 的增量複製作業。</span><span class="sxs-lookup"><span data-stu-id="92942-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="92942-104">語法</span><span class="sxs-lookup"><span data-stu-id="92942-104">SYNTAX</span></span>

### <span data-ttu-id="92942-105">ContainerInstance (預設) </span><span class="sxs-lookup"><span data-stu-id="92942-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92942-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="92942-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92942-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="92942-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92942-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="92942-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92942-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="92942-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92942-110">描述</span><span class="sxs-lookup"><span data-stu-id="92942-110">DESCRIPTION</span></span>
<span data-ttu-id="92942-111">啟動從頁面 Blob 快照到指定目的地頁面 Blob 的增量複製作業。</span><span class="sxs-lookup"><span data-stu-id="92942-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="92942-112">在 中查看此功能的更多詳細資料 https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob 。</span><span class="sxs-lookup"><span data-stu-id="92942-112">See more details of the feature in https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="92942-113">例子</span><span class="sxs-lookup"><span data-stu-id="92942-113">EXAMPLES</span></span>

### <span data-ttu-id="92942-114">範例 1：根據 Blob 名稱和快照時間啟動增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="92942-115">此命令會啟動按 Blob 名稱和快照時間執行增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="92942-116">範例 2：使用來源 uri 啟動增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="92942-117">此命令會使用來源 uri 啟動增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="92942-118">範例 3：從 GetAzureStorageContainer 使用容器管線開始增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="92942-119">此命令會使用來自 GetAzureStorageContainer 的容器管線啟動增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="92942-120">範例 4：啟動增量複製作業，從 CloudPageBlob 物件到具有 Blob 名稱的目的地 Blob</span><span class="sxs-lookup"><span data-stu-id="92942-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="92942-121">此命令會啟動以 Blob 名稱從 CloudPageBlob 物件到目的地 Blob 的增量複製作業</span><span class="sxs-lookup"><span data-stu-id="92942-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="92942-122">參數</span><span class="sxs-lookup"><span data-stu-id="92942-122">PARAMETERS</span></span>

### <span data-ttu-id="92942-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="92942-123">-AbsoluteUri</span></span>
<span data-ttu-id="92942-124">來源的絕對 Uri。</span><span class="sxs-lookup"><span data-stu-id="92942-124">Absolute Uri to the source.</span></span> <span data-ttu-id="92942-125">請注意，如果來源需要任何認證，應在 Uri 中提供認證。</span><span class="sxs-lookup"><span data-stu-id="92942-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="92942-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92942-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="92942-127">用戶端會針對每個要求的最大執行時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="92942-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="92942-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="92942-128">-CloudBlob</span></span>
<span data-ttu-id="92942-129">來自 Azure 儲存用戶端文件庫的 CloudBlob 物件。</span><span class="sxs-lookup"><span data-stu-id="92942-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="92942-130">您可以建立或Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92942-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="92942-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="92942-131">-CloudBlobContainer</span></span>
<span data-ttu-id="92942-132">來自 Azure 儲存體用戶端庫的 CloudBlobContainer 物件。</span><span class="sxs-lookup"><span data-stu-id="92942-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="92942-133">您可以建立或Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92942-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="92942-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="92942-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="92942-135">同時同步處理工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="92942-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="92942-136">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="92942-136">The default value is 10.</span></span>

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

### <span data-ttu-id="92942-137">-內容</span><span class="sxs-lookup"><span data-stu-id="92942-137">-Context</span></span>
<span data-ttu-id="92942-138">來源 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="92942-138">Source Azure Storage Context.</span></span> <span data-ttu-id="92942-139">您可以使用 Cmdlet New-AzStorageContext建立。</span><span class="sxs-lookup"><span data-stu-id="92942-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="92942-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92942-140">-DefaultProfile</span></span>
<span data-ttu-id="92942-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92942-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92942-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="92942-142">-DestBlob</span></span>
<span data-ttu-id="92942-143">目的地 Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="92942-143">Destination blob name</span></span>

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

### <span data-ttu-id="92942-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="92942-144">-DestCloudBlob</span></span>
<span data-ttu-id="92942-145">Destination CloudBlob 物件</span><span class="sxs-lookup"><span data-stu-id="92942-145">Destination CloudBlob object</span></span>

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

### <span data-ttu-id="92942-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="92942-146">-DestContainer</span></span>
<span data-ttu-id="92942-147">目的地容器名稱</span><span class="sxs-lookup"><span data-stu-id="92942-147">Destination container name</span></span>

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

### <span data-ttu-id="92942-148">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="92942-148">-DestContext</span></span>
<span data-ttu-id="92942-149">目的地 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="92942-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="92942-150">您可以使用 Cmdlet New-AzStorageContext建立。</span><span class="sxs-lookup"><span data-stu-id="92942-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="92942-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92942-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="92942-152">伺服器會在每個要求中以碼錶示時間。</span><span class="sxs-lookup"><span data-stu-id="92942-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="92942-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="92942-153">-SrcBlob</span></span>
<span data-ttu-id="92942-154">來源頁面 Blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="92942-154">Source page blob name.</span></span>

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

### <span data-ttu-id="92942-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="92942-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="92942-156">來源頁面 Blob 快照時間。</span><span class="sxs-lookup"><span data-stu-id="92942-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="92942-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="92942-157">-SrcContainer</span></span>
<span data-ttu-id="92942-158">來源容器名稱</span><span class="sxs-lookup"><span data-stu-id="92942-158">Source Container name</span></span>

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

### <span data-ttu-id="92942-159">-確認</span><span class="sxs-lookup"><span data-stu-id="92942-159">-Confirm</span></span>
<span data-ttu-id="92942-160">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="92942-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92942-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92942-161">-WhatIf</span></span>
<span data-ttu-id="92942-162">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92942-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92942-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92942-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92942-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92942-164">CommonParameters</span></span>
<span data-ttu-id="92942-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92942-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92942-166">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="92942-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92942-167">輸入</span><span class="sxs-lookup"><span data-stu-id="92942-167">INPUTS</span></span>

### <span data-ttu-id="92942-168">Microsoft.Azure.storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="92942-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="92942-169">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="92942-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="92942-170">System.String</span><span class="sxs-lookup"><span data-stu-id="92942-170">System.String</span></span>

### <span data-ttu-id="92942-171">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="92942-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="92942-172">輸出</span><span class="sxs-lookup"><span data-stu-id="92942-172">OUTPUTS</span></span>

### <span data-ttu-id="92942-173">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="92942-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="92942-174">筆記</span><span class="sxs-lookup"><span data-stu-id="92942-174">NOTES</span></span>

## <span data-ttu-id="92942-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="92942-175">RELATED LINKS</span></span>
