---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 6dd5082485d8028a0f1593db9c84bdc571b8c6bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914185"
---
# <span data-ttu-id="1175f-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="1175f-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="1175f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1175f-102">SYNOPSIS</span></span>
<span data-ttu-id="1175f-103">刪除指定的批次處理資料庫。</span><span class="sxs-lookup"><span data-stu-id="1175f-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="1175f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1175f-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1175f-105">描述</span><span class="sxs-lookup"><span data-stu-id="1175f-105">DESCRIPTION</span></span>
<span data-ttu-id="1175f-106">**Remove-AzBatchPool** Cmdlet 會刪除指定的 Azure 批次處理資料庫。</span><span class="sxs-lookup"><span data-stu-id="1175f-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="1175f-107">系統會提示您確認，除非您使用 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="1175f-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="1175f-108">例子</span><span class="sxs-lookup"><span data-stu-id="1175f-108">EXAMPLES</span></span>

### <span data-ttu-id="1175f-109">範例 1：根據資料庫識別碼刪除批次處理資料庫</span><span class="sxs-lookup"><span data-stu-id="1175f-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="1175f-110">此命令會刪除具有 ID MyPool 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="1175f-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="1175f-111">刪除作業進行之前，系統會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1175f-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="1175f-112">範例 2：強制刪除所有批次處理資料庫</span><span class="sxs-lookup"><span data-stu-id="1175f-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="1175f-113">此命令會刪除所有批次處理資料庫。</span><span class="sxs-lookup"><span data-stu-id="1175f-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="1175f-114">由於 *有 Force* 參數存在，因此確認提示會隱藏。</span><span class="sxs-lookup"><span data-stu-id="1175f-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="1175f-115">參數</span><span class="sxs-lookup"><span data-stu-id="1175f-115">PARAMETERS</span></span>

### <span data-ttu-id="1175f-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="1175f-116">-BatchContext</span></span>
<span data-ttu-id="1175f-117">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="1175f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1175f-118">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="1175f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1175f-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="1175f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1175f-120">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1175f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1175f-121">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="1175f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1175f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1175f-122">-DefaultProfile</span></span>
<span data-ttu-id="1175f-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1175f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1175f-124">-強制</span><span class="sxs-lookup"><span data-stu-id="1175f-124">-Force</span></span>
<span data-ttu-id="1175f-125">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1175f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1175f-126">-Id</span><span class="sxs-lookup"><span data-stu-id="1175f-126">-Id</span></span>
<span data-ttu-id="1175f-127">指定要刪除的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="1175f-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="1175f-128">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="1175f-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="1175f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1175f-129">-Confirm</span></span>
<span data-ttu-id="1175f-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1175f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1175f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1175f-131">-WhatIf</span></span>
<span data-ttu-id="1175f-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1175f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1175f-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1175f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1175f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1175f-134">CommonParameters</span></span>
<span data-ttu-id="1175f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1175f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1175f-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1175f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1175f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1175f-137">INPUTS</span></span>

### <span data-ttu-id="1175f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1175f-138">System.String</span></span>

### <span data-ttu-id="1175f-139">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="1175f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1175f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1175f-140">OUTPUTS</span></span>

### <span data-ttu-id="1175f-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1175f-141">System.Void</span></span>

## <span data-ttu-id="1175f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1175f-142">NOTES</span></span>

## <span data-ttu-id="1175f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1175f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1175f-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1175f-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1175f-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="1175f-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="1175f-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="1175f-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="1175f-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1175f-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
