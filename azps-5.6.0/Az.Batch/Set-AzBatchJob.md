---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: cc084f276f379013125693e3314ff1eab8a7b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905218"
---
# <span data-ttu-id="a1f50-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="a1f50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1f50-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f50-103">更新批次工作。</span><span class="sxs-lookup"><span data-stu-id="a1f50-103">Updates a Batch job.</span></span>

## <span data-ttu-id="a1f50-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1f50-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f50-105">描述</span><span class="sxs-lookup"><span data-stu-id="a1f50-105">DESCRIPTION</span></span>
<span data-ttu-id="a1f50-106">**Set-AzBatchJob** Cmdlet 會更新 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="a1f50-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="a1f50-107">使用 Get-AzBatchJob Cmdlet 取得 **PSCloudJob** 物件。</span><span class="sxs-lookup"><span data-stu-id="a1f50-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="a1f50-108">修改該物件的屬性，然後使用目前的 Cmdlet 來提交您變更的批次處理服務。</span><span class="sxs-lookup"><span data-stu-id="a1f50-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a1f50-109">例子</span><span class="sxs-lookup"><span data-stu-id="a1f50-109">EXAMPLES</span></span>

### <span data-ttu-id="a1f50-110">範例 1：更新工作</span><span class="sxs-lookup"><span data-stu-id="a1f50-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="a1f50-111">第一個命令會使用 **Get-AzBatchJob** 取得工作，然後將它儲存在$Job變數中。</span><span class="sxs-lookup"><span data-stu-id="a1f50-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="a1f50-112">第二個命令會修改物件$Job規格。</span><span class="sxs-lookup"><span data-stu-id="a1f50-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="a1f50-113">最後一個命令會更新 Batch 服務，以配合 $Job。</span><span class="sxs-lookup"><span data-stu-id="a1f50-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="a1f50-114">參數</span><span class="sxs-lookup"><span data-stu-id="a1f50-114">PARAMETERS</span></span>

### <span data-ttu-id="a1f50-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="a1f50-115">-BatchContext</span></span>
<span data-ttu-id="a1f50-116">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="a1f50-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a1f50-117">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="a1f50-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a1f50-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="a1f50-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a1f50-119">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a1f50-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a1f50-120">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1f50-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a1f50-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f50-121">-DefaultProfile</span></span>
<span data-ttu-id="a1f50-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1f50-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1f50-123">-Job</span><span class="sxs-lookup"><span data-stu-id="a1f50-123">-Job</span></span>
<span data-ttu-id="a1f50-124">指定此 **Cmdlet 更新批次處理服務的 PSCloudJob。**</span><span class="sxs-lookup"><span data-stu-id="a1f50-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f50-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f50-125">CommonParameters</span></span>
<span data-ttu-id="a1f50-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1f50-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f50-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1f50-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f50-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a1f50-128">INPUTS</span></span>

### <span data-ttu-id="a1f50-129">Microsoft.Azure.Commands.Batch。Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="a1f50-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="a1f50-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a1f50-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a1f50-131">OUTPUTS</span></span>

### <span data-ttu-id="a1f50-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="a1f50-132">System.Void</span></span>

## <span data-ttu-id="a1f50-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a1f50-133">NOTES</span></span>

## <span data-ttu-id="a1f50-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1f50-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1f50-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="a1f50-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a1f50-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a1f50-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a1f50-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a1f50-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a1f50-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a1f50-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1f50-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="a1f50-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a1f50-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
