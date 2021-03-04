---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: 83ac1df0259d39dd1db301e836479193b17f1dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914178"
---
# <span data-ttu-id="d9b27-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9b27-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="d9b27-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9b27-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b27-103">刪除批次工作。</span><span class="sxs-lookup"><span data-stu-id="d9b27-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="d9b27-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9b27-104">SYNTAX</span></span>

### <span data-ttu-id="d9b27-105">Id</span><span class="sxs-lookup"><span data-stu-id="d9b27-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b27-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b27-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b27-107">描述</span><span class="sxs-lookup"><span data-stu-id="d9b27-107">DESCRIPTION</span></span>
<span data-ttu-id="d9b27-108">**Remove-AzBatchTask** Cmdlet 會刪除 Azure 批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="d9b27-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="d9b27-109">除非您指定 Force 參數，否則此 Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9b27-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="d9b27-110">例子</span><span class="sxs-lookup"><span data-stu-id="d9b27-110">EXAMPLES</span></span>

### <span data-ttu-id="d9b27-111">範例 1：刪除批次工作</span><span class="sxs-lookup"><span data-stu-id="d9b27-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="d9b27-112">此命令會刪除識別碼為 Job-000001 的工作下具有識別碼工作 23 的工作。</span><span class="sxs-lookup"><span data-stu-id="d9b27-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d9b27-113">命令會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9b27-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d9b27-114">使用 **Get-AzBatchAccountKey** Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="d9b27-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d9b27-115">範例 2：使用管線刪除批次工作而不確認</span><span class="sxs-lookup"><span data-stu-id="d9b27-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="d9b27-116">此命令會使用 **Get-AzBatchTask Cmdlet** 在具有識別碼 Job-000001 的工作中取得識別碼工作 26 的批次工作。</span><span class="sxs-lookup"><span data-stu-id="d9b27-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="d9b27-117">該命令會使用管線運算子，將工作傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9b27-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d9b27-118">命令會刪除該工作。</span><span class="sxs-lookup"><span data-stu-id="d9b27-118">The command deletes that task.</span></span>
<span data-ttu-id="d9b27-119">此命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d9b27-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d9b27-120">因此，命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9b27-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d9b27-121">參數</span><span class="sxs-lookup"><span data-stu-id="d9b27-121">PARAMETERS</span></span>

### <span data-ttu-id="d9b27-122">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d9b27-122">-BatchContext</span></span>
<span data-ttu-id="d9b27-123">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d9b27-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9b27-124">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d9b27-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9b27-125">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="d9b27-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9b27-126">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d9b27-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9b27-127">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b27-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9b27-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b27-128">-DefaultProfile</span></span>
<span data-ttu-id="d9b27-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9b27-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b27-130">-強制</span><span class="sxs-lookup"><span data-stu-id="d9b27-130">-Force</span></span>
<span data-ttu-id="d9b27-131">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d9b27-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9b27-132">-Id</span><span class="sxs-lookup"><span data-stu-id="d9b27-132">-Id</span></span>
<span data-ttu-id="d9b27-133">指定此 Cmdlet 刪除的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9b27-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="d9b27-134">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d9b27-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d9b27-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b27-135">-InputObject</span></span>
<span data-ttu-id="d9b27-136">指定此 Cmdlet 刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="d9b27-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="d9b27-137">若要取得 **PSCloudTask** 物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9b27-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="d9b27-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9b27-138">-JobId</span></span>
<span data-ttu-id="d9b27-139">指定包含該工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9b27-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="d9b27-140">-確認</span><span class="sxs-lookup"><span data-stu-id="d9b27-140">-Confirm</span></span>
<span data-ttu-id="d9b27-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9b27-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b27-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b27-142">-WhatIf</span></span>
<span data-ttu-id="d9b27-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9b27-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b27-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9b27-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b27-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b27-145">CommonParameters</span></span>
<span data-ttu-id="d9b27-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9b27-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b27-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9b27-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b27-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d9b27-148">INPUTS</span></span>

### <span data-ttu-id="d9b27-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d9b27-149">System.String</span></span>

### <span data-ttu-id="d9b27-150">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d9b27-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="d9b27-151">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d9b27-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d9b27-152">輸出</span><span class="sxs-lookup"><span data-stu-id="d9b27-152">OUTPUTS</span></span>

### <span data-ttu-id="d9b27-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="d9b27-153">System.Void</span></span>

## <span data-ttu-id="d9b27-154">筆記</span><span class="sxs-lookup"><span data-stu-id="d9b27-154">NOTES</span></span>

## <span data-ttu-id="d9b27-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9b27-155">RELATED LINKS</span></span>

[<span data-ttu-id="d9b27-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d9b27-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d9b27-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9b27-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="d9b27-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9b27-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="d9b27-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9b27-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="d9b27-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9b27-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="d9b27-161">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d9b27-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
