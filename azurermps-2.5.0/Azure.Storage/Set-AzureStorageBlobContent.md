---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
ms.openlocfilehash: 319765dac96d40ec510a45bffb19248e041b1333
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802637"
---
# <span data-ttu-id="02cac-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="02cac-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="02cac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02cac-102">SYNOPSIS</span></span>
<span data-ttu-id="02cac-103">將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02cac-104">句法</span><span class="sxs-lookup"><span data-stu-id="02cac-104">SYNTAX</span></span>

### <span data-ttu-id="02cac-105">SendManual (預設) </span><span class="sxs-lookup"><span data-stu-id="02cac-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02cac-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="02cac-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02cac-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="02cac-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02cac-108">說明</span><span class="sxs-lookup"><span data-stu-id="02cac-108">DESCRIPTION</span></span>
<span data-ttu-id="02cac-109">**AzureStorageBlobContent** Cmdlet 會將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="02cac-110">示例</span><span class="sxs-lookup"><span data-stu-id="02cac-110">EXAMPLES</span></span>

### <span data-ttu-id="02cac-111">範例1：上傳命名的檔案</span><span class="sxs-lookup"><span data-stu-id="02cac-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="02cac-112">這個命令會將名為 PlanningData 的檔案上傳到名為 Planning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="02cac-113">範例2：上傳目前資料夾底下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="02cac-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="02cac-114">這個命令使用核心的 Windows PowerShell Cmdlet Get-ChildItem 來取得目前資料夾和子資料夾中的所有檔案，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="02cac-115">**AzureStorageBlobContent** Cmdlet 會將檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="02cac-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="02cac-116">範例3：覆寫現有的 blob</span><span class="sxs-lookup"><span data-stu-id="02cac-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="02cac-117">這個命令會使用 Get-AzureStorageBlob Cmdlet，在 ContosoUploads 容器中取得名為 Planning2015 的 blob，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="02cac-118">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="02cac-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="02cac-119">這個命令不會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="02cac-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="02cac-120">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02cac-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="02cac-121">如果您確認命令，Cmdlet 會覆寫現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="02cac-122">範例4：使用管線將檔案上傳到容器</span><span class="sxs-lookup"><span data-stu-id="02cac-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="02cac-123">這個命令會使用 **AzureStorageContainer** Cmdlet 來取得以字串 ContosoUpload 開頭的容器，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="02cac-124">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="02cac-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="02cac-125">範例5：將檔案上傳到含中繼資料的頁面 blob，並 PremiumPageBlobTier 為 P10</span><span class="sxs-lookup"><span data-stu-id="02cac-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="02cac-126">第一個命令會建立包含 blob 中繼資料的雜湊資料表，並將該雜湊資料表儲存在 $Metadata 變數中。</span><span class="sxs-lookup"><span data-stu-id="02cac-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="02cac-127">第二個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="02cac-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="02cac-128">Blob 包括儲存在 $Metadata 中的中繼資料，並以 P10 的方式 PremiumPageBlobTier。</span><span class="sxs-lookup"><span data-stu-id="02cac-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="02cac-129">範例6：將檔案上傳到具有指定 blob 屬性的 blob</span><span class="sxs-lookup"><span data-stu-id="02cac-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="02cac-130">這個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器，且具有指定的 blob 屬性。</span><span class="sxs-lookup"><span data-stu-id="02cac-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="02cac-131">參數</span><span class="sxs-lookup"><span data-stu-id="02cac-131">PARAMETERS</span></span>

### <span data-ttu-id="02cac-132">-Blob</span><span class="sxs-lookup"><span data-stu-id="02cac-132">-Blob</span></span>
<span data-ttu-id="02cac-133">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="02cac-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="02cac-134">這個 Cmdlet 會將檔案上傳到此參數指定的 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="02cac-135">-BlobType</span></span>
<span data-ttu-id="02cac-136">指定此 Cmdlet 上傳的 blob 類型。</span><span class="sxs-lookup"><span data-stu-id="02cac-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="02cac-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="02cac-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02cac-138">框圖</span><span class="sxs-lookup"><span data-stu-id="02cac-138">Block</span></span>
- <span data-ttu-id="02cac-139">[預設值] 為 [區塊] 的頁面。</span><span class="sxs-lookup"><span data-stu-id="02cac-139">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02cac-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="02cac-141">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="02cac-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="02cac-142">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="02cac-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="02cac-143">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="02cac-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="02cac-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="02cac-144">-CloudBlob</span></span>
<span data-ttu-id="02cac-145">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="02cac-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="02cac-146">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-146">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="02cac-147">-CloudBlobContainer</span></span>
<span data-ttu-id="02cac-148">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="02cac-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="02cac-149">這個 Cmdlet 會將內容上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="02cac-150">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-150">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="02cac-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="02cac-152">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="02cac-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="02cac-153">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="02cac-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="02cac-154">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="02cac-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="02cac-155">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="02cac-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="02cac-156">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="02cac-156">The default value is 10.</span></span>

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

### <span data-ttu-id="02cac-157">-容器</span><span class="sxs-lookup"><span data-stu-id="02cac-157">-Container</span></span>
<span data-ttu-id="02cac-158">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="02cac-158">Specifies the name of a container.</span></span>
<span data-ttu-id="02cac-159">這個 Cmdlet 會將檔案上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="02cac-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-160">-內容</span><span class="sxs-lookup"><span data-stu-id="02cac-160">-Context</span></span>
<span data-ttu-id="02cac-161">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="02cac-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="02cac-162">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-162">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02cac-163">-DefaultProfile</span></span>
<span data-ttu-id="02cac-164">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02cac-164">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-165">檔案</span><span class="sxs-lookup"><span data-stu-id="02cac-165">-File</span></span>
<span data-ttu-id="02cac-166">指定檔案的本機檔案路徑，以將它上傳成 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="02cac-166">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-167">-Force</span><span class="sxs-lookup"><span data-stu-id="02cac-167">-Force</span></span>
<span data-ttu-id="02cac-168">表示此 Cmdlet 會覆寫現有的 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="02cac-168">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="02cac-169">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="02cac-169">-Metadata</span></span>
<span data-ttu-id="02cac-170">指定上傳的 blob 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="02cac-170">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-171">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="02cac-171">-PremiumPageBlobTier</span></span>
<span data-ttu-id="02cac-172">頁面 Blob 層</span><span class="sxs-lookup"><span data-stu-id="02cac-172">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-173">-屬性</span><span class="sxs-lookup"><span data-stu-id="02cac-173">-Properties</span></span>
<span data-ttu-id="02cac-174">指定上傳的 blob 的屬性。</span><span class="sxs-lookup"><span data-stu-id="02cac-174">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="02cac-175">支援的屬性為： CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="02cac-175">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cac-176">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02cac-176">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="02cac-177">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="02cac-177">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="02cac-178">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="02cac-178">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="02cac-179">-確認</span><span class="sxs-lookup"><span data-stu-id="02cac-179">-Confirm</span></span>
<span data-ttu-id="02cac-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02cac-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02cac-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02cac-181">-WhatIf</span></span>
<span data-ttu-id="02cac-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02cac-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02cac-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02cac-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02cac-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02cac-184">CommonParameters</span></span>
<span data-ttu-id="02cac-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02cac-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02cac-186">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02cac-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02cac-187">輸入</span><span class="sxs-lookup"><span data-stu-id="02cac-187">INPUTS</span></span>

### <span data-ttu-id="02cac-188">System.object</span><span class="sxs-lookup"><span data-stu-id="02cac-188">System.String</span></span>

### <span data-ttu-id="02cac-189">[WindowsAzure] CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="02cac-189">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="02cac-190">[WindowsAzure] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="02cac-190">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="02cac-191">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="02cac-191">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="02cac-192">輸出</span><span class="sxs-lookup"><span data-stu-id="02cac-192">OUTPUTS</span></span>

### <span data-ttu-id="02cac-193">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="02cac-193">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="02cac-194">筆記</span><span class="sxs-lookup"><span data-stu-id="02cac-194">NOTES</span></span>

## <span data-ttu-id="02cac-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="02cac-195">RELATED LINKS</span></span>

[<span data-ttu-id="02cac-196">AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="02cac-196">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="02cac-197">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="02cac-197">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="02cac-198">移除-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="02cac-198">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
