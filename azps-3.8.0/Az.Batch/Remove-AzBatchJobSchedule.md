---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958372"
---
# <span data-ttu-id="e1c65-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e1c65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1c65-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c65-103">移除批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="e1c65-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="e1c65-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1c65-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c65-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1c65-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c65-106">**AzBatchJobSchedule** Cmdlet 會移除 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="e1c65-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="e1c65-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1c65-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c65-108">範例1：刪除批次作業排程</span><span class="sxs-lookup"><span data-stu-id="e1c65-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="e1c65-109">這個命令會刪除具有識別碼 MyJobSchedule 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="e1c65-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="e1c65-110">命令會在刪除工作之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1c65-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="e1c65-111">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="e1c65-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e1c65-112">範例2：不需使用管線確認即可刪除批次作業</span><span class="sxs-lookup"><span data-stu-id="e1c65-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="e1c65-113">這個命令會透過使用 Get-AzBatchJobSchedule Cmdlet 來取得 ID 為 MyJobSchedule 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="e1c65-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="e1c65-114">透過使用管線運算子，命令會將作業排程傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1c65-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e1c65-115">該命令會刪除該作業排程。</span><span class="sxs-lookup"><span data-stu-id="e1c65-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="e1c65-116">因為命令包含 *Force* 參數，所以它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1c65-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e1c65-117">參數</span><span class="sxs-lookup"><span data-stu-id="e1c65-117">PARAMETERS</span></span>

### <span data-ttu-id="e1c65-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e1c65-118">-BatchContext</span></span>
<span data-ttu-id="e1c65-119">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e1c65-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e1c65-120">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e1c65-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e1c65-121">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="e1c65-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e1c65-122">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e1c65-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e1c65-123">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="e1c65-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e1c65-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c65-124">-DefaultProfile</span></span>
<span data-ttu-id="e1c65-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1c65-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1c65-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e1c65-126">-Force</span></span>
<span data-ttu-id="e1c65-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e1c65-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1c65-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e1c65-128">-Id</span></span>
<span data-ttu-id="e1c65-129">指定要移除之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1c65-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="e1c65-130">-確認</span><span class="sxs-lookup"><span data-stu-id="e1c65-130">-Confirm</span></span>
<span data-ttu-id="e1c65-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1c65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c65-132">-WhatIf</span></span>
<span data-ttu-id="e1c65-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1c65-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1c65-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1c65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c65-135">CommonParameters</span></span>
<span data-ttu-id="e1c65-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1c65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c65-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1c65-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c65-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e1c65-138">INPUTS</span></span>

### <span data-ttu-id="e1c65-139">System.object</span><span class="sxs-lookup"><span data-stu-id="e1c65-139">System.String</span></span>

### <span data-ttu-id="e1c65-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e1c65-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e1c65-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e1c65-141">OUTPUTS</span></span>

### <span data-ttu-id="e1c65-142">System.void</span><span class="sxs-lookup"><span data-stu-id="e1c65-142">System.Void</span></span>

## <span data-ttu-id="e1c65-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e1c65-143">NOTES</span></span>

## <span data-ttu-id="e1c65-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1c65-144">RELATED LINKS</span></span>

[<span data-ttu-id="e1c65-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e1c65-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e1c65-147">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e1c65-148">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e1c65-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="e1c65-150">停止 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c65-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


