---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 36ae8a00237be287262de0cc9eac4022b9efc9d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957446"
---
# <span data-ttu-id="4c199-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4c199-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="4c199-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c199-102">SYNOPSIS</span></span>
<span data-ttu-id="4c199-103">開始複製 blob。</span><span class="sxs-lookup"><span data-stu-id="4c199-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="4c199-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c199-104">SYNTAX</span></span>

### <span data-ttu-id="4c199-105">[容器] (預設) </span><span class="sxs-lookup"><span data-stu-id="4c199-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c199-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c199-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c199-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c199-109">名</span><span class="sxs-lookup"><span data-stu-id="4c199-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c199-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c199-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c199-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c199-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="4c199-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c199-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="4c199-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c199-115">說明</span><span class="sxs-lookup"><span data-stu-id="4c199-115">DESCRIPTION</span></span>
<span data-ttu-id="4c199-116">**開始-AzStorageBlobCopy** Cmdlet 會開始複製 blob。</span><span class="sxs-lookup"><span data-stu-id="4c199-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="4c199-117">示例</span><span class="sxs-lookup"><span data-stu-id="4c199-117">EXAMPLES</span></span>

### <span data-ttu-id="4c199-118">範例1：複製命名的 blob</span><span class="sxs-lookup"><span data-stu-id="4c199-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="4c199-119">這個命令會從名為 ContosoUploads 的容器中開始將名為 ContosoPlanning2015 的 blob 複製作業啟動到名為 ContosoArchives 的容器。</span><span class="sxs-lookup"><span data-stu-id="4c199-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="4c199-120">範例2：取得容器以指定要複製的 blob</span><span class="sxs-lookup"><span data-stu-id="4c199-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="4c199-121">這個命令會透過使用 **AzStorageContainer** Cmdlet 來取得名為 ContosoUploads 的容器，然後使用管線運算子將容器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c199-122">該 Cmdlet 會啟動名為 ContosoPlanning2015 的 blob 的複製操作。</span><span class="sxs-lookup"><span data-stu-id="4c199-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="4c199-123">上一個 Cmdlet 會提供來源容器。</span><span class="sxs-lookup"><span data-stu-id="4c199-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="4c199-124">*DestContainer* 參數會將 ContosoArchives 指定為目標容器。</span><span class="sxs-lookup"><span data-stu-id="4c199-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="4c199-125">範例3：取得容器中的所有 blob 並複製</span><span class="sxs-lookup"><span data-stu-id="4c199-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="4c199-126">這個命令會透過使用 **AzStorageBlob** Cmdlet，在名為 ContosoUploads 的容器中取得 blob，然後使用管線運算子將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c199-127">該 Cmdlet 會將 blob 的複製操作啟動到名為 ContosoArchives 的容器。</span><span class="sxs-lookup"><span data-stu-id="4c199-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="4c199-128">範例4：複製指定為物件的 blob</span><span class="sxs-lookup"><span data-stu-id="4c199-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="4c199-129">第一個命令會在名為 ContosoUploads 的容器中取得名為 ContosoPlanning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="4c199-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="4c199-130">該命令會將該物件儲存在 $SrcBlob 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c199-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="4c199-131">第二個命令會在名為 ContosoArchives 的容器中取得名為 ContosoPlanning2015Archived 的 blob。</span><span class="sxs-lookup"><span data-stu-id="4c199-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="4c199-132">該命令會將該物件儲存在 $DestBlob 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c199-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="4c199-133">最後一個命令會從來源容器開始複製作業至目的地容器。</span><span class="sxs-lookup"><span data-stu-id="4c199-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="4c199-134">此命令使用標準點符號來指定 $SrcBlob 和 $DestBlob blob 的 **ICloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c199-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="4c199-135">範例5：從 URI 複製 blob</span><span class="sxs-lookup"><span data-stu-id="4c199-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="4c199-136">這個命令會針對使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容，然後將該金鑰儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c199-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="4c199-137">第二個命令會將檔案從指定的 URI 複製到名為 ContosoArchive 的容器中名為 ContosoPlanning 的 blob。</span><span class="sxs-lookup"><span data-stu-id="4c199-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="4c199-138">命令會在儲存在 $CoNtext 的內容中開始複製操作。</span><span class="sxs-lookup"><span data-stu-id="4c199-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="4c199-139">範例6：將區塊 blob 複製到具有新 blob 名稱的目標容器，並將 [目標 blob StandardBlobTier] 設為 [熱]，RehydratePriority [高]</span><span class="sxs-lookup"><span data-stu-id="4c199-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="4c199-140">這個命令會將區塊 blob 的複製作業啟動至具有新 blob 名稱的目標容器，並將 [目標 blob StandardBlobTier] 設定為 [熱]，RehydratePriority [高]</span><span class="sxs-lookup"><span data-stu-id="4c199-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="4c199-141">參數</span><span class="sxs-lookup"><span data-stu-id="4c199-141">PARAMETERS</span></span>

### <span data-ttu-id="4c199-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="4c199-142">-AbsoluteUri</span></span>
<span data-ttu-id="4c199-143">指定要複製到 Azure 儲存區 blob 之檔案的絕對 URI。</span><span class="sxs-lookup"><span data-stu-id="4c199-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="4c199-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c199-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4c199-145">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c199-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4c199-146">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="4c199-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4c199-147">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c199-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4c199-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4c199-148">-CloudBlob</span></span>
<span data-ttu-id="4c199-149">從 Azure 儲存空間用戶端文件庫指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c199-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="4c199-150">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4c199-151">-CloudBlobContainer</span></span>
<span data-ttu-id="4c199-152">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c199-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="4c199-153">這個 Cmdlet 會從此參數指定的容器複製 blob。</span><span class="sxs-lookup"><span data-stu-id="4c199-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="4c199-154">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="4c199-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4c199-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4c199-156">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="4c199-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4c199-157">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="4c199-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4c199-158">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="4c199-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4c199-159">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="4c199-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4c199-160">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="4c199-160">The default value is 10.</span></span>

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

### <span data-ttu-id="4c199-161">-內容</span><span class="sxs-lookup"><span data-stu-id="4c199-161">-Context</span></span>
<span data-ttu-id="4c199-162">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4c199-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4c199-163">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="4c199-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c199-164">-DefaultProfile</span></span>
<span data-ttu-id="4c199-165">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c199-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c199-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="4c199-166">-DestBlob</span></span>
<span data-ttu-id="4c199-167">指定目的地 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c199-167">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="4c199-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="4c199-168">-DestCloudBlob</span></span>
<span data-ttu-id="4c199-169">指定目的地 **CloudBlob** 物件</span><span class="sxs-lookup"><span data-stu-id="4c199-169">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="4c199-170">-DestContainer</span></span>
<span data-ttu-id="4c199-171">指定目的地容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c199-171">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-172">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="4c199-172">-DestContext</span></span>
<span data-ttu-id="4c199-173">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4c199-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4c199-174">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4c199-175">-Force</span><span class="sxs-lookup"><span data-stu-id="4c199-175">-Force</span></span>
<span data-ttu-id="4c199-176">表示此 Cmdlet 會覆寫目的地 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4c199-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="4c199-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="4c199-178">[特優] 頁面 Blob 層級</span><span class="sxs-lookup"><span data-stu-id="4c199-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="4c199-179">-RehydratePriority</span></span>
<span data-ttu-id="4c199-180">封鎖 Blob RehydratePriority。</span><span class="sxs-lookup"><span data-stu-id="4c199-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="4c199-181">指出 rehydrate 已封存的 blob 時要使用的優先順序。</span><span class="sxs-lookup"><span data-stu-id="4c199-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="4c199-182">有效值為高/標準值。</span><span class="sxs-lookup"><span data-stu-id="4c199-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c199-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4c199-184">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c199-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4c199-185">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c199-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4c199-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="4c199-186">-SrcBlob</span></span>
<span data-ttu-id="4c199-187">指定來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c199-187">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="4c199-188">-SrcContainer</span></span>
<span data-ttu-id="4c199-189">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c199-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="4c199-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="4c199-190">-SrcDir</span></span>
<span data-ttu-id="4c199-191">從 Azure 儲存空間用戶端文件庫指定 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c199-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="4c199-192">-SrcFile</span></span>
<span data-ttu-id="4c199-193">從 Azure 儲存空間用戶端文件庫指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c199-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="4c199-194">您可以建立它或使用 Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="4c199-195">-SrcFilePath</span></span>
<span data-ttu-id="4c199-196">指定來原始目錄或來源共用的來源檔案相對路徑。</span><span class="sxs-lookup"><span data-stu-id="4c199-196">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="4c199-197">-SrcShare</span></span>
<span data-ttu-id="4c199-198">從 Azure 儲存空間用戶端文件庫指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c199-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="4c199-199">您可以建立它或使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="4c199-200">-SrcShareName</span></span>
<span data-ttu-id="4c199-201">指定來源共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4c199-201">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c199-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="4c199-202">-StandardBlobTier</span></span>
<span data-ttu-id="4c199-203">封鎖 Blob 層級，有效值為熱/冷卻/封存。</span><span class="sxs-lookup"><span data-stu-id="4c199-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="4c199-204">中查看詳細資料 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="4c199-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="4c199-205">-確認</span><span class="sxs-lookup"><span data-stu-id="4c199-205">-Confirm</span></span>
<span data-ttu-id="4c199-206">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c199-206">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c199-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c199-207">-WhatIf</span></span>
<span data-ttu-id="4c199-208">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c199-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c199-209">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c199-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c199-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c199-210">CommonParameters</span></span>
<span data-ttu-id="4c199-211">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c199-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c199-212">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c199-212">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c199-213">輸入</span><span class="sxs-lookup"><span data-stu-id="4c199-213">INPUTS</span></span>

### <span data-ttu-id="4c199-214">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="4c199-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="4c199-215">[CloudBlobContainer]。</span><span class="sxs-lookup"><span data-stu-id="4c199-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="4c199-216">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="4c199-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="4c199-217">System.object</span><span class="sxs-lookup"><span data-stu-id="4c199-217">System.String</span></span>

### <span data-ttu-id="4c199-218">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="4c199-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c199-219">輸出</span><span class="sxs-lookup"><span data-stu-id="4c199-219">OUTPUTS</span></span>

### <span data-ttu-id="4c199-220">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="4c199-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="4c199-221">筆記</span><span class="sxs-lookup"><span data-stu-id="4c199-221">NOTES</span></span>

## <span data-ttu-id="4c199-222">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c199-222">RELATED LINKS</span></span>

[<span data-ttu-id="4c199-223">AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="4c199-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="4c199-224">停止 AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4c199-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
