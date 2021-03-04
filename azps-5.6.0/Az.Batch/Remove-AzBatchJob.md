---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: e4f84e977e19dcd71731eb5ed09cae82dc5b3a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907818"
---
# <span data-ttu-id="e5ce6-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5ce6-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="e5ce6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ce6-103">刪除批次工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="e5ce6-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5ce6-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ce6-105">描述</span><span class="sxs-lookup"><span data-stu-id="e5ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ce6-106">**Remove-AzBatchJob** Cmdlet 會刪除 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="e5ce6-107">除非您指定 *Force* 參數，否則此 Cmdlet 會先提示您確認，然後再移除工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="e5ce6-108">例子</span><span class="sxs-lookup"><span data-stu-id="e5ce6-108">EXAMPLES</span></span>

### <span data-ttu-id="e5ce6-109">範例 1：刪除批次工作</span><span class="sxs-lookup"><span data-stu-id="e5ce6-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="e5ce6-110">此命令會刪除具有識別碼 Job-000001 的工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e5ce6-111">命令會先提示您確認，然後再刪除工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="e5ce6-112">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e5ce6-113">範例 2：使用管線刪除批次工作而不確認</span><span class="sxs-lookup"><span data-stu-id="e5ce6-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="e5ce6-114">此命令會使用 Cmdlet，獲得具有識別碼 Job-000002 的工作Get-AzBatchJob工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="e5ce6-115">該命令會使用管線運算子，將工作傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e5ce6-116">命令會刪除該工作。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-116">The command deletes that job.</span></span>
<span data-ttu-id="e5ce6-117">由於命令包含 *Force* 參數，因此不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e5ce6-118">參數</span><span class="sxs-lookup"><span data-stu-id="e5ce6-118">PARAMETERS</span></span>

### <span data-ttu-id="e5ce6-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e5ce6-119">-BatchContext</span></span>
<span data-ttu-id="e5ce6-120">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e5ce6-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e5ce6-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e5ce6-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e5ce6-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e5ce6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ce6-125">-DefaultProfile</span></span>
<span data-ttu-id="e5ce6-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ce6-127">-強制</span><span class="sxs-lookup"><span data-stu-id="e5ce6-127">-Force</span></span>
<span data-ttu-id="e5ce6-128">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5ce6-129">-Id</span><span class="sxs-lookup"><span data-stu-id="e5ce6-129">-Id</span></span>
<span data-ttu-id="e5ce6-130">指定此 Cmdlet 刪除的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="e5ce6-131">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="e5ce6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e5ce6-132">-Confirm</span></span>
<span data-ttu-id="e5ce6-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ce6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ce6-134">-WhatIf</span></span>
<span data-ttu-id="e5ce6-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5ce6-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ce6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ce6-137">CommonParameters</span></span>
<span data-ttu-id="e5ce6-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5ce6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ce6-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5ce6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ce6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e5ce6-140">INPUTS</span></span>

### <span data-ttu-id="e5ce6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e5ce6-141">System.String</span></span>

### <span data-ttu-id="e5ce6-142">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e5ce6-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e5ce6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e5ce6-143">OUTPUTS</span></span>

### <span data-ttu-id="e5ce6-144">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5ce6-144">System.Void</span></span>

## <span data-ttu-id="e5ce6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e5ce6-145">NOTES</span></span>

## <span data-ttu-id="e5ce6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5ce6-146">RELATED LINKS</span></span>

[<span data-ttu-id="e5ce6-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5ce6-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="e5ce6-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5ce6-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="e5ce6-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5ce6-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e5ce6-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e5ce6-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e5ce6-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5ce6-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e5ce6-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5ce6-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="e5ce6-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5ce6-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
