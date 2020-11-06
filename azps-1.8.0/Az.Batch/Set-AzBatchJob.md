---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 86e977c3d538c9eeb5f26da7d70db1726adf119b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623272"
---
# <span data-ttu-id="1561b-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="1561b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1561b-102">SYNOPSIS</span></span>
<span data-ttu-id="1561b-103">更新批次作業。</span><span class="sxs-lookup"><span data-stu-id="1561b-103">Updates a Batch job.</span></span>

## <span data-ttu-id="1561b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1561b-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1561b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1561b-105">DESCRIPTION</span></span>
<span data-ttu-id="1561b-106">**AzBatchJob** Cmdlet 會更新 Azure Batch 作業。</span><span class="sxs-lookup"><span data-stu-id="1561b-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="1561b-107">使用 Get-AzBatchJob Cmdlet 來取得 **PSCloudJob** 物件。</span><span class="sxs-lookup"><span data-stu-id="1561b-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="1561b-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="1561b-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1561b-109">示例</span><span class="sxs-lookup"><span data-stu-id="1561b-109">EXAMPLES</span></span>

### <span data-ttu-id="1561b-110">範例1：更新作業</span><span class="sxs-lookup"><span data-stu-id="1561b-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="1561b-111">第一個命令會使用 **AzBatchJob** 來取得作業，然後將它儲存在 $Job 變數中。</span><span class="sxs-lookup"><span data-stu-id="1561b-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="1561b-112">第二個命令會修改 $Job 物件的優先順序規格。</span><span class="sxs-lookup"><span data-stu-id="1561b-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="1561b-113">最後一個命令會更新批次服務，以符合 $Job 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="1561b-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="1561b-114">參數</span><span class="sxs-lookup"><span data-stu-id="1561b-114">PARAMETERS</span></span>

### <span data-ttu-id="1561b-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="1561b-115">-BatchContext</span></span>
<span data-ttu-id="1561b-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="1561b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1561b-117">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="1561b-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1561b-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="1561b-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1561b-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1561b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1561b-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="1561b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1561b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1561b-121">-DefaultProfile</span></span>
<span data-ttu-id="1561b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1561b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1561b-123">-工作</span><span class="sxs-lookup"><span data-stu-id="1561b-123">-Job</span></span>
<span data-ttu-id="1561b-124">指定此 Cmdlet 更新批次服務的 **PSCloudJob** 。</span><span class="sxs-lookup"><span data-stu-id="1561b-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="1561b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1561b-125">CommonParameters</span></span>
<span data-ttu-id="1561b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1561b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1561b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1561b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1561b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1561b-128">INPUTS</span></span>

### <span data-ttu-id="1561b-129">Microsoft.Azure.Commands.Batch。PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1561b-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="1561b-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="1561b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1561b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1561b-131">OUTPUTS</span></span>

### <span data-ttu-id="1561b-132">System.void</span><span class="sxs-lookup"><span data-stu-id="1561b-132">System.Void</span></span>

## <span data-ttu-id="1561b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1561b-133">NOTES</span></span>

## <span data-ttu-id="1561b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1561b-134">RELATED LINKS</span></span>

[<span data-ttu-id="1561b-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="1561b-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="1561b-137">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1561b-138">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1561b-138">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1561b-139">新-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="1561b-140">移除-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="1561b-141">停止 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1561b-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="1561b-142">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1561b-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


