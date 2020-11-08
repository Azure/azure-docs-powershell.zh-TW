---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 403bcc5a85001b6d98c67f91d995eb05bc948752
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140549"
---
# <span data-ttu-id="50393-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="50393-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="50393-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50393-102">SYNOPSIS</span></span>
<span data-ttu-id="50393-103">將計算節點服務記錄檔上傳到 Azure 儲存體容器。</span><span class="sxs-lookup"><span data-stu-id="50393-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="50393-104">句法</span><span class="sxs-lookup"><span data-stu-id="50393-104">SYNTAX</span></span>

### <span data-ttu-id="50393-105">AzureBatchComputeNodeServiceLogUpload (預設) </span><span class="sxs-lookup"><span data-stu-id="50393-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50393-106">標識號</span><span class="sxs-lookup"><span data-stu-id="50393-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50393-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="50393-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50393-108">說明</span><span class="sxs-lookup"><span data-stu-id="50393-108">DESCRIPTION</span></span>
<span data-ttu-id="50393-109">如果您遇到錯誤，且想要升級至 Azure 支援，此 Cmdlet 會從計算節點收集 Azure Batch 服務記錄檔。</span><span class="sxs-lookup"><span data-stu-id="50393-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="50393-110">Azure Batch 服務記錄檔應該與 Azure 支援共用，以協助調試批次服務的問題。</span><span class="sxs-lookup"><span data-stu-id="50393-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="50393-111">示例</span><span class="sxs-lookup"><span data-stu-id="50393-111">EXAMPLES</span></span>

### <span data-ttu-id="50393-112">範例1</span><span class="sxs-lookup"><span data-stu-id="50393-112">Example 1</span></span>
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

<span data-ttu-id="50393-113">上傳在2018年1月1日之前或之後的 [計算] 節點服務記錄，這些記錄是從 [計算] 節點中取得的 [池 id] （在計算節點所在的池子），以及 [計算] 節點識別碼中取得。</span><span class="sxs-lookup"><span data-stu-id="50393-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="50393-114">範例2</span><span class="sxs-lookup"><span data-stu-id="50393-114">Example 2</span></span>
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

<span data-ttu-id="50393-115">上傳 [在2018年1月1日] 或 [年1月 2018 10 日] （從 [計算] 節點提供）的 [緩衝集區 id]、[計算] 節點所駐留的 [池]，以及 [計算] 節點識別碼中的 [計算] 節點服務記錄。</span><span class="sxs-lookup"><span data-stu-id="50393-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="50393-116">範例3</span><span class="sxs-lookup"><span data-stu-id="50393-116">Example 3</span></span>
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

<span data-ttu-id="50393-117">上傳在2018年1月1日之前或之後的 [計算節點] 服務記錄（從 [計算節點] 物件取得，2018年1月10日之前）。</span><span class="sxs-lookup"><span data-stu-id="50393-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="50393-118">參數</span><span class="sxs-lookup"><span data-stu-id="50393-118">PARAMETERS</span></span>

### <span data-ttu-id="50393-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="50393-119">-BatchContext</span></span>
<span data-ttu-id="50393-120">與批次服務互動時要使用的 BatchAccountCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="50393-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="50393-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="50393-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="50393-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="50393-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="50393-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="50393-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="50393-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="50393-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="50393-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="50393-125">-ComputeNode</span></span>
<span data-ttu-id="50393-126">指定要從中檢索服務記錄的 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="50393-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="50393-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="50393-127">-ComputeNodeId</span></span>
<span data-ttu-id="50393-128">計算節點的 id。</span><span class="sxs-lookup"><span data-stu-id="50393-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="50393-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="50393-129">-ContainerUrl</span></span>
<span data-ttu-id="50393-130">Azure 儲存空間的容器 url。</span><span class="sxs-lookup"><span data-stu-id="50393-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="50393-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50393-131">-DefaultProfile</span></span>
<span data-ttu-id="50393-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50393-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50393-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="50393-133">-EndTime</span></span>
<span data-ttu-id="50393-134">要上傳服務記錄的結束時間 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="50393-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="50393-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="50393-135">-PoolId</span></span>
<span data-ttu-id="50393-136">包含計算節點之池的 id。</span><span class="sxs-lookup"><span data-stu-id="50393-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="50393-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="50393-137">-StartTime</span></span>
<span data-ttu-id="50393-138">要上傳服務記錄的開始時間。</span><span class="sxs-lookup"><span data-stu-id="50393-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="50393-139">-確認</span><span class="sxs-lookup"><span data-stu-id="50393-139">-Confirm</span></span>
<span data-ttu-id="50393-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50393-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50393-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50393-141">-WhatIf</span></span>
<span data-ttu-id="50393-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50393-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50393-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50393-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50393-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50393-144">CommonParameters</span></span>
<span data-ttu-id="50393-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50393-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50393-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50393-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50393-147">輸入</span><span class="sxs-lookup"><span data-stu-id="50393-147">INPUTS</span></span>

### <span data-ttu-id="50393-148">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="50393-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="50393-149">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="50393-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="50393-150">輸出</span><span class="sxs-lookup"><span data-stu-id="50393-150">OUTPUTS</span></span>

### <span data-ttu-id="50393-151">Microsoft.Azure.Commands.Batch。PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="50393-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="50393-152">筆記</span><span class="sxs-lookup"><span data-stu-id="50393-152">NOTES</span></span>

## <span data-ttu-id="50393-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="50393-153">RELATED LINKS</span></span>
