---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 4bc06ca07c95986f75062a64a0f86475f7720ff1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915141"
---
# <span data-ttu-id="2584d-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="2584d-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="2584d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2584d-102">SYNOPSIS</span></span>
<span data-ttu-id="2584d-103">獲得 Azure 儲存體 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="2584d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2584d-104">SYNTAX</span></span>

### <span data-ttu-id="2584d-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="2584d-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2584d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2584d-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2584d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2584d-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2584d-108">描述</span><span class="sxs-lookup"><span data-stu-id="2584d-108">DESCRIPTION</span></span>
<span data-ttu-id="2584d-109">**Get-AzStorageBlobCopyState** Cmdlet 會取得 Azure 儲存體 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="2584d-110">它應該在複製目的地 Blob 上執行。</span><span class="sxs-lookup"><span data-stu-id="2584d-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="2584d-111">例子</span><span class="sxs-lookup"><span data-stu-id="2584d-111">EXAMPLES</span></span>

### <span data-ttu-id="2584d-112">範例 1：取得 Blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="2584d-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="2584d-113">此命令會獲得容器 ContosoUploads 中名為 ContosoPlanning2015 的 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="2584d-114">範例 2：使用管線取得 Blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="2584d-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="2584d-115">此命令會使用 **Get-AzStorageBlob** Cmdlet，在名為 ContosoUploads 的容器中取得名為 ContosoPlanning2015 的 Blob，然後使用管線運算子將結果傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2584d-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2584d-116">**Get-AzStorageBlobCopyState** Cmdlet 會取得該 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="2584d-117">範例 3：使用管線取得容器內 Blob 的複製狀態</span><span class="sxs-lookup"><span data-stu-id="2584d-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="2584d-118">此命令會使用 **Get-AzStorageBlob** Cmdlet 來命名容器，然後將結果傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2584d-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="2584d-119">**Get-AzStorageContainer Cmdlet** 會取得該容器中名為 ContosoPlanning2015 之 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="2584d-120">範例 4：啟動複製和管線以取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="2584d-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="2584d-121">第一個命令會開始將 Blob "ContosoPlanning2015" 複製到 "ContosoPlanning2015_copy"，並輸出 destiantion Blob 物件。</span><span class="sxs-lookup"><span data-stu-id="2584d-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="2584d-122">第二個命令管線將 destiantion Blob 物件用於 Get-AzStorageBlobCopyState，以取得 Blob 複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="2584d-123">參數</span><span class="sxs-lookup"><span data-stu-id="2584d-123">PARAMETERS</span></span>

### <span data-ttu-id="2584d-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="2584d-124">-Blob</span></span>
<span data-ttu-id="2584d-125">指定 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2584d-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="2584d-126">此 Cmdlet 會針對此參數指定的 Azure 儲存體 Blob，獲得 Blob 複製作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="2584d-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2584d-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2584d-128">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="2584d-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2584d-129">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="2584d-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2584d-130">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2584d-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2584d-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2584d-131">-CloudBlob</span></span>
<span data-ttu-id="2584d-132">從 **Azure 儲存用戶端文件庫指定 CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="2584d-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="2584d-133">若要取得 **CloudBlob** 物件，請使用 Get-AzStorageBlob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2584d-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="2584d-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2584d-134">-CloudBlobContainer</span></span>
<span data-ttu-id="2584d-135">從 **Azure 儲存用戶端文件庫指定 CloudBlobContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="2584d-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2584d-136">此 Cmdlet 會在此參數指定的容器中，獲得 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="2584d-137">若要取得 **CloudBlobContainer** 物件，請使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2584d-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="2584d-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2584d-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2584d-139">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="2584d-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2584d-140">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="2584d-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2584d-141">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="2584d-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2584d-142">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="2584d-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2584d-143">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="2584d-143">The default value is 10.</span></span>

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

### <span data-ttu-id="2584d-144">-Container</span><span class="sxs-lookup"><span data-stu-id="2584d-144">-Container</span></span>
<span data-ttu-id="2584d-145">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2584d-145">Specifies the name of a container.</span></span>
<span data-ttu-id="2584d-146">此 Cmdlet 會在此參數指定的容器中，獲得 Blob 的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="2584d-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="2584d-147">-內容</span><span class="sxs-lookup"><span data-stu-id="2584d-147">-Context</span></span>
<span data-ttu-id="2584d-148">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2584d-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2584d-149">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2584d-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2584d-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2584d-150">-DefaultProfile</span></span>
<span data-ttu-id="2584d-151">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2584d-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2584d-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2584d-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2584d-153">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="2584d-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2584d-154">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2584d-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2584d-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="2584d-155">-WaitForComplete</span></span>
<span data-ttu-id="2584d-156">表示此 Cmdlet 會等待複製完成。</span><span class="sxs-lookup"><span data-stu-id="2584d-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="2584d-157">如果您未指定此參數，此 Cmdlet 會立即返回結果。</span><span class="sxs-lookup"><span data-stu-id="2584d-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="2584d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2584d-158">CommonParameters</span></span>
<span data-ttu-id="2584d-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2584d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2584d-160">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2584d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2584d-161">輸入</span><span class="sxs-lookup"><span data-stu-id="2584d-161">INPUTS</span></span>

### <span data-ttu-id="2584d-162">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2584d-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2584d-163">Microsoft.Azure.storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2584d-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="2584d-164">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2584d-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2584d-165">輸出</span><span class="sxs-lookup"><span data-stu-id="2584d-165">OUTPUTS</span></span>

### <span data-ttu-id="2584d-166">Microsoft.Azure.storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="2584d-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="2584d-167">筆記</span><span class="sxs-lookup"><span data-stu-id="2584d-167">NOTES</span></span>

## <span data-ttu-id="2584d-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="2584d-168">RELATED LINKS</span></span>

[<span data-ttu-id="2584d-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2584d-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="2584d-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2584d-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


