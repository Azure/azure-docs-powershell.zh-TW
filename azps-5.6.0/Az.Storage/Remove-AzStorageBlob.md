---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 12bfa9ab7e35bab3421bee71cf5ea0787c95a86d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901630"
---
# <span data-ttu-id="4f369-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4f369-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="4f369-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4f369-102">SYNOPSIS</span></span>
<span data-ttu-id="4f369-103">移除指定的儲存 Blob。</span><span class="sxs-lookup"><span data-stu-id="4f369-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="4f369-104">語法</span><span class="sxs-lookup"><span data-stu-id="4f369-104">SYNTAX</span></span>

### <span data-ttu-id="4f369-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="4f369-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f369-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="4f369-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f369-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="4f369-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f369-108">描述</span><span class="sxs-lookup"><span data-stu-id="4f369-108">DESCRIPTION</span></span>
<span data-ttu-id="4f369-109">**Remove-AzStorageBlob** Cmdlet 會從 Azure 中的儲存帳戶移除指定的 Blob。</span><span class="sxs-lookup"><span data-stu-id="4f369-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="4f369-110">例子</span><span class="sxs-lookup"><span data-stu-id="4f369-110">EXAMPLES</span></span>

### <span data-ttu-id="4f369-111">範例 1：根據名稱移除儲存 Blob</span><span class="sxs-lookup"><span data-stu-id="4f369-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="4f369-112">此命令會移除以名稱識別的 Blob。</span><span class="sxs-lookup"><span data-stu-id="4f369-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="4f369-113">範例 2：使用管線移除儲存 Blob</span><span class="sxs-lookup"><span data-stu-id="4f369-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="4f369-114">此命令使用管線。</span><span class="sxs-lookup"><span data-stu-id="4f369-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="4f369-115">範例 3：使用管線移除儲存 Blob</span><span class="sxs-lookup"><span data-stu-id="4f369-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="4f369-116">此命令使用星號 (\*) 萬用字元和管線來取回 Blob 或 Blob，然後將它們移除。</span><span class="sxs-lookup"><span data-stu-id="4f369-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="4f369-117">範例 4：移除單一 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="4f369-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="4f369-118">此命令會移除使用 VersionId 的單一 Blob 版本。</span><span class="sxs-lookup"><span data-stu-id="4f369-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="4f369-119">範例 5：移除單一 Blob 快照</span><span class="sxs-lookup"><span data-stu-id="4f369-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="4f369-120">此命令會使用 SnapshotTime 移除單一 Blob 快照。</span><span class="sxs-lookup"><span data-stu-id="4f369-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="4f369-121">參數</span><span class="sxs-lookup"><span data-stu-id="4f369-121">PARAMETERS</span></span>

### <span data-ttu-id="4f369-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="4f369-122">-Blob</span></span>
<span data-ttu-id="4f369-123">指定您想要移除的 Blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="4f369-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="4f369-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="4f369-124">-BlobBaseClient</span></span>
<span data-ttu-id="4f369-125">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="4f369-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="4f369-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4f369-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4f369-127">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="4f369-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4f369-128">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="4f369-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4f369-129">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f369-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4f369-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4f369-130">-CloudBlob</span></span>
<span data-ttu-id="4f369-131">指定雲端 Blob。</span><span class="sxs-lookup"><span data-stu-id="4f369-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="4f369-132">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f369-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="4f369-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4f369-133">-CloudBlobContainer</span></span>
<span data-ttu-id="4f369-134">從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="4f369-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="4f369-135">您可以使用 Cmdlet Get-AzStorageContainer取得它。</span><span class="sxs-lookup"><span data-stu-id="4f369-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="4f369-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4f369-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4f369-137">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="4f369-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4f369-138">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="4f369-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4f369-139">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="4f369-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4f369-140">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="4f369-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4f369-141">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="4f369-141">The default value is 10.</span></span>

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

### <span data-ttu-id="4f369-142">-Container</span><span class="sxs-lookup"><span data-stu-id="4f369-142">-Container</span></span>
<span data-ttu-id="4f369-143">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f369-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="4f369-144">-內容</span><span class="sxs-lookup"><span data-stu-id="4f369-144">-Context</span></span>
<span data-ttu-id="4f369-145">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="4f369-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4f369-146">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="4f369-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="4f369-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f369-147">-DefaultProfile</span></span>
<span data-ttu-id="4f369-148">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f369-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f369-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="4f369-149">-DeleteSnapshot</span></span>
<span data-ttu-id="4f369-150">指定刪除所有快照，但不要刪除基本 Blob。</span><span class="sxs-lookup"><span data-stu-id="4f369-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="4f369-151">如果未指定此參數，基準 Blob 及其快照會一併刪除。</span><span class="sxs-lookup"><span data-stu-id="4f369-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="4f369-152">系統會提示使用者確認刪除作業。</span><span class="sxs-lookup"><span data-stu-id="4f369-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="4f369-153">-強制</span><span class="sxs-lookup"><span data-stu-id="4f369-153">-Force</span></span>
<span data-ttu-id="4f369-154">表示此 Cmdlet 會移除 Blob 及其快照，但不確認。</span><span class="sxs-lookup"><span data-stu-id="4f369-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="4f369-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f369-155">-PassThru</span></span>
<span data-ttu-id="4f369-156">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="4f369-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4f369-157">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f369-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4f369-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4f369-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4f369-159">指定要讀取 Cmdlet 的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4f369-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="4f369-160">如果未指定，Cmdlet 會從預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4f369-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="4f369-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="4f369-161">-SnapshotTime</span></span>
<span data-ttu-id="4f369-162">Blob 快照時間</span><span class="sxs-lookup"><span data-stu-id="4f369-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="4f369-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="4f369-163">-VersionId</span></span>
<span data-ttu-id="4f369-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="4f369-164">Blob VersionId</span></span>

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

### <span data-ttu-id="4f369-165">-確認</span><span class="sxs-lookup"><span data-stu-id="4f369-165">-Confirm</span></span>
<span data-ttu-id="4f369-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4f369-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f369-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f369-167">-WhatIf</span></span>
<span data-ttu-id="4f369-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f369-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f369-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f369-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f369-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f369-170">CommonParameters</span></span>
<span data-ttu-id="4f369-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4f369-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f369-172">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4f369-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f369-173">輸入</span><span class="sxs-lookup"><span data-stu-id="4f369-173">INPUTS</span></span>

### <span data-ttu-id="4f369-174">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4f369-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="4f369-175">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4f369-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="4f369-176">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4f369-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4f369-177">輸出</span><span class="sxs-lookup"><span data-stu-id="4f369-177">OUTPUTS</span></span>

### <span data-ttu-id="4f369-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f369-178">System.Boolean</span></span>

## <span data-ttu-id="4f369-179">筆記</span><span class="sxs-lookup"><span data-stu-id="4f369-179">NOTES</span></span>

## <span data-ttu-id="4f369-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f369-180">RELATED LINKS</span></span>

[<span data-ttu-id="4f369-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4f369-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="4f369-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4f369-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="4f369-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4f369-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
