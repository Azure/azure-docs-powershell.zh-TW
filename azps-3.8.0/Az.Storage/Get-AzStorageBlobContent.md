---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 3f8c85ac8f6a93438176fb20acd98fdb84733927
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957183"
---
# <span data-ttu-id="7e8d6-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e8d6-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="7e8d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8d6-103">下載儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="7e8d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e8d6-104">SYNTAX</span></span>

### <span data-ttu-id="7e8d6-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="7e8d6-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e8d6-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="7e8d6-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e8d6-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="7e8d6-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e8d6-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e8d6-108">DESCRIPTION</span></span>
<span data-ttu-id="7e8d6-109">**AzStorageBlobContent** Cmdlet 會下載指定的儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="7e8d6-110">如果 blob 名稱對於本機電腦無效，則此 Cmdlet 會在可能的情況下自動解決此情況。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="7e8d6-111">示例</span><span class="sxs-lookup"><span data-stu-id="7e8d6-111">EXAMPLES</span></span>

### <span data-ttu-id="7e8d6-112">範例1：依名稱下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="7e8d6-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="7e8d6-113">這個命令會依名稱下載 blob。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="7e8d6-114">範例2：使用管線下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="7e8d6-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="7e8d6-115">這個命令會使用管線來尋找及下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="7e8d6-116">範例3：使用管線和萬用字元下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="7e8d6-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="7e8d6-117">這個範例使用星號萬用字元和管線來尋找及下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="7e8d6-118">範例4：取得 blob 物件並將它儲存在變數中，然後使用 blob 物件下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="7e8d6-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="7e8d6-119">這個範例會先取得 blob 物件，並將它儲存在變數中，然後使用 blob 物件下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="7e8d6-120">參數</span><span class="sxs-lookup"><span data-stu-id="7e8d6-120">PARAMETERS</span></span>

### <span data-ttu-id="7e8d6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e8d6-121">-AsJob</span></span>
<span data-ttu-id="7e8d6-122">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7e8d6-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="7e8d6-123">-Blob</span></span>
<span data-ttu-id="7e8d6-124">指定要下載的 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8d6-125">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="7e8d6-125">-CheckMd5</span></span>
<span data-ttu-id="7e8d6-126">指定是否要檢查已下載檔案的 Md5 加總。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-126">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="7e8d6-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e8d6-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7e8d6-128">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7e8d6-129">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7e8d6-130">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7e8d6-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7e8d6-131">-CloudBlob</span></span>
<span data-ttu-id="7e8d6-132">指定雲端 blob。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-132">Specifies a cloud blob.</span></span>
<span data-ttu-id="7e8d6-133">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="7e8d6-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7e8d6-134">-CloudBlobContainer</span></span>
<span data-ttu-id="7e8d6-135">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-135">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="7e8d6-136">您可以建立或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-136">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="7e8d6-137">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7e8d6-137">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7e8d6-138">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-138">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7e8d6-139">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-139">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7e8d6-140">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-140">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7e8d6-141">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-141">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7e8d6-142">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-142">The default value is 10.</span></span>

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

### <span data-ttu-id="7e8d6-143">-容器</span><span class="sxs-lookup"><span data-stu-id="7e8d6-143">-Container</span></span>
<span data-ttu-id="7e8d6-144">指定包含您要下載之 blob 的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-144">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8d6-145">-內容</span><span class="sxs-lookup"><span data-stu-id="7e8d6-145">-Context</span></span>
<span data-ttu-id="7e8d6-146">指定您想要從中下載 blob 內容的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-146">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="7e8d6-147">您可以使用 New-AzStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-147">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="7e8d6-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8d6-148">-DefaultProfile</span></span>
<span data-ttu-id="7e8d6-149">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e8d6-150">-目的地</span><span class="sxs-lookup"><span data-stu-id="7e8d6-150">-Destination</span></span>
<span data-ttu-id="7e8d6-151">指定要儲存下載檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-151">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8d6-152">-Force</span><span class="sxs-lookup"><span data-stu-id="7e8d6-152">-Force</span></span>
<span data-ttu-id="7e8d6-153">覆寫現有檔案而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-153">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="7e8d6-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e8d6-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7e8d6-155">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7e8d6-156">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7e8d6-157">-確認</span><span class="sxs-lookup"><span data-stu-id="7e8d6-157">-Confirm</span></span>
<span data-ttu-id="7e8d6-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e8d6-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e8d6-159">-WhatIf</span></span>
<span data-ttu-id="7e8d6-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e8d6-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e8d6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8d6-162">CommonParameters</span></span>
<span data-ttu-id="7e8d6-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8d6-164">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8d6-165">輸入</span><span class="sxs-lookup"><span data-stu-id="7e8d6-165">INPUTS</span></span>

### <span data-ttu-id="7e8d6-166">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-166">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="7e8d6-167">[CloudBlobContainer]。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-167">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="7e8d6-168">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="7e8d6-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e8d6-169">輸出</span><span class="sxs-lookup"><span data-stu-id="7e8d6-169">OUTPUTS</span></span>

### <span data-ttu-id="7e8d6-170">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-170">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="7e8d6-171">筆記</span><span class="sxs-lookup"><span data-stu-id="7e8d6-171">NOTES</span></span>
* <span data-ttu-id="7e8d6-172">如果 blob 名稱對於本機電腦無效，則此 Cmdlet 會 autoresolves 它（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="7e8d6-172">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="7e8d6-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e8d6-173">RELATED LINKS</span></span>

[<span data-ttu-id="7e8d6-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e8d6-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="7e8d6-175">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7e8d6-175">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="7e8d6-176">移除-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7e8d6-176">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
