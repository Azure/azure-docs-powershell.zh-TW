---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/a2772c13c7cb665d7485636044c46f8c9222fc68
ms.openlocfilehash: c7acda834cda53a86073692dc6c888ce2803d859
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455008"
---
# <span data-ttu-id="94839-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94839-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="94839-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94839-102">SYNOPSIS</span></span>
<span data-ttu-id="94839-103">將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94839-104">句法</span><span class="sxs-lookup"><span data-stu-id="94839-104">SYNTAX</span></span>

### <span data-ttu-id="94839-105">SendManual (預設) </span><span class="sxs-lookup"><span data-stu-id="94839-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94839-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="94839-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94839-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="94839-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94839-108">說明</span><span class="sxs-lookup"><span data-stu-id="94839-108">DESCRIPTION</span></span>
<span data-ttu-id="94839-109">**AzureStorageBlobContent** Cmdlet 會將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="94839-110">示例</span><span class="sxs-lookup"><span data-stu-id="94839-110">EXAMPLES</span></span>

### <span data-ttu-id="94839-111">範例1：上傳命名的檔案</span><span class="sxs-lookup"><span data-stu-id="94839-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="94839-112">這個命令會將名為 PlanningData 的檔案上傳到名為 Planning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="94839-113">範例2：上傳目前資料夾底下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="94839-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="94839-114">這個命令使用核心的 Windows PowerShell Cmdlet Get-ChildItem 來取得目前資料夾和子資料夾中的所有檔案，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94839-115">**AzureStorageBlobContent** Cmdlet 會將檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="94839-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="94839-116">範例3：覆寫現有的 blob</span><span class="sxs-lookup"><span data-stu-id="94839-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="94839-117">這個命令會使用 Get-AzureStorageBlob Cmdlet，在 ContosoUploads 容器中取得名為 Planning2015 的 blob，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="94839-118">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="94839-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="94839-119">這個命令不會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="94839-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="94839-120">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94839-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="94839-121">如果您確認命令，Cmdlet 會覆寫現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="94839-122">範例4：使用管線將檔案上傳到容器</span><span class="sxs-lookup"><span data-stu-id="94839-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="94839-123">這個命令會使用 **AzureStorageContainer** Cmdlet 來取得以字串 ContosoUpload 開頭的容器，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="94839-124">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="94839-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="94839-125">範例5：將檔案上傳到含中繼資料的頁面 blob，並 PremiumPageBlobTier 為 P10</span><span class="sxs-lookup"><span data-stu-id="94839-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="94839-126">第一個命令會建立包含 blob 中繼資料的雜湊資料表，並將該雜湊資料表儲存在 $Metadata 變數中。</span><span class="sxs-lookup"><span data-stu-id="94839-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="94839-127">第二個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="94839-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="94839-128">Blob 包括儲存在 $Metadata 中的中繼資料，並以 P10 的方式 PremiumPageBlobTier。</span><span class="sxs-lookup"><span data-stu-id="94839-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

## <span data-ttu-id="94839-129">參數</span><span class="sxs-lookup"><span data-stu-id="94839-129">PARAMETERS</span></span>

### <span data-ttu-id="94839-130">-Blob</span><span class="sxs-lookup"><span data-stu-id="94839-130">-Blob</span></span>
<span data-ttu-id="94839-131">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="94839-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="94839-132">這個 Cmdlet 會將檔案上傳到此參數指定的 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94839-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="94839-133">-BlobType</span></span>
<span data-ttu-id="94839-134">指定此 Cmdlet 上傳的 blob 類型。</span><span class="sxs-lookup"><span data-stu-id="94839-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="94839-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="94839-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94839-136">框圖</span><span class="sxs-lookup"><span data-stu-id="94839-136">Block</span></span>
- <span data-ttu-id="94839-137">紙張</span><span class="sxs-lookup"><span data-stu-id="94839-137">Page</span></span>

<span data-ttu-id="94839-138">預設值為 Block。</span><span class="sxs-lookup"><span data-stu-id="94839-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94839-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="94839-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="94839-140">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="94839-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="94839-141">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="94839-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="94839-142">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="94839-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="94839-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="94839-143">-CloudBlob</span></span>
<span data-ttu-id="94839-144">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="94839-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="94839-145">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="94839-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="94839-146">-CloudBlobContainer</span></span>
<span data-ttu-id="94839-147">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="94839-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="94839-148">這個 Cmdlet 會將內容上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="94839-149">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="94839-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="94839-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="94839-151">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="94839-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="94839-152">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="94839-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="94839-153">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="94839-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="94839-154">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="94839-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="94839-155">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="94839-155">The default value is 10.</span></span>

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

### <span data-ttu-id="94839-156">-容器</span><span class="sxs-lookup"><span data-stu-id="94839-156">-Container</span></span>
<span data-ttu-id="94839-157">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="94839-157">Specifies the name of a container.</span></span>
<span data-ttu-id="94839-158">這個 Cmdlet 會將檔案上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="94839-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94839-159">-內容</span><span class="sxs-lookup"><span data-stu-id="94839-159">-Context</span></span>
<span data-ttu-id="94839-160">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="94839-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="94839-161">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="94839-162">檔案</span><span class="sxs-lookup"><span data-stu-id="94839-162">-File</span></span>
<span data-ttu-id="94839-163">指定檔案的本機檔案路徑，以將它上傳成 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="94839-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94839-164">-Force</span><span class="sxs-lookup"><span data-stu-id="94839-164">-Force</span></span>
<span data-ttu-id="94839-165">表示此 Cmdlet 會覆寫現有的 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94839-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="94839-166">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="94839-166">-Metadata</span></span>
<span data-ttu-id="94839-167">指定上傳的 blob 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="94839-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94839-168">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="94839-168">-PremiumPageBlobTier</span></span>
<span data-ttu-id="94839-169">頁面 Blob 層</span><span class="sxs-lookup"><span data-stu-id="94839-169">Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94839-170">-屬性</span><span class="sxs-lookup"><span data-stu-id="94839-170">-Properties</span></span>
<span data-ttu-id="94839-171">指定上傳的 blob 的屬性。</span><span class="sxs-lookup"><span data-stu-id="94839-171">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94839-172">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="94839-172">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="94839-173">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="94839-173">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="94839-174">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="94839-174">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="94839-175">-確認</span><span class="sxs-lookup"><span data-stu-id="94839-175">-Confirm</span></span>
<span data-ttu-id="94839-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94839-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94839-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94839-177">-WhatIf</span></span>
<span data-ttu-id="94839-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94839-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94839-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94839-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94839-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94839-180">CommonParameters</span></span>
<span data-ttu-id="94839-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94839-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94839-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94839-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94839-183">輸入</span><span class="sxs-lookup"><span data-stu-id="94839-183">INPUTS</span></span>

### <span data-ttu-id="94839-184">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="94839-184">IStorageContext</span></span>

<span data-ttu-id="94839-185">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="94839-185">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="94839-186">輸出</span><span class="sxs-lookup"><span data-stu-id="94839-186">OUTPUTS</span></span>

### <span data-ttu-id="94839-187">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="94839-187">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="94839-188">筆記</span><span class="sxs-lookup"><span data-stu-id="94839-188">NOTES</span></span>

## <span data-ttu-id="94839-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="94839-189">RELATED LINKS</span></span>

[<span data-ttu-id="94839-190">AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94839-190">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="94839-191">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="94839-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="94839-192">移除-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="94839-192">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
