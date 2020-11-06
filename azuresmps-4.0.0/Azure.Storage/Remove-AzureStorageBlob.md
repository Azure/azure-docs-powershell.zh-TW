---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b40585f584cc8c2634acab54e6862e4163c6b7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443164"
---
# <span data-ttu-id="9883f-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9883f-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="9883f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9883f-102">SYNOPSIS</span></span>
<span data-ttu-id="9883f-103">移除指定的儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="9883f-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="9883f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9883f-104">SYNTAX</span></span>

### <span data-ttu-id="9883f-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="9883f-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9883f-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9883f-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9883f-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9883f-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9883f-108">說明</span><span class="sxs-lookup"><span data-stu-id="9883f-108">DESCRIPTION</span></span>
<span data-ttu-id="9883f-109">**AzureStorageBlob** Cmdlet 會將指定的 Blob 從 Azure 中的儲存空間帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="9883f-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="9883f-110">示例</span><span class="sxs-lookup"><span data-stu-id="9883f-110">EXAMPLES</span></span>

### <span data-ttu-id="9883f-111">範例1：依名稱移除儲存 blob</span><span class="sxs-lookup"><span data-stu-id="9883f-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="9883f-112">這個命令會移除其名稱所識別的 blob。</span><span class="sxs-lookup"><span data-stu-id="9883f-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="9883f-113">範例2：使用管線移除儲存 blob</span><span class="sxs-lookup"><span data-stu-id="9883f-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="9883f-114">這個命令會使用管線。</span><span class="sxs-lookup"><span data-stu-id="9883f-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="9883f-115">範例3：使用管線移除儲存區 blob</span><span class="sxs-lookup"><span data-stu-id="9883f-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="9883f-116">這個命令使用星號 ( \* ) 萬用字元和管線來檢索 blob 或 blob，然後將它們移除。</span><span class="sxs-lookup"><span data-stu-id="9883f-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="9883f-117">參數</span><span class="sxs-lookup"><span data-stu-id="9883f-117">PARAMETERS</span></span>

### <span data-ttu-id="9883f-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="9883f-118">-Blob</span></span>
<span data-ttu-id="9883f-119">指定要移除之 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9883f-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="9883f-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9883f-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9883f-121">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9883f-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9883f-122">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="9883f-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9883f-123">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9883f-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9883f-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9883f-124">-CloudBlob</span></span>
<span data-ttu-id="9883f-125">指定雲端 blob。</span><span class="sxs-lookup"><span data-stu-id="9883f-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="9883f-126">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9883f-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="9883f-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9883f-127">-CloudBlobContainer</span></span>
<span data-ttu-id="9883f-128">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="9883f-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9883f-129">您可以使用 Get-AzureStorageContainer Cmdlet 來取得它。</span><span class="sxs-lookup"><span data-stu-id="9883f-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="9883f-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9883f-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9883f-131">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="9883f-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9883f-132">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="9883f-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9883f-133">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="9883f-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9883f-134">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="9883f-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9883f-135">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="9883f-135">The default value is 10.</span></span>

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

### <span data-ttu-id="9883f-136">-容器</span><span class="sxs-lookup"><span data-stu-id="9883f-136">-Container</span></span>
<span data-ttu-id="9883f-137">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9883f-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="9883f-138">-內容</span><span class="sxs-lookup"><span data-stu-id="9883f-138">-Context</span></span>
<span data-ttu-id="9883f-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="9883f-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9883f-140">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="9883f-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="9883f-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="9883f-141">-DeleteSnapshot</span></span>
<span data-ttu-id="9883f-142">指定要刪除所有快照，但不是基底 blob。</span><span class="sxs-lookup"><span data-stu-id="9883f-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="9883f-143">如果未指定此參數，則會將基底與其快照一起刪除。</span><span class="sxs-lookup"><span data-stu-id="9883f-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="9883f-144">系統會提示使用者確認刪除操作。</span><span class="sxs-lookup"><span data-stu-id="9883f-144">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="9883f-145">-Force</span><span class="sxs-lookup"><span data-stu-id="9883f-145">-Force</span></span>
<span data-ttu-id="9883f-146">表示此 Cmdlet 不需確認即移除 blob 及其快照。</span><span class="sxs-lookup"><span data-stu-id="9883f-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="9883f-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9883f-147">-PassThru</span></span>
<span data-ttu-id="9883f-148">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="9883f-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9883f-149">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9883f-149">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9883f-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9883f-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9883f-151">指定要讀取之 Cmdlet 的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9883f-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="9883f-152">如果沒有指定，則會從預設設定檔讀取 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9883f-152">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="9883f-153">-確認</span><span class="sxs-lookup"><span data-stu-id="9883f-153">-Confirm</span></span>
<span data-ttu-id="9883f-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9883f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9883f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9883f-155">-WhatIf</span></span>
<span data-ttu-id="9883f-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9883f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9883f-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9883f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9883f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9883f-158">CommonParameters</span></span>
<span data-ttu-id="9883f-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9883f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9883f-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9883f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9883f-161">輸入</span><span class="sxs-lookup"><span data-stu-id="9883f-161">INPUTS</span></span>

## <span data-ttu-id="9883f-162">輸出</span><span class="sxs-lookup"><span data-stu-id="9883f-162">OUTPUTS</span></span>

## <span data-ttu-id="9883f-163">筆記</span><span class="sxs-lookup"><span data-stu-id="9883f-163">NOTES</span></span>

## <span data-ttu-id="9883f-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="9883f-164">RELATED LINKS</span></span>

[<span data-ttu-id="9883f-165">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9883f-165">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9883f-166">AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9883f-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="9883f-167">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9883f-167">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)