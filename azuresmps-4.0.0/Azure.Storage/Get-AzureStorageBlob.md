---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
ms.openlocfilehash: f7b68be6981343d14f7d1d8530a0af3c3eee199c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443480"
---
# <span data-ttu-id="de740-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="de740-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="de740-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de740-102">SYNOPSIS</span></span>
<span data-ttu-id="de740-103">列出容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="de740-104">句法</span><span class="sxs-lookup"><span data-stu-id="de740-104">SYNTAX</span></span>

### <span data-ttu-id="de740-105">BlobName (預設) </span><span class="sxs-lookup"><span data-stu-id="de740-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de740-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="de740-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="de740-107">說明</span><span class="sxs-lookup"><span data-stu-id="de740-107">DESCRIPTION</span></span>
<span data-ttu-id="de740-108">**AzureStorageBlob** Cmdlet 會在 Azure 儲存空間帳戶的指定容器中列出 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="de740-109">示例</span><span class="sxs-lookup"><span data-stu-id="de740-109">EXAMPLES</span></span>

### <span data-ttu-id="de740-110">範例1：透過 blob 名稱取得 blob</span><span class="sxs-lookup"><span data-stu-id="de740-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="de740-111">這個命令使用 blob 名稱和萬用字元來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="de740-112">範例2：使用管線取得 blob</span><span class="sxs-lookup"><span data-stu-id="de740-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="de740-113">這個命令會使用管線來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="de740-114">範例3：透過名稱首碼取得 blob</span><span class="sxs-lookup"><span data-stu-id="de740-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="de740-115">這個命令會使用名稱首碼來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="de740-116">範例4：多個批次中的清單 blob</span><span class="sxs-lookup"><span data-stu-id="de740-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="de740-117">這個範例使用 *MaxCount* 和 *ContinuationToken* 參數，以多個批次列出 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="de740-118">前四個命令會將值指派給要在範例中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="de740-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="de740-119">第五個命令指定一個 **Do** 語句，該語句使用 **AzureStorageBlob** Cmdlet 來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="de740-120">該語句包含儲存在 $Token 變數中的延續標記。</span><span class="sxs-lookup"><span data-stu-id="de740-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="de740-121">在迴圈執行時 $Token 變更值。</span><span class="sxs-lookup"><span data-stu-id="de740-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="de740-122">如需詳細資訊，請輸入 `Get-Help About_Do` 。</span><span class="sxs-lookup"><span data-stu-id="de740-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="de740-123">最後一個命令會使用 **Echo** 命令來顯示合計。</span><span class="sxs-lookup"><span data-stu-id="de740-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="de740-124">參數</span><span class="sxs-lookup"><span data-stu-id="de740-124">PARAMETERS</span></span>

### <span data-ttu-id="de740-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="de740-125">-Blob</span></span>
<span data-ttu-id="de740-126">指定可用於萬用字元搜尋的名稱或名稱模式。</span><span class="sxs-lookup"><span data-stu-id="de740-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="de740-127">如果未指定任何 blob 名稱，則 Cmdlet 會列出指定容器中的所有 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="de740-128">如果為此參數指定一個值，則 Cmdlet 會列出名稱與此參數相符的所有 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de740-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de740-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="de740-130">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="de740-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="de740-131">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="de740-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="de740-132">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="de740-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="de740-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="de740-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="de740-134">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="de740-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="de740-135">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="de740-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="de740-136">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="de740-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="de740-137">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="de740-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="de740-138">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="de740-138">The default value is 10.</span></span>

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

### <span data-ttu-id="de740-139">-容器</span><span class="sxs-lookup"><span data-stu-id="de740-139">-Container</span></span>
<span data-ttu-id="de740-140">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="de740-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de740-141">-內容</span><span class="sxs-lookup"><span data-stu-id="de740-141">-Context</span></span>
<span data-ttu-id="de740-142">指定您想要取得其 blob 清單的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="de740-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="de740-143">您可以使用 New-AzureStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="de740-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="de740-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="de740-144">-ContinuationToken</span></span>
<span data-ttu-id="de740-145">指定 blob 清單的延續標記。</span><span class="sxs-lookup"><span data-stu-id="de740-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="de740-146">使用此參數與 *MaxCount* 參數，在多個批次中列出 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de740-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="de740-147">-MaxCount</span></span>
<span data-ttu-id="de740-148">指定此 Cmdlet 傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="de740-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="de740-149">-Prefix</span><span class="sxs-lookup"><span data-stu-id="de740-149">-Prefix</span></span>
<span data-ttu-id="de740-150">針對您要取得的 blob 名稱指定一個前置詞。</span><span class="sxs-lookup"><span data-stu-id="de740-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="de740-151">這個參數不支援使用正則運算式或萬用字元來進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="de740-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="de740-152">這表示如果容器只有一個名為 "My"、"MyBlob1" 和 "MyBlob2" 的 blob，且您指定了 "-Prefix My \*"，則 Cmdlet 不會傳回 blob。</span><span class="sxs-lookup"><span data-stu-id="de740-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="de740-153">不過，如果您指定了 "-Prefix My"，此 Cmdlet 會傳回 "My"、"MyBlob1" 和 "MyBlob2"。</span><span class="sxs-lookup"><span data-stu-id="de740-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de740-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de740-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="de740-155">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="de740-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="de740-156">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="de740-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="de740-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de740-157">CommonParameters</span></span>
<span data-ttu-id="de740-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de740-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de740-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de740-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de740-160">輸入</span><span class="sxs-lookup"><span data-stu-id="de740-160">INPUTS</span></span>

## <span data-ttu-id="de740-161">輸出</span><span class="sxs-lookup"><span data-stu-id="de740-161">OUTPUTS</span></span>

### <span data-ttu-id="de740-162">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="de740-162">AzureStorageBlob</span></span>

## <span data-ttu-id="de740-163">筆記</span><span class="sxs-lookup"><span data-stu-id="de740-163">NOTES</span></span>
* <span data-ttu-id="de740-164">摘要</span><span class="sxs-lookup"><span data-stu-id="de740-164">SYNOPSIS</span></span>

## <span data-ttu-id="de740-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="de740-165">RELATED LINKS</span></span>

[<span data-ttu-id="de740-166">AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="de740-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="de740-167">移除-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="de740-167">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="de740-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="de740-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


