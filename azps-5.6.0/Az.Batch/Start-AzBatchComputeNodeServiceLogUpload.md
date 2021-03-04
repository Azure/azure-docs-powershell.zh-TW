---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 84d0d1711c9ed29aa48c4845787529a46686da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907910"
---
# <span data-ttu-id="a864d-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="a864d-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="a864d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a864d-102">SYNOPSIS</span></span>
<span data-ttu-id="a864d-103">將計算節點服務記錄檔案上傳到 Azure 儲存容器。</span><span class="sxs-lookup"><span data-stu-id="a864d-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="a864d-104">語法</span><span class="sxs-lookup"><span data-stu-id="a864d-104">SYNTAX</span></span>

### <span data-ttu-id="a864d-105">AzureBatchComputeNodeServiceLogUpload (預設) </span><span class="sxs-lookup"><span data-stu-id="a864d-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a864d-106">Id</span><span class="sxs-lookup"><span data-stu-id="a864d-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a864d-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="a864d-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a864d-108">描述</span><span class="sxs-lookup"><span data-stu-id="a864d-108">DESCRIPTION</span></span>
<span data-ttu-id="a864d-109">如果您遇到錯誤，並想要升級至 Azure 支援，此 Cmdlet 會從計算節點收集 Azure Batch 服務記錄檔案。</span><span class="sxs-lookup"><span data-stu-id="a864d-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="a864d-110">Azure Batch 服務記錄檔案應該與 Azure 支援人員共用，協助解決批次處理服務的問題。</span><span class="sxs-lookup"><span data-stu-id="a864d-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="a864d-111">例子</span><span class="sxs-lookup"><span data-stu-id="a864d-111">EXAMPLES</span></span>

### <span data-ttu-id="a864d-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a864d-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="a864d-113">上傳在 2018 年 1 月 1 日午夜當天或之後所撰寫的計算節點服務記錄，這些記錄從計算節點取得、計算節點所在之資料庫的給定資料庫識別碼，以及計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="a864d-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="a864d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="a864d-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="a864d-115">上傳在 2018 年 1 月 1 日午夜及 2018 年 1 月 10 日午夜之前所撰寫的計算節點服務記錄，這些記錄從計算節點取得、計算節點所在之資料庫的資料庫識別碼，以及計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="a864d-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="a864d-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="a864d-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="a864d-117">上傳在 2018 年 1 月 1 日午夜及 2018 年 1 月 10 日午夜之前所撰寫的計算節點服務記錄，這些記錄是從計算節點物件取得。</span><span class="sxs-lookup"><span data-stu-id="a864d-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="a864d-118">參數</span><span class="sxs-lookup"><span data-stu-id="a864d-118">PARAMETERS</span></span>

### <span data-ttu-id="a864d-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="a864d-119">-BatchContext</span></span>
<span data-ttu-id="a864d-120">BatchAccountCoNtext 實例，用於與批次處理服務互動。</span><span class="sxs-lookup"><span data-stu-id="a864d-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="a864d-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="a864d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="a864d-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="a864d-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="a864d-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a864d-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="a864d-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="a864d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a864d-125">-ComputeNode</span></span>
<span data-ttu-id="a864d-126">指定 **從哪個 PSComputeNode** 物件中取回服務記錄。</span><span class="sxs-lookup"><span data-stu-id="a864d-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a864d-127">-ComputeNodeId</span></span>
<span data-ttu-id="a864d-128">計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a864d-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="a864d-129">-ContainerUrl</span></span>
<span data-ttu-id="a864d-130">Azure 儲存空間的容器 URL。</span><span class="sxs-lookup"><span data-stu-id="a864d-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a864d-131">-DefaultProfile</span></span>
<span data-ttu-id="a864d-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a864d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a864d-133">-EndTime</span></span>
<span data-ttu-id="a864d-134">要上傳的服務記錄結束時間 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="a864d-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a864d-135">-PoolId</span></span>
<span data-ttu-id="a864d-136">包含計算節點之集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="a864d-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a864d-137">-StartTime</span></span>
<span data-ttu-id="a864d-138">要上傳的服務記錄開始時間。</span><span class="sxs-lookup"><span data-stu-id="a864d-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-139">-確認</span><span class="sxs-lookup"><span data-stu-id="a864d-139">-Confirm</span></span>
<span data-ttu-id="a864d-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a864d-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a864d-141">-WhatIf</span></span>
<span data-ttu-id="a864d-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a864d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a864d-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a864d-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a864d-144">CommonParameters</span></span>
<span data-ttu-id="a864d-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a864d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a864d-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a864d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a864d-147">輸入</span><span class="sxs-lookup"><span data-stu-id="a864d-147">INPUTS</span></span>

### <span data-ttu-id="a864d-148">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a864d-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a864d-149">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="a864d-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a864d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a864d-150">OUTPUTS</span></span>

### <span data-ttu-id="a864d-151">Microsoft.Azure.Commands.Batch。Models.PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="a864d-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="a864d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a864d-152">NOTES</span></span>

## <span data-ttu-id="a864d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a864d-153">RELATED LINKS</span></span>
