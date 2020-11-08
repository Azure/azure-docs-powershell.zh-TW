---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 4d15680902cb324561983877fef317d20ed94704
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799485"
---
# <span data-ttu-id="176b0-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="176b0-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="176b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="176b0-102">SYNOPSIS</span></span>
<span data-ttu-id="176b0-103">刪除批次作業。</span><span class="sxs-lookup"><span data-stu-id="176b0-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="176b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="176b0-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="176b0-105">DESCRIPTION</span></span>
<span data-ttu-id="176b0-106">**AzBatchJob** Cmdlet 會刪除 Azure 批次作業。</span><span class="sxs-lookup"><span data-stu-id="176b0-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="176b0-107">除非您指定 *Force* 參數，否則這個 Cmdlet 會在您移除作業之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="176b0-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="176b0-108">示例</span><span class="sxs-lookup"><span data-stu-id="176b0-108">EXAMPLES</span></span>

### <span data-ttu-id="176b0-109">範例1：刪除批次作業</span><span class="sxs-lookup"><span data-stu-id="176b0-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="176b0-110">這個命令會刪除具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="176b0-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="176b0-111">命令會在刪除工作之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="176b0-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="176b0-112">使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="176b0-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="176b0-113">範例2：不需使用管線確認即可刪除批次作業</span><span class="sxs-lookup"><span data-stu-id="176b0-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="176b0-114">這個命令會透過使用 Get-AzBatchJob Cmdlet 來取得具有識別碼 Job 000002 的作業。</span><span class="sxs-lookup"><span data-stu-id="176b0-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="176b0-115">命令會使用管線運算子，將該作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="176b0-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="176b0-116">該命令會刪除該作業。</span><span class="sxs-lookup"><span data-stu-id="176b0-116">The command deletes that job.</span></span>
<span data-ttu-id="176b0-117">因為命令包含 *Force* 參數，所以它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="176b0-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="176b0-118">參數</span><span class="sxs-lookup"><span data-stu-id="176b0-118">PARAMETERS</span></span>

### <span data-ttu-id="176b0-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="176b0-119">-BatchContext</span></span>
<span data-ttu-id="176b0-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="176b0-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="176b0-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="176b0-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="176b0-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="176b0-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="176b0-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="176b0-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="176b0-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="176b0-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="176b0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176b0-125">-DefaultProfile</span></span>
<span data-ttu-id="176b0-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="176b0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="176b0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="176b0-127">-Force</span></span>
<span data-ttu-id="176b0-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="176b0-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="176b0-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="176b0-129">-Id</span></span>
<span data-ttu-id="176b0-130">指定此 Cmdlet 刪除之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="176b0-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="176b0-131">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="176b0-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="176b0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="176b0-132">-Confirm</span></span>
<span data-ttu-id="176b0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="176b0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176b0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176b0-134">-WhatIf</span></span>
<span data-ttu-id="176b0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="176b0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176b0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="176b0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176b0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176b0-137">CommonParameters</span></span>
<span data-ttu-id="176b0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="176b0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176b0-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="176b0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176b0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="176b0-140">INPUTS</span></span>

### <span data-ttu-id="176b0-141">System.object</span><span class="sxs-lookup"><span data-stu-id="176b0-141">System.String</span></span>

### <span data-ttu-id="176b0-142">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="176b0-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="176b0-143">輸出</span><span class="sxs-lookup"><span data-stu-id="176b0-143">OUTPUTS</span></span>

### <span data-ttu-id="176b0-144">System.void</span><span class="sxs-lookup"><span data-stu-id="176b0-144">System.Void</span></span>

## <span data-ttu-id="176b0-145">筆記</span><span class="sxs-lookup"><span data-stu-id="176b0-145">NOTES</span></span>

## <span data-ttu-id="176b0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="176b0-146">RELATED LINKS</span></span>

[<span data-ttu-id="176b0-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="176b0-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="176b0-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="176b0-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="176b0-149">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="176b0-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="176b0-150">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="176b0-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="176b0-151">新-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="176b0-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="176b0-152">停止 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="176b0-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="176b0-153">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="176b0-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

