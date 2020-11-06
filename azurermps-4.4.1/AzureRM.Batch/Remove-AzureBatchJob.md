---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453587"
---
# <span data-ttu-id="d719c-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d719c-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="d719c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d719c-102">SYNOPSIS</span></span>
<span data-ttu-id="d719c-103">刪除批次作業。</span><span class="sxs-lookup"><span data-stu-id="d719c-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d719c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d719c-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d719c-105">說明</span><span class="sxs-lookup"><span data-stu-id="d719c-105">DESCRIPTION</span></span>
<span data-ttu-id="d719c-106">**AzureBatchJob** Cmdlet 會刪除 Azure 批次作業。</span><span class="sxs-lookup"><span data-stu-id="d719c-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="d719c-107">除非您指定 *Force* 參數，否則這個 Cmdlet 會在您移除作業之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d719c-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="d719c-108">示例</span><span class="sxs-lookup"><span data-stu-id="d719c-108">EXAMPLES</span></span>

### <span data-ttu-id="d719c-109">範例1：刪除批次作業</span><span class="sxs-lookup"><span data-stu-id="d719c-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="d719c-110">這個命令會刪除具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="d719c-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d719c-111">命令會在刪除工作之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d719c-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="d719c-112">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="d719c-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d719c-113">範例2：不需使用管線確認即可刪除批次作業</span><span class="sxs-lookup"><span data-stu-id="d719c-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="d719c-114">這個命令會透過使用 Get-AzureBatchJob Cmdlet 來取得具有識別碼 Job 000002 的作業。</span><span class="sxs-lookup"><span data-stu-id="d719c-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="d719c-115">命令會使用管線運算子，將該作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d719c-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d719c-116">該命令會刪除該作業。</span><span class="sxs-lookup"><span data-stu-id="d719c-116">The command deletes that job.</span></span>
<span data-ttu-id="d719c-117">因為命令包含 *Force* 參數，所以它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d719c-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d719c-118">參數</span><span class="sxs-lookup"><span data-stu-id="d719c-118">PARAMETERS</span></span>

### <span data-ttu-id="d719c-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="d719c-119">-BatchContext</span></span>
<span data-ttu-id="d719c-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="d719c-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d719c-121">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d719c-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d719c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d719c-122">-Force</span></span>
<span data-ttu-id="d719c-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d719c-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d719c-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d719c-124">-Id</span></span>
<span data-ttu-id="d719c-125">指定此 Cmdlet 刪除之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d719c-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="d719c-126">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="d719c-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d719c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d719c-127">-Confirm</span></span>
<span data-ttu-id="d719c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d719c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d719c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d719c-129">-WhatIf</span></span>
<span data-ttu-id="d719c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d719c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d719c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d719c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d719c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d719c-132">-DefaultProfile</span></span>
<span data-ttu-id="d719c-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d719c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d719c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d719c-134">CommonParameters</span></span>
<span data-ttu-id="d719c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d719c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d719c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d719c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d719c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d719c-137">INPUTS</span></span>

### <span data-ttu-id="d719c-138">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="d719c-138">BatchAccountContext</span></span>
<span data-ttu-id="d719c-139">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d719c-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="d719c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d719c-140">OUTPUTS</span></span>

## <span data-ttu-id="d719c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d719c-141">NOTES</span></span>

## <span data-ttu-id="d719c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d719c-142">RELATED LINKS</span></span>

[<span data-ttu-id="d719c-143">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d719c-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="d719c-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d719c-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="d719c-145">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d719c-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="d719c-146">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d719c-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d719c-147">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d719c-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="d719c-148">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d719c-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="d719c-149">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d719c-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


