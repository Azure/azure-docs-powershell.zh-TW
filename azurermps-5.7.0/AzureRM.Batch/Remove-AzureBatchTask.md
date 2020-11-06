---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454727"
---
# <span data-ttu-id="d011b-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d011b-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="d011b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d011b-102">SYNOPSIS</span></span>
<span data-ttu-id="d011b-103">刪除批次任務。</span><span class="sxs-lookup"><span data-stu-id="d011b-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d011b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d011b-104">SYNTAX</span></span>

### <span data-ttu-id="d011b-105">標識號</span><span class="sxs-lookup"><span data-stu-id="d011b-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d011b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d011b-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d011b-107">說明</span><span class="sxs-lookup"><span data-stu-id="d011b-107">DESCRIPTION</span></span>
<span data-ttu-id="d011b-108">**AzureBatchTask** Cmdlet 會刪除 Azure Batch 任務。</span><span class="sxs-lookup"><span data-stu-id="d011b-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="d011b-109">除非您指定 *Force* 參數，否則這個 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d011b-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="d011b-110">示例</span><span class="sxs-lookup"><span data-stu-id="d011b-110">EXAMPLES</span></span>

### <span data-ttu-id="d011b-111">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="d011b-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="d011b-112">這個命令會在具有 ID 作業的作業下，刪除具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="d011b-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d011b-113">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d011b-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d011b-114">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="d011b-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d011b-115">範例2：使用管線（無確認）刪除批次工作</span><span class="sxs-lookup"><span data-stu-id="d011b-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="d011b-116">這個命令會透過使用 **AzureBatchTask** Cmdlet 來取得作業中具有 id 作業000001的 Task26 的批次工作。</span><span class="sxs-lookup"><span data-stu-id="d011b-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="d011b-117">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d011b-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d011b-118">該命令會刪除該任務。</span><span class="sxs-lookup"><span data-stu-id="d011b-118">The command deletes that task.</span></span>
<span data-ttu-id="d011b-119">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d011b-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d011b-120">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d011b-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d011b-121">參數</span><span class="sxs-lookup"><span data-stu-id="d011b-121">PARAMETERS</span></span>

### <span data-ttu-id="d011b-122">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d011b-122">-BatchContext</span></span>
<span data-ttu-id="d011b-123">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d011b-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d011b-124">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d011b-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d011b-125">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="d011b-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d011b-126">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d011b-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d011b-127">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="d011b-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d011b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d011b-128">-DefaultProfile</span></span>
<span data-ttu-id="d011b-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d011b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d011b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="d011b-130">-Force</span></span>
<span data-ttu-id="d011b-131">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d011b-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d011b-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d011b-132">-Id</span></span>
<span data-ttu-id="d011b-133">指定此 Cmdlet 刪除的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="d011b-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="d011b-134">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="d011b-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d011b-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d011b-135">-InputObject</span></span>
<span data-ttu-id="d011b-136">指定此 Cmdlet 刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="d011b-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="d011b-137">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d011b-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="d011b-138">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="d011b-138">-JobId</span></span>
<span data-ttu-id="d011b-139">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="d011b-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="d011b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="d011b-140">-Confirm</span></span>
<span data-ttu-id="d011b-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d011b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d011b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d011b-142">-WhatIf</span></span>
<span data-ttu-id="d011b-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d011b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d011b-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d011b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d011b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d011b-145">CommonParameters</span></span>
<span data-ttu-id="d011b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d011b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d011b-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d011b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d011b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d011b-148">INPUTS</span></span>

### <span data-ttu-id="d011b-149">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d011b-149">BatchAccountContext</span></span>
<span data-ttu-id="d011b-150">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d011b-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d011b-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d011b-151">PSCloudTask</span></span>
<span data-ttu-id="d011b-152">形參 "InputObject" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d011b-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="d011b-153">輸出</span><span class="sxs-lookup"><span data-stu-id="d011b-153">OUTPUTS</span></span>

## <span data-ttu-id="d011b-154">筆記</span><span class="sxs-lookup"><span data-stu-id="d011b-154">NOTES</span></span>

## <span data-ttu-id="d011b-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="d011b-155">RELATED LINKS</span></span>

[<span data-ttu-id="d011b-156">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d011b-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d011b-157">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d011b-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="d011b-158">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d011b-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="d011b-159">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d011b-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="d011b-160">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d011b-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="d011b-161">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d011b-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


