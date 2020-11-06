---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 73c1efe9e25fa02dc06f367eae1d010562eba56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457443"
---
# <span data-ttu-id="38283-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="38283-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="38283-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38283-102">SYNOPSIS</span></span>
<span data-ttu-id="38283-103">啟用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="38283-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38283-104">句法</span><span class="sxs-lookup"><span data-stu-id="38283-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38283-105">說明</span><span class="sxs-lookup"><span data-stu-id="38283-105">DESCRIPTION</span></span>
<span data-ttu-id="38283-106">**Enable-AzureBatchAutoScale** Cmdlet 可自動縮放指定的池子。</span><span class="sxs-lookup"><span data-stu-id="38283-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="38283-107">示例</span><span class="sxs-lookup"><span data-stu-id="38283-107">EXAMPLES</span></span>

### <span data-ttu-id="38283-108">範例1：針對文件庫啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="38283-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="38283-109">第一個命令會定義公式，然後將它儲存到 $Formula 變數。</span><span class="sxs-lookup"><span data-stu-id="38283-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="38283-110">第二個命令會使用 $Formula 中的公式，在名為 MyPool 的池子上啟用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="38283-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="38283-111">參數</span><span class="sxs-lookup"><span data-stu-id="38283-111">PARAMETERS</span></span>

### <span data-ttu-id="38283-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="38283-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="38283-113">指定在根據自動縮放公式自動調整池大小之前， (數分鐘內所經過的時間（以分鐘為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="38283-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="38283-114">預設值為15分鐘，最小值為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="38283-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38283-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="38283-115">-AutoScaleFormula</span></span>
<span data-ttu-id="38283-116">在池中指定所需計算節點數的公式。</span><span class="sxs-lookup"><span data-stu-id="38283-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38283-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="38283-117">-BatchContext</span></span>
<span data-ttu-id="38283-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="38283-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="38283-119">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="38283-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="38283-120">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="38283-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="38283-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="38283-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="38283-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="38283-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38283-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38283-123">-DefaultProfile</span></span>
<span data-ttu-id="38283-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38283-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38283-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="38283-125">-Id</span></span>
<span data-ttu-id="38283-126">指定要啟用自動縮放的池物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="38283-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38283-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38283-127">CommonParameters</span></span>
<span data-ttu-id="38283-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38283-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38283-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38283-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38283-130">輸入</span><span class="sxs-lookup"><span data-stu-id="38283-130">INPUTS</span></span>

### <span data-ttu-id="38283-131">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="38283-131">BatchAccountContext</span></span>
<span data-ttu-id="38283-132">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="38283-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="38283-133">字串</span><span class="sxs-lookup"><span data-stu-id="38283-133">String</span></span>
<span data-ttu-id="38283-134">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="38283-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="38283-135">輸出</span><span class="sxs-lookup"><span data-stu-id="38283-135">OUTPUTS</span></span>

## <span data-ttu-id="38283-136">筆記</span><span class="sxs-lookup"><span data-stu-id="38283-136">NOTES</span></span>

## <span data-ttu-id="38283-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="38283-137">RELATED LINKS</span></span>

[<span data-ttu-id="38283-138">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="38283-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="38283-139">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="38283-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="38283-140">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38283-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


