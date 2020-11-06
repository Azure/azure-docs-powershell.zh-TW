---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d9a602e3e946e28dd04b67c030aeec2aecc3ec93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614486"
---
# <span data-ttu-id="ed0a3-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ed0a3-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="ed0a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed0a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0a3-103">將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="ed0a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed0a3-104">SYNTAX</span></span>

### <span data-ttu-id="ed0a3-105">SendManual (預設) </span><span class="sxs-lookup"><span data-stu-id="ed0a3-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed0a3-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ed0a3-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed0a3-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ed0a3-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed0a3-108">說明</span><span class="sxs-lookup"><span data-stu-id="ed0a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ed0a3-109">**AzStorageBlobContent** Cmdlet 會將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="ed0a3-110">示例</span><span class="sxs-lookup"><span data-stu-id="ed0a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ed0a3-111">範例1：上傳命名的檔案</span><span class="sxs-lookup"><span data-stu-id="ed0a3-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="ed0a3-112">這個命令會將名為 PlanningData 的檔案上傳到名為 Planning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="ed0a3-113">範例2：上傳目前資料夾底下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="ed0a3-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="ed0a3-114">這個命令使用核心的 Windows PowerShell Cmdlet Get-ChildItem 來取得目前資料夾和子資料夾中的所有檔案，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed0a3-115">**AzStorageBlobContent** Cmdlet 會將檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="ed0a3-116">範例3：覆寫現有的 blob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="ed0a3-117">這個命令會使用 Get-AzStorageBlob Cmdlet，在 ContosoUploads 容器中取得名為 Planning2015 的 blob，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="ed0a3-118">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="ed0a3-119">這個命令不會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="ed0a3-120">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="ed0a3-121">如果您確認命令，Cmdlet 會覆寫現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="ed0a3-122">範例4：使用管線將檔案上傳到容器</span><span class="sxs-lookup"><span data-stu-id="ed0a3-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="ed0a3-123">這個命令會使用 **AzStorageContainer** Cmdlet 來取得以字串 ContosoUpload 開頭的容器，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="ed0a3-124">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="ed0a3-125">範例5：將檔案上傳到含中繼資料的頁面 blob，並 PremiumPageBlobTier 為 P10</span><span class="sxs-lookup"><span data-stu-id="ed0a3-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="ed0a3-126">第一個命令會建立包含 blob 中繼資料的雜湊資料表，並將該雜湊資料表儲存在 $Metadata 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="ed0a3-127">第二個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="ed0a3-128">Blob 包括儲存在 $Metadata 中的中繼資料，並以 P10 的方式 PremiumPageBlobTier。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="ed0a3-129">範例6：將檔案上傳到具有指定 blob 屬性的 blob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="ed0a3-130">這個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器，且具有指定的 blob 屬性。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="ed0a3-131">參數</span><span class="sxs-lookup"><span data-stu-id="ed0a3-131">PARAMETERS</span></span>

### <span data-ttu-id="ed0a3-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-132">-AsJob</span></span>
<span data-ttu-id="ed0a3-133">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ed0a3-134">-Blob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-134">-Blob</span></span>
<span data-ttu-id="ed0a3-135">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="ed0a3-136">這個 Cmdlet 會將檔案上傳到此參數指定的 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed0a3-137">-BlobType</span><span class="sxs-lookup"><span data-stu-id="ed0a3-137">-BlobType</span></span>
<span data-ttu-id="ed0a3-138">指定此 Cmdlet 上傳的 blob 類型。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="ed0a3-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed0a3-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed0a3-140">框圖</span><span class="sxs-lookup"><span data-stu-id="ed0a3-140">Block</span></span>
- <span data-ttu-id="ed0a3-141">[預設值] 為 [區塊] 的頁面。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-141">Page The default value is Block.</span></span>

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

### <span data-ttu-id="ed0a3-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed0a3-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ed0a3-143">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed0a3-144">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed0a3-145">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed0a3-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-146">-CloudBlob</span></span>
<span data-ttu-id="ed0a3-147">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="ed0a3-148">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ed0a3-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ed0a3-149">-CloudBlobContainer</span></span>
<span data-ttu-id="ed0a3-150">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ed0a3-151">這個 Cmdlet 會將內容上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="ed0a3-152">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="ed0a3-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ed0a3-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ed0a3-154">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ed0a3-155">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ed0a3-156">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ed0a3-157">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ed0a3-158">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-158">The default value is 10.</span></span>

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

### <span data-ttu-id="ed0a3-159">-容器</span><span class="sxs-lookup"><span data-stu-id="ed0a3-159">-Container</span></span>
<span data-ttu-id="ed0a3-160">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-160">Specifies the name of a container.</span></span>
<span data-ttu-id="ed0a3-161">這個 Cmdlet 會將檔案上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed0a3-162">-內容</span><span class="sxs-lookup"><span data-stu-id="ed0a3-162">-Context</span></span>
<span data-ttu-id="ed0a3-163">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ed0a3-164">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="ed0a3-165">若要使用從 SAS 權杖建立且沒有讀取權限的儲存空間內容，請需要 add-Force 參數來略過檢查 blob existance。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

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

### <span data-ttu-id="ed0a3-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0a3-166">-DefaultProfile</span></span>
<span data-ttu-id="ed0a3-167">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0a3-168">檔案</span><span class="sxs-lookup"><span data-stu-id="ed0a3-168">-File</span></span>
<span data-ttu-id="ed0a3-169">指定檔案的本機檔案路徑，以將它上傳成 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-169">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="ed0a3-170">-Force</span><span class="sxs-lookup"><span data-stu-id="ed0a3-170">-Force</span></span>
<span data-ttu-id="ed0a3-171">表示此 Cmdlet 會覆寫現有的 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ed0a3-172">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="ed0a3-172">-Metadata</span></span>
<span data-ttu-id="ed0a3-173">指定上傳的 blob 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-173">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="ed0a3-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="ed0a3-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="ed0a3-175">頁面 Blob 層</span><span class="sxs-lookup"><span data-stu-id="ed0a3-175">Page Blob Tier</span></span>

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

### <span data-ttu-id="ed0a3-176">-屬性</span><span class="sxs-lookup"><span data-stu-id="ed0a3-176">-Properties</span></span>
<span data-ttu-id="ed0a3-177">指定上傳的 blob 的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="ed0a3-178">支援的屬性為： CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="ed0a3-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed0a3-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ed0a3-180">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ed0a3-181">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ed0a3-182">-確認</span><span class="sxs-lookup"><span data-stu-id="ed0a3-182">-Confirm</span></span>
<span data-ttu-id="ed0a3-183">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed0a3-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed0a3-184">-WhatIf</span></span>
<span data-ttu-id="ed0a3-185">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed0a3-186">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed0a3-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0a3-187">CommonParameters</span></span>
<span data-ttu-id="ed0a3-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0a3-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0a3-190">輸入</span><span class="sxs-lookup"><span data-stu-id="ed0a3-190">INPUTS</span></span>

### <span data-ttu-id="ed0a3-191">System.object</span><span class="sxs-lookup"><span data-stu-id="ed0a3-191">System.String</span></span>

### <span data-ttu-id="ed0a3-192">[WindowsAzure] CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ed0a3-192">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ed0a3-193">[WindowsAzure] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-193">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ed0a3-194">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ed0a3-194">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ed0a3-195">輸出</span><span class="sxs-lookup"><span data-stu-id="ed0a3-195">OUTPUTS</span></span>

### <span data-ttu-id="ed0a3-196">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="ed0a3-196">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ed0a3-197">筆記</span><span class="sxs-lookup"><span data-stu-id="ed0a3-197">NOTES</span></span>

## <span data-ttu-id="ed0a3-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed0a3-198">RELATED LINKS</span></span>

[<span data-ttu-id="ed0a3-199">AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ed0a3-199">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="ed0a3-200">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-200">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ed0a3-201">移除-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ed0a3-201">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)