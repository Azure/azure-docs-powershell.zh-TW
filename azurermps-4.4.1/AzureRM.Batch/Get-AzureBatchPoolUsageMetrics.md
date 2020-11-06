---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 4f985859cb26372a6ffc68b8521d08033fdc6670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457319"
---
# <span data-ttu-id="90026-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="90026-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="90026-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90026-102">SYNOPSIS</span></span>
<span data-ttu-id="90026-103">取得批次帳戶的 [池使用量] 度量單位。</span><span class="sxs-lookup"><span data-stu-id="90026-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90026-104">句法</span><span class="sxs-lookup"><span data-stu-id="90026-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90026-105">說明</span><span class="sxs-lookup"><span data-stu-id="90026-105">DESCRIPTION</span></span>
<span data-ttu-id="90026-106">AzureBatchPoolUsageMetrics Cmdlet 會針對指定的帳號， **取得** 依資源池匯總的使用度量單位。</span><span class="sxs-lookup"><span data-stu-id="90026-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="90026-107">您可以取得特定泳池和時間範圍的統計資料。</span><span class="sxs-lookup"><span data-stu-id="90026-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="90026-108">示例</span><span class="sxs-lookup"><span data-stu-id="90026-108">EXAMPLES</span></span>

### <span data-ttu-id="90026-109">範例1：取得時間範圍的池子使用度量單位</span><span class="sxs-lookup"><span data-stu-id="90026-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="90026-110">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="90026-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="90026-111">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="90026-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="90026-112">接下來的兩個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="90026-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="90026-113">這些命令會將這些值儲存在 $StartTime，並 $EndTime 變數，以用於最終命令。</span><span class="sxs-lookup"><span data-stu-id="90026-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="90026-114">最後一個命令會傳回指定開始與結束時間之間的每個時間間隔內，依池匯總的所有池使用方式度量單位。</span><span class="sxs-lookup"><span data-stu-id="90026-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="90026-115">範例2：使用篩選取得泳池使用衡量標準</span><span class="sxs-lookup"><span data-stu-id="90026-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="90026-116">這個命令會傳回名為 ContosoPool 的 pool 的使用指標。</span><span class="sxs-lookup"><span data-stu-id="90026-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="90026-117">命令會指定篩選字串來指定該池子，並使用與上一個範例相同的 $CoNtext 值。</span><span class="sxs-lookup"><span data-stu-id="90026-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="90026-118">參數</span><span class="sxs-lookup"><span data-stu-id="90026-118">PARAMETERS</span></span>

### <span data-ttu-id="90026-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="90026-119">-BatchContext</span></span>
<span data-ttu-id="90026-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="90026-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="90026-121">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90026-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="90026-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="90026-122">-EndTime</span></span>
<span data-ttu-id="90026-123">指定此 Cmdlet 取得使用度量單位之時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="90026-123">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="90026-124">指定至少在兩小時前的時間。</span><span class="sxs-lookup"><span data-stu-id="90026-124">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="90026-125">如果您沒有指定結束時間，此 Cmdlet 會使用目前可用的上一個匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="90026-125">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="90026-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="90026-126">-Filter</span></span>
<span data-ttu-id="90026-127">指定要用來篩選此 Cmdlet retruns 之度量的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="90026-127">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="90026-128">只有具有字串值的 **poolId** 有效屬性。</span><span class="sxs-lookup"><span data-stu-id="90026-128">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="90026-129">可能的作業如下： eq、ge、gt、le、lt、startswith。</span><span class="sxs-lookup"><span data-stu-id="90026-129">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="90026-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="90026-130">-StartTime</span></span>
<span data-ttu-id="90026-131">指定此 Cmdlet 取得使用方式度量單位的時間範圍起點。</span><span class="sxs-lookup"><span data-stu-id="90026-131">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="90026-132">指定至少在兩到半時間之前的時間。</span><span class="sxs-lookup"><span data-stu-id="90026-132">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="90026-133">如果您沒有指定開始時間，此 Cmdlet 會使用目前可用的上一個匯總間隔。</span><span class="sxs-lookup"><span data-stu-id="90026-133">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="90026-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90026-134">-DefaultProfile</span></span>
<span data-ttu-id="90026-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90026-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90026-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90026-136">CommonParameters</span></span>
<span data-ttu-id="90026-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90026-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90026-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90026-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90026-139">輸入</span><span class="sxs-lookup"><span data-stu-id="90026-139">INPUTS</span></span>

### <span data-ttu-id="90026-140">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="90026-140">BatchAccountContext</span></span>
<span data-ttu-id="90026-141">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="90026-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="90026-142">輸出</span><span class="sxs-lookup"><span data-stu-id="90026-142">OUTPUTS</span></span>

### <span data-ttu-id="90026-143">PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="90026-143">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="90026-144">筆記</span><span class="sxs-lookup"><span data-stu-id="90026-144">NOTES</span></span>

## <span data-ttu-id="90026-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="90026-145">RELATED LINKS</span></span>

[<span data-ttu-id="90026-146">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="90026-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="90026-147">AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="90026-147">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="90026-148">AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="90026-148">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


