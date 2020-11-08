---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 9536de21d205a051f0a0a2ea6f4a83c759b94c8c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968679"
---
# <span data-ttu-id="0a6ab-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a6ab-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="0a6ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6ab-103">停止批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="0a6ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a6ab-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a6ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6ab-106">**AzBatchJobSchedule** Cmdlet 會停止 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="0a6ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6ab-108">範例1：停止作業排程</span><span class="sxs-lookup"><span data-stu-id="0a6ab-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="0a6ab-109">這個命令會停止具有識別碼 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0a6ab-110">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0a6ab-111">參數</span><span class="sxs-lookup"><span data-stu-id="0a6ab-111">PARAMETERS</span></span>

### <span data-ttu-id="0a6ab-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0a6ab-112">-BatchContext</span></span>
<span data-ttu-id="0a6ab-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0a6ab-114">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0a6ab-115">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0a6ab-116">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0a6ab-117">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0a6ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6ab-118">-DefaultProfile</span></span>
<span data-ttu-id="0a6ab-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a6ab-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0a6ab-120">-Id</span></span>
<span data-ttu-id="0a6ab-121">指定此 Cmdlet 停止的作業排程 ID。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0a6ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6ab-122">CommonParameters</span></span>
<span data-ttu-id="0a6ab-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6ab-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a6ab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6ab-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0a6ab-125">INPUTS</span></span>

### <span data-ttu-id="0a6ab-126">System.object</span><span class="sxs-lookup"><span data-stu-id="0a6ab-126">System.String</span></span>

### <span data-ttu-id="0a6ab-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0a6ab-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0a6ab-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0a6ab-128">OUTPUTS</span></span>

### <span data-ttu-id="0a6ab-129">System.void</span><span class="sxs-lookup"><span data-stu-id="0a6ab-129">System.Void</span></span>

## <span data-ttu-id="0a6ab-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0a6ab-130">NOTES</span></span>

## <span data-ttu-id="0a6ab-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a6ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="0a6ab-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a6ab-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="0a6ab-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a6ab-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="0a6ab-134">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0a6ab-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0a6ab-135">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a6ab-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="0a6ab-136">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a6ab-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="0a6ab-137">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a6ab-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="0a6ab-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a6ab-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

