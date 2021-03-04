---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915609"
---
# <span data-ttu-id="02d6e-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="02d6e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="02d6e-103">設定工作排程。</span><span class="sxs-lookup"><span data-stu-id="02d6e-103">Sets a job schedule.</span></span>

## <span data-ttu-id="02d6e-104">語法</span><span class="sxs-lookup"><span data-stu-id="02d6e-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d6e-105">描述</span><span class="sxs-lookup"><span data-stu-id="02d6e-105">DESCRIPTION</span></span>
<span data-ttu-id="02d6e-106">**Set-AzBatchJobSchedule** Cmdlet 會設定 Azure 批次處理服務中的工作排程。</span><span class="sxs-lookup"><span data-stu-id="02d6e-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="02d6e-107">例子</span><span class="sxs-lookup"><span data-stu-id="02d6e-107">EXAMPLES</span></span>

### <span data-ttu-id="02d6e-108">範例 1：更新工作排程</span><span class="sxs-lookup"><span data-stu-id="02d6e-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="02d6e-109">第一個命令會使用 **Get-AzBatchJobSchedule** 取得工作，然後將它儲存在$JobSchedule變數中。</span><span class="sxs-lookup"><span data-stu-id="02d6e-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="02d6e-110">第二個命令會修改物件的週期 `$JobSchedule.Schedule` 間隔。</span><span class="sxs-lookup"><span data-stu-id="02d6e-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="02d6e-111">最後一個命令會更新 Batch 服務，以配合 $JobSchedule。</span><span class="sxs-lookup"><span data-stu-id="02d6e-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="02d6e-112">參數</span><span class="sxs-lookup"><span data-stu-id="02d6e-112">PARAMETERS</span></span>

### <span data-ttu-id="02d6e-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="02d6e-113">-BatchContext</span></span>
<span data-ttu-id="02d6e-114">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="02d6e-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02d6e-115">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="02d6e-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="02d6e-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="02d6e-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="02d6e-117">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="02d6e-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="02d6e-118">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="02d6e-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="02d6e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d6e-119">-DefaultProfile</span></span>
<span data-ttu-id="02d6e-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02d6e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d6e-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-121">-JobSchedule</span></span>
<span data-ttu-id="02d6e-122">指定 **代表工作排程的 PSCloudJobSchedule** 物件。</span><span class="sxs-lookup"><span data-stu-id="02d6e-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="02d6e-123">若要取得 **PSCloudJobSchedule** 物件，請使用 Get-AzBatchJobSchedule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02d6e-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02d6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d6e-124">CommonParameters</span></span>
<span data-ttu-id="02d6e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02d6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d6e-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02d6e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d6e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="02d6e-127">INPUTS</span></span>

### <span data-ttu-id="02d6e-128">Microsoft.Azure.Commands.Batch。Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="02d6e-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="02d6e-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="02d6e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="02d6e-130">OUTPUTS</span></span>

### <span data-ttu-id="02d6e-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="02d6e-131">System.Void</span></span>

## <span data-ttu-id="02d6e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="02d6e-132">NOTES</span></span>

## <span data-ttu-id="02d6e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="02d6e-133">RELATED LINKS</span></span>

[<span data-ttu-id="02d6e-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="02d6e-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="02d6e-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="02d6e-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="02d6e-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="02d6e-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="02d6e-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


