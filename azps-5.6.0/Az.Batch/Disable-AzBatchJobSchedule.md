---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 54b9f9b60c1d424e6fd62ede85e517b40df1d062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917426"
---
# <span data-ttu-id="cc28d-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc28d-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="cc28d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc28d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc28d-103">停用批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="cc28d-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="cc28d-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc28d-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc28d-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc28d-105">DESCRIPTION</span></span>
<span data-ttu-id="cc28d-106">**Disable-AzBatchJobSchedule** Cmdlet 會停用 Azure 批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="cc28d-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="cc28d-107">如果您停用排程，系統不會根據該排程建立工作。</span><span class="sxs-lookup"><span data-stu-id="cc28d-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="cc28d-108">您可以稍後啟用停用的排程。</span><span class="sxs-lookup"><span data-stu-id="cc28d-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="cc28d-109">例子</span><span class="sxs-lookup"><span data-stu-id="cc28d-109">EXAMPLES</span></span>

### <span data-ttu-id="cc28d-110">範例 1：停用工作排程</span><span class="sxs-lookup"><span data-stu-id="cc28d-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="cc28d-111">此命令會停用具有 ID JobSchedule17 的工作排程。</span><span class="sxs-lookup"><span data-stu-id="cc28d-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cc28d-112">使用 **Get-AzBatchAccountKey** Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="cc28d-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cc28d-113">參數</span><span class="sxs-lookup"><span data-stu-id="cc28d-113">PARAMETERS</span></span>

### <span data-ttu-id="cc28d-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="cc28d-114">-BatchContext</span></span>
<span data-ttu-id="cc28d-115">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="cc28d-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cc28d-116">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="cc28d-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cc28d-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="cc28d-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cc28d-118">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="cc28d-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cc28d-119">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="cc28d-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cc28d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc28d-120">-DefaultProfile</span></span>
<span data-ttu-id="cc28d-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc28d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc28d-122">-Id</span><span class="sxs-lookup"><span data-stu-id="cc28d-122">-Id</span></span>
<span data-ttu-id="cc28d-123">指定此 Cmdlet 停用的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc28d-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="cc28d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc28d-124">CommonParameters</span></span>
<span data-ttu-id="cc28d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc28d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc28d-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc28d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc28d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cc28d-127">INPUTS</span></span>

### <span data-ttu-id="cc28d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cc28d-128">System.String</span></span>

### <span data-ttu-id="cc28d-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="cc28d-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cc28d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cc28d-130">OUTPUTS</span></span>

### <span data-ttu-id="cc28d-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="cc28d-131">System.Void</span></span>

## <span data-ttu-id="cc28d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cc28d-132">NOTES</span></span>

## <span data-ttu-id="cc28d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc28d-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc28d-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc28d-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="cc28d-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cc28d-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cc28d-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc28d-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="cc28d-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc28d-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="cc28d-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc28d-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="cc28d-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc28d-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="cc28d-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cc28d-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
