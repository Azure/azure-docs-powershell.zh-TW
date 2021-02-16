---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141474"
---
# <span data-ttu-id="95863-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="95863-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="95863-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95863-102">SYNOPSIS</span></span>
<span data-ttu-id="95863-103">取得計算節點的遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="95863-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="95863-104">句法</span><span class="sxs-lookup"><span data-stu-id="95863-104">SYNTAX</span></span>

### <span data-ttu-id="95863-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="95863-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95863-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="95863-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95863-107">說明</span><span class="sxs-lookup"><span data-stu-id="95863-107">DESCRIPTION</span></span>
<span data-ttu-id="95863-108">**AzBatchRemoteLoginSetting** Cmdlet 會針對虛擬機器基礎結構池中的計算節點取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="95863-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="95863-109">示例</span><span class="sxs-lookup"><span data-stu-id="95863-109">EXAMPLES</span></span>

### <span data-ttu-id="95863-110">範例1：取得池中所有節點的遠端登入設定</span><span class="sxs-lookup"><span data-stu-id="95863-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="95863-111">第一個命令會使用 **AzBatchAccountKey** 來取得包含訂閱之便捷鍵的批次帳戶內容。</span><span class="sxs-lookup"><span data-stu-id="95863-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="95863-112">該命令會將內容儲存在 $CoNtext 變數中，以用於下一個命令。</span><span class="sxs-lookup"><span data-stu-id="95863-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="95863-113">第二個命令會使用 **AzBatchComputeNode** 來取得 ID 為 ContosoPool 的池中的每個計算節點。</span><span class="sxs-lookup"><span data-stu-id="95863-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="95863-114">命令會使用管線運算子，將每個電腦節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95863-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95863-115">此命令會針對每個計算節點取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="95863-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="95863-116">範例2：取得節點的遠端登入設定</span><span class="sxs-lookup"><span data-stu-id="95863-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="95863-117">第一個命令會取得包含您訂閱之便捷鍵的批次帳戶內容，然後將其儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="95863-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="95863-118">第二個命令會針對在擁有識別碼 ContosoPool 的池中，針對具有指定識別碼的 compute 節點，取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="95863-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="95863-119">參數</span><span class="sxs-lookup"><span data-stu-id="95863-119">PARAMETERS</span></span>

### <span data-ttu-id="95863-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="95863-120">-BatchContext</span></span>
<span data-ttu-id="95863-121">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="95863-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="95863-122">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** ，請使用 Get-AzBatchAccountKey Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95863-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="95863-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="95863-123">-ComputeNode</span></span>
<span data-ttu-id="95863-124">指定作為 **PSComputeNode** 物件的計算節點，此 Cmdlet 會取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="95863-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="95863-125">若要取得計算節點物件，請使用 Get-AzBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95863-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="95863-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="95863-126">-ComputeNodeId</span></span>
<span data-ttu-id="95863-127">指定要取得其遠端登入設定的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="95863-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="95863-128">這個 Cmdlet 會取得遠端登入設定。</span><span class="sxs-lookup"><span data-stu-id="95863-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="95863-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95863-129">-DefaultProfile</span></span>
<span data-ttu-id="95863-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95863-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95863-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="95863-131">-PoolId</span></span>
<span data-ttu-id="95863-132">指定包含虛擬機器之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="95863-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="95863-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95863-133">CommonParameters</span></span>
<span data-ttu-id="95863-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95863-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95863-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95863-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95863-136">輸入</span><span class="sxs-lookup"><span data-stu-id="95863-136">INPUTS</span></span>

### <span data-ttu-id="95863-137">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="95863-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="95863-138">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="95863-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="95863-139">輸出</span><span class="sxs-lookup"><span data-stu-id="95863-139">OUTPUTS</span></span>

### <span data-ttu-id="95863-140">Microsoft.Azure.Commands.Batch。PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="95863-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="95863-141">筆記</span><span class="sxs-lookup"><span data-stu-id="95863-141">NOTES</span></span>

## <span data-ttu-id="95863-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="95863-142">RELATED LINKS</span></span>

[<span data-ttu-id="95863-143">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="95863-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="95863-144">AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95863-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="95863-145">AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="95863-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="95863-146">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="95863-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
