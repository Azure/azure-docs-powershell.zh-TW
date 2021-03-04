---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: b3c2e5809cf2f9aa13a11600351c64a825caf5d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915142"
---
# <span data-ttu-id="530a0-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="530a0-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="530a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="530a0-102">SYNOPSIS</span></span>
<span data-ttu-id="530a0-103">下載儲存 Blob。</span><span class="sxs-lookup"><span data-stu-id="530a0-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="530a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="530a0-104">SYNTAX</span></span>

### <span data-ttu-id="530a0-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="530a0-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="530a0-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="530a0-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="530a0-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="530a0-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="530a0-108">描述</span><span class="sxs-lookup"><span data-stu-id="530a0-108">DESCRIPTION</span></span>
<span data-ttu-id="530a0-109">**Get-AzStorageBlobContent** Cmdlet 會下載指定的儲存 Blob。</span><span class="sxs-lookup"><span data-stu-id="530a0-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="530a0-110">如果 Blob 名稱對本地電腦無效，此 Cmdlet 會盡可能自動解析。</span><span class="sxs-lookup"><span data-stu-id="530a0-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="530a0-111">例子</span><span class="sxs-lookup"><span data-stu-id="530a0-111">EXAMPLES</span></span>

### <span data-ttu-id="530a0-112">範例 1：按名稱下載 Blob 內容</span><span class="sxs-lookup"><span data-stu-id="530a0-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="530a0-113">此命令會按名稱下載 Blob。</span><span class="sxs-lookup"><span data-stu-id="530a0-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="530a0-114">範例 2：使用管線下載 Blob 內容</span><span class="sxs-lookup"><span data-stu-id="530a0-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="530a0-115">此命令使用管線來尋找及下載 Blob 內容。</span><span class="sxs-lookup"><span data-stu-id="530a0-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="530a0-116">範例 3：使用管線和萬用字元下載 Blob 內容</span><span class="sxs-lookup"><span data-stu-id="530a0-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="530a0-117">此範例使用星號萬用字元和管線來尋找及下載 Blob 內容。</span><span class="sxs-lookup"><span data-stu-id="530a0-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="530a0-118">範例 4：取得 Blob 物件並將其儲存在變數中，然後使用 Blob 物件下載 Blob 內容</span><span class="sxs-lookup"><span data-stu-id="530a0-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="530a0-119">此範例先取得 Blob 物件並將其儲存為變數，然後下載包含 Blob 物件的 Blob 內容。</span><span class="sxs-lookup"><span data-stu-id="530a0-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="530a0-120">參數</span><span class="sxs-lookup"><span data-stu-id="530a0-120">PARAMETERS</span></span>

### <span data-ttu-id="530a0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="530a0-121">-AsJob</span></span>
<span data-ttu-id="530a0-122">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="530a0-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="530a0-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="530a0-123">-Blob</span></span>
<span data-ttu-id="530a0-124">指定要下載的 Blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="530a0-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="530a0-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="530a0-125">-BlobBaseClient</span></span>
<span data-ttu-id="530a0-126">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="530a0-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="530a0-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="530a0-127">-CheckMd5</span></span>
<span data-ttu-id="530a0-128">指定是否要針對下載的檔案檢查 Md5 加總。</span><span class="sxs-lookup"><span data-stu-id="530a0-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="530a0-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="530a0-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="530a0-130">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="530a0-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="530a0-131">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="530a0-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="530a0-132">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="530a0-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="530a0-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="530a0-133">-CloudBlob</span></span>
<span data-ttu-id="530a0-134">指定雲端 Blob。</span><span class="sxs-lookup"><span data-stu-id="530a0-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="530a0-135">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="530a0-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="530a0-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="530a0-136">-CloudBlobContainer</span></span>
<span data-ttu-id="530a0-137">從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="530a0-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="530a0-138">您可以建立它，或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="530a0-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="530a0-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="530a0-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="530a0-140">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="530a0-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="530a0-141">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="530a0-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="530a0-142">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="530a0-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="530a0-143">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="530a0-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="530a0-144">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="530a0-144">The default value is 10.</span></span>

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

### <span data-ttu-id="530a0-145">-Container</span><span class="sxs-lookup"><span data-stu-id="530a0-145">-Container</span></span>
<span data-ttu-id="530a0-146">指定包含您想要下載之 Blob 的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="530a0-146">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="530a0-147">-內容</span><span class="sxs-lookup"><span data-stu-id="530a0-147">-Context</span></span>
<span data-ttu-id="530a0-148">指定要下載 Blob 內容的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="530a0-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="530a0-149">您可以使用 New-AzStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="530a0-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="530a0-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530a0-150">-DefaultProfile</span></span>
<span data-ttu-id="530a0-151">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="530a0-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="530a0-152">-目的地</span><span class="sxs-lookup"><span data-stu-id="530a0-152">-Destination</span></span>
<span data-ttu-id="530a0-153">指定儲存下載檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="530a0-153">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="530a0-154">-強制</span><span class="sxs-lookup"><span data-stu-id="530a0-154">-Force</span></span>
<span data-ttu-id="530a0-155">覆寫現有的檔案而不確認。</span><span class="sxs-lookup"><span data-stu-id="530a0-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="530a0-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="530a0-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="530a0-157">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="530a0-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="530a0-158">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="530a0-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="530a0-159">-確認</span><span class="sxs-lookup"><span data-stu-id="530a0-159">-Confirm</span></span>
<span data-ttu-id="530a0-160">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="530a0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="530a0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="530a0-161">-WhatIf</span></span>
<span data-ttu-id="530a0-162">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="530a0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="530a0-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="530a0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="530a0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530a0-164">CommonParameters</span></span>
<span data-ttu-id="530a0-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="530a0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530a0-166">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="530a0-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530a0-167">輸入</span><span class="sxs-lookup"><span data-stu-id="530a0-167">INPUTS</span></span>

### <span data-ttu-id="530a0-168">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="530a0-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="530a0-169">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="530a0-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="530a0-170">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="530a0-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="530a0-171">輸出</span><span class="sxs-lookup"><span data-stu-id="530a0-171">OUTPUTS</span></span>

### <span data-ttu-id="530a0-172">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="530a0-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="530a0-173">筆記</span><span class="sxs-lookup"><span data-stu-id="530a0-173">NOTES</span></span>
* <span data-ttu-id="530a0-174">如果 Blob 名稱對本地電腦無效，此 Cmdlet 會盡可能自動解決它。</span><span class="sxs-lookup"><span data-stu-id="530a0-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="530a0-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="530a0-175">RELATED LINKS</span></span>

[<span data-ttu-id="530a0-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="530a0-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="530a0-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="530a0-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="530a0-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="530a0-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
