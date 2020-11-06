---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: eddc442dd442fbb64f7b075f49a3c638ea6920e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451551"
---
# <span data-ttu-id="8c672-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8c672-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="8c672-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c672-102">SYNOPSIS</span></span>
<span data-ttu-id="8c672-103">將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c672-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c672-104">SYNTAX</span></span>

### <span data-ttu-id="8c672-105">SendManual (預設) </span><span class="sxs-lookup"><span data-stu-id="8c672-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c672-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="8c672-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c672-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="8c672-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c672-108">說明</span><span class="sxs-lookup"><span data-stu-id="8c672-108">DESCRIPTION</span></span>
<span data-ttu-id="8c672-109">**AzureStorageBlobContent** Cmdlet 會將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="8c672-110">示例</span><span class="sxs-lookup"><span data-stu-id="8c672-110">EXAMPLES</span></span>

### <span data-ttu-id="8c672-111">範例1：上傳命名的檔案</span><span class="sxs-lookup"><span data-stu-id="8c672-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="8c672-112">這個命令會將名為 PlanningData 的檔案上傳到名為 Planning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="8c672-113">範例2：上傳目前資料夾底下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="8c672-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="8c672-114">這個命令使用核心的 Windows PowerShell Cmdlet Get-ChildItem 來取得目前資料夾和子資料夾中的所有檔案，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8c672-115">**AzureStorageBlobContent** Cmdlet 會將檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="8c672-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="8c672-116">範例3：覆寫現有的 blob</span><span class="sxs-lookup"><span data-stu-id="8c672-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="8c672-117">這個命令會使用 Get-AzureStorageBlob Cmdlet，在 ContosoUploads 容器中取得名為 Planning2015 的 blob，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="8c672-118">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="8c672-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="8c672-119">這個命令不會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="8c672-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="8c672-120">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c672-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="8c672-121">如果您確認命令，Cmdlet 會覆寫現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="8c672-122">範例4：使用管線將檔案上傳到容器</span><span class="sxs-lookup"><span data-stu-id="8c672-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="8c672-123">這個命令會使用 **AzureStorageContainer** Cmdlet 來取得以字串 ContosoUpload 開頭的容器，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="8c672-124">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="8c672-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="8c672-125">範例5：將檔案上傳到含中繼資料的頁面 blob，並 PremiumPageBlobTier 為 P10</span><span class="sxs-lookup"><span data-stu-id="8c672-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="8c672-126">第一個命令會建立包含 blob 中繼資料的雜湊資料表，並將該雜湊資料表儲存在 $Metadata 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c672-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="8c672-127">第二個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="8c672-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="8c672-128">Blob 包括儲存在 $Metadata 中的中繼資料，並以 P10 的方式 PremiumPageBlobTier。</span><span class="sxs-lookup"><span data-stu-id="8c672-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="8c672-129">範例6：將檔案上傳到具有指定 blob 屬性的 blob</span><span class="sxs-lookup"><span data-stu-id="8c672-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="8c672-130">這個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器，且具有指定的 blob 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c672-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="8c672-131">參數</span><span class="sxs-lookup"><span data-stu-id="8c672-131">PARAMETERS</span></span>

### <span data-ttu-id="8c672-132">-Blob</span><span class="sxs-lookup"><span data-stu-id="8c672-132">-Blob</span></span>
<span data-ttu-id="8c672-133">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c672-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="8c672-134">這個 Cmdlet 會將檔案上傳到此參數指定的 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c672-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="8c672-135">-BlobType</span></span>
<span data-ttu-id="8c672-136">指定此 Cmdlet 上傳的 blob 類型。</span><span class="sxs-lookup"><span data-stu-id="8c672-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="8c672-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8c672-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c672-138">框圖</span><span class="sxs-lookup"><span data-stu-id="8c672-138">Block</span></span>
- <span data-ttu-id="8c672-139">紙張</span><span class="sxs-lookup"><span data-stu-id="8c672-139">Page</span></span>

<span data-ttu-id="8c672-140">預設值為 Block。</span><span class="sxs-lookup"><span data-stu-id="8c672-140">The default value is Block.</span></span>

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

### <span data-ttu-id="8c672-141">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8c672-141">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8c672-142">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c672-142">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8c672-143">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="8c672-143">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8c672-144">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c672-144">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8c672-145">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8c672-145">-CloudBlob</span></span>
<span data-ttu-id="8c672-146">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c672-146">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="8c672-147">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-147">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="8c672-148">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8c672-148">-CloudBlobContainer</span></span>
<span data-ttu-id="8c672-149">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c672-149">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8c672-150">這個 Cmdlet 會將內容上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-150">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="8c672-151">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-151">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="8c672-152">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8c672-152">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8c672-153">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="8c672-153">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8c672-154">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="8c672-154">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8c672-155">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="8c672-155">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8c672-156">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="8c672-156">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8c672-157">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="8c672-157">The default value is 10.</span></span>

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

### <span data-ttu-id="8c672-158">-容器</span><span class="sxs-lookup"><span data-stu-id="8c672-158">-Container</span></span>
<span data-ttu-id="8c672-159">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c672-159">Specifies the name of a container.</span></span>
<span data-ttu-id="8c672-160">這個 Cmdlet 會將檔案上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="8c672-160">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c672-161">-內容</span><span class="sxs-lookup"><span data-stu-id="8c672-161">-Context</span></span>
<span data-ttu-id="8c672-162">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8c672-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8c672-163">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-163">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8c672-164">檔案</span><span class="sxs-lookup"><span data-stu-id="8c672-164">-File</span></span>
<span data-ttu-id="8c672-165">指定檔案的本機檔案路徑，以將它上傳成 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="8c672-165">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="8c672-166">-Force</span><span class="sxs-lookup"><span data-stu-id="8c672-166">-Force</span></span>
<span data-ttu-id="8c672-167">表示此 Cmdlet 會覆寫現有的 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8c672-167">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8c672-168">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="8c672-168">-Metadata</span></span>
<span data-ttu-id="8c672-169">指定上傳的 blob 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8c672-169">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="8c672-170">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="8c672-170">-PremiumPageBlobTier</span></span>
<span data-ttu-id="8c672-171">頁面 Blob 層</span><span class="sxs-lookup"><span data-stu-id="8c672-171">Page Blob Tier</span></span>

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

### <span data-ttu-id="8c672-172">-屬性</span><span class="sxs-lookup"><span data-stu-id="8c672-172">-Properties</span></span>
<span data-ttu-id="8c672-173">指定上傳的 blob 的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c672-173">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="8c672-174">支援的屬性為： CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="8c672-174">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="8c672-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8c672-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8c672-176">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c672-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8c672-177">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c672-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8c672-178">-確認</span><span class="sxs-lookup"><span data-stu-id="8c672-178">-Confirm</span></span>
<span data-ttu-id="8c672-179">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c672-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c672-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c672-180">-WhatIf</span></span>
<span data-ttu-id="8c672-181">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c672-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c672-182">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c672-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c672-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c672-183">CommonParameters</span></span>
<span data-ttu-id="8c672-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c672-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c672-185">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c672-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c672-186">輸入</span><span class="sxs-lookup"><span data-stu-id="8c672-186">INPUTS</span></span>

### <span data-ttu-id="8c672-187">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8c672-187">IStorageContext</span></span>

<span data-ttu-id="8c672-188">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8c672-188">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8c672-189">輸出</span><span class="sxs-lookup"><span data-stu-id="8c672-189">OUTPUTS</span></span>

### <span data-ttu-id="8c672-190">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="8c672-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="8c672-191">筆記</span><span class="sxs-lookup"><span data-stu-id="8c672-191">NOTES</span></span>

## <span data-ttu-id="8c672-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c672-192">RELATED LINKS</span></span>

[<span data-ttu-id="8c672-193">AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8c672-193">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="8c672-194">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8c672-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="8c672-195">移除-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8c672-195">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
