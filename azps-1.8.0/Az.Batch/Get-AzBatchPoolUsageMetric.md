---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 480a39602f0218ed05122005a657c7e7870f7e88
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623318"
---
# <span data-ttu-id="b3456-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="b3456-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="b3456-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3456-102">SYNOPSIS</span></span>
<span data-ttu-id="b3456-103">取得批次帳戶的 [池使用量] 度量單位。</span><span class="sxs-lookup"><span data-stu-id="b3456-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="b3456-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3456-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3456-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3456-105">DESCRIPTION</span></span>
<span data-ttu-id="b3456-106">AzBatchPoolUsageMetric Cmdlet 會針對指定的帳號， **取得** 依資源池匯總的使用度量單位。</span><span class="sxs-lookup"><span data-stu-id="b3456-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="b3456-107">您可以取得特定泳池和時間範圍的統計資料。</span><span class="sxs-lookup"><span data-stu-id="b3456-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="b3456-108">示例</span><span class="sxs-lookup"><span data-stu-id="b3456-108">EXAMPLES</span></span>

### <span data-ttu-id="b3456-109">範例1：取得時間範圍的池子使用度量單位</span><span class="sxs-lookup"><span data-stu-id="b3456-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="b3456-110">第一個命令會使用 **AzBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="b3456-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="b3456-111">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="b3456-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="b3456-112">接下來的兩個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="b3456-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="b3456-113">這些命令會將這些值儲存在 $StartTime，並 $EndTime 變數，以用於最終命令。</span><span class="sxs-lookup"><span data-stu-id="b3456-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="b3456-114">最後一個命令會傳回指定開始與結束時間之間的每個時間間隔內，依池匯總的所有池使用方式度量單位。</span><span class="sxs-lookup"><span data-stu-id="b3456-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="b3456-115">範例2：使用篩選取得泳池使用衡量標準</span><span class="sxs-lookup"><span data-stu-id="b3456-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="b3456-116">這個命令會傳回名為 ContosoPool 的 pool 的使用指標。</span><span class="sxs-lookup"><span data-stu-id="b3456-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="b3456-117">命令會指定篩選字串來指定該池子，並使用與上一個範例相同的 $CoNtext 值。</span><span class="sxs-lookup"><span data-stu-id="b3456-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="b3456-118">參數</span><span class="sxs-lookup"><span data-stu-id="b3456-118">PARAMETERS</span></span>

### <span data-ttu-id="b3456-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3456-119">-BatchContext</span></span>
<span data-ttu-id="b3456-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="b3456-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b3456-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="b3456-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b3456-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="b3456-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b3456-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b3456-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b3456-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="b3456-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b3456-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3456-125">-DefaultProfile</span></span>
<span data-ttu-id="b3456-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3456-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3456-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b3456-127">-EndTime</span></span>
<span data-ttu-id="b3456-128">指定此 Cmdlet 取得使用度量單位之時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="b3456-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="b3456-129">指定至少在兩小時前的時間。</span><span class="sxs-lookup"><span data-stu-id="b3456-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="b3456-130">如果您沒有指定結束時間，此 Cmdlet 會使用目前可用的上一個匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="b3456-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3456-131">-篩選</span><span class="sxs-lookup"><span data-stu-id="b3456-131">-Filter</span></span>
<span data-ttu-id="b3456-132">指定要用來篩選此 Cmdlet retruns 之度量的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="b3456-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="b3456-133">只有具有字串值的 **poolId** 有效屬性。</span><span class="sxs-lookup"><span data-stu-id="b3456-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="b3456-134">可能的作業如下： eq、ge、gt、le、lt、startswith。</span><span class="sxs-lookup"><span data-stu-id="b3456-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3456-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b3456-135">-StartTime</span></span>
<span data-ttu-id="b3456-136">指定此 Cmdlet 取得使用方式度量單位的時間範圍起點。</span><span class="sxs-lookup"><span data-stu-id="b3456-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="b3456-137">指定至少在兩到半時間之前的時間。</span><span class="sxs-lookup"><span data-stu-id="b3456-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="b3456-138">如果您沒有指定開始時間，此 Cmdlet 會使用目前可用的上一個匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="b3456-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3456-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3456-139">CommonParameters</span></span>
<span data-ttu-id="b3456-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3456-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3456-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3456-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3456-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b3456-142">INPUTS</span></span>

### <span data-ttu-id="b3456-143">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3456-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b3456-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b3456-144">OUTPUTS</span></span>

### <span data-ttu-id="b3456-145">Microsoft.Azure.Commands.Batch。PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="b3456-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="b3456-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b3456-146">NOTES</span></span>

## <span data-ttu-id="b3456-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3456-147">RELATED LINKS</span></span>

[<span data-ttu-id="b3456-148">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b3456-148">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b3456-149">AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="b3456-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="b3456-150">AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="b3456-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)

