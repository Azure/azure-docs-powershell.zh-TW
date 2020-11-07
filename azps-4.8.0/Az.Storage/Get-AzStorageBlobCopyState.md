---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968979"
---
# <span data-ttu-id="f7b73-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="f7b73-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="f7b73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7b73-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b73-103">取得 Azure 儲存區 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="f7b73-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7b73-104">SYNTAX</span></span>

### <span data-ttu-id="f7b73-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="f7b73-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f7b73-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="f7b73-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f7b73-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="f7b73-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f7b73-108">說明</span><span class="sxs-lookup"><span data-stu-id="f7b73-108">DESCRIPTION</span></span>
<span data-ttu-id="f7b73-109">**AzStorageBlobCopyState** Cmdlet 會取得 Azure 儲存空間 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="f7b73-110">它應該在複製的目的地 blob 上執行。</span><span class="sxs-lookup"><span data-stu-id="f7b73-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="f7b73-111">示例</span><span class="sxs-lookup"><span data-stu-id="f7b73-111">EXAMPLES</span></span>

### <span data-ttu-id="f7b73-112">範例1：取得 blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="f7b73-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="f7b73-113">這個命令會取得容器 ContosoUploads 中名為 ContosoPlanning2015 的 blob 複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="f7b73-114">範例2：使用管線取得 blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="f7b73-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="f7b73-115">這個命令會透過使用 **AzStorageBlob** Cmdlet 來取得名為 ContosoUploads 之容器中名為 ContosoPlanning2015 的 blob，然後使用管線運算子將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7b73-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f7b73-116">**AzStorageBlobCopyState** Cmdlet 會取得該 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="f7b73-117">範例3：使用管線在容器中取得 blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="f7b73-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="f7b73-118">這個命令會取得使用 **AzStorageBlob** Cmdlet 命名的容器，然後將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7b73-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="f7b73-119">**AzStorageContainer** Cmdlet 會取得該容器中名為 ContosoPlanning2015 的 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="f7b73-120">範例4：啟動複製和管線以取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="f7b73-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="f7b73-121">第一個命令會開始將 blob "ContosoPlanning2015" 複製到 "ContosoPlanning2015_copy"，並輸出 destiantion blob 物件。</span><span class="sxs-lookup"><span data-stu-id="f7b73-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="f7b73-122">第二個命令管線是 destiantion blob 物件來取得 AzStorageBlobCopyState，以取得 blob 複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="f7b73-123">參數</span><span class="sxs-lookup"><span data-stu-id="f7b73-123">PARAMETERS</span></span>

### <span data-ttu-id="f7b73-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="f7b73-124">-Blob</span></span>
<span data-ttu-id="f7b73-125">指定 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7b73-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="f7b73-126">這個 Cmdlet 會取得此參數指定之 Azure 存儲 blob 的 blob 複製作業狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7b73-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f7b73-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f7b73-128">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7b73-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f7b73-129">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="f7b73-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f7b73-130">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7b73-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f7b73-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f7b73-131">-CloudBlob</span></span>
<span data-ttu-id="f7b73-132">從 Azure 儲存空間用戶端文件庫指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="f7b73-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="f7b73-133">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7b73-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="f7b73-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f7b73-134">-CloudBlobContainer</span></span>
<span data-ttu-id="f7b73-135">指定 Azure 存儲用戶端文件庫中的 **CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="f7b73-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="f7b73-136">這個 Cmdlet 會取得此參數指定容器中 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="f7b73-137">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7b73-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="f7b73-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f7b73-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f7b73-139">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="f7b73-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f7b73-140">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="f7b73-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f7b73-141">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="f7b73-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f7b73-142">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="f7b73-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f7b73-143">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="f7b73-143">The default value is 10.</span></span>

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

### <span data-ttu-id="f7b73-144">-容器</span><span class="sxs-lookup"><span data-stu-id="f7b73-144">-Container</span></span>
<span data-ttu-id="f7b73-145">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7b73-145">Specifies the name of a container.</span></span>
<span data-ttu-id="f7b73-146">這個 Cmdlet 會取得此參數指定容器中 blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="f7b73-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7b73-147">-內容</span><span class="sxs-lookup"><span data-stu-id="f7b73-147">-Context</span></span>
<span data-ttu-id="f7b73-148">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="f7b73-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f7b73-149">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7b73-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f7b73-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b73-150">-DefaultProfile</span></span>
<span data-ttu-id="f7b73-151">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7b73-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b73-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f7b73-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f7b73-153">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7b73-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f7b73-154">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7b73-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f7b73-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f7b73-155">-WaitForComplete</span></span>
<span data-ttu-id="f7b73-156">表示此 Cmdlet 會等待複本完成。</span><span class="sxs-lookup"><span data-stu-id="f7b73-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="f7b73-157">如果您沒有指定此參數，這個 Cmdlet 會立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="f7b73-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="f7b73-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b73-158">CommonParameters</span></span>
<span data-ttu-id="f7b73-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7b73-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b73-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7b73-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b73-161">輸入</span><span class="sxs-lookup"><span data-stu-id="f7b73-161">INPUTS</span></span>

### <span data-ttu-id="f7b73-162">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="f7b73-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="f7b73-163">[CloudBlobContainer]。</span><span class="sxs-lookup"><span data-stu-id="f7b73-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="f7b73-164">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="f7b73-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f7b73-165">輸出</span><span class="sxs-lookup"><span data-stu-id="f7b73-165">OUTPUTS</span></span>

### <span data-ttu-id="f7b73-166">[CopyState]。</span><span class="sxs-lookup"><span data-stu-id="f7b73-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="f7b73-167">筆記</span><span class="sxs-lookup"><span data-stu-id="f7b73-167">NOTES</span></span>

## <span data-ttu-id="f7b73-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7b73-168">RELATED LINKS</span></span>

[<span data-ttu-id="f7b73-169">開始-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7b73-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="f7b73-170">停止 AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7b73-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


