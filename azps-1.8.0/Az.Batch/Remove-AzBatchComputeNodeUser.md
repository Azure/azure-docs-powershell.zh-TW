---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: a57707b10fc103e860fe579e75d7d4ad09cfd0e3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623287"
---
# <span data-ttu-id="a927f-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="a927f-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="a927f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a927f-102">SYNOPSIS</span></span>
<span data-ttu-id="a927f-103">從批次計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="a927f-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="a927f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a927f-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a927f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a927f-105">DESCRIPTION</span></span>
<span data-ttu-id="a927f-106">**AzBatchComputeNodeUser** Cmdlet 會從 Azure Batch 計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="a927f-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="a927f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a927f-107">EXAMPLES</span></span>

### <span data-ttu-id="a927f-108">範例1：不需確認就能從計算節點刪除使用者</span><span class="sxs-lookup"><span data-stu-id="a927f-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="a927f-109">這個命令會從名為 ComputeNode01 的計算節點中刪除名為 User14 的使用者。</span><span class="sxs-lookup"><span data-stu-id="a927f-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="a927f-110">Compute 節點位於名為 Pool01 的 pool 中。</span><span class="sxs-lookup"><span data-stu-id="a927f-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="a927f-111">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="a927f-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a927f-112">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a927f-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a927f-113">參數</span><span class="sxs-lookup"><span data-stu-id="a927f-113">PARAMETERS</span></span>

### <span data-ttu-id="a927f-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="a927f-114">-BatchContext</span></span>
<span data-ttu-id="a927f-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="a927f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a927f-116">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="a927f-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a927f-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="a927f-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a927f-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a927f-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a927f-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="a927f-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a927f-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a927f-120">-ComputeNodeId</span></span>
<span data-ttu-id="a927f-121">指定此 Cmdlet 刪除使用者帳戶的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="a927f-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="a927f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a927f-122">-DefaultProfile</span></span>
<span data-ttu-id="a927f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a927f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a927f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a927f-124">-Name</span></span>
<span data-ttu-id="a927f-125">指定要刪除的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a927f-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="a927f-126">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="a927f-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="a927f-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a927f-127">-PoolId</span></span>
<span data-ttu-id="a927f-128">指定包含要刪除其使用者帳戶之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="a927f-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="a927f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a927f-129">-Confirm</span></span>
<span data-ttu-id="a927f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a927f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a927f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a927f-131">-WhatIf</span></span>
<span data-ttu-id="a927f-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a927f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a927f-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a927f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a927f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a927f-134">CommonParameters</span></span>
<span data-ttu-id="a927f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a927f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a927f-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a927f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a927f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a927f-137">INPUTS</span></span>

### <span data-ttu-id="a927f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a927f-138">System.String</span></span>

### <span data-ttu-id="a927f-139">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="a927f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a927f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a927f-140">OUTPUTS</span></span>

### <span data-ttu-id="a927f-141">System.void</span><span class="sxs-lookup"><span data-stu-id="a927f-141">System.Void</span></span>

## <span data-ttu-id="a927f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a927f-142">NOTES</span></span>

## <span data-ttu-id="a927f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a927f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a927f-144">新-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="a927f-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="a927f-145">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a927f-145">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a927f-146">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a927f-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


