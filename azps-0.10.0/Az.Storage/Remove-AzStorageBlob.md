---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: ed2701a5cdb15b02a2627fc3bacc42861a1fdbb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795075"
---
# <span data-ttu-id="1f5d8-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="1f5d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5d8-103">移除指定的儲存區 blob。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="1f5d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f5d8-104">SYNTAX</span></span>

### <span data-ttu-id="1f5d8-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="1f5d8-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f5d8-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="1f5d8-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f5d8-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="1f5d8-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f5d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="1f5d8-108">DESCRIPTION</span></span>
<span data-ttu-id="1f5d8-109">**AzStorageBlob** Cmdlet 會將指定的 Blob 從 Azure 中的儲存空間帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="1f5d8-110">示例</span><span class="sxs-lookup"><span data-stu-id="1f5d8-110">EXAMPLES</span></span>

### <span data-ttu-id="1f5d8-111">範例1：依名稱移除儲存 blob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="1f5d8-112">這個命令會移除其名稱所識別的 blob。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="1f5d8-113">範例2：使用管線移除儲存 blob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="1f5d8-114">這個命令會使用管線。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="1f5d8-115">範例3：使用管線移除儲存區 blob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="1f5d8-116">這個命令使用星號 ( \* ) 萬用字元和管線來檢索 blob 或 blob，然後將它們移除。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="1f5d8-117">參數</span><span class="sxs-lookup"><span data-stu-id="1f5d8-117">PARAMETERS</span></span>

### <span data-ttu-id="1f5d8-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-118">-Blob</span></span>
<span data-ttu-id="1f5d8-119">指定要移除之 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="1f5d8-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f5d8-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1f5d8-121">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1f5d8-122">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1f5d8-123">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1f5d8-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-124">-CloudBlob</span></span>
<span data-ttu-id="1f5d8-125">指定雲端 blob。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="1f5d8-126">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f5d8-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1f5d8-127">-CloudBlobContainer</span></span>
<span data-ttu-id="1f5d8-128">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="1f5d8-129">您可以使用 Get-AzStorageContainer Cmdlet 來取得它。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f5d8-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1f5d8-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1f5d8-131">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1f5d8-132">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1f5d8-133">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1f5d8-134">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1f5d8-135">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-135">The default value is 10.</span></span>

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

### <span data-ttu-id="1f5d8-136">-容器</span><span class="sxs-lookup"><span data-stu-id="1f5d8-136">-Container</span></span>
<span data-ttu-id="1f5d8-137">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="1f5d8-138">-內容</span><span class="sxs-lookup"><span data-stu-id="1f5d8-138">-Context</span></span>
<span data-ttu-id="1f5d8-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1f5d8-140">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="1f5d8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5d8-141">-DefaultProfile</span></span>
<span data-ttu-id="1f5d8-142">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f5d8-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="1f5d8-143">-DeleteSnapshot</span></span>
<span data-ttu-id="1f5d8-144">指定要刪除所有快照，但不是基底 blob。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="1f5d8-145">如果未指定此參數，則會將基底與其快照一起刪除。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="1f5d8-146">系統會提示使用者確認刪除操作。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="1f5d8-147">-Force</span><span class="sxs-lookup"><span data-stu-id="1f5d8-147">-Force</span></span>
<span data-ttu-id="1f5d8-148">表示此 Cmdlet 不需確認即移除 blob 及其快照。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="1f5d8-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f5d8-149">-PassThru</span></span>
<span data-ttu-id="1f5d8-150">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1f5d8-151">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1f5d8-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f5d8-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1f5d8-153">指定要讀取之 Cmdlet 的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="1f5d8-154">如果沒有指定，則會從預設設定檔讀取 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="1f5d8-155">-確認</span><span class="sxs-lookup"><span data-stu-id="1f5d8-155">-Confirm</span></span>
<span data-ttu-id="1f5d8-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f5d8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f5d8-157">-WhatIf</span></span>
<span data-ttu-id="1f5d8-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f5d8-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f5d8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5d8-160">CommonParameters</span></span>
<span data-ttu-id="1f5d8-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5d8-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f5d8-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5d8-163">輸入</span><span class="sxs-lookup"><span data-stu-id="1f5d8-163">INPUTS</span></span>

### <span data-ttu-id="1f5d8-164">[WindowsAz] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-164">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="1f5d8-165">[WindowsAz] CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1f5d8-165">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="1f5d8-166">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="1f5d8-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f5d8-167">輸出</span><span class="sxs-lookup"><span data-stu-id="1f5d8-167">OUTPUTS</span></span>

### <span data-ttu-id="1f5d8-168">System.object</span><span class="sxs-lookup"><span data-stu-id="1f5d8-168">System.Boolean</span></span>

## <span data-ttu-id="1f5d8-169">筆記</span><span class="sxs-lookup"><span data-stu-id="1f5d8-169">NOTES</span></span>

## <span data-ttu-id="1f5d8-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f5d8-170">RELATED LINKS</span></span>

[<span data-ttu-id="1f5d8-171">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1f5d8-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="1f5d8-172">AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1f5d8-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="1f5d8-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1f5d8-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
