---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137518"
---
# <span data-ttu-id="dcffb-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dcffb-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="dcffb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcffb-102">SYNOPSIS</span></span>
<span data-ttu-id="dcffb-103">從批次計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dcffb-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="dcffb-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcffb-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcffb-105">說明</span><span class="sxs-lookup"><span data-stu-id="dcffb-105">DESCRIPTION</span></span>
<span data-ttu-id="dcffb-106">**AzBatchComputeNodeUser** Cmdlet 會從 Azure Batch 計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dcffb-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="dcffb-107">示例</span><span class="sxs-lookup"><span data-stu-id="dcffb-107">EXAMPLES</span></span>

### <span data-ttu-id="dcffb-108">範例1：不需確認就能從計算節點刪除使用者</span><span class="sxs-lookup"><span data-stu-id="dcffb-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="dcffb-109">這個命令會從名為 ComputeNode01 的計算節點中刪除名為 User14 的使用者。</span><span class="sxs-lookup"><span data-stu-id="dcffb-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="dcffb-110">Compute 節點位於名為 Pool01 的 pool 中。</span><span class="sxs-lookup"><span data-stu-id="dcffb-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="dcffb-111">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="dcffb-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="dcffb-112">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcffb-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dcffb-113">參數</span><span class="sxs-lookup"><span data-stu-id="dcffb-113">PARAMETERS</span></span>

### <span data-ttu-id="dcffb-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="dcffb-114">-BatchContext</span></span>
<span data-ttu-id="dcffb-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="dcffb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dcffb-116">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="dcffb-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dcffb-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="dcffb-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dcffb-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dcffb-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dcffb-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="dcffb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dcffb-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="dcffb-120">-ComputeNodeId</span></span>
<span data-ttu-id="dcffb-121">指定此 Cmdlet 刪除使用者帳戶的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcffb-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcffb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcffb-122">-DefaultProfile</span></span>
<span data-ttu-id="dcffb-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcffb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcffb-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="dcffb-124">-Name</span></span>
<span data-ttu-id="dcffb-125">指定要刪除的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="dcffb-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="dcffb-126">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="dcffb-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcffb-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="dcffb-127">-PoolId</span></span>
<span data-ttu-id="dcffb-128">指定包含要刪除其使用者帳戶之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="dcffb-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcffb-129">-確認</span><span class="sxs-lookup"><span data-stu-id="dcffb-129">-Confirm</span></span>
<span data-ttu-id="dcffb-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcffb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcffb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcffb-131">-WhatIf</span></span>
<span data-ttu-id="dcffb-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcffb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcffb-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcffb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcffb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcffb-134">CommonParameters</span></span>
<span data-ttu-id="dcffb-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcffb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcffb-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dcffb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcffb-137">輸入</span><span class="sxs-lookup"><span data-stu-id="dcffb-137">INPUTS</span></span>

### <span data-ttu-id="dcffb-138">System.object</span><span class="sxs-lookup"><span data-stu-id="dcffb-138">System.String</span></span>

### <span data-ttu-id="dcffb-139">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="dcffb-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dcffb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="dcffb-140">OUTPUTS</span></span>

### <span data-ttu-id="dcffb-141">System.void</span><span class="sxs-lookup"><span data-stu-id="dcffb-141">System.Void</span></span>

## <span data-ttu-id="dcffb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="dcffb-142">NOTES</span></span>

## <span data-ttu-id="dcffb-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcffb-143">RELATED LINKS</span></span>

[<span data-ttu-id="dcffb-144">新-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dcffb-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="dcffb-145">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dcffb-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dcffb-146">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dcffb-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
