---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: fa9945e80bfc3b94cf29e0751bc1ceedb36d12bd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968683"
---
# <span data-ttu-id="2baaa-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2baaa-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="2baaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2baaa-102">SYNOPSIS</span></span>
<span data-ttu-id="2baaa-103">停止批次作業。</span><span class="sxs-lookup"><span data-stu-id="2baaa-103">Stops a Batch job.</span></span>

## <span data-ttu-id="2baaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="2baaa-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2baaa-105">說明</span><span class="sxs-lookup"><span data-stu-id="2baaa-105">DESCRIPTION</span></span>
<span data-ttu-id="2baaa-106">**AzBatchJob** Cmdlet 會停止 Azure 批次作業。</span><span class="sxs-lookup"><span data-stu-id="2baaa-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="2baaa-107">這個命令會將工作標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="2baaa-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="2baaa-108">示例</span><span class="sxs-lookup"><span data-stu-id="2baaa-108">EXAMPLES</span></span>

### <span data-ttu-id="2baaa-109">範例1：停止批次作業</span><span class="sxs-lookup"><span data-stu-id="2baaa-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="2baaa-110">這個命令會停止具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="2baaa-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2baaa-111">該命令會指定您選擇停止作業的原因。</span><span class="sxs-lookup"><span data-stu-id="2baaa-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="2baaa-112">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="2baaa-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2baaa-113">參數</span><span class="sxs-lookup"><span data-stu-id="2baaa-113">PARAMETERS</span></span>

### <span data-ttu-id="2baaa-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2baaa-114">-BatchContext</span></span>
<span data-ttu-id="2baaa-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2baaa-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2baaa-116">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="2baaa-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2baaa-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="2baaa-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2baaa-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="2baaa-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2baaa-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="2baaa-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2baaa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2baaa-120">-DefaultProfile</span></span>
<span data-ttu-id="2baaa-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2baaa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2baaa-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2baaa-122">-Id</span></span>
<span data-ttu-id="2baaa-123">指定此 Cmdlet 停止的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="2baaa-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="2baaa-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="2baaa-124">-TerminateReason</span></span>
<span data-ttu-id="2baaa-125">指定您決定停止作業的原因。</span><span class="sxs-lookup"><span data-stu-id="2baaa-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="2baaa-126">這個 Cmdlet 會將此文字儲存為作業的 **TerminateReason** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2baaa-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="2baaa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2baaa-127">CommonParameters</span></span>
<span data-ttu-id="2baaa-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2baaa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2baaa-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2baaa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2baaa-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2baaa-130">INPUTS</span></span>

### <span data-ttu-id="2baaa-131">System.object</span><span class="sxs-lookup"><span data-stu-id="2baaa-131">System.String</span></span>

### <span data-ttu-id="2baaa-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2baaa-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2baaa-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2baaa-133">OUTPUTS</span></span>

### <span data-ttu-id="2baaa-134">System.void</span><span class="sxs-lookup"><span data-stu-id="2baaa-134">System.Void</span></span>

## <span data-ttu-id="2baaa-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2baaa-135">NOTES</span></span>

## <span data-ttu-id="2baaa-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2baaa-136">RELATED LINKS</span></span>

[<span data-ttu-id="2baaa-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2baaa-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2baaa-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2baaa-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="2baaa-139">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2baaa-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2baaa-140">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2baaa-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2baaa-141">新-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2baaa-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2baaa-142">移除-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2baaa-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2baaa-143">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2baaa-143">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


