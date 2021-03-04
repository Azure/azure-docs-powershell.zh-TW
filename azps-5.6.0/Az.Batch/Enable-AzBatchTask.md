---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 902c7ab5f6125716e03e846a4f1ebc3925aae43f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911197"
---
# <span data-ttu-id="abe2a-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="abe2a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="abe2a-102">SYNOPSIS</span></span>
<span data-ttu-id="abe2a-103">重新啟用工作。</span><span class="sxs-lookup"><span data-stu-id="abe2a-103">Reactivates a task.</span></span>

## <span data-ttu-id="abe2a-104">語法</span><span class="sxs-lookup"><span data-stu-id="abe2a-104">SYNTAX</span></span>

### <span data-ttu-id="abe2a-105">Id</span><span class="sxs-lookup"><span data-stu-id="abe2a-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe2a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="abe2a-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe2a-107">描述</span><span class="sxs-lookup"><span data-stu-id="abe2a-107">DESCRIPTION</span></span>
<span data-ttu-id="abe2a-108">**Enable-AzBatchTask** Cmdlet 會重新啟用工作。</span><span class="sxs-lookup"><span data-stu-id="abe2a-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="abe2a-109">如果任務已用盡重試計數，此 Cmdlet 仍可讓它執行。</span><span class="sxs-lookup"><span data-stu-id="abe2a-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="abe2a-110">例子</span><span class="sxs-lookup"><span data-stu-id="abe2a-110">EXAMPLES</span></span>

### <span data-ttu-id="abe2a-111">範例 1：重新啟用工作</span><span class="sxs-lookup"><span data-stu-id="abe2a-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="abe2a-112">此命令會重新啟用 Job Job7 中的任務 2。</span><span class="sxs-lookup"><span data-stu-id="abe2a-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="abe2a-113">範例 2：使用管線重新啟用工作</span><span class="sxs-lookup"><span data-stu-id="abe2a-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="abe2a-114">此命令會使用 Cmdlet 在具有識別碼 Job8 的工作中，獲得具有識別碼工作 3 的批次Get-AzBatchTask工作。</span><span class="sxs-lookup"><span data-stu-id="abe2a-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="abe2a-115">該命令會使用管線運算子，將工作傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abe2a-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="abe2a-116">命令會重新啟用該工作。</span><span class="sxs-lookup"><span data-stu-id="abe2a-116">The command reactivates that task.</span></span>

## <span data-ttu-id="abe2a-117">參數</span><span class="sxs-lookup"><span data-stu-id="abe2a-117">PARAMETERS</span></span>

### <span data-ttu-id="abe2a-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="abe2a-118">-BatchContext</span></span>
<span data-ttu-id="abe2a-119">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="abe2a-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="abe2a-120">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="abe2a-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="abe2a-121">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="abe2a-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="abe2a-122">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="abe2a-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="abe2a-123">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="abe2a-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="abe2a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe2a-124">-DefaultProfile</span></span>
<span data-ttu-id="abe2a-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="abe2a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abe2a-126">-Id</span><span class="sxs-lookup"><span data-stu-id="abe2a-126">-Id</span></span>
<span data-ttu-id="abe2a-127">指定要重新啟用的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="abe2a-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="abe2a-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="abe2a-128">-JobId</span></span>
<span data-ttu-id="abe2a-129">指定包含該工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="abe2a-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="abe2a-130">-工作</span><span class="sxs-lookup"><span data-stu-id="abe2a-130">-Task</span></span>
<span data-ttu-id="abe2a-131">指定此 Cmdlet 重新啟用的工作。</span><span class="sxs-lookup"><span data-stu-id="abe2a-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="abe2a-132">若要取得 **PSCloudTask** 物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abe2a-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="abe2a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="abe2a-133">-Confirm</span></span>
<span data-ttu-id="abe2a-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="abe2a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe2a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe2a-135">-WhatIf</span></span>
<span data-ttu-id="abe2a-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abe2a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abe2a-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abe2a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe2a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe2a-138">CommonParameters</span></span>
<span data-ttu-id="abe2a-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="abe2a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe2a-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abe2a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe2a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="abe2a-141">INPUTS</span></span>

### <span data-ttu-id="abe2a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="abe2a-142">System.String</span></span>

### <span data-ttu-id="abe2a-143">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="abe2a-144">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="abe2a-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="abe2a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="abe2a-145">OUTPUTS</span></span>

### <span data-ttu-id="abe2a-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="abe2a-146">System.Void</span></span>

## <span data-ttu-id="abe2a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="abe2a-147">NOTES</span></span>

## <span data-ttu-id="abe2a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="abe2a-148">RELATED LINKS</span></span>

[<span data-ttu-id="abe2a-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="abe2a-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="abe2a-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="abe2a-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="abe2a-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="abe2a-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="abe2a-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="abe2a-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


