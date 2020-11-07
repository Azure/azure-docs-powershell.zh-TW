---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799518"
---
# <span data-ttu-id="5899b-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5899b-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="5899b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5899b-102">SYNOPSIS</span></span>
<span data-ttu-id="5899b-103">重新啟動任務。</span><span class="sxs-lookup"><span data-stu-id="5899b-103">Reactivates a task.</span></span>

## <span data-ttu-id="5899b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5899b-104">SYNTAX</span></span>

### <span data-ttu-id="5899b-105">標識號</span><span class="sxs-lookup"><span data-stu-id="5899b-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5899b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5899b-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5899b-107">說明</span><span class="sxs-lookup"><span data-stu-id="5899b-107">DESCRIPTION</span></span>
<span data-ttu-id="5899b-108">**Enable-AzBatchTask** Cmdlet 會重新開機任務。</span><span class="sxs-lookup"><span data-stu-id="5899b-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="5899b-109">如果工作已用盡其重試計數，這個 Cmdlet 就能讓它執行。</span><span class="sxs-lookup"><span data-stu-id="5899b-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="5899b-110">示例</span><span class="sxs-lookup"><span data-stu-id="5899b-110">EXAMPLES</span></span>

### <span data-ttu-id="5899b-111">範例1：重新啟用任務</span><span class="sxs-lookup"><span data-stu-id="5899b-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="5899b-112">這個命令會重新啟動作業 Job7 中的任務 Task2。</span><span class="sxs-lookup"><span data-stu-id="5899b-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="5899b-113">範例2：使用管線重新啟用任務</span><span class="sxs-lookup"><span data-stu-id="5899b-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="5899b-114">這個命令會透過使用 Get-AzBatchTask Cmdlet 來取得含有 ID Job8 作業中的識別碼 Task3 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="5899b-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="5899b-115">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5899b-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5899b-116">該命令會重新啟動該工作。</span><span class="sxs-lookup"><span data-stu-id="5899b-116">The command reactivates that task.</span></span>

## <span data-ttu-id="5899b-117">參數</span><span class="sxs-lookup"><span data-stu-id="5899b-117">PARAMETERS</span></span>

### <span data-ttu-id="5899b-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5899b-118">-BatchContext</span></span>
<span data-ttu-id="5899b-119">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5899b-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5899b-120">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5899b-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5899b-121">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5899b-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5899b-122">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5899b-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5899b-123">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="5899b-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5899b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5899b-124">-DefaultProfile</span></span>
<span data-ttu-id="5899b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5899b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5899b-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5899b-126">-Id</span></span>
<span data-ttu-id="5899b-127">指定要重新啟用的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="5899b-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="5899b-128">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="5899b-128">-JobId</span></span>
<span data-ttu-id="5899b-129">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="5899b-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="5899b-130">-任務</span><span class="sxs-lookup"><span data-stu-id="5899b-130">-Task</span></span>
<span data-ttu-id="5899b-131">指定此 Cmdlet 重新啟動的工作。</span><span class="sxs-lookup"><span data-stu-id="5899b-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="5899b-132">若要取得 **PSCloudTask** 物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5899b-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="5899b-133">-確認</span><span class="sxs-lookup"><span data-stu-id="5899b-133">-Confirm</span></span>
<span data-ttu-id="5899b-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5899b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5899b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5899b-135">-WhatIf</span></span>
<span data-ttu-id="5899b-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5899b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5899b-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5899b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5899b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5899b-138">CommonParameters</span></span>
<span data-ttu-id="5899b-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5899b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5899b-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5899b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5899b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5899b-141">INPUTS</span></span>

### <span data-ttu-id="5899b-142">System.object</span><span class="sxs-lookup"><span data-stu-id="5899b-142">System.String</span></span>

### <span data-ttu-id="5899b-143">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5899b-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="5899b-144">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5899b-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5899b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5899b-145">OUTPUTS</span></span>

### <span data-ttu-id="5899b-146">System.void</span><span class="sxs-lookup"><span data-stu-id="5899b-146">System.Void</span></span>

## <span data-ttu-id="5899b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5899b-147">NOTES</span></span>

## <span data-ttu-id="5899b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="5899b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5899b-149">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5899b-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5899b-150">AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5899b-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="5899b-151">新-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5899b-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="5899b-152">移除-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5899b-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="5899b-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5899b-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="5899b-154">停止 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5899b-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


