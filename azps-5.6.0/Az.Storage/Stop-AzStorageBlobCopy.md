---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 1be012a9a9c5a62cbd08451849f8d50e9a5d52a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903938"
---
# <span data-ttu-id="04758-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04758-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="04758-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04758-102">SYNOPSIS</span></span>
<span data-ttu-id="04758-103">停止複製作業。</span><span class="sxs-lookup"><span data-stu-id="04758-103">Stops a copy operation.</span></span>

## <span data-ttu-id="04758-104">語法</span><span class="sxs-lookup"><span data-stu-id="04758-104">SYNTAX</span></span>

### <span data-ttu-id="04758-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="04758-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04758-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="04758-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04758-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="04758-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04758-108">描述</span><span class="sxs-lookup"><span data-stu-id="04758-108">DESCRIPTION</span></span>
<span data-ttu-id="04758-109">**Stop-AzStorageBlobCopy** Cmdlet 會停止對指定目的地 Blob 的複製作業。</span><span class="sxs-lookup"><span data-stu-id="04758-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="04758-110">例子</span><span class="sxs-lookup"><span data-stu-id="04758-110">EXAMPLES</span></span>

### <span data-ttu-id="04758-111">範例 1：根據名稱停止複製作業</span><span class="sxs-lookup"><span data-stu-id="04758-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="04758-112">此命令會以名稱停止複製作業。</span><span class="sxs-lookup"><span data-stu-id="04758-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="04758-113">範例 2：使用管線停止複製作業</span><span class="sxs-lookup"><span data-stu-id="04758-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="04758-114">此命令會從 **Get-AzStorageContainer** 傳遞管線上的容器，以停止複製作業。</span><span class="sxs-lookup"><span data-stu-id="04758-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="04758-115">範例 3：使用管線和管道停止複製Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="04758-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="04758-116">此範例會從 Cmdlet 傳遞管線上的容器，以停止Get-AzStorageBlob作業。</span><span class="sxs-lookup"><span data-stu-id="04758-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="04758-117">參數</span><span class="sxs-lookup"><span data-stu-id="04758-117">PARAMETERS</span></span>

### <span data-ttu-id="04758-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="04758-118">-Blob</span></span>
<span data-ttu-id="04758-119">指定 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="04758-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="04758-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04758-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="04758-121">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="04758-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="04758-122">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="04758-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="04758-123">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="04758-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="04758-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04758-124">-CloudBlob</span></span>
<span data-ttu-id="04758-125">從 **Azure 儲存用戶端文件庫指定 CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="04758-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="04758-126">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04758-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="04758-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="04758-127">-CloudBlobContainer</span></span>
<span data-ttu-id="04758-128">從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="04758-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="04758-129">您可以建立物件，或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04758-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="04758-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="04758-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="04758-131">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="04758-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="04758-132">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="04758-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="04758-133">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="04758-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="04758-134">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="04758-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="04758-135">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="04758-135">The default value is 10.</span></span>

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

### <span data-ttu-id="04758-136">-Container</span><span class="sxs-lookup"><span data-stu-id="04758-136">-Container</span></span>
<span data-ttu-id="04758-137">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="04758-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="04758-138">-內容</span><span class="sxs-lookup"><span data-stu-id="04758-138">-Context</span></span>
<span data-ttu-id="04758-139">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="04758-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="04758-140">您可以使用 Cmdlet 建立New-AzStorageContext內容。</span><span class="sxs-lookup"><span data-stu-id="04758-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04758-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="04758-141">-CopyId</span></span>
<span data-ttu-id="04758-142">指定複製識別碼。</span><span class="sxs-lookup"><span data-stu-id="04758-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="04758-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04758-143">-DefaultProfile</span></span>
<span data-ttu-id="04758-144">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="04758-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04758-145">-強制</span><span class="sxs-lookup"><span data-stu-id="04758-145">-Force</span></span>
<span data-ttu-id="04758-146">停止指定 Blob 上目前的複製工作，而不會提示確認。</span><span class="sxs-lookup"><span data-stu-id="04758-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="04758-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04758-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="04758-148">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="04758-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="04758-149">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="04758-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="04758-150">-確認</span><span class="sxs-lookup"><span data-stu-id="04758-150">-Confirm</span></span>
<span data-ttu-id="04758-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="04758-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04758-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04758-152">-WhatIf</span></span>
<span data-ttu-id="04758-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04758-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04758-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04758-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04758-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04758-155">CommonParameters</span></span>
<span data-ttu-id="04758-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04758-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04758-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="04758-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04758-158">輸入</span><span class="sxs-lookup"><span data-stu-id="04758-158">INPUTS</span></span>

### <span data-ttu-id="04758-159">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04758-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="04758-160">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="04758-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="04758-161">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="04758-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04758-162">輸出</span><span class="sxs-lookup"><span data-stu-id="04758-162">OUTPUTS</span></span>

### <span data-ttu-id="04758-163">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="04758-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="04758-164">筆記</span><span class="sxs-lookup"><span data-stu-id="04758-164">NOTES</span></span>

## <span data-ttu-id="04758-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="04758-165">RELATED LINKS</span></span>

[<span data-ttu-id="04758-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="04758-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="04758-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="04758-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="04758-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04758-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="04758-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="04758-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
