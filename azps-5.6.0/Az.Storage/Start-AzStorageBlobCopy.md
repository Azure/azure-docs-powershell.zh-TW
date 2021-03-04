---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 754ac7657561ba52e28f90d951c0843a8c206484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915013"
---
# <span data-ttu-id="8a0f2-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8a0f2-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="8a0f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0f2-103">開始複製 Blob。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="8a0f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a0f2-104">SYNTAX</span></span>

### <span data-ttu-id="8a0f2-105">ContainerName (預設) </span><span class="sxs-lookup"><span data-stu-id="8a0f2-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="8a0f2-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="8a0f2-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0f2-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="8a0f2-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a0f2-115">描述</span><span class="sxs-lookup"><span data-stu-id="8a0f2-115">DESCRIPTION</span></span>
<span data-ttu-id="8a0f2-116">**Start-AzStorageBlobCopy Cmdlet** 會開始複製 Blob。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="8a0f2-117">例子</span><span class="sxs-lookup"><span data-stu-id="8a0f2-117">EXAMPLES</span></span>

### <span data-ttu-id="8a0f2-118">範例 1：複製命名 Blob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="8a0f2-119">此命令會啟動名為 ContosoPlanning2015 的 Blob 從名為 ContosoUploads 的容器複製到名為 ContosoArchives 的容器。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="8a0f2-120">範例 2：取得容器以指定要複製的 Blob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="8a0f2-121">此命令會使用 **Get-AzStorageContainer** Cmdlet 取得名為 ContosoUploads 的容器，然後使用管線運算子將容器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8a0f2-122">該 Cmdlet 會啟動名為 ContosoPlanning2015 之 Blob 的複製作業。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="8a0f2-123">先前的 Cmdlet 會提供來源容器。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="8a0f2-124">*DestContainer* 參數會指定 ContosoArchives 做為目的地容器。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="8a0f2-125">範例 3：取得容器中的所有 Blob 並複製它們</span><span class="sxs-lookup"><span data-stu-id="8a0f2-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="8a0f2-126">此命令會使用 **Get-AzStorageBlob** Cmdlet 取得容器中名為 ContosoUploads 的 Blob，然後使用管線運算子將結果傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8a0f2-127">該 Cmdlet 會啟動 Blob 的複製作業至名為 ContosoArchives 的容器。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="8a0f2-128">範例 4：複製指定為物件的 Blob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="8a0f2-129">第一個命令會從名為 ContosoUploads 的容器中，獲得名為 ContosoPlanning2015 的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="8a0f2-130">該命令會儲存該物件在$SrcBlob變數中。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="8a0f2-131">第二個命令會從名為 ContosoArchives 的容器中，獲得名為 ContosoPlanning2015Archived 的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="8a0f2-132">該命令將該物件儲存在$DestBlob變數中。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="8a0f2-133">最後一個命令會啟動從來源容器到目的地容器的複製作業。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="8a0f2-134">命令使用標準點標記法來指定物件和$SrcBlob的 **iCloudBlob** $DestBlob物件。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="8a0f2-135">範例 5：從 URI 複製 Blob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="8a0f2-136">此命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文，然後將該金鑰$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="8a0f2-137">第二個命令將檔案從指定的 URI 複製到名為 ContosoArchive 的容器中名為 ContosoPlanning 的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="8a0f2-138">命令會開始複製作業至儲存在 $CoNtext 中。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="8a0f2-139">沒有來源儲存內容，因此來源 Uri 必須擁有來源物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="8a0f2-140">例如：如果來源不是公用 Azure Blob，則 Uri 應包含具有 Blob 讀取存取權之 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="8a0f2-141">範例 6：使用新的 Blob 名稱將區塊 Blob 複製到目標容器，並設定目標 Blob StandardBlobTier 為 Hot，RehydratePriority 設為 High</span><span class="sxs-lookup"><span data-stu-id="8a0f2-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="8a0f2-142">此命令會以新的 Blob 名稱開始將區塊 Blob 複製到目的地容器，並設定目標 Blob StandardBlobTier 為 Hot，RehydratePriority 設為 High</span><span class="sxs-lookup"><span data-stu-id="8a0f2-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="8a0f2-143">參數</span><span class="sxs-lookup"><span data-stu-id="8a0f2-143">PARAMETERS</span></span>

### <span data-ttu-id="8a0f2-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="8a0f2-144">-AbsoluteUri</span></span>
<span data-ttu-id="8a0f2-145">指定要複製到 Azure 儲存體 Blob 的檔案絕對 URI。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="8a0f2-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="8a0f2-146">-BlobBaseClient</span></span>
<span data-ttu-id="8a0f2-147">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="8a0f2-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a0f2-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a0f2-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8a0f2-149">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8a0f2-150">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8a0f2-151">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8a0f2-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-152">-CloudBlob</span></span>
<span data-ttu-id="8a0f2-153">從 **Azure 儲存用戶端文件庫指定 CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8a0f2-154">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8a0f2-155">-CloudBlobContainer</span></span>
<span data-ttu-id="8a0f2-156">從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8a0f2-157">此 Cmdlet 會從此參數指定的容器複製 Blob。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="8a0f2-158">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8a0f2-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8a0f2-160">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8a0f2-161">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8a0f2-162">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8a0f2-163">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8a0f2-164">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-164">The default value is 10.</span></span>

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

### <span data-ttu-id="8a0f2-165">-內容</span><span class="sxs-lookup"><span data-stu-id="8a0f2-165">-Context</span></span>
<span data-ttu-id="8a0f2-166">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8a0f2-167">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0f2-168">-DefaultProfile</span></span>
<span data-ttu-id="8a0f2-169">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a0f2-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-170">-DestBlob</span></span>
<span data-ttu-id="8a0f2-171">指定目的地 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="8a0f2-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-172">-DestCloudBlob</span></span>
<span data-ttu-id="8a0f2-173">指定目的地 **CloudBlob** 物件</span><span class="sxs-lookup"><span data-stu-id="8a0f2-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="8a0f2-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="8a0f2-174">-DestContainer</span></span>
<span data-ttu-id="8a0f2-175">指定目的地容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="8a0f2-176">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="8a0f2-176">-DestContext</span></span>
<span data-ttu-id="8a0f2-177">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8a0f2-178">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-179">-強制</span><span class="sxs-lookup"><span data-stu-id="8a0f2-179">-Force</span></span>
<span data-ttu-id="8a0f2-180">表示此 Cmdlet 覆寫目的地 Blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8a0f2-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="8a0f2-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="8a0f2-182">進一頁 Blob 層</span><span class="sxs-lookup"><span data-stu-id="8a0f2-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0f2-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="8a0f2-183">-RehydratePriority</span></span>
<span data-ttu-id="8a0f2-184">封鎖 Blob RehydratePriority。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="8a0f2-185">表示要重新水合已存檔 Blob 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="8a0f2-186">有效值為高/標準。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0f2-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a0f2-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8a0f2-188">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8a0f2-189">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8a0f2-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-190">-SrcBlob</span></span>
<span data-ttu-id="8a0f2-191">指定來源 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="8a0f2-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="8a0f2-192">-SrcContainer</span></span>
<span data-ttu-id="8a0f2-193">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="8a0f2-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="8a0f2-194">-SrcDir</span></span>
<span data-ttu-id="8a0f2-195">從 **Azure 儲存體用戶端文件庫指定 CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="8a0f2-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="8a0f2-196">-SrcFile</span></span>
<span data-ttu-id="8a0f2-197">從 Azure 儲存用戶端文件庫指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8a0f2-198">您可以建立或Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="8a0f2-199">-SrcFilePath</span></span>
<span data-ttu-id="8a0f2-200">指定來原始目錄或來源共用的來源檔案相對路徑。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="8a0f2-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="8a0f2-201">-SrcShare</span></span>
<span data-ttu-id="8a0f2-202">從 **Azure 儲存用戶端文件庫指定 CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8a0f2-203">您可以建立或Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="8a0f2-204">-SrcShareName</span></span>
<span data-ttu-id="8a0f2-205">指定來源共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="8a0f2-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="8a0f2-206">-StandardBlobTier</span></span>
<span data-ttu-id="8a0f2-207">封鎖 Blob 層，有效的值為 Hot/Cool/Archive。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="8a0f2-208">請參閱 https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="8a0f2-208">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0f2-209">-確認</span><span class="sxs-lookup"><span data-stu-id="8a0f2-209">-Confirm</span></span>
<span data-ttu-id="8a0f2-210">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a0f2-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a0f2-211">-WhatIf</span></span>
<span data-ttu-id="8a0f2-212">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a0f2-213">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a0f2-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0f2-214">CommonParameters</span></span>
<span data-ttu-id="8a0f2-215">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0f2-216">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8a0f2-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0f2-217">輸入</span><span class="sxs-lookup"><span data-stu-id="8a0f2-217">INPUTS</span></span>

### <span data-ttu-id="8a0f2-218">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="8a0f2-219">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8a0f2-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="8a0f2-220">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="8a0f2-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="8a0f2-221">System.String</span><span class="sxs-lookup"><span data-stu-id="8a0f2-221">System.String</span></span>

### <span data-ttu-id="8a0f2-222">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8a0f2-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a0f2-223">輸出</span><span class="sxs-lookup"><span data-stu-id="8a0f2-223">OUTPUTS</span></span>

### <span data-ttu-id="8a0f2-224">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8a0f2-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="8a0f2-225">筆記</span><span class="sxs-lookup"><span data-stu-id="8a0f2-225">NOTES</span></span>

## <span data-ttu-id="8a0f2-226">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a0f2-226">RELATED LINKS</span></span>

[<span data-ttu-id="8a0f2-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="8a0f2-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="8a0f2-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8a0f2-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
