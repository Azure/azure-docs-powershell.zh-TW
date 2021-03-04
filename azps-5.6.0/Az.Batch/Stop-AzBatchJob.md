---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: 43ec21e3c2bb7a0f80dc14c8051e4c3fed20ac42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917801"
---
# <span data-ttu-id="81c72-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81c72-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="81c72-102">簡介</span><span class="sxs-lookup"><span data-stu-id="81c72-102">SYNOPSIS</span></span>
<span data-ttu-id="81c72-103">停止批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="81c72-103">Stops a Batch job.</span></span>

## <span data-ttu-id="81c72-104">語法</span><span class="sxs-lookup"><span data-stu-id="81c72-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c72-105">描述</span><span class="sxs-lookup"><span data-stu-id="81c72-105">DESCRIPTION</span></span>
<span data-ttu-id="81c72-106">**Stop-AzBatchJob** Cmdlet 會停止 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="81c72-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="81c72-107">此命令會將工作標記為已完成。</span><span class="sxs-lookup"><span data-stu-id="81c72-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="81c72-108">例子</span><span class="sxs-lookup"><span data-stu-id="81c72-108">EXAMPLES</span></span>

### <span data-ttu-id="81c72-109">範例 1：停止批次處理工作</span><span class="sxs-lookup"><span data-stu-id="81c72-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="81c72-110">此命令會停止具有識別碼 Job-000001 的工作。</span><span class="sxs-lookup"><span data-stu-id="81c72-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="81c72-111">命令會指定您選擇停止工作的原因。</span><span class="sxs-lookup"><span data-stu-id="81c72-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="81c72-112">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="81c72-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="81c72-113">參數</span><span class="sxs-lookup"><span data-stu-id="81c72-113">PARAMETERS</span></span>

### <span data-ttu-id="81c72-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="81c72-114">-BatchContext</span></span>
<span data-ttu-id="81c72-115">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="81c72-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81c72-116">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="81c72-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="81c72-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="81c72-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="81c72-118">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="81c72-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="81c72-119">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="81c72-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="81c72-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c72-120">-DefaultProfile</span></span>
<span data-ttu-id="81c72-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="81c72-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c72-122">-Id</span><span class="sxs-lookup"><span data-stu-id="81c72-122">-Id</span></span>
<span data-ttu-id="81c72-123">指定此 Cmdlet 停止的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="81c72-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="81c72-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="81c72-124">-TerminateReason</span></span>
<span data-ttu-id="81c72-125">指定您決定停止工作的原因。</span><span class="sxs-lookup"><span data-stu-id="81c72-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="81c72-126">此 Cmdlet 會儲存此文字做為 **工作的 TerminateReason** 屬性。</span><span class="sxs-lookup"><span data-stu-id="81c72-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c72-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c72-127">CommonParameters</span></span>
<span data-ttu-id="81c72-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="81c72-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c72-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81c72-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c72-130">輸入</span><span class="sxs-lookup"><span data-stu-id="81c72-130">INPUTS</span></span>

### <span data-ttu-id="81c72-131">System.String</span><span class="sxs-lookup"><span data-stu-id="81c72-131">System.String</span></span>

### <span data-ttu-id="81c72-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="81c72-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="81c72-133">輸出</span><span class="sxs-lookup"><span data-stu-id="81c72-133">OUTPUTS</span></span>

### <span data-ttu-id="81c72-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="81c72-134">System.Void</span></span>

## <span data-ttu-id="81c72-135">筆記</span><span class="sxs-lookup"><span data-stu-id="81c72-135">NOTES</span></span>

## <span data-ttu-id="81c72-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="81c72-136">RELATED LINKS</span></span>

[<span data-ttu-id="81c72-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81c72-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="81c72-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81c72-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="81c72-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="81c72-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="81c72-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81c72-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="81c72-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81c72-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="81c72-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81c72-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="81c72-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81c72-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
