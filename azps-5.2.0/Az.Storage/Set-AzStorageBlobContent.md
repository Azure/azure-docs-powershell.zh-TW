---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d99bde2839e1b4e91d6299cd47319827a57f4f33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279908"
---
# <span data-ttu-id="e379c-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e379c-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="e379c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e379c-102">SYNOPSIS</span></span>
<span data-ttu-id="e379c-103">將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="e379c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e379c-104">SYNTAX</span></span>

### <span data-ttu-id="e379c-105">SendManual (預設) </span><span class="sxs-lookup"><span data-stu-id="e379c-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e379c-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="e379c-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e379c-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="e379c-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e379c-108">說明</span><span class="sxs-lookup"><span data-stu-id="e379c-108">DESCRIPTION</span></span>
<span data-ttu-id="e379c-109">**AzStorageBlobContent** Cmdlet 會將本機檔案上傳到 Azure 儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="e379c-110">示例</span><span class="sxs-lookup"><span data-stu-id="e379c-110">EXAMPLES</span></span>

### <span data-ttu-id="e379c-111">範例1：上傳命名的檔案</span><span class="sxs-lookup"><span data-stu-id="e379c-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="e379c-112">這個命令會將名為 PlanningData 的檔案上傳到名為 Planning2015 的 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="e379c-113">範例2：上傳目前資料夾底下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="e379c-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="e379c-114">這個命令使用核心的 Windows PowerShell Cmdlet Get-ChildItem 來取得目前資料夾和子資料夾中的所有檔案，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e379c-115">**AzStorageBlobContent** Cmdlet 會將檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="e379c-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="e379c-116">範例3：覆寫現有的 blob</span><span class="sxs-lookup"><span data-stu-id="e379c-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="e379c-117">這個命令會使用 Get-AzStorageBlob Cmdlet，在 ContosoUploads 容器中取得名為 Planning2015 的 blob，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="e379c-118">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="e379c-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="e379c-119">這個命令不會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e379c-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="e379c-120">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e379c-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="e379c-121">如果您確認命令，Cmdlet 會覆寫現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="e379c-122">範例4：使用管線將檔案上傳到容器</span><span class="sxs-lookup"><span data-stu-id="e379c-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="e379c-123">這個命令會使用 **AzStorageContainer** Cmdlet 來取得以字串 ContosoUpload 開頭的容器，然後將該 blob 傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="e379c-124">此命令會將名為 ContosoPlanning 的檔案上傳為 Planning2015。</span><span class="sxs-lookup"><span data-stu-id="e379c-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="e379c-125">範例5：將檔案上傳到含中繼資料的頁面 blob，並 PremiumPageBlobTier 為 P10</span><span class="sxs-lookup"><span data-stu-id="e379c-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="e379c-126">第一個命令會建立包含 blob 中繼資料的雜湊資料表，並將該雜湊資料表儲存在 $Metadata 變數中。</span><span class="sxs-lookup"><span data-stu-id="e379c-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="e379c-127">第二個命令會將名為 ContosoPlanning 的檔案上傳到名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="e379c-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="e379c-128">Blob 包括儲存在 $Metadata 中的中繼資料，並以 P10 的方式 PremiumPageBlobTier。</span><span class="sxs-lookup"><span data-stu-id="e379c-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="e379c-129">範例6：將檔案上傳到具有指定 blob 屬性的 blob，並將 StandardBlobTier 設定為超酷</span><span class="sxs-lookup"><span data-stu-id="e379c-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="e379c-130">這個命令會將檔案 c:\temp\index.html 上傳到名為 contosouploads 的容器，並將 StandardBlobTier 設定為超酷。</span><span class="sxs-lookup"><span data-stu-id="e379c-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="e379c-131">這個命令會透過 [MimeMapping]：： GetMimeMapping ( # A1 API，將 ContentType 值設定為 blob 屬性。</span><span class="sxs-lookup"><span data-stu-id="e379c-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="e379c-132">參數</span><span class="sxs-lookup"><span data-stu-id="e379c-132">PARAMETERS</span></span>

### <span data-ttu-id="e379c-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e379c-133">-AsJob</span></span>
<span data-ttu-id="e379c-134">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e379c-135">-Blob</span><span class="sxs-lookup"><span data-stu-id="e379c-135">-Blob</span></span>
<span data-ttu-id="e379c-136">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e379c-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="e379c-137">這個 Cmdlet 會將檔案上傳到此參數指定的 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="e379c-138">-BlobType</span><span class="sxs-lookup"><span data-stu-id="e379c-138">-BlobType</span></span>
<span data-ttu-id="e379c-139">指定此 Cmdlet 上傳的 blob 類型。</span><span class="sxs-lookup"><span data-stu-id="e379c-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="e379c-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e379c-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e379c-141">框圖</span><span class="sxs-lookup"><span data-stu-id="e379c-141">Block</span></span>
- <span data-ttu-id="e379c-142">紙張</span><span class="sxs-lookup"><span data-stu-id="e379c-142">Page</span></span>
- <span data-ttu-id="e379c-143">附加預設值為 Block。</span><span class="sxs-lookup"><span data-stu-id="e379c-143">Append The default value is Block.</span></span>

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

### <span data-ttu-id="e379c-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e379c-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e379c-145">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e379c-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e379c-146">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="e379c-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e379c-147">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e379c-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e379c-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e379c-148">-CloudBlob</span></span>
<span data-ttu-id="e379c-149">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="e379c-149">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="e379c-150">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e379c-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e379c-151">-CloudBlobContainer</span></span>
<span data-ttu-id="e379c-152">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="e379c-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="e379c-153">這個 Cmdlet 會將內容上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-153">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="e379c-154">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e379c-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e379c-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e379c-156">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="e379c-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e379c-157">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="e379c-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e379c-158">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="e379c-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e379c-159">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="e379c-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e379c-160">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="e379c-160">The default value is 10.</span></span>

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

### <span data-ttu-id="e379c-161">-容器</span><span class="sxs-lookup"><span data-stu-id="e379c-161">-Container</span></span>
<span data-ttu-id="e379c-162">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e379c-162">Specifies the name of a container.</span></span>
<span data-ttu-id="e379c-163">這個 Cmdlet 會將檔案上傳到此參數指定的容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="e379c-163">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="e379c-164">-內容</span><span class="sxs-lookup"><span data-stu-id="e379c-164">-Context</span></span>
<span data-ttu-id="e379c-165">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="e379c-165">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e379c-166">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-166">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="e379c-167">若要使用從 SAS 權杖建立且沒有讀取權限的儲存空間內容，請需要 add-Force 參數來略過檢查 blob 存在性。</span><span class="sxs-lookup"><span data-stu-id="e379c-167">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="e379c-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e379c-168">-DefaultProfile</span></span>
<span data-ttu-id="e379c-169">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e379c-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e379c-170">檔案</span><span class="sxs-lookup"><span data-stu-id="e379c-170">-File</span></span>
<span data-ttu-id="e379c-171">指定檔案的本機檔案路徑，以將它上傳成 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="e379c-171">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="e379c-172">-Force</span><span class="sxs-lookup"><span data-stu-id="e379c-172">-Force</span></span>
<span data-ttu-id="e379c-173">表示此 Cmdlet 會覆寫現有的 blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e379c-173">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e379c-174">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="e379c-174">-Metadata</span></span>
<span data-ttu-id="e379c-175">指定上傳的 blob 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e379c-175">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="e379c-176">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="e379c-176">-PremiumPageBlobTier</span></span>
<span data-ttu-id="e379c-177">頁面 Blob 層</span><span class="sxs-lookup"><span data-stu-id="e379c-177">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e379c-178">-屬性</span><span class="sxs-lookup"><span data-stu-id="e379c-178">-Properties</span></span>
<span data-ttu-id="e379c-179">指定上傳的 blob 的屬性。</span><span class="sxs-lookup"><span data-stu-id="e379c-179">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="e379c-180">支援的屬性為： CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="e379c-180">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="e379c-181">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e379c-181">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e379c-182">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e379c-182">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e379c-183">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e379c-183">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="e379c-184">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="e379c-184">-StandardBlobTier</span></span>
<span data-ttu-id="e379c-185">封鎖 Blob 層級，有效值為熱/冷卻/封存。</span><span class="sxs-lookup"><span data-stu-id="e379c-185">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="e379c-186">中查看詳細資料 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="e379c-186">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="e379c-187">-確認</span><span class="sxs-lookup"><span data-stu-id="e379c-187">-Confirm</span></span>
<span data-ttu-id="e379c-188">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e379c-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e379c-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e379c-189">-WhatIf</span></span>
<span data-ttu-id="e379c-190">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e379c-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e379c-191">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e379c-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e379c-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e379c-192">CommonParameters</span></span>
<span data-ttu-id="e379c-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e379c-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e379c-194">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e379c-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e379c-195">輸入</span><span class="sxs-lookup"><span data-stu-id="e379c-195">INPUTS</span></span>

### <span data-ttu-id="e379c-196">System.object</span><span class="sxs-lookup"><span data-stu-id="e379c-196">System.String</span></span>

### <span data-ttu-id="e379c-197">[CloudBlobContainer]。</span><span class="sxs-lookup"><span data-stu-id="e379c-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="e379c-198">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="e379c-198">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e379c-199">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="e379c-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e379c-200">輸出</span><span class="sxs-lookup"><span data-stu-id="e379c-200">OUTPUTS</span></span>

### <span data-ttu-id="e379c-201">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="e379c-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="e379c-202">筆記</span><span class="sxs-lookup"><span data-stu-id="e379c-202">NOTES</span></span>

## <span data-ttu-id="e379c-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="e379c-203">RELATED LINKS</span></span>

[<span data-ttu-id="e379c-204">AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e379c-204">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="e379c-205">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e379c-205">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e379c-206">移除-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e379c-206">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
