---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625482"
---
# <span data-ttu-id="0affb-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0affb-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="0affb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0affb-102">SYNOPSIS</span></span>
<span data-ttu-id="0affb-103">重新啟動任務。</span><span class="sxs-lookup"><span data-stu-id="0affb-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0affb-104">句法</span><span class="sxs-lookup"><span data-stu-id="0affb-104">SYNTAX</span></span>

### <span data-ttu-id="0affb-105">標識號</span><span class="sxs-lookup"><span data-stu-id="0affb-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0affb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0affb-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0affb-107">說明</span><span class="sxs-lookup"><span data-stu-id="0affb-107">DESCRIPTION</span></span>
<span data-ttu-id="0affb-108">**Enable-AzureBatchTask** Cmdlet 會重新開機任務。</span><span class="sxs-lookup"><span data-stu-id="0affb-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="0affb-109">如果工作已用盡其重試計數，這個 Cmdlet 就能讓它執行。</span><span class="sxs-lookup"><span data-stu-id="0affb-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="0affb-110">示例</span><span class="sxs-lookup"><span data-stu-id="0affb-110">EXAMPLES</span></span>

### <span data-ttu-id="0affb-111">範例1：重新啟用任務</span><span class="sxs-lookup"><span data-stu-id="0affb-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="0affb-112">這個命令會重新啟動作業 Job7 中的任務 Task2。</span><span class="sxs-lookup"><span data-stu-id="0affb-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="0affb-113">範例2：使用管線重新啟用任務</span><span class="sxs-lookup"><span data-stu-id="0affb-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="0affb-114">這個命令會透過使用 Get-AzureBatchTask Cmdlet 來取得含有 ID Job8 作業中的識別碼 Task3 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="0affb-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="0affb-115">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0affb-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0affb-116">該命令會重新啟動該工作。</span><span class="sxs-lookup"><span data-stu-id="0affb-116">The command reactivates that task.</span></span>

## <span data-ttu-id="0affb-117">參數</span><span class="sxs-lookup"><span data-stu-id="0affb-117">PARAMETERS</span></span>

### <span data-ttu-id="0affb-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0affb-118">-BatchContext</span></span>
<span data-ttu-id="0affb-119">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="0affb-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0affb-120">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="0affb-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0affb-121">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="0affb-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0affb-122">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0affb-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0affb-123">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="0affb-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0affb-124">-DefaultProfile</span></span>
<span data-ttu-id="0affb-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0affb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0affb-126">-Id</span></span>
<span data-ttu-id="0affb-127">指定要重新啟用的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="0affb-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-128">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="0affb-128">-JobId</span></span>
<span data-ttu-id="0affb-129">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="0affb-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-130">-任務</span><span class="sxs-lookup"><span data-stu-id="0affb-130">-Task</span></span>
<span data-ttu-id="0affb-131">指定此 Cmdlet 重新啟動的工作。</span><span class="sxs-lookup"><span data-stu-id="0affb-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="0affb-132">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0affb-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0affb-133">-Confirm</span></span>
<span data-ttu-id="0affb-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0affb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0affb-135">-WhatIf</span></span>
<span data-ttu-id="0affb-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0affb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0affb-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0affb-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0affb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0affb-138">CommonParameters</span></span>
<span data-ttu-id="0affb-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0affb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0affb-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0affb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0affb-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0affb-141">INPUTS</span></span>

### <span data-ttu-id="0affb-142">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0affb-142">BatchAccountContext</span></span>
<span data-ttu-id="0affb-143">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0affb-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0affb-144">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0affb-144">PSCloudTask</span></span>
<span data-ttu-id="0affb-145">形參 "Task" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0affb-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="0affb-146">輸出</span><span class="sxs-lookup"><span data-stu-id="0affb-146">OUTPUTS</span></span>

## <span data-ttu-id="0affb-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0affb-147">NOTES</span></span>

## <span data-ttu-id="0affb-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0affb-148">RELATED LINKS</span></span>

[<span data-ttu-id="0affb-149">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0affb-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0affb-150">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0affb-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="0affb-151">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0affb-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="0affb-152">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0affb-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="0affb-153">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0affb-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="0affb-154">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0affb-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


