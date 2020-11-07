---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626349"
---
# <span data-ttu-id="ee798-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ee798-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="ee798-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee798-102">SYNOPSIS</span></span>
<span data-ttu-id="ee798-103">重新啟動任務。</span><span class="sxs-lookup"><span data-stu-id="ee798-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee798-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee798-104">SYNTAX</span></span>

### <span data-ttu-id="ee798-105">標識號</span><span class="sxs-lookup"><span data-stu-id="ee798-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee798-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ee798-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee798-107">說明</span><span class="sxs-lookup"><span data-stu-id="ee798-107">DESCRIPTION</span></span>
<span data-ttu-id="ee798-108">**Enable-AzureBatchTask** Cmdlet 會重新開機任務。</span><span class="sxs-lookup"><span data-stu-id="ee798-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="ee798-109">如果工作已用盡其重試計數，這個 Cmdlet 就能讓它執行。</span><span class="sxs-lookup"><span data-stu-id="ee798-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="ee798-110">示例</span><span class="sxs-lookup"><span data-stu-id="ee798-110">EXAMPLES</span></span>

### <span data-ttu-id="ee798-111">範例1：重新啟用任務</span><span class="sxs-lookup"><span data-stu-id="ee798-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="ee798-112">這個命令會重新啟動作業 Job7 中的任務 Task2。</span><span class="sxs-lookup"><span data-stu-id="ee798-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="ee798-113">範例2：使用管線重新啟用任務</span><span class="sxs-lookup"><span data-stu-id="ee798-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="ee798-114">這個命令會透過使用 Get-AzureBatchTask Cmdlet 來取得含有 ID Job8 作業中的識別碼 Task3 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="ee798-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="ee798-115">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee798-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ee798-116">該命令會重新啟動該工作。</span><span class="sxs-lookup"><span data-stu-id="ee798-116">The command reactivates that task.</span></span>

## <span data-ttu-id="ee798-117">參數</span><span class="sxs-lookup"><span data-stu-id="ee798-117">PARAMETERS</span></span>

### <span data-ttu-id="ee798-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ee798-118">-BatchContext</span></span>
<span data-ttu-id="ee798-119">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ee798-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ee798-120">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee798-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ee798-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ee798-121">-Id</span></span>
<span data-ttu-id="ee798-122">指定要重新啟用的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee798-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="ee798-123">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="ee798-123">-JobId</span></span>
<span data-ttu-id="ee798-124">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee798-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="ee798-125">-任務</span><span class="sxs-lookup"><span data-stu-id="ee798-125">-Task</span></span>
<span data-ttu-id="ee798-126">指定此 Cmdlet 重新啟動的工作。</span><span class="sxs-lookup"><span data-stu-id="ee798-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="ee798-127">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee798-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="ee798-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ee798-128">-Confirm</span></span>
<span data-ttu-id="ee798-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee798-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee798-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee798-130">-WhatIf</span></span>
<span data-ttu-id="ee798-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee798-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee798-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee798-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee798-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee798-133">-DefaultProfile</span></span>
<span data-ttu-id="ee798-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee798-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee798-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee798-135">CommonParameters</span></span>
<span data-ttu-id="ee798-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee798-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee798-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee798-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee798-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ee798-138">INPUTS</span></span>

### <span data-ttu-id="ee798-139">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ee798-139">BatchAccountContext</span></span>
<span data-ttu-id="ee798-140">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ee798-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ee798-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ee798-141">PSCloudTask</span></span>
<span data-ttu-id="ee798-142">形參 "Task" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ee798-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="ee798-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ee798-143">OUTPUTS</span></span>

## <span data-ttu-id="ee798-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ee798-144">NOTES</span></span>

## <span data-ttu-id="ee798-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee798-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee798-146">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ee798-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ee798-147">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ee798-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="ee798-148">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ee798-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="ee798-149">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ee798-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="ee798-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ee798-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="ee798-151">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ee798-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


