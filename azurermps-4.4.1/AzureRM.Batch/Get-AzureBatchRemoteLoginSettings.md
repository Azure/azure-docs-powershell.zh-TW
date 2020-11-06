---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 848f0cf3d2d36b9ff5c80792c23d126956dccfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457308"
---
# <span data-ttu-id="2d5bf-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="2d5bf-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="2d5bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2d5bf-103">取得計算節點的遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d5bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d5bf-104">SYNTAX</span></span>

### <span data-ttu-id="2d5bf-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="2d5bf-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d5bf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2d5bf-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d5bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="2d5bf-107">DESCRIPTION</span></span>
<span data-ttu-id="2d5bf-108">**AzureBatchRemoteLoginSettings** Cmdlet 會針對虛擬機器基礎結構池中的計算節點取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="2d5bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="2d5bf-109">EXAMPLES</span></span>

### <span data-ttu-id="2d5bf-110">範例1：取得池中所有節點的遠端登入設定</span><span class="sxs-lookup"><span data-stu-id="2d5bf-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="2d5bf-111">第一個命令會使用 **AzureRmBatchAccountKeys** 來取得包含訂閱之便捷鍵的批次帳戶內容。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="2d5bf-112">該命令會將內容儲存在 $CoNtext 變數中，以用於下一個命令。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="2d5bf-113">第二個命令會使用 **AzureBatchComputeNode** 來取得 ID 為 ContosoPool 的池中的每個計算節點。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="2d5bf-114">命令會使用管線運算子，將每個電腦節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2d5bf-115">此命令會針對每個計算節點取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="2d5bf-116">範例2：取得節點的遠端登入設定</span><span class="sxs-lookup"><span data-stu-id="2d5bf-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="2d5bf-117">第一個命令會取得包含您訂閱之便捷鍵的批次帳戶內容，然後將其儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="2d5bf-118">第二個命令會針對在擁有識別碼 ContosoPool 的池中，針對具有指定識別碼的 compute 節點，取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="2d5bf-119">參數</span><span class="sxs-lookup"><span data-stu-id="2d5bf-119">PARAMETERS</span></span>

### <span data-ttu-id="2d5bf-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2d5bf-120">-BatchContext</span></span>
<span data-ttu-id="2d5bf-121">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2d5bf-122">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** ，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2d5bf-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2d5bf-123">-ComputeNode</span></span>
<span data-ttu-id="2d5bf-124">指定作為 **PSComputeNode** 物件的計算節點，此 Cmdlet 會取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="2d5bf-125">若要取得計算節點物件，請使用 Get-AzureBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d5bf-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="2d5bf-126">-ComputeNodeId</span></span>
<span data-ttu-id="2d5bf-127">指定要取得其遠端登入設定的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="2d5bf-128">這個 Cmdlet 會取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="2d5bf-129">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2d5bf-129">-PoolId</span></span>
<span data-ttu-id="2d5bf-130">指定包含虛擬機器之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-130">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="2d5bf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d5bf-131">-DefaultProfile</span></span>
<span data-ttu-id="2d5bf-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d5bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d5bf-133">CommonParameters</span></span>
<span data-ttu-id="2d5bf-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d5bf-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d5bf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d5bf-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2d5bf-136">INPUTS</span></span>

### <span data-ttu-id="2d5bf-137">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2d5bf-137">BatchAccountContext</span></span>
<span data-ttu-id="2d5bf-138">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2d5bf-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2d5bf-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="2d5bf-139">PSComputeNode</span></span>
<span data-ttu-id="2d5bf-140">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2d5bf-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="2d5bf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="2d5bf-141">OUTPUTS</span></span>

### <span data-ttu-id="2d5bf-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="2d5bf-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="2d5bf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2d5bf-143">NOTES</span></span>

## <span data-ttu-id="2d5bf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d5bf-144">RELATED LINKS</span></span>

[<span data-ttu-id="2d5bf-145">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2d5bf-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2d5bf-146">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2d5bf-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="2d5bf-147">AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="2d5bf-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="2d5bf-148">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d5bf-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


