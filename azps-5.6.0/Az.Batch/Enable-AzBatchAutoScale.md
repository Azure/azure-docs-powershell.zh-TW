---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: b7b63da46832c94466a58bb04f62436a6778af96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912477"
---
# <span data-ttu-id="14bd0-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="14bd0-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="14bd0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="14bd0-103">啟用自動縮放資料庫。</span><span class="sxs-lookup"><span data-stu-id="14bd0-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="14bd0-104">語法</span><span class="sxs-lookup"><span data-stu-id="14bd0-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14bd0-105">描述</span><span class="sxs-lookup"><span data-stu-id="14bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="14bd0-106">**Enable-AzBatchAutoScale** Cmdlet 可啟用指定資料庫的自動縮放功能。</span><span class="sxs-lookup"><span data-stu-id="14bd0-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="14bd0-107">例子</span><span class="sxs-lookup"><span data-stu-id="14bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="14bd0-108">範例 1：啟用自動縮放功能</span><span class="sxs-lookup"><span data-stu-id="14bd0-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="14bd0-109">第一個命令會定義公式，然後將它$Formula變數。</span><span class="sxs-lookup"><span data-stu-id="14bd0-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="14bd0-110">第二個命令會使用 $Formula 中的公式，在名為 MyPool 的$Formula。</span><span class="sxs-lookup"><span data-stu-id="14bd0-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="14bd0-111">參數</span><span class="sxs-lookup"><span data-stu-id="14bd0-111">PARAMETERS</span></span>

### <span data-ttu-id="14bd0-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="14bd0-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="14bd0-113">指定根據自動縮放 (，) 自動調整資料庫大小之前經過的時間量 ，以分鐘計算。</span><span class="sxs-lookup"><span data-stu-id="14bd0-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="14bd0-114">預設值為 15 分鐘，最小值為 5 分鐘。</span><span class="sxs-lookup"><span data-stu-id="14bd0-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="14bd0-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="14bd0-115">-AutoScaleFormula</span></span>
<span data-ttu-id="14bd0-116">指定計算節點數量所需的公式。</span><span class="sxs-lookup"><span data-stu-id="14bd0-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="14bd0-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="14bd0-117">-BatchContext</span></span>
<span data-ttu-id="14bd0-118">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="14bd0-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14bd0-119">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="14bd0-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14bd0-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="14bd0-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14bd0-121">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="14bd0-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14bd0-122">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="14bd0-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="14bd0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14bd0-123">-DefaultProfile</span></span>
<span data-ttu-id="14bd0-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14bd0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14bd0-125">-Id</span><span class="sxs-lookup"><span data-stu-id="14bd0-125">-Id</span></span>
<span data-ttu-id="14bd0-126">指定要啟用自動縮放功能之資料組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="14bd0-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="14bd0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14bd0-127">CommonParameters</span></span>
<span data-ttu-id="14bd0-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14bd0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14bd0-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14bd0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14bd0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="14bd0-130">INPUTS</span></span>

### <span data-ttu-id="14bd0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="14bd0-131">System.String</span></span>

### <span data-ttu-id="14bd0-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="14bd0-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="14bd0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="14bd0-133">OUTPUTS</span></span>

### <span data-ttu-id="14bd0-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="14bd0-134">System.Void</span></span>

## <span data-ttu-id="14bd0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="14bd0-135">NOTES</span></span>

## <span data-ttu-id="14bd0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="14bd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="14bd0-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="14bd0-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="14bd0-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="14bd0-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="14bd0-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="14bd0-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
