---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 6200ee0d929aaadccb8e2be0e8fb646929907d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453584"
---
# <span data-ttu-id="9e69c-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e69c-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="9e69c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e69c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e69c-103">刪除批次任務。</span><span class="sxs-lookup"><span data-stu-id="9e69c-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e69c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e69c-104">SYNTAX</span></span>

### <span data-ttu-id="9e69c-105">標識號</span><span class="sxs-lookup"><span data-stu-id="9e69c-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e69c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9e69c-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e69c-107">說明</span><span class="sxs-lookup"><span data-stu-id="9e69c-107">DESCRIPTION</span></span>
<span data-ttu-id="9e69c-108">**AzureBatchTask** Cmdlet 會刪除 Azure Batch 任務。</span><span class="sxs-lookup"><span data-stu-id="9e69c-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="9e69c-109">除非您指定 *Force* 參數，否則這個 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e69c-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="9e69c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9e69c-110">EXAMPLES</span></span>

### <span data-ttu-id="9e69c-111">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="9e69c-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="9e69c-112">這個命令會在具有 ID 作業的作業下，刪除具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="9e69c-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="9e69c-113">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e69c-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="9e69c-114">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="9e69c-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9e69c-115">範例2：使用管線（無確認）刪除批次工作</span><span class="sxs-lookup"><span data-stu-id="9e69c-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="9e69c-116">這個命令會透過使用 **AzureBatchTask** Cmdlet 來取得作業中具有 id 作業000001的 Task26 的批次工作。</span><span class="sxs-lookup"><span data-stu-id="9e69c-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="9e69c-117">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e69c-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e69c-118">該命令會刪除該任務。</span><span class="sxs-lookup"><span data-stu-id="9e69c-118">The command deletes that task.</span></span>
<span data-ttu-id="9e69c-119">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="9e69c-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9e69c-120">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e69c-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9e69c-121">參數</span><span class="sxs-lookup"><span data-stu-id="9e69c-121">PARAMETERS</span></span>

### <span data-ttu-id="9e69c-122">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9e69c-122">-BatchContext</span></span>
<span data-ttu-id="9e69c-123">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9e69c-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9e69c-124">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e69c-124">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9e69c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9e69c-125">-Force</span></span>
<span data-ttu-id="9e69c-126">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9e69c-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e69c-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9e69c-127">-Id</span></span>
<span data-ttu-id="9e69c-128">指定此 Cmdlet 刪除的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e69c-128">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="9e69c-129">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="9e69c-129">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="9e69c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e69c-130">-InputObject</span></span>
<span data-ttu-id="9e69c-131">指定此 Cmdlet 刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="9e69c-131">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="9e69c-132">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e69c-132">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="9e69c-133">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="9e69c-133">-JobId</span></span>
<span data-ttu-id="9e69c-134">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e69c-134">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="9e69c-135">-確認</span><span class="sxs-lookup"><span data-stu-id="9e69c-135">-Confirm</span></span>
<span data-ttu-id="9e69c-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e69c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e69c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e69c-137">-WhatIf</span></span>
<span data-ttu-id="9e69c-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e69c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e69c-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e69c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e69c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e69c-140">-DefaultProfile</span></span>
<span data-ttu-id="9e69c-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e69c-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e69c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e69c-142">CommonParameters</span></span>
<span data-ttu-id="9e69c-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e69c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e69c-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e69c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e69c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="9e69c-145">INPUTS</span></span>

### <span data-ttu-id="9e69c-146">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9e69c-146">BatchAccountContext</span></span>
<span data-ttu-id="9e69c-147">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9e69c-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9e69c-148">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="9e69c-148">PSCloudTask</span></span>
<span data-ttu-id="9e69c-149">形參 "InputObject" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9e69c-149">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="9e69c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="9e69c-150">OUTPUTS</span></span>

## <span data-ttu-id="9e69c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9e69c-151">NOTES</span></span>

## <span data-ttu-id="9e69c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e69c-152">RELATED LINKS</span></span>

[<span data-ttu-id="9e69c-153">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9e69c-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9e69c-154">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e69c-154">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="9e69c-155">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e69c-155">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="9e69c-156">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e69c-156">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="9e69c-157">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="9e69c-157">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="9e69c-158">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9e69c-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


