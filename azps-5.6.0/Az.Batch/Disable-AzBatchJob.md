---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: fabc983e8c7b70685477a640d408beb65251b253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914198"
---
# <span data-ttu-id="2836f-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2836f-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="2836f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2836f-102">SYNOPSIS</span></span>
<span data-ttu-id="2836f-103">停用批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-103">Disables a Batch job.</span></span>

## <span data-ttu-id="2836f-104">語法</span><span class="sxs-lookup"><span data-stu-id="2836f-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2836f-105">描述</span><span class="sxs-lookup"><span data-stu-id="2836f-105">DESCRIPTION</span></span>
<span data-ttu-id="2836f-106">**Disable-AzBatchJob** Cmdlet 會停用 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="2836f-107">啟用工作之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="2836f-108">停用的工作不會執行新工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="2836f-109">您可以稍後啟用停用的工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="2836f-110">例子</span><span class="sxs-lookup"><span data-stu-id="2836f-110">EXAMPLES</span></span>

### <span data-ttu-id="2836f-111">範例 1：停用批次處理工作</span><span class="sxs-lookup"><span data-stu-id="2836f-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="2836f-112">此命令會停用具有識別碼 Job-000001 的工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2836f-113">命令會終止工作的進行中工作。</span><span class="sxs-lookup"><span data-stu-id="2836f-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="2836f-114">使用 **Get-AzBatchAccountKey** Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="2836f-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2836f-115">參數</span><span class="sxs-lookup"><span data-stu-id="2836f-115">PARAMETERS</span></span>

### <span data-ttu-id="2836f-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2836f-116">-BatchContext</span></span>
<span data-ttu-id="2836f-117">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2836f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2836f-118">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="2836f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2836f-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="2836f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2836f-120">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="2836f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2836f-121">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="2836f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2836f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2836f-122">-DefaultProfile</span></span>
<span data-ttu-id="2836f-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2836f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2836f-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="2836f-124">-DisableJobOption</span></span>
<span data-ttu-id="2836f-125">指定處理與此 Cmdlet 停用之工作相關聯的活動工作之處理方法。</span><span class="sxs-lookup"><span data-stu-id="2836f-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="2836f-126">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="2836f-126">Valid values are:</span></span>
- <span data-ttu-id="2836f-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="2836f-127">Requeue</span></span>
- <span data-ttu-id="2836f-128">終止</span><span class="sxs-lookup"><span data-stu-id="2836f-128">Terminate</span></span>
- <span data-ttu-id="2836f-129">等</span><span class="sxs-lookup"><span data-stu-id="2836f-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2836f-130">-Id</span><span class="sxs-lookup"><span data-stu-id="2836f-130">-Id</span></span>
<span data-ttu-id="2836f-131">指定此 Cmdlet 停用的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="2836f-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2836f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2836f-132">CommonParameters</span></span>
<span data-ttu-id="2836f-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2836f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2836f-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2836f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2836f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2836f-135">INPUTS</span></span>

### <span data-ttu-id="2836f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2836f-136">System.String</span></span>

### <span data-ttu-id="2836f-137">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2836f-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2836f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2836f-138">OUTPUTS</span></span>

### <span data-ttu-id="2836f-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="2836f-139">System.Void</span></span>

## <span data-ttu-id="2836f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2836f-140">NOTES</span></span>

## <span data-ttu-id="2836f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="2836f-141">RELATED LINKS</span></span>

[<span data-ttu-id="2836f-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2836f-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="2836f-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2836f-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2836f-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2836f-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2836f-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2836f-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2836f-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2836f-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2836f-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2836f-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2836f-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2836f-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
