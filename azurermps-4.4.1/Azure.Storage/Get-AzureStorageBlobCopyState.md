---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6a61e076bf91d1ed994f9745d18a6f4832925250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624868"
---
# <span data-ttu-id="efabe-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="efabe-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="efabe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efabe-102">SYNOPSIS</span></span>
<span data-ttu-id="efabe-103">取得 Azure 儲存區 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efabe-104">句法</span><span class="sxs-lookup"><span data-stu-id="efabe-104">SYNTAX</span></span>

### <span data-ttu-id="efabe-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="efabe-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="efabe-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="efabe-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="efabe-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="efabe-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="efabe-108">說明</span><span class="sxs-lookup"><span data-stu-id="efabe-108">DESCRIPTION</span></span>
<span data-ttu-id="efabe-109">**AzureStorageBlobCopyState** Cmdlet 會取得 Azure 儲存空間 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="efabe-110">示例</span><span class="sxs-lookup"><span data-stu-id="efabe-110">EXAMPLES</span></span>

### <span data-ttu-id="efabe-111">範例1：取得 blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="efabe-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="efabe-112">這個命令會取得容器 ContosoUploads 中名為 ContosoPlanning2015 的 blob 複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="efabe-113">範例2：使用管線取得 blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="efabe-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="efabe-114">這個命令會透過使用 **AzureStorageBlob** Cmdlet 來取得名為 ContosoUploads 之容器中名為 ContosoPlanning2015 的 blob，然後使用管線運算子將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efabe-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="efabe-115">**AzureStorageBlobCopyState** Cmdlet 會取得該 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="efabe-116">範例3：使用管線在容器中取得 blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="efabe-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="efabe-117">這個命令會取得使用 **AzureStorageBlob** Cmdlet 命名的容器，然後將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efabe-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="efabe-118">**AzureStorageContainer** Cmdlet 會取得該容器中名為 ContosoPlanning2015 的 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="efabe-119">參數</span><span class="sxs-lookup"><span data-stu-id="efabe-119">PARAMETERS</span></span>

### <span data-ttu-id="efabe-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="efabe-120">-Blob</span></span>
<span data-ttu-id="efabe-121">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="efabe-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="efabe-122">這個 Cmdlet 會取得此參數指定之 Azure 存儲 blob 的 blob 複製作業狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efabe-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efabe-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="efabe-124">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="efabe-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="efabe-125">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="efabe-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="efabe-126">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="efabe-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="efabe-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="efabe-127">-CloudBlob</span></span>
<span data-ttu-id="efabe-128">從 Azure 儲存空間用戶端文件庫指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="efabe-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="efabe-129">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efabe-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efabe-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="efabe-130">-CloudBlobContainer</span></span>
<span data-ttu-id="efabe-131">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="efabe-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="efabe-132">這個 Cmdlet 會取得此參數指定容器中 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="efabe-133">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efabe-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efabe-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="efabe-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="efabe-135">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="efabe-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="efabe-136">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="efabe-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="efabe-137">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="efabe-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="efabe-138">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="efabe-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="efabe-139">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="efabe-139">The default value is 10.</span></span>

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

### <span data-ttu-id="efabe-140">-容器</span><span class="sxs-lookup"><span data-stu-id="efabe-140">-Container</span></span>
<span data-ttu-id="efabe-141">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="efabe-141">Specifies the name of a container.</span></span>
<span data-ttu-id="efabe-142">這個 Cmdlet 會取得此參數指定容器中 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="efabe-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efabe-143">-內容</span><span class="sxs-lookup"><span data-stu-id="efabe-143">-Context</span></span>
<span data-ttu-id="efabe-144">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="efabe-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="efabe-145">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efabe-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efabe-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="efabe-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="efabe-147">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="efabe-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="efabe-148">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="efabe-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="efabe-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="efabe-149">-WaitForComplete</span></span>
<span data-ttu-id="efabe-150">表示此 Cmdlet 會等待複本完成。</span><span class="sxs-lookup"><span data-stu-id="efabe-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="efabe-151">如果您沒有指定此參數，這個 Cmdlet 會立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="efabe-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="efabe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efabe-152">CommonParameters</span></span>
<span data-ttu-id="efabe-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efabe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efabe-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efabe-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efabe-155">輸入</span><span class="sxs-lookup"><span data-stu-id="efabe-155">INPUTS</span></span>

### <span data-ttu-id="efabe-156">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="efabe-156">IStorageContext</span></span>

<span data-ttu-id="efabe-157">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="efabe-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="efabe-158">輸出</span><span class="sxs-lookup"><span data-stu-id="efabe-158">OUTPUTS</span></span>

### <span data-ttu-id="efabe-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="efabe-159">CopyState</span></span>

## <span data-ttu-id="efabe-160">筆記</span><span class="sxs-lookup"><span data-stu-id="efabe-160">NOTES</span></span>

## <span data-ttu-id="efabe-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="efabe-161">RELATED LINKS</span></span>

[<span data-ttu-id="efabe-162">開始-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="efabe-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="efabe-163">停止 AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="efabe-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


