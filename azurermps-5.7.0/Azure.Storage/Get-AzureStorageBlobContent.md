---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
ms.openlocfilehash: 5023643ae57ab73ea625254f7b2362c947209f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446587"
---
# <span data-ttu-id="a0d3d-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0d3d-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="a0d3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d3d-103">下載儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0d3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0d3d-104">SYNTAX</span></span>

### <span data-ttu-id="a0d3d-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="a0d3d-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d3d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a0d3d-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d3d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a0d3d-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d3d-108">說明</span><span class="sxs-lookup"><span data-stu-id="a0d3d-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d3d-109">**AzureStorageBlobContent** Cmdlet 會下載指定的儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="a0d3d-110">如果 blob 名稱對於本機電腦無效，則此 Cmdlet 會在可能的情況下自動解決此情況。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="a0d3d-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0d3d-111">EXAMPLES</span></span>

### <span data-ttu-id="a0d3d-112">範例1：依名稱下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="a0d3d-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="a0d3d-113">這個命令會依名稱下載 blob。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="a0d3d-114">範例2：使用管線下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="a0d3d-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="a0d3d-115">這個命令會使用管線來尋找及下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="a0d3d-116">範例3：使用管線和萬用字元下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="a0d3d-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="a0d3d-117">這個範例使用星號萬用字元和管線來尋找及下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="a0d3d-118">參數</span><span class="sxs-lookup"><span data-stu-id="a0d3d-118">PARAMETERS</span></span>

### <span data-ttu-id="a0d3d-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="a0d3d-119">-Blob</span></span>
<span data-ttu-id="a0d3d-120">指定要下載的 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d3d-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="a0d3d-121">-CheckMd5</span></span>
<span data-ttu-id="a0d3d-122">指定是否要檢查已下載檔案的 Md5 加總。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="a0d3d-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0d3d-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0d3d-124">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0d3d-125">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0d3d-126">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0d3d-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a0d3d-127">-CloudBlob</span></span>
<span data-ttu-id="a0d3d-128">指定雲端 blob。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="a0d3d-129">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a0d3d-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a0d3d-130">-CloudBlobContainer</span></span>
<span data-ttu-id="a0d3d-131">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="a0d3d-132">您可以建立或使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a0d3d-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0d3d-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0d3d-134">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0d3d-135">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0d3d-136">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0d3d-137">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0d3d-138">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-138">The default value is 10.</span></span>

<span data-ttu-id="a0d3d-139">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-139">The default value is 10.</span></span>

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

### <span data-ttu-id="a0d3d-140">-容器</span><span class="sxs-lookup"><span data-stu-id="a0d3d-140">-Container</span></span>
<span data-ttu-id="a0d3d-141">指定包含您要下載之 blob 的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d3d-142">-內容</span><span class="sxs-lookup"><span data-stu-id="a0d3d-142">-Context</span></span>
<span data-ttu-id="a0d3d-143">指定您想要從中下載 blob 內容的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="a0d3d-144">您可以使用 New-AzureStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="a0d3d-145">-目的地</span><span class="sxs-lookup"><span data-stu-id="a0d3d-145">-Destination</span></span>
<span data-ttu-id="a0d3d-146">指定要儲存下載檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d3d-147">-Force</span><span class="sxs-lookup"><span data-stu-id="a0d3d-147">-Force</span></span>
<span data-ttu-id="a0d3d-148">覆寫現有檔案而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="a0d3d-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0d3d-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0d3d-150">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a0d3d-151">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a0d3d-152">-確認</span><span class="sxs-lookup"><span data-stu-id="a0d3d-152">-Confirm</span></span>
<span data-ttu-id="a0d3d-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d3d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d3d-154">-WhatIf</span></span>
<span data-ttu-id="a0d3d-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d3d-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d3d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d3d-157">CommonParameters</span></span>
<span data-ttu-id="a0d3d-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d3d-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d3d-160">輸入</span><span class="sxs-lookup"><span data-stu-id="a0d3d-160">INPUTS</span></span>

### <span data-ttu-id="a0d3d-161">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a0d3d-161">IStorageContext</span></span>

<span data-ttu-id="a0d3d-162">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a0d3d-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="a0d3d-163">輸出</span><span class="sxs-lookup"><span data-stu-id="a0d3d-163">OUTPUTS</span></span>

### <span data-ttu-id="a0d3d-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0d3d-164">AzureStorageContainer</span></span>

## <span data-ttu-id="a0d3d-165">筆記</span><span class="sxs-lookup"><span data-stu-id="a0d3d-165">NOTES</span></span>
* <span data-ttu-id="a0d3d-166">如果 blob 名稱對於本機電腦無效，則此 Cmdlet 會 autoresolves 它（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="a0d3d-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="a0d3d-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0d3d-167">RELATED LINKS</span></span>

[<span data-ttu-id="a0d3d-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0d3d-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="a0d3d-169">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0d3d-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="a0d3d-170">移除-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0d3d-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
