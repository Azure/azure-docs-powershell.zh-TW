---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281847"
---
# <span data-ttu-id="47a50-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="47a50-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="47a50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47a50-102">SYNOPSIS</span></span>
<span data-ttu-id="47a50-103">啟用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="47a50-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="47a50-104">句法</span><span class="sxs-lookup"><span data-stu-id="47a50-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47a50-105">說明</span><span class="sxs-lookup"><span data-stu-id="47a50-105">DESCRIPTION</span></span>
<span data-ttu-id="47a50-106">**Enable-AzBatchAutoScale** Cmdlet 可自動縮放指定的池子。</span><span class="sxs-lookup"><span data-stu-id="47a50-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="47a50-107">示例</span><span class="sxs-lookup"><span data-stu-id="47a50-107">EXAMPLES</span></span>

### <span data-ttu-id="47a50-108">範例1：針對文件庫啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="47a50-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="47a50-109">第一個命令會定義公式，然後將它儲存到 $Formula 變數。</span><span class="sxs-lookup"><span data-stu-id="47a50-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="47a50-110">第二個命令會使用 $Formula 中的公式，在名為 MyPool 的池子上啟用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="47a50-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="47a50-111">參數</span><span class="sxs-lookup"><span data-stu-id="47a50-111">PARAMETERS</span></span>

### <span data-ttu-id="47a50-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="47a50-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="47a50-113">指定在根據自動縮放公式自動調整池大小之前， (數分鐘內所經過的時間（以分鐘為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="47a50-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="47a50-114">預設值為15分鐘，最小值為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="47a50-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a50-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="47a50-115">-AutoScaleFormula</span></span>
<span data-ttu-id="47a50-116">在池中指定所需計算節點數的公式。</span><span class="sxs-lookup"><span data-stu-id="47a50-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="47a50-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="47a50-117">-BatchContext</span></span>
<span data-ttu-id="47a50-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="47a50-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="47a50-119">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="47a50-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="47a50-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="47a50-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="47a50-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="47a50-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="47a50-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="47a50-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="47a50-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a50-123">-DefaultProfile</span></span>
<span data-ttu-id="47a50-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47a50-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47a50-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="47a50-125">-Id</span></span>
<span data-ttu-id="47a50-126">指定要啟用自動縮放的池物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="47a50-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="47a50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a50-127">CommonParameters</span></span>
<span data-ttu-id="47a50-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47a50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a50-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47a50-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a50-130">輸入</span><span class="sxs-lookup"><span data-stu-id="47a50-130">INPUTS</span></span>

### <span data-ttu-id="47a50-131">System.object</span><span class="sxs-lookup"><span data-stu-id="47a50-131">System.String</span></span>

### <span data-ttu-id="47a50-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="47a50-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="47a50-133">輸出</span><span class="sxs-lookup"><span data-stu-id="47a50-133">OUTPUTS</span></span>

### <span data-ttu-id="47a50-134">System.void</span><span class="sxs-lookup"><span data-stu-id="47a50-134">System.Void</span></span>

## <span data-ttu-id="47a50-135">筆記</span><span class="sxs-lookup"><span data-stu-id="47a50-135">NOTES</span></span>

## <span data-ttu-id="47a50-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="47a50-136">RELATED LINKS</span></span>

[<span data-ttu-id="47a50-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="47a50-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="47a50-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="47a50-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="47a50-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47a50-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
