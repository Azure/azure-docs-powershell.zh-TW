---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 7d23774085bb467ca091aa500cf67ee43fa2aa46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909234"
---
# <span data-ttu-id="a23ac-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="a23ac-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="a23ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a23ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a23ac-103">獲得批次帳戶的集中使用計量。</span><span class="sxs-lookup"><span data-stu-id="a23ac-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="a23ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="a23ac-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a23ac-105">描述</span><span class="sxs-lookup"><span data-stu-id="a23ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a23ac-106">**Get-AzBatchPoolUsageMetric** Cmdlet 會取得指定帳戶的使用計量，在個別時間間隔內根據集合匯總。</span><span class="sxs-lookup"><span data-stu-id="a23ac-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="a23ac-107">您可以取得特定資料庫和一個時間範圍的統計資料。</span><span class="sxs-lookup"><span data-stu-id="a23ac-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="a23ac-108">例子</span><span class="sxs-lookup"><span data-stu-id="a23ac-108">EXAMPLES</span></span>

### <span data-ttu-id="a23ac-109">範例 1：取得時間範圍的集中使用計量</span><span class="sxs-lookup"><span data-stu-id="a23ac-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
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

<span data-ttu-id="a23ac-110">第一個命令會使用 **Get-AzBatchAccountKey，為名為 ContosoBatchAccount** 的批次帳戶建立帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="a23ac-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="a23ac-111">命令會在此變數中儲存$CoNtext參照。</span><span class="sxs-lookup"><span data-stu-id="a23ac-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="a23ac-112">接下來兩個命令會使用 Cmdlet 建立 **DateTime** 物件Get-Date物件。</span><span class="sxs-lookup"><span data-stu-id="a23ac-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="a23ac-113">這些命令會將這些值儲存在$StartTime$EndTime變數中，以用於最後一個命令。</span><span class="sxs-lookup"><span data-stu-id="a23ac-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="a23ac-114">最後一個命令會根據集合，在指定的開始與結束時間之間的時間間隔內，會以集合方式，會以集合的形式，會以集合方式，會以所有集合方式，來將集合使用狀況計量。</span><span class="sxs-lookup"><span data-stu-id="a23ac-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="a23ac-115">範例 2：使用篩選取得計算區使用量計量</span><span class="sxs-lookup"><span data-stu-id="a23ac-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="a23ac-116">此命令會針對名為 ContosoPool 的集中，會返回使用量計量。</span><span class="sxs-lookup"><span data-stu-id="a23ac-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="a23ac-117">命令會指定篩選字串以指定該資料$CoNtext值與上一個範例相同。</span><span class="sxs-lookup"><span data-stu-id="a23ac-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="a23ac-118">參數</span><span class="sxs-lookup"><span data-stu-id="a23ac-118">PARAMETERS</span></span>

### <span data-ttu-id="a23ac-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="a23ac-119">-BatchContext</span></span>
<span data-ttu-id="a23ac-120">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="a23ac-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a23ac-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="a23ac-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a23ac-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="a23ac-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a23ac-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a23ac-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a23ac-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="a23ac-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a23ac-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23ac-125">-DefaultProfile</span></span>
<span data-ttu-id="a23ac-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a23ac-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a23ac-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a23ac-127">-EndTime</span></span>
<span data-ttu-id="a23ac-128">指定此 Cmdlet 會獲得使用計量的一個時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="a23ac-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="a23ac-129">指定至少兩小時前的時間。</span><span class="sxs-lookup"><span data-stu-id="a23ac-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="a23ac-130">如果您未指定結束時間，此 Cmdlet 會使用目前可用的最後一個匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="a23ac-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="a23ac-131">-篩選</span><span class="sxs-lookup"><span data-stu-id="a23ac-131">-Filter</span></span>
<span data-ttu-id="a23ac-132">指定 OData 篩選子句，以用於篩選此 Cmdlet 會返回的度量。</span><span class="sxs-lookup"><span data-stu-id="a23ac-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="a23ac-133">唯一有效的屬性是 **包含字串值的 poolId。**</span><span class="sxs-lookup"><span data-stu-id="a23ac-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="a23ac-134">可能的操作如下：eq、ge、gt、le、lt、startswith。</span><span class="sxs-lookup"><span data-stu-id="a23ac-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="a23ac-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a23ac-135">-StartTime</span></span>
<span data-ttu-id="a23ac-136">指定此 Cmdlet 會獲得使用計量的開始時間範圍。</span><span class="sxs-lookup"><span data-stu-id="a23ac-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="a23ac-137">指定至少兩個半小時之前的時間。</span><span class="sxs-lookup"><span data-stu-id="a23ac-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="a23ac-138">如果您未指定開始時間，此 Cmdlet 會使用目前可用的最後一個匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="a23ac-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="a23ac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23ac-139">CommonParameters</span></span>
<span data-ttu-id="a23ac-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a23ac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23ac-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a23ac-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23ac-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a23ac-142">INPUTS</span></span>

### <span data-ttu-id="a23ac-143">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="a23ac-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a23ac-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a23ac-144">OUTPUTS</span></span>

### <span data-ttu-id="a23ac-145">Microsoft.Azure.Commands.Batch。Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="a23ac-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="a23ac-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a23ac-146">NOTES</span></span>

## <span data-ttu-id="a23ac-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a23ac-147">RELATED LINKS</span></span>

[<span data-ttu-id="a23ac-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a23ac-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a23ac-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="a23ac-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="a23ac-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="a23ac-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
