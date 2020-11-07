---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
ms.openlocfilehash: 67a6a9d706b8865ebca4290649a30bc8e9817569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624641"
---
# <span data-ttu-id="6fd66-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6fd66-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="6fd66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fd66-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd66-103">停止複製操作。</span><span class="sxs-lookup"><span data-stu-id="6fd66-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fd66-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fd66-104">SYNTAX</span></span>

### <span data-ttu-id="6fd66-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="6fd66-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fd66-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6fd66-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fd66-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6fd66-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fd66-108">說明</span><span class="sxs-lookup"><span data-stu-id="6fd66-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd66-109">**AzureStorageBlobCopy** Cmdlet 會停止複製操作至指定的目的地 blob。</span><span class="sxs-lookup"><span data-stu-id="6fd66-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="6fd66-110">示例</span><span class="sxs-lookup"><span data-stu-id="6fd66-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd66-111">範例1：停止複製操作（依名稱）</span><span class="sxs-lookup"><span data-stu-id="6fd66-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="6fd66-112">這個命令會依名稱停止複製操作。</span><span class="sxs-lookup"><span data-stu-id="6fd66-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="6fd66-113">範例2：使用管線停止複製操作</span><span class="sxs-lookup"><span data-stu-id="6fd66-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="6fd66-114">這個命令會從 **AzureStorageContainer** 傳送管線上的容器，以停止複製操作。</span><span class="sxs-lookup"><span data-stu-id="6fd66-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="6fd66-115">範例3：使用管線和 Get-AzureStorageBlob 停止複製操作</span><span class="sxs-lookup"><span data-stu-id="6fd66-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="6fd66-116">這個範例會從 Get-AzureStorageBlob Cmdlet 傳送管線上的容器，以停止複製操作。</span><span class="sxs-lookup"><span data-stu-id="6fd66-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="6fd66-117">參數</span><span class="sxs-lookup"><span data-stu-id="6fd66-117">PARAMETERS</span></span>

### <span data-ttu-id="6fd66-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="6fd66-118">-Blob</span></span>
<span data-ttu-id="6fd66-119">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fd66-119">Specifies the name of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd66-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6fd66-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6fd66-121">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6fd66-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6fd66-122">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="6fd66-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6fd66-123">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6fd66-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6fd66-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6fd66-124">-CloudBlob</span></span>
<span data-ttu-id="6fd66-125">從 Azure 儲存空間用戶端文件庫指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="6fd66-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6fd66-126">若要取得 **CloudBlob** 物件，請使用 Get-AzureStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fd66-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6fd66-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6fd66-127">-CloudBlobContainer</span></span>
<span data-ttu-id="6fd66-128">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="6fd66-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6fd66-129">您可以建立物件或使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fd66-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6fd66-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6fd66-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6fd66-131">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="6fd66-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6fd66-132">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="6fd66-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6fd66-133">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="6fd66-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6fd66-134">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="6fd66-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6fd66-135">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="6fd66-135">The default value is 10.</span></span>

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

### <span data-ttu-id="6fd66-136">-容器</span><span class="sxs-lookup"><span data-stu-id="6fd66-136">-Container</span></span>
<span data-ttu-id="6fd66-137">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fd66-137">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd66-138">-內容</span><span class="sxs-lookup"><span data-stu-id="6fd66-138">-Context</span></span>
<span data-ttu-id="6fd66-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6fd66-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6fd66-140">您可以使用 New-AzureStorageContext Cmdlet 來建立內容。</span><span class="sxs-lookup"><span data-stu-id="6fd66-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6fd66-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="6fd66-141">-CopyId</span></span>
<span data-ttu-id="6fd66-142">指定複製識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fd66-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="6fd66-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd66-143">-DefaultProfile</span></span>
<span data-ttu-id="6fd66-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fd66-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd66-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6fd66-145">-Force</span></span>
<span data-ttu-id="6fd66-146">停止指定 blob 上的目前複製工作，而不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6fd66-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6fd66-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6fd66-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6fd66-148">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6fd66-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6fd66-149">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6fd66-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6fd66-150">-確認</span><span class="sxs-lookup"><span data-stu-id="6fd66-150">-Confirm</span></span>
<span data-ttu-id="6fd66-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fd66-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd66-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd66-152">-WhatIf</span></span>
<span data-ttu-id="6fd66-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fd66-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd66-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fd66-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd66-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd66-155">CommonParameters</span></span>
<span data-ttu-id="6fd66-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fd66-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd66-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6fd66-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd66-158">輸入</span><span class="sxs-lookup"><span data-stu-id="6fd66-158">INPUTS</span></span>

### <span data-ttu-id="6fd66-159">[WindowsAzure] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6fd66-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6fd66-160">[WindowsAzure] CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6fd66-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6fd66-161">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="6fd66-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6fd66-162">輸出</span><span class="sxs-lookup"><span data-stu-id="6fd66-162">OUTPUTS</span></span>

### <span data-ttu-id="6fd66-163">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="6fd66-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6fd66-164">筆記</span><span class="sxs-lookup"><span data-stu-id="6fd66-164">NOTES</span></span>

## <span data-ttu-id="6fd66-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fd66-165">RELATED LINKS</span></span>

[<span data-ttu-id="6fd66-166">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6fd66-166">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="6fd66-167">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6fd66-167">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="6fd66-168">開始-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6fd66-168">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="6fd66-169">AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="6fd66-169">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
