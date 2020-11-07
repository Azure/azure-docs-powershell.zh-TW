---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
ms.openlocfilehash: 054aa003752c27849c44eb00654313c395c255ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625044"
---
# <span data-ttu-id="6ea7f-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ea7f-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="6ea7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ea7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea7f-103">開始複製 blob。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ea7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ea7f-104">SYNTAX</span></span>

### <span data-ttu-id="6ea7f-105">[容器] (預設) </span><span class="sxs-lookup"><span data-stu-id="6ea7f-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-109">名</span><span class="sxs-lookup"><span data-stu-id="6ea7f-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="6ea7f-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea7f-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="6ea7f-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea7f-115">說明</span><span class="sxs-lookup"><span data-stu-id="6ea7f-115">DESCRIPTION</span></span>
<span data-ttu-id="6ea7f-116">**開始-AzureStorageBlobCopy** Cmdlet 會開始複製 blob。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="6ea7f-117">示例</span><span class="sxs-lookup"><span data-stu-id="6ea7f-117">EXAMPLES</span></span>

### <span data-ttu-id="6ea7f-118">範例1：複製命名的 blob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="6ea7f-119">這個命令會從名為 ContosoUploads 的容器中開始將名為 ContosoPlanning2015 的 blob 複製作業啟動到名為 ContosoArchives 的容器。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="6ea7f-120">範例2：取得容器以指定要複製的 blob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="6ea7f-121">這個命令會透過使用 **AzureStorageContainer** Cmdlet 來取得名為 ContosoUploads 的容器，然後使用管線運算子將容器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ea7f-122">該 Cmdlet 會啟動名為 ContosoPlanning2015 的 blob 的複製操作。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="6ea7f-123">上一個 Cmdlet 會提供來源容器。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="6ea7f-124">*DestContainer* 參數會將 ContosoArchives 指定為目標容器。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="6ea7f-125">範例3：取得容器中的所有 blob 並複製</span><span class="sxs-lookup"><span data-stu-id="6ea7f-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="6ea7f-126">這個命令會透過使用 **AzureStorageBlob** Cmdlet，在名為 ContosoUploads 的容器中取得 blob，然後使用管線運算子將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ea7f-127">該 Cmdlet 會將 blob 的複製操作啟動到名為 ContosoArchives 的容器。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="6ea7f-128">範例4：複製指定為物件的 blob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="6ea7f-129">第一個命令會在名為 ContosoUploads 的容器中取得名為 ContosoPlanning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="6ea7f-130">該命令會將該物件儲存在 $SrcBlob 變數中。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="6ea7f-131">第二個命令會在名為 ContosoArchives 的容器中取得名為 ContosoPlanning2015Archived 的 blob。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="6ea7f-132">該命令會將該物件儲存在 $DestBlob 變數中。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="6ea7f-133">最後一個命令會從來源容器開始複製作業至目的地容器。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="6ea7f-134">此命令使用標準點符號來指定 $SrcBlob 和 $DestBlob blob 的 **ICloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="6ea7f-135">範例5：從 URI 複製 blob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="6ea7f-136">這個命令會針對使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容，然後將該金鑰儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="6ea7f-137">第二個命令會將檔案從指定的 URI 複製到名為 ContosoArchive 的容器中名為 ContosoPlanning 的 blob。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="6ea7f-138">命令會在儲存在 $CoNtext 的內容中開始複製操作。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="6ea7f-139">參數</span><span class="sxs-lookup"><span data-stu-id="6ea7f-139">PARAMETERS</span></span>

### <span data-ttu-id="6ea7f-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="6ea7f-140">-AbsoluteUri</span></span>
<span data-ttu-id="6ea7f-141">指定要複製到 Azure 儲存區 blob 之檔案的絕對 URI。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="6ea7f-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ea7f-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ea7f-143">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ea7f-144">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ea7f-145">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6ea7f-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-146">-CloudBlob</span></span>
<span data-ttu-id="6ea7f-147">從 Azure 儲存空間用戶端文件庫指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6ea7f-148">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6ea7f-149">-CloudBlobContainer</span></span>
<span data-ttu-id="6ea7f-150">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6ea7f-151">這個 Cmdlet 會從此參數指定的容器複製 blob。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="6ea7f-152">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6ea7f-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ea7f-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ea7f-154">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ea7f-155">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ea7f-156">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ea7f-157">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ea7f-158">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-158">The default value is 10.</span></span>

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

### <span data-ttu-id="6ea7f-159">-內容</span><span class="sxs-lookup"><span data-stu-id="6ea7f-159">-Context</span></span>
<span data-ttu-id="6ea7f-160">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ea7f-161">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="6ea7f-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-162">-DestBlob</span></span>
<span data-ttu-id="6ea7f-163">指定目的地 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="6ea7f-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-164">-DestCloudBlob</span></span>
<span data-ttu-id="6ea7f-165">指定目的地 **CloudBlob** 物件</span><span class="sxs-lookup"><span data-stu-id="6ea7f-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="6ea7f-166">-DestContainer</span></span>
<span data-ttu-id="6ea7f-167">指定目的地容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-168">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ea7f-168">-DestContext</span></span>
<span data-ttu-id="6ea7f-169">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ea7f-170">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ea7f-171">-Force</span><span class="sxs-lookup"><span data-stu-id="6ea7f-171">-Force</span></span>
<span data-ttu-id="6ea7f-172">表示此 Cmdlet 會覆寫目的地 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-173">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="6ea7f-173">-PremiumPageBlobTier</span></span>
<span data-ttu-id="6ea7f-174">[特優] 頁面 Blob 層級</span><span class="sxs-lookup"><span data-stu-id="6ea7f-174">Premium Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ea7f-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ea7f-176">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6ea7f-177">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6ea7f-178">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-178">-SrcBlob</span></span>
<span data-ttu-id="6ea7f-179">指定來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-179">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-180">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="6ea7f-180">-SrcContainer</span></span>
<span data-ttu-id="6ea7f-181">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-181">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="6ea7f-182">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="6ea7f-182">-SrcDir</span></span>
<span data-ttu-id="6ea7f-183">從 Azure 儲存空間用戶端文件庫指定 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-183">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-184">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="6ea7f-184">-SrcFile</span></span>
<span data-ttu-id="6ea7f-185">從 Azure 存儲用戶端文件庫 Specifes **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-185">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6ea7f-186">您可以建立它或使用 Get-AzureStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-186">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-187">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="6ea7f-187">-SrcFilePath</span></span>
<span data-ttu-id="6ea7f-188">指定來原始目錄或來源共用的來源檔案相對路徑。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-188">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-189">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="6ea7f-189">-SrcShare</span></span>
<span data-ttu-id="6ea7f-190">從 Azure 儲存空間用戶端文件庫指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-190">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6ea7f-191">您可以建立它或使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-191">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-192">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="6ea7f-192">-SrcShareName</span></span>
<span data-ttu-id="6ea7f-193">指定來源共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-193">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea7f-194">-確認</span><span class="sxs-lookup"><span data-stu-id="6ea7f-194">-Confirm</span></span>
<span data-ttu-id="6ea7f-195">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea7f-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea7f-196">-WhatIf</span></span>
<span data-ttu-id="6ea7f-197">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea7f-198">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea7f-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea7f-199">CommonParameters</span></span>
<span data-ttu-id="6ea7f-200">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea7f-201">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea7f-202">輸入</span><span class="sxs-lookup"><span data-stu-id="6ea7f-202">INPUTS</span></span>

### <span data-ttu-id="6ea7f-203">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ea7f-203">CloudBlob</span></span>

<span data-ttu-id="6ea7f-204">形參 "CloudBlob" 接受管線中 "CloudBlob" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ea7f-204">Parameter 'CloudBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="6ea7f-205">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ea7f-205">IStorageContext</span></span>

<span data-ttu-id="6ea7f-206">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ea7f-206">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="6ea7f-207">CloudFile</span><span class="sxs-lookup"><span data-stu-id="6ea7f-207">CloudFile</span></span>

<span data-ttu-id="6ea7f-208">形參 "SrcFile" 接受管線中 "CloudFile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ea7f-208">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="6ea7f-209">輸出</span><span class="sxs-lookup"><span data-stu-id="6ea7f-209">OUTPUTS</span></span>

### <span data-ttu-id="6ea7f-210">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="6ea7f-210">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6ea7f-211">筆記</span><span class="sxs-lookup"><span data-stu-id="6ea7f-211">NOTES</span></span>

## <span data-ttu-id="6ea7f-212">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ea7f-212">RELATED LINKS</span></span>

[<span data-ttu-id="6ea7f-213">AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="6ea7f-213">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="6ea7f-214">停止 AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ea7f-214">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)