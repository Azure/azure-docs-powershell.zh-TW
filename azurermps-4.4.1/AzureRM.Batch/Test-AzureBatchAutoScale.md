---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623520"
---
# <span data-ttu-id="99865-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="99865-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="99865-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99865-102">SYNOPSIS</span></span>
<span data-ttu-id="99865-103">取得池中自動縮放公式的結果。</span><span class="sxs-lookup"><span data-stu-id="99865-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99865-104">句法</span><span class="sxs-lookup"><span data-stu-id="99865-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99865-105">說明</span><span class="sxs-lookup"><span data-stu-id="99865-105">DESCRIPTION</span></span>
<span data-ttu-id="99865-106">**Test AzureBatchAutoScale** Cmdlet 會在指定的池中取得自動縮放公式的結果。</span><span class="sxs-lookup"><span data-stu-id="99865-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="99865-107">示例</span><span class="sxs-lookup"><span data-stu-id="99865-107">EXAMPLES</span></span>

### <span data-ttu-id="99865-108">範例1：評估資源庫上的自動縮放公式</span><span class="sxs-lookup"><span data-stu-id="99865-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="99865-109">第一個命令會將公式儲存在 $Formula 變數中，以供在範例中使用。</span><span class="sxs-lookup"><span data-stu-id="99865-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="99865-110">第二個命令會針對具有識別碼 ContosoPool 的池中評估自動縮放公式。</span><span class="sxs-lookup"><span data-stu-id="99865-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="99865-111">最後一個命令會使用標準的點語法來顯示 **結果** 。</span><span class="sxs-lookup"><span data-stu-id="99865-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="99865-112">參數</span><span class="sxs-lookup"><span data-stu-id="99865-112">PARAMETERS</span></span>

### <span data-ttu-id="99865-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="99865-113">-AutoScaleFormula</span></span>
<span data-ttu-id="99865-114">在池中指定所需計算節點數的公式。</span><span class="sxs-lookup"><span data-stu-id="99865-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="99865-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="99865-115">-BatchContext</span></span>
<span data-ttu-id="99865-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="99865-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99865-117">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99865-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="99865-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="99865-118">-Id</span></span>
<span data-ttu-id="99865-119">指定要測試自動縮放比例的 [池] 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="99865-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="99865-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99865-120">-DefaultProfile</span></span>
<span data-ttu-id="99865-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99865-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99865-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99865-122">CommonParameters</span></span>
<span data-ttu-id="99865-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99865-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99865-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99865-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99865-125">輸入</span><span class="sxs-lookup"><span data-stu-id="99865-125">INPUTS</span></span>

### <span data-ttu-id="99865-126">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="99865-126">BatchAccountContext</span></span>
<span data-ttu-id="99865-127">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="99865-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="99865-128">字串</span><span class="sxs-lookup"><span data-stu-id="99865-128">String</span></span>
<span data-ttu-id="99865-129">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="99865-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="99865-130">輸出</span><span class="sxs-lookup"><span data-stu-id="99865-130">OUTPUTS</span></span>

### <span data-ttu-id="99865-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="99865-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="99865-132">筆記</span><span class="sxs-lookup"><span data-stu-id="99865-132">NOTES</span></span>

## <span data-ttu-id="99865-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="99865-133">RELATED LINKS</span></span>

[<span data-ttu-id="99865-134">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="99865-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="99865-135">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="99865-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="99865-136">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="99865-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="99865-137">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="99865-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


