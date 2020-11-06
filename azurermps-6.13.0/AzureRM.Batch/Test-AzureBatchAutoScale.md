---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 3dc458c5b23e3bd6f8bde39e02152e8c2b76f6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451920"
---
# <span data-ttu-id="c0b22-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c0b22-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="c0b22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0b22-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b22-103">取得池中自動縮放公式的結果。</span><span class="sxs-lookup"><span data-stu-id="c0b22-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0b22-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0b22-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0b22-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0b22-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b22-106">**Test AzureBatchAutoScale** Cmdlet 會在指定的池中取得自動縮放公式的結果。</span><span class="sxs-lookup"><span data-stu-id="c0b22-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="c0b22-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0b22-107">EXAMPLES</span></span>

### <span data-ttu-id="c0b22-108">範例1：評估資源庫上的自動縮放公式</span><span class="sxs-lookup"><span data-stu-id="c0b22-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="c0b22-109">第一個命令會將公式儲存在 $Formula 變數中，以供在範例中使用。</span><span class="sxs-lookup"><span data-stu-id="c0b22-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="c0b22-110">第二個命令會針對具有識別碼 ContosoPool 的池中評估自動縮放公式。</span><span class="sxs-lookup"><span data-stu-id="c0b22-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="c0b22-111">最後一個命令會使用標準的點語法來顯示 **結果** 。</span><span class="sxs-lookup"><span data-stu-id="c0b22-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="c0b22-112">參數</span><span class="sxs-lookup"><span data-stu-id="c0b22-112">PARAMETERS</span></span>

### <span data-ttu-id="c0b22-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="c0b22-113">-AutoScaleFormula</span></span>
<span data-ttu-id="c0b22-114">在池中指定所需計算節點數的公式。</span><span class="sxs-lookup"><span data-stu-id="c0b22-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b22-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0b22-115">-BatchContext</span></span>
<span data-ttu-id="c0b22-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="c0b22-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0b22-117">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="c0b22-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0b22-118">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="c0b22-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0b22-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c0b22-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0b22-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="c0b22-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0b22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b22-121">-DefaultProfile</span></span>
<span data-ttu-id="c0b22-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0b22-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b22-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c0b22-123">-Id</span></span>
<span data-ttu-id="c0b22-124">指定要測試自動縮放比例的 [池] 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0b22-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="c0b22-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b22-125">CommonParameters</span></span>
<span data-ttu-id="c0b22-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0b22-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b22-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0b22-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b22-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c0b22-128">INPUTS</span></span>

### <span data-ttu-id="c0b22-129">System.object</span><span class="sxs-lookup"><span data-stu-id="c0b22-129">System.String</span></span>

### <span data-ttu-id="c0b22-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0b22-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c0b22-131">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c0b22-131">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c0b22-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c0b22-132">OUTPUTS</span></span>

### <span data-ttu-id="c0b22-133">Microsoft.Azure.Commands.Batch。PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="c0b22-133">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="c0b22-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c0b22-134">NOTES</span></span>

## <span data-ttu-id="c0b22-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0b22-135">RELATED LINKS</span></span>

[<span data-ttu-id="c0b22-136">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c0b22-136">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="c0b22-137">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c0b22-137">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="c0b22-138">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c0b22-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c0b22-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0b22-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


