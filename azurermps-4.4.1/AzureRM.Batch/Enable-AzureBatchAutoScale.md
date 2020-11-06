---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a85ac52622bb752b2e3437eb096f229c4d8e762
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456916"
---
# <span data-ttu-id="32325-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="32325-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="32325-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32325-102">SYNOPSIS</span></span>
<span data-ttu-id="32325-103">啟用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="32325-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32325-104">句法</span><span class="sxs-lookup"><span data-stu-id="32325-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32325-105">說明</span><span class="sxs-lookup"><span data-stu-id="32325-105">DESCRIPTION</span></span>
<span data-ttu-id="32325-106">**Enable-AzureBatchAutoScale** Cmdlet 可自動縮放指定的池子。</span><span class="sxs-lookup"><span data-stu-id="32325-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="32325-107">示例</span><span class="sxs-lookup"><span data-stu-id="32325-107">EXAMPLES</span></span>

### <span data-ttu-id="32325-108">範例1：針對文件庫啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="32325-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="32325-109">第一個命令會定義公式，然後將它儲存到 $Formula 變數。</span><span class="sxs-lookup"><span data-stu-id="32325-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="32325-110">第二個命令會使用 $Formula 中的公式，在名為 MyPool 的池子上啟用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="32325-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="32325-111">參數</span><span class="sxs-lookup"><span data-stu-id="32325-111">PARAMETERS</span></span>

### <span data-ttu-id="32325-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="32325-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="32325-113">指定在根據自動縮放公式自動調整池大小之前， (數分鐘內所經過的時間（以分鐘為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="32325-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="32325-114">預設值為15分鐘，最小值為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="32325-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="32325-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="32325-115">-AutoScaleFormula</span></span>
<span data-ttu-id="32325-116">在池中指定所需計算節點數的公式。</span><span class="sxs-lookup"><span data-stu-id="32325-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="32325-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="32325-117">-BatchContext</span></span>
<span data-ttu-id="32325-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="32325-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="32325-119">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32325-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="32325-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="32325-120">-Id</span></span>
<span data-ttu-id="32325-121">指定要啟用自動縮放的池物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="32325-121">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="32325-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32325-122">-DefaultProfile</span></span>
<span data-ttu-id="32325-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32325-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32325-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32325-124">CommonParameters</span></span>
<span data-ttu-id="32325-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32325-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32325-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32325-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32325-127">輸入</span><span class="sxs-lookup"><span data-stu-id="32325-127">INPUTS</span></span>

### <span data-ttu-id="32325-128">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="32325-128">BatchAccountContext</span></span>
<span data-ttu-id="32325-129">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="32325-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="32325-130">字串</span><span class="sxs-lookup"><span data-stu-id="32325-130">String</span></span>
<span data-ttu-id="32325-131">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="32325-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="32325-132">輸出</span><span class="sxs-lookup"><span data-stu-id="32325-132">OUTPUTS</span></span>

## <span data-ttu-id="32325-133">筆記</span><span class="sxs-lookup"><span data-stu-id="32325-133">NOTES</span></span>

## <span data-ttu-id="32325-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="32325-134">RELATED LINKS</span></span>

[<span data-ttu-id="32325-135">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="32325-135">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="32325-136">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="32325-136">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="32325-137">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32325-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


