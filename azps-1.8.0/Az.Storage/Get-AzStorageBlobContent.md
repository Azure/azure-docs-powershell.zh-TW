---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 76af94e4ab2518a47fad03f31a2f0f24bb0d0422
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614615"
---
# <span data-ttu-id="c7419-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c7419-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="c7419-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7419-102">SYNOPSIS</span></span>
<span data-ttu-id="c7419-103">下載儲存 blob。</span><span class="sxs-lookup"><span data-stu-id="c7419-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="c7419-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7419-104">SYNTAX</span></span>

### <span data-ttu-id="c7419-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="c7419-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7419-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c7419-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7419-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c7419-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7419-108">說明</span><span class="sxs-lookup"><span data-stu-id="c7419-108">DESCRIPTION</span></span>
<span data-ttu-id="c7419-109">**AzStorageBlobContent** Cmdlet 會下載指定的儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="c7419-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="c7419-110">如果 blob 名稱對於本機電腦無效，則此 Cmdlet 會在可能的情況下自動解決此情況。</span><span class="sxs-lookup"><span data-stu-id="c7419-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="c7419-111">示例</span><span class="sxs-lookup"><span data-stu-id="c7419-111">EXAMPLES</span></span>

### <span data-ttu-id="c7419-112">範例1：依名稱下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="c7419-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="c7419-113">這個命令會依名稱下載 blob。</span><span class="sxs-lookup"><span data-stu-id="c7419-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="c7419-114">範例2：使用管線下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="c7419-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="c7419-115">這個命令會使用管線來尋找及下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="c7419-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="c7419-116">範例3：使用管線和萬用字元下載 blob 內容</span><span class="sxs-lookup"><span data-stu-id="c7419-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="c7419-117">這個範例使用星號萬用字元和管線來尋找及下載 blob 內容。</span><span class="sxs-lookup"><span data-stu-id="c7419-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="c7419-118">參數</span><span class="sxs-lookup"><span data-stu-id="c7419-118">PARAMETERS</span></span>

### <span data-ttu-id="c7419-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7419-119">-AsJob</span></span>
<span data-ttu-id="c7419-120">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7419-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c7419-121">-Blob</span><span class="sxs-lookup"><span data-stu-id="c7419-121">-Blob</span></span>
<span data-ttu-id="c7419-122">指定要下載的 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="c7419-122">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="c7419-123">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="c7419-123">-CheckMd5</span></span>
<span data-ttu-id="c7419-124">指定是否要檢查已下載檔案的 Md5 加總。</span><span class="sxs-lookup"><span data-stu-id="c7419-124">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="c7419-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7419-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c7419-126">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7419-126">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c7419-127">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="c7419-127">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c7419-128">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7419-128">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c7419-129">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c7419-129">-CloudBlob</span></span>
<span data-ttu-id="c7419-130">指定雲端 blob。</span><span class="sxs-lookup"><span data-stu-id="c7419-130">Specifies a cloud blob.</span></span>
<span data-ttu-id="c7419-131">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7419-131">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="c7419-132">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c7419-132">-CloudBlobContainer</span></span>
<span data-ttu-id="c7419-133">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="c7419-133">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="c7419-134">您可以建立或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7419-134">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="c7419-135">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c7419-135">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c7419-136">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="c7419-136">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c7419-137">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="c7419-137">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c7419-138">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="c7419-138">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c7419-139">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="c7419-139">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c7419-140">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="c7419-140">The default value is 10.</span></span>
<span data-ttu-id="c7419-141">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="c7419-141">The default value is 10.</span></span>

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

### <span data-ttu-id="c7419-142">-容器</span><span class="sxs-lookup"><span data-stu-id="c7419-142">-Container</span></span>
<span data-ttu-id="c7419-143">指定包含您要下載之 blob 的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="c7419-143">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="c7419-144">-內容</span><span class="sxs-lookup"><span data-stu-id="c7419-144">-Context</span></span>
<span data-ttu-id="c7419-145">指定您想要從中下載 blob 內容的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c7419-145">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="c7419-146">您可以使用 New-AzStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c7419-146">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="c7419-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7419-147">-DefaultProfile</span></span>
<span data-ttu-id="c7419-148">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7419-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7419-149">-目的地</span><span class="sxs-lookup"><span data-stu-id="c7419-149">-Destination</span></span>
<span data-ttu-id="c7419-150">指定要儲存下載檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="c7419-150">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="c7419-151">-Force</span><span class="sxs-lookup"><span data-stu-id="c7419-151">-Force</span></span>
<span data-ttu-id="c7419-152">覆寫現有檔案而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7419-152">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="c7419-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7419-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c7419-154">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7419-154">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c7419-155">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7419-155">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c7419-156">-確認</span><span class="sxs-lookup"><span data-stu-id="c7419-156">-Confirm</span></span>
<span data-ttu-id="c7419-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7419-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7419-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7419-158">-WhatIf</span></span>
<span data-ttu-id="c7419-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7419-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7419-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7419-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7419-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7419-161">CommonParameters</span></span>
<span data-ttu-id="c7419-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7419-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7419-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7419-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7419-164">輸入</span><span class="sxs-lookup"><span data-stu-id="c7419-164">INPUTS</span></span>

### <span data-ttu-id="c7419-165">[WindowsAzure] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c7419-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c7419-166">[WindowsAzure] CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c7419-166">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c7419-167">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c7419-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7419-168">輸出</span><span class="sxs-lookup"><span data-stu-id="c7419-168">OUTPUTS</span></span>

### <span data-ttu-id="c7419-169">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="c7419-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c7419-170">筆記</span><span class="sxs-lookup"><span data-stu-id="c7419-170">NOTES</span></span>
* <span data-ttu-id="c7419-171">如果 blob 名稱對於本機電腦無效，則此 Cmdlet 會 autoresolves 它（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="c7419-171">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="c7419-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7419-172">RELATED LINKS</span></span>

[<span data-ttu-id="c7419-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c7419-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="c7419-174">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c7419-174">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c7419-175">移除-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c7419-175">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
