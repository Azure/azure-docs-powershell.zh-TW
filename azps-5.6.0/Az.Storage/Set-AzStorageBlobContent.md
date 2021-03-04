---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 66cad13b7c3b1596b2ce369b454f5a0f9ff54b8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907962"
---
# <span data-ttu-id="e6193-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e6193-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="e6193-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6193-102">SYNOPSIS</span></span>
<span data-ttu-id="e6193-103">將本地檔案上傳到 Azure 儲存體 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="e6193-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6193-104">SYNTAX</span></span>

### <span data-ttu-id="e6193-105">SendManual (預設) </span><span class="sxs-lookup"><span data-stu-id="e6193-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6193-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="e6193-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6193-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="e6193-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6193-108">描述</span><span class="sxs-lookup"><span data-stu-id="e6193-108">DESCRIPTION</span></span>
<span data-ttu-id="e6193-109">**Set-AzStorageBlobContent** Cmdlet 會上傳一個本地檔案至 Azure 儲存體 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="e6193-110">例子</span><span class="sxs-lookup"><span data-stu-id="e6193-110">EXAMPLES</span></span>

### <span data-ttu-id="e6193-111">範例 1：上傳已命名的檔案</span><span class="sxs-lookup"><span data-stu-id="e6193-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="e6193-112">此命令會上傳名為 PlanningData 的檔案至名為 Planning2015 的 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="e6193-113">範例 2：上傳目前資料夾下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="e6193-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="e6193-114">此命令使用核心 Windows PowerShell Cmdlet Get-ChildItem 取得目前資料夾和子資料夾中的所有檔案，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e6193-115">**Set-AzStorageBlobContent** Cmdlet 會上傳檔案至名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="e6193-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="e6193-116">範例 3：覆寫現有的 Blob</span><span class="sxs-lookup"><span data-stu-id="e6193-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="e6193-117">此命令會使用 Get-AzStorageBlob Cmdlet 在 ContosoUploads 容器中，獲得名為 Planning2015 的 Blob，然後將該 Blob 傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="e6193-118">該命令會上傳名為 ContosoPlanning 為規劃2015 的檔案。</span><span class="sxs-lookup"><span data-stu-id="e6193-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="e6193-119">此命令不會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e6193-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="e6193-120">命令會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6193-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="e6193-121">如果您確認命令，Cmdlet 會覆寫現有的 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="e6193-122">範例 4：使用管線將檔案上傳至容器</span><span class="sxs-lookup"><span data-stu-id="e6193-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="e6193-123">此命令會取得使用 **Get-AzStorageContainer** Cmdlet 以字串 ContosoUpload 開頭的容器，然後將該 Blob 傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="e6193-124">該命令會上傳名為 ContosoPlanning 為規劃2015 的檔案。</span><span class="sxs-lookup"><span data-stu-id="e6193-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="e6193-125">範例 5：將檔案上傳至包含中繼資料的頁面 blob，將 PremiumPageBlobTier 上傳為 P10</span><span class="sxs-lookup"><span data-stu-id="e6193-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="e6193-126">第一個命令會建立包含 Blob 中繼資料的雜湊表，並儲存該雜湊$Metadata變數。</span><span class="sxs-lookup"><span data-stu-id="e6193-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="e6193-127">第二個命令會上傳名為 ContosoPlanning 的檔案至名為 ContosoUploads 的容器。</span><span class="sxs-lookup"><span data-stu-id="e6193-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="e6193-128">Blob 包含儲存在 $Metadata 中的中繼資料，而且具有 PremiumPageBlobTier 作為 P10。</span><span class="sxs-lookup"><span data-stu-id="e6193-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="e6193-129">範例 6：將檔案上傳到具有指定 Blob 屬性的 Blob，並設定 StandardBlobTier 為 Cool</span><span class="sxs-lookup"><span data-stu-id="e6193-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="e6193-130">此命令會上傳檔案至c:\temp\index.htmblob 屬性為 contosouploads 的容器，並設定 StandardBlobTier 為 Cool。</span><span class="sxs-lookup"><span data-stu-id="e6193-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="e6193-131">此命令會由 [System.Web.MimeMapping]：：GetMimeMapping () API。</span><span class="sxs-lookup"><span data-stu-id="e6193-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="e6193-132">範例 7：使用加密範圍將檔案上傳到 Blob</span><span class="sxs-lookup"><span data-stu-id="e6193-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="e6193-133">此命令會上傳檔案至具有加密範圍的 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="e6193-134">參數</span><span class="sxs-lookup"><span data-stu-id="e6193-134">PARAMETERS</span></span>

### <span data-ttu-id="e6193-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6193-135">-AsJob</span></span>
<span data-ttu-id="e6193-136">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e6193-137">-Blob</span><span class="sxs-lookup"><span data-stu-id="e6193-137">-Blob</span></span>
<span data-ttu-id="e6193-138">指定 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6193-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="e6193-139">此 Cmdlet 會上傳檔案至此參數指定的 Azure 儲存體 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6193-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="e6193-140">-BlobType</span></span>
<span data-ttu-id="e6193-141">指定此 Cmdlet 上傳的 Blob 類型。</span><span class="sxs-lookup"><span data-stu-id="e6193-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="e6193-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e6193-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6193-143">塊</span><span class="sxs-lookup"><span data-stu-id="e6193-143">Block</span></span>
- <span data-ttu-id="e6193-144">網頁</span><span class="sxs-lookup"><span data-stu-id="e6193-144">Page</span></span>
- <span data-ttu-id="e6193-145">附加預設值為封鎖。</span><span class="sxs-lookup"><span data-stu-id="e6193-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="e6193-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e6193-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e6193-147">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="e6193-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e6193-148">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="e6193-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e6193-149">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e6193-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e6193-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e6193-150">-CloudBlob</span></span>
<span data-ttu-id="e6193-151">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="e6193-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="e6193-152">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="e6193-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e6193-153">-CloudBlobContainer</span></span>
<span data-ttu-id="e6193-154">從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="e6193-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="e6193-155">此 Cmdlet 會上傳內容至此參數指定之容器中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="e6193-156">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="e6193-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e6193-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e6193-158">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="e6193-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e6193-159">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="e6193-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e6193-160">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="e6193-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e6193-161">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="e6193-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e6193-162">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="e6193-162">The default value is 10.</span></span>

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

### <span data-ttu-id="e6193-163">-Container</span><span class="sxs-lookup"><span data-stu-id="e6193-163">-Container</span></span>
<span data-ttu-id="e6193-164">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6193-164">Specifies the name of a container.</span></span>
<span data-ttu-id="e6193-165">此 Cmdlet 會在此參數指定的容器中將檔案上傳到 Blob。</span><span class="sxs-lookup"><span data-stu-id="e6193-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6193-166">-內容</span><span class="sxs-lookup"><span data-stu-id="e6193-166">-Context</span></span>
<span data-ttu-id="e6193-167">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="e6193-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e6193-168">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="e6193-169">若要在沒有讀取權限的情況下使用從 SAS Token 所建立儲存內容，需要新增 -Force 參數來略過檢查 Blob 是否存在。</span><span class="sxs-lookup"><span data-stu-id="e6193-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="e6193-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6193-170">-DefaultProfile</span></span>
<span data-ttu-id="e6193-171">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6193-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6193-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e6193-172">-EncryptionScope</span></span>
<span data-ttu-id="e6193-173">要求 Blob 時所使用的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="e6193-173">Encryption scope to be used when making requests to the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6193-174">-檔案</span><span class="sxs-lookup"><span data-stu-id="e6193-174">-File</span></span>
<span data-ttu-id="e6193-175">指定要上傳為 Blob 內容的檔案之本地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e6193-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="e6193-176">-強制</span><span class="sxs-lookup"><span data-stu-id="e6193-176">-Force</span></span>
<span data-ttu-id="e6193-177">表示此 Cmdlet 覆寫現有的 Blob，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6193-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e6193-178">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="e6193-178">-Metadata</span></span>
<span data-ttu-id="e6193-179">指定上傳 Blob 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e6193-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="e6193-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="e6193-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="e6193-181">頁面 Blob 層</span><span class="sxs-lookup"><span data-stu-id="e6193-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="e6193-182">-Properties</span><span class="sxs-lookup"><span data-stu-id="e6193-182">-Properties</span></span>
<span data-ttu-id="e6193-183">指定上傳 Blob 的屬性。</span><span class="sxs-lookup"><span data-stu-id="e6193-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="e6193-184">支援的屬性為：CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="e6193-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="e6193-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e6193-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e6193-186">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="e6193-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e6193-187">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e6193-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="e6193-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="e6193-188">-StandardBlobTier</span></span>
<span data-ttu-id="e6193-189">封鎖 Blob 層，有效的值為 Hot/Cool/Archive。</span><span class="sxs-lookup"><span data-stu-id="e6193-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="e6193-190">請參閱 https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="e6193-190">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="e6193-191">-確認</span><span class="sxs-lookup"><span data-stu-id="e6193-191">-Confirm</span></span>
<span data-ttu-id="e6193-192">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6193-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6193-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6193-193">-WhatIf</span></span>
<span data-ttu-id="e6193-194">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6193-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6193-195">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6193-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6193-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6193-196">CommonParameters</span></span>
<span data-ttu-id="e6193-197">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6193-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6193-198">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e6193-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6193-199">輸入</span><span class="sxs-lookup"><span data-stu-id="e6193-199">INPUTS</span></span>

### <span data-ttu-id="e6193-200">System.String</span><span class="sxs-lookup"><span data-stu-id="e6193-200">System.String</span></span>

### <span data-ttu-id="e6193-201">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e6193-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="e6193-202">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e6193-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e6193-203">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="e6193-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e6193-204">輸出</span><span class="sxs-lookup"><span data-stu-id="e6193-204">OUTPUTS</span></span>

### <span data-ttu-id="e6193-205">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e6193-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="e6193-206">筆記</span><span class="sxs-lookup"><span data-stu-id="e6193-206">NOTES</span></span>

## <span data-ttu-id="e6193-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6193-207">RELATED LINKS</span></span>

[<span data-ttu-id="e6193-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e6193-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="e6193-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e6193-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e6193-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e6193-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
