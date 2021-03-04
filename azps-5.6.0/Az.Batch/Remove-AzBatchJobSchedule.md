---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 5e227662e8c0ce1011172eded7b218f627efbbbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916596"
---
# <span data-ttu-id="96233-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="96233-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96233-102">SYNOPSIS</span></span>
<span data-ttu-id="96233-103">移除批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="96233-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="96233-104">語法</span><span class="sxs-lookup"><span data-stu-id="96233-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96233-105">描述</span><span class="sxs-lookup"><span data-stu-id="96233-105">DESCRIPTION</span></span>
<span data-ttu-id="96233-106">**Remove-AzBatchJobSchedule** Cmdlet 會移除 Azure 批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="96233-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="96233-107">例子</span><span class="sxs-lookup"><span data-stu-id="96233-107">EXAMPLES</span></span>

### <span data-ttu-id="96233-108">範例 1：刪除批次工作排程</span><span class="sxs-lookup"><span data-stu-id="96233-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="96233-109">此命令會刪除具有 ID MyJobSchedule 的工作排程。</span><span class="sxs-lookup"><span data-stu-id="96233-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="96233-110">命令會先提示您確認，然後再刪除工作。</span><span class="sxs-lookup"><span data-stu-id="96233-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="96233-111">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="96233-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="96233-112">範例 2：使用管線刪除批次工作而不確認</span><span class="sxs-lookup"><span data-stu-id="96233-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="96233-113">此命令會使用 Cmdlet，獲得具有 ID MyJobSchedule 的工作Get-AzBatchJobSchedule排程。</span><span class="sxs-lookup"><span data-stu-id="96233-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="96233-114">該命令會使用管線運算子，將該工作排程傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96233-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96233-115">命令會刪除該工作排程。</span><span class="sxs-lookup"><span data-stu-id="96233-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="96233-116">由於命令包含 *Force* 參數，因此不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96233-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="96233-117">參數</span><span class="sxs-lookup"><span data-stu-id="96233-117">PARAMETERS</span></span>

### <span data-ttu-id="96233-118">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="96233-118">-BatchContext</span></span>
<span data-ttu-id="96233-119">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="96233-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96233-120">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="96233-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="96233-121">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="96233-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="96233-122">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="96233-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="96233-123">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="96233-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="96233-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96233-124">-DefaultProfile</span></span>
<span data-ttu-id="96233-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96233-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96233-126">-強制</span><span class="sxs-lookup"><span data-stu-id="96233-126">-Force</span></span>
<span data-ttu-id="96233-127">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="96233-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96233-128">-Id</span><span class="sxs-lookup"><span data-stu-id="96233-128">-Id</span></span>
<span data-ttu-id="96233-129">指定要移除的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="96233-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="96233-130">-確認</span><span class="sxs-lookup"><span data-stu-id="96233-130">-Confirm</span></span>
<span data-ttu-id="96233-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96233-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96233-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96233-132">-WhatIf</span></span>
<span data-ttu-id="96233-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96233-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96233-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96233-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96233-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96233-135">CommonParameters</span></span>
<span data-ttu-id="96233-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96233-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96233-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96233-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96233-138">輸入</span><span class="sxs-lookup"><span data-stu-id="96233-138">INPUTS</span></span>

### <span data-ttu-id="96233-139">System.String</span><span class="sxs-lookup"><span data-stu-id="96233-139">System.String</span></span>

### <span data-ttu-id="96233-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="96233-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="96233-141">輸出</span><span class="sxs-lookup"><span data-stu-id="96233-141">OUTPUTS</span></span>

### <span data-ttu-id="96233-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="96233-142">System.Void</span></span>

## <span data-ttu-id="96233-143">筆記</span><span class="sxs-lookup"><span data-stu-id="96233-143">NOTES</span></span>

## <span data-ttu-id="96233-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="96233-144">RELATED LINKS</span></span>

[<span data-ttu-id="96233-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="96233-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="96233-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="96233-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="96233-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="96233-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="96233-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


