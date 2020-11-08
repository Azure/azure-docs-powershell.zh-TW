---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140768"
---
# <span data-ttu-id="4cf13-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4cf13-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="4cf13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cf13-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf13-103">移除指定的儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="4cf13-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="4cf13-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cf13-104">SYNTAX</span></span>

### <span data-ttu-id="4cf13-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="4cf13-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cf13-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="4cf13-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cf13-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="4cf13-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cf13-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cf13-108">DESCRIPTION</span></span>
<span data-ttu-id="4cf13-109">**AzStorageBlob** Cmdlet 會將指定的 Blob 從 Azure 中的儲存空間帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="4cf13-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="4cf13-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cf13-110">EXAMPLES</span></span>

### <span data-ttu-id="4cf13-111">範例1：依名稱移除儲存 blob</span><span class="sxs-lookup"><span data-stu-id="4cf13-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="4cf13-112">這個命令會移除其名稱所識別的 blob。</span><span class="sxs-lookup"><span data-stu-id="4cf13-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="4cf13-113">範例2：使用管線移除儲存 blob</span><span class="sxs-lookup"><span data-stu-id="4cf13-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="4cf13-114">這個命令會使用管線。</span><span class="sxs-lookup"><span data-stu-id="4cf13-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="4cf13-115">範例3：使用管線移除儲存區 blob</span><span class="sxs-lookup"><span data-stu-id="4cf13-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="4cf13-116">這個命令使用星號 ( \* ) 萬用字元和管線來檢索 blob 或 blob，然後將它們移除。</span><span class="sxs-lookup"><span data-stu-id="4cf13-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="4cf13-117">範例4：移除單一 blob 版本</span><span class="sxs-lookup"><span data-stu-id="4cf13-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="4cf13-118">這個命令會在 VersionId 中移除單一 blob verion。</span><span class="sxs-lookup"><span data-stu-id="4cf13-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="4cf13-119">範例5：移除單一 blob 快照</span><span class="sxs-lookup"><span data-stu-id="4cf13-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="4cf13-120">這個命令會將單一的 blob 快照與 SnapshotTime 移除。</span><span class="sxs-lookup"><span data-stu-id="4cf13-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="4cf13-121">參數</span><span class="sxs-lookup"><span data-stu-id="4cf13-121">PARAMETERS</span></span>

### <span data-ttu-id="4cf13-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="4cf13-122">-Blob</span></span>
<span data-ttu-id="4cf13-123">指定要移除之 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf13-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="4cf13-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="4cf13-124">-BlobBaseClient</span></span>
<span data-ttu-id="4cf13-125">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="4cf13-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="4cf13-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cf13-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cf13-127">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4cf13-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cf13-128">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="4cf13-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cf13-129">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cf13-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cf13-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4cf13-130">-CloudBlob</span></span>
<span data-ttu-id="4cf13-131">指定雲端 blob。</span><span class="sxs-lookup"><span data-stu-id="4cf13-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="4cf13-132">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf13-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="4cf13-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4cf13-133">-CloudBlobContainer</span></span>
<span data-ttu-id="4cf13-134">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="4cf13-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="4cf13-135">您可以使用 Get-AzStorageContainer Cmdlet 來取得它。</span><span class="sxs-lookup"><span data-stu-id="4cf13-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="4cf13-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cf13-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cf13-137">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="4cf13-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cf13-138">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="4cf13-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cf13-139">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="4cf13-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cf13-140">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="4cf13-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cf13-141">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="4cf13-141">The default value is 10.</span></span>

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

### <span data-ttu-id="4cf13-142">-容器</span><span class="sxs-lookup"><span data-stu-id="4cf13-142">-Container</span></span>
<span data-ttu-id="4cf13-143">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf13-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="4cf13-144">-內容</span><span class="sxs-lookup"><span data-stu-id="4cf13-144">-Context</span></span>
<span data-ttu-id="4cf13-145">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4cf13-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4cf13-146">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="4cf13-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="4cf13-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf13-147">-DefaultProfile</span></span>
<span data-ttu-id="4cf13-148">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cf13-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf13-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="4cf13-149">-DeleteSnapshot</span></span>
<span data-ttu-id="4cf13-150">指定要刪除所有快照，但不是基底 blob。</span><span class="sxs-lookup"><span data-stu-id="4cf13-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="4cf13-151">如果未指定此參數，則會將基底與其快照一起刪除。</span><span class="sxs-lookup"><span data-stu-id="4cf13-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="4cf13-152">系統會提示使用者確認刪除操作。</span><span class="sxs-lookup"><span data-stu-id="4cf13-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="4cf13-153">-Force</span><span class="sxs-lookup"><span data-stu-id="4cf13-153">-Force</span></span>
<span data-ttu-id="4cf13-154">表示此 Cmdlet 不需確認即移除 blob 及其快照。</span><span class="sxs-lookup"><span data-stu-id="4cf13-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="4cf13-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cf13-155">-PassThru</span></span>
<span data-ttu-id="4cf13-156">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="4cf13-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4cf13-157">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4cf13-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4cf13-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cf13-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cf13-159">指定要讀取之 Cmdlet 的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4cf13-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="4cf13-160">如果沒有指定，則會從預設設定檔讀取 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf13-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="4cf13-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="4cf13-161">-SnapshotTime</span></span>
<span data-ttu-id="4cf13-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="4cf13-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf13-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="4cf13-163">-VersionId</span></span>
<span data-ttu-id="4cf13-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="4cf13-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf13-165">-確認</span><span class="sxs-lookup"><span data-stu-id="4cf13-165">-Confirm</span></span>
<span data-ttu-id="4cf13-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cf13-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf13-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf13-167">-WhatIf</span></span>
<span data-ttu-id="4cf13-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cf13-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf13-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf13-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf13-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf13-170">CommonParameters</span></span>
<span data-ttu-id="4cf13-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cf13-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf13-172">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cf13-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf13-173">輸入</span><span class="sxs-lookup"><span data-stu-id="4cf13-173">INPUTS</span></span>

### <span data-ttu-id="4cf13-174">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="4cf13-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="4cf13-175">[CloudBlobContainer]。</span><span class="sxs-lookup"><span data-stu-id="4cf13-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="4cf13-176">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="4cf13-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4cf13-177">輸出</span><span class="sxs-lookup"><span data-stu-id="4cf13-177">OUTPUTS</span></span>

### <span data-ttu-id="4cf13-178">System.object</span><span class="sxs-lookup"><span data-stu-id="4cf13-178">System.Boolean</span></span>

## <span data-ttu-id="4cf13-179">筆記</span><span class="sxs-lookup"><span data-stu-id="4cf13-179">NOTES</span></span>

## <span data-ttu-id="4cf13-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cf13-180">RELATED LINKS</span></span>

[<span data-ttu-id="4cf13-181">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4cf13-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="4cf13-182">AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4cf13-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="4cf13-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4cf13-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
