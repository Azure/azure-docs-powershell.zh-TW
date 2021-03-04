---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 4b6d508dde18544c00ac3539921e83bd235e6fef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914189"
---
# <span data-ttu-id="37a77-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="37a77-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="37a77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37a77-102">SYNOPSIS</span></span>
<span data-ttu-id="37a77-103">從批次處理計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="37a77-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="37a77-104">語法</span><span class="sxs-lookup"><span data-stu-id="37a77-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37a77-105">描述</span><span class="sxs-lookup"><span data-stu-id="37a77-105">DESCRIPTION</span></span>
<span data-ttu-id="37a77-106">**Remove-AzBatchComputeNodeUser** Cmdlet 會從 Azure Batch 計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="37a77-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="37a77-107">例子</span><span class="sxs-lookup"><span data-stu-id="37a77-107">EXAMPLES</span></span>

### <span data-ttu-id="37a77-108">範例 1：從計算節點刪除使用者而不確認</span><span class="sxs-lookup"><span data-stu-id="37a77-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="37a77-109">此命令會從名為 ComputeNode01 的計算節點中刪除名為 User14 的使用者。</span><span class="sxs-lookup"><span data-stu-id="37a77-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="37a77-110">計算節點位於名為 Pool01 的集中。</span><span class="sxs-lookup"><span data-stu-id="37a77-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="37a77-111">此命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="37a77-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="37a77-112">因此，命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37a77-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="37a77-113">參數</span><span class="sxs-lookup"><span data-stu-id="37a77-113">PARAMETERS</span></span>

### <span data-ttu-id="37a77-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="37a77-114">-BatchContext</span></span>
<span data-ttu-id="37a77-115">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="37a77-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="37a77-116">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="37a77-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="37a77-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="37a77-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="37a77-118">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="37a77-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="37a77-119">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a77-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="37a77-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="37a77-120">-ComputeNodeId</span></span>
<span data-ttu-id="37a77-121">指定此 Cmdlet 刪除使用者帳戶之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37a77-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="37a77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a77-122">-DefaultProfile</span></span>
<span data-ttu-id="37a77-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37a77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37a77-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="37a77-124">-Name</span></span>
<span data-ttu-id="37a77-125">指定要刪除的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="37a77-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="37a77-126">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="37a77-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="37a77-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="37a77-127">-PoolId</span></span>
<span data-ttu-id="37a77-128">指定包含要刪除使用者帳戶之計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37a77-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="37a77-129">-確認</span><span class="sxs-lookup"><span data-stu-id="37a77-129">-Confirm</span></span>
<span data-ttu-id="37a77-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37a77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37a77-131">-WhatIf</span></span>
<span data-ttu-id="37a77-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37a77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37a77-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37a77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a77-134">CommonParameters</span></span>
<span data-ttu-id="37a77-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37a77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a77-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37a77-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a77-137">輸入</span><span class="sxs-lookup"><span data-stu-id="37a77-137">INPUTS</span></span>

### <span data-ttu-id="37a77-138">System.String</span><span class="sxs-lookup"><span data-stu-id="37a77-138">System.String</span></span>

### <span data-ttu-id="37a77-139">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="37a77-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="37a77-140">輸出</span><span class="sxs-lookup"><span data-stu-id="37a77-140">OUTPUTS</span></span>

### <span data-ttu-id="37a77-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="37a77-141">System.Void</span></span>

## <span data-ttu-id="37a77-142">筆記</span><span class="sxs-lookup"><span data-stu-id="37a77-142">NOTES</span></span>

## <span data-ttu-id="37a77-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="37a77-143">RELATED LINKS</span></span>

[<span data-ttu-id="37a77-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="37a77-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="37a77-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="37a77-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="37a77-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37a77-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
