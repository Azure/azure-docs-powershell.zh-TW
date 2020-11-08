---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141153"
---
# <span data-ttu-id="6ae72-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ae72-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="6ae72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ae72-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae72-103">刪除批次任務。</span><span class="sxs-lookup"><span data-stu-id="6ae72-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="6ae72-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ae72-104">SYNTAX</span></span>

### <span data-ttu-id="6ae72-105">標識號</span><span class="sxs-lookup"><span data-stu-id="6ae72-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ae72-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ae72-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ae72-107">說明</span><span class="sxs-lookup"><span data-stu-id="6ae72-107">DESCRIPTION</span></span>
<span data-ttu-id="6ae72-108">**AzBatchTask** Cmdlet 會刪除 Azure Batch 任務。</span><span class="sxs-lookup"><span data-stu-id="6ae72-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="6ae72-109">除非您指定 *Force* 參數，否則這個 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ae72-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="6ae72-110">示例</span><span class="sxs-lookup"><span data-stu-id="6ae72-110">EXAMPLES</span></span>

### <span data-ttu-id="6ae72-111">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="6ae72-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="6ae72-112">這個命令會在具有 ID 作業的作業下，刪除具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="6ae72-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6ae72-113">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ae72-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6ae72-114">使用 **AzBatchAccountKey** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="6ae72-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6ae72-115">範例2：使用管線（無確認）刪除批次工作</span><span class="sxs-lookup"><span data-stu-id="6ae72-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="6ae72-116">這個命令會透過使用 **AzBatchTask** Cmdlet 來取得作業中具有 id 作業000001的 Task26 的批次工作。</span><span class="sxs-lookup"><span data-stu-id="6ae72-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="6ae72-117">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ae72-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ae72-118">該命令會刪除該任務。</span><span class="sxs-lookup"><span data-stu-id="6ae72-118">The command deletes that task.</span></span>
<span data-ttu-id="6ae72-119">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="6ae72-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6ae72-120">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ae72-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6ae72-121">參數</span><span class="sxs-lookup"><span data-stu-id="6ae72-121">PARAMETERS</span></span>

### <span data-ttu-id="6ae72-122">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ae72-122">-BatchContext</span></span>
<span data-ttu-id="6ae72-123">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="6ae72-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ae72-124">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="6ae72-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6ae72-125">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="6ae72-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6ae72-126">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6ae72-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6ae72-127">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="6ae72-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6ae72-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae72-128">-DefaultProfile</span></span>
<span data-ttu-id="6ae72-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ae72-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ae72-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6ae72-130">-Force</span></span>
<span data-ttu-id="6ae72-131">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6ae72-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ae72-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6ae72-132">-Id</span></span>
<span data-ttu-id="6ae72-133">指定此 Cmdlet 刪除的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ae72-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6ae72-134">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="6ae72-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae72-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ae72-135">-InputObject</span></span>
<span data-ttu-id="6ae72-136">指定此 Cmdlet 刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="6ae72-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6ae72-137">若要取得 **PSCloudTask** 物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ae72-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae72-138">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="6ae72-138">-JobId</span></span>
<span data-ttu-id="6ae72-139">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ae72-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae72-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6ae72-140">-Confirm</span></span>
<span data-ttu-id="6ae72-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ae72-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ae72-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae72-142">-WhatIf</span></span>
<span data-ttu-id="6ae72-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ae72-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ae72-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ae72-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ae72-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae72-145">CommonParameters</span></span>
<span data-ttu-id="6ae72-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ae72-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae72-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6ae72-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae72-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6ae72-148">INPUTS</span></span>

### <span data-ttu-id="6ae72-149">System.object</span><span class="sxs-lookup"><span data-stu-id="6ae72-149">System.String</span></span>

### <span data-ttu-id="6ae72-150">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6ae72-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="6ae72-151">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ae72-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6ae72-152">輸出</span><span class="sxs-lookup"><span data-stu-id="6ae72-152">OUTPUTS</span></span>

### <span data-ttu-id="6ae72-153">System.void</span><span class="sxs-lookup"><span data-stu-id="6ae72-153">System.Void</span></span>

## <span data-ttu-id="6ae72-154">筆記</span><span class="sxs-lookup"><span data-stu-id="6ae72-154">NOTES</span></span>

## <span data-ttu-id="6ae72-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ae72-155">RELATED LINKS</span></span>

[<span data-ttu-id="6ae72-156">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ae72-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6ae72-157">AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ae72-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="6ae72-158">新-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ae72-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="6ae72-159">移除-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ae72-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="6ae72-160">停止 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ae72-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="6ae72-161">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ae72-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
