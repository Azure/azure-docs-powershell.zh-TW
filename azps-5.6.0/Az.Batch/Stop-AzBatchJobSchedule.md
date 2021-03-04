---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 85226072ca3e94a1e9cd10cd5a29e4fbee229c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905209"
---
# <span data-ttu-id="dfa94-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa94-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="dfa94-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dfa94-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa94-103">停止批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="dfa94-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="dfa94-104">語法</span><span class="sxs-lookup"><span data-stu-id="dfa94-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa94-105">描述</span><span class="sxs-lookup"><span data-stu-id="dfa94-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa94-106">**Stop-AzBatchJobSchedule** Cmdlet 會停止 Azure 批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="dfa94-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="dfa94-107">例子</span><span class="sxs-lookup"><span data-stu-id="dfa94-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa94-108">範例 1：停止工作排程</span><span class="sxs-lookup"><span data-stu-id="dfa94-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="dfa94-109">此命令會停止具有 ID JobSchedule17 的工作排程。</span><span class="sxs-lookup"><span data-stu-id="dfa94-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="dfa94-110">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="dfa94-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dfa94-111">參數</span><span class="sxs-lookup"><span data-stu-id="dfa94-111">PARAMETERS</span></span>

### <span data-ttu-id="dfa94-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="dfa94-112">-BatchContext</span></span>
<span data-ttu-id="dfa94-113">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="dfa94-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dfa94-114">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="dfa94-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dfa94-115">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="dfa94-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dfa94-116">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dfa94-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dfa94-117">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="dfa94-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dfa94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa94-118">-DefaultProfile</span></span>
<span data-ttu-id="dfa94-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfa94-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfa94-120">-Id</span><span class="sxs-lookup"><span data-stu-id="dfa94-120">-Id</span></span>
<span data-ttu-id="dfa94-121">指定此 Cmdlet 停止的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfa94-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="dfa94-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa94-122">CommonParameters</span></span>
<span data-ttu-id="dfa94-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dfa94-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa94-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfa94-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa94-125">輸入</span><span class="sxs-lookup"><span data-stu-id="dfa94-125">INPUTS</span></span>

### <span data-ttu-id="dfa94-126">System.String</span><span class="sxs-lookup"><span data-stu-id="dfa94-126">System.String</span></span>

### <span data-ttu-id="dfa94-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="dfa94-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dfa94-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dfa94-128">OUTPUTS</span></span>

### <span data-ttu-id="dfa94-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="dfa94-129">System.Void</span></span>

## <span data-ttu-id="dfa94-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dfa94-130">NOTES</span></span>

## <span data-ttu-id="dfa94-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfa94-131">RELATED LINKS</span></span>

[<span data-ttu-id="dfa94-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa94-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="dfa94-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa94-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="dfa94-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dfa94-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dfa94-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa94-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="dfa94-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa94-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="dfa94-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dfa94-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="dfa94-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfa94-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
