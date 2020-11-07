---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: ce2a7c6d01af33de585d4ac8adef83d03dbd33bc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968651"
---
# <span data-ttu-id="b4fba-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4fba-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="b4fba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4fba-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fba-103">刪除指定的批次池。</span><span class="sxs-lookup"><span data-stu-id="b4fba-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="b4fba-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4fba-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4fba-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4fba-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fba-106">**AzBatchPool** Cmdlet 會刪除指定的 Azure 批次池。</span><span class="sxs-lookup"><span data-stu-id="b4fba-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="b4fba-107">除非您使用 *Force* 參數，否則系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4fba-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="b4fba-108">示例</span><span class="sxs-lookup"><span data-stu-id="b4fba-108">EXAMPLES</span></span>

### <span data-ttu-id="b4fba-109">範例1：依 [池 ID] 刪除批次池</span><span class="sxs-lookup"><span data-stu-id="b4fba-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="b4fba-110">這個命令會刪除 ID 為 MyPool 的池。</span><span class="sxs-lookup"><span data-stu-id="b4fba-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="b4fba-111">在執行 delete 操作之前，系統會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b4fba-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="b4fba-112">範例2：強行刪除所有批次池</span><span class="sxs-lookup"><span data-stu-id="b4fba-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="b4fba-113">這個命令會刪除所有的批次池。</span><span class="sxs-lookup"><span data-stu-id="b4fba-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="b4fba-114">因為 *Force* 參數存在，所以會抑制確認提示。</span><span class="sxs-lookup"><span data-stu-id="b4fba-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="b4fba-115">參數</span><span class="sxs-lookup"><span data-stu-id="b4fba-115">PARAMETERS</span></span>

### <span data-ttu-id="b4fba-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="b4fba-116">-BatchContext</span></span>
<span data-ttu-id="b4fba-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="b4fba-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4fba-118">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="b4fba-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4fba-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="b4fba-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4fba-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b4fba-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4fba-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="b4fba-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4fba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fba-122">-DefaultProfile</span></span>
<span data-ttu-id="b4fba-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4fba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4fba-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b4fba-124">-Force</span></span>
<span data-ttu-id="b4fba-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b4fba-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4fba-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b4fba-126">-Id</span></span>
<span data-ttu-id="b4fba-127">指定要刪除之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="b4fba-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="b4fba-128">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="b4fba-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b4fba-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b4fba-129">-Confirm</span></span>
<span data-ttu-id="b4fba-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b4fba-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4fba-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4fba-131">-WhatIf</span></span>
<span data-ttu-id="b4fba-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4fba-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4fba-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4fba-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4fba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fba-134">CommonParameters</span></span>
<span data-ttu-id="b4fba-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4fba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fba-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4fba-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fba-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b4fba-137">INPUTS</span></span>

### <span data-ttu-id="b4fba-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b4fba-138">System.String</span></span>

### <span data-ttu-id="b4fba-139">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="b4fba-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4fba-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b4fba-140">OUTPUTS</span></span>

### <span data-ttu-id="b4fba-141">System.void</span><span class="sxs-lookup"><span data-stu-id="b4fba-141">System.Void</span></span>

## <span data-ttu-id="b4fba-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b4fba-142">NOTES</span></span>

## <span data-ttu-id="b4fba-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4fba-143">RELATED LINKS</span></span>

[<span data-ttu-id="b4fba-144">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4fba-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b4fba-145">AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4fba-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="b4fba-146">新-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4fba-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="b4fba-147">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4fba-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


