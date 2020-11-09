---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287016"
---
# <span data-ttu-id="35d3e-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35d3e-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="35d3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="35d3e-103">停止批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="35d3e-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="35d3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="35d3e-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35d3e-105">說明</span><span class="sxs-lookup"><span data-stu-id="35d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="35d3e-106">**AzBatchJobSchedule** Cmdlet 會停止 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="35d3e-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="35d3e-107">示例</span><span class="sxs-lookup"><span data-stu-id="35d3e-107">EXAMPLES</span></span>

### <span data-ttu-id="35d3e-108">範例1：停止作業排程</span><span class="sxs-lookup"><span data-stu-id="35d3e-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="35d3e-109">這個命令會停止具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="35d3e-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="35d3e-110">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="35d3e-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="35d3e-111">參數</span><span class="sxs-lookup"><span data-stu-id="35d3e-111">PARAMETERS</span></span>

### <span data-ttu-id="35d3e-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="35d3e-112">-BatchContext</span></span>
<span data-ttu-id="35d3e-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="35d3e-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="35d3e-114">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="35d3e-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="35d3e-115">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="35d3e-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="35d3e-116">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="35d3e-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="35d3e-117">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="35d3e-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="35d3e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d3e-118">-DefaultProfile</span></span>
<span data-ttu-id="35d3e-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35d3e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35d3e-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="35d3e-120">-Id</span></span>
<span data-ttu-id="35d3e-121">指定此 Cmdlet 停止的作業排程 ID。</span><span class="sxs-lookup"><span data-stu-id="35d3e-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="35d3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d3e-122">CommonParameters</span></span>
<span data-ttu-id="35d3e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35d3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d3e-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="35d3e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d3e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="35d3e-125">INPUTS</span></span>

### <span data-ttu-id="35d3e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="35d3e-126">System.String</span></span>

### <span data-ttu-id="35d3e-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="35d3e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="35d3e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="35d3e-128">OUTPUTS</span></span>

### <span data-ttu-id="35d3e-129">System.void</span><span class="sxs-lookup"><span data-stu-id="35d3e-129">System.Void</span></span>

## <span data-ttu-id="35d3e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="35d3e-130">NOTES</span></span>

## <span data-ttu-id="35d3e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="35d3e-131">RELATED LINKS</span></span>

[<span data-ttu-id="35d3e-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35d3e-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="35d3e-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35d3e-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="35d3e-134">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="35d3e-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="35d3e-135">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35d3e-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="35d3e-136">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35d3e-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="35d3e-137">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35d3e-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="35d3e-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="35d3e-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
