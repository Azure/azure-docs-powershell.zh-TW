---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136809"
---
# <span data-ttu-id="79980-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="79980-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="79980-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79980-102">SYNOPSIS</span></span>
<span data-ttu-id="79980-103">建立以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="79980-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="79980-104">句法</span><span class="sxs-lookup"><span data-stu-id="79980-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79980-105">說明</span><span class="sxs-lookup"><span data-stu-id="79980-105">DESCRIPTION</span></span>
<span data-ttu-id="79980-106">**新的-AzHDInsightClusterAutoscaleScheduleCondition** Cmdlet 會建立以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="79980-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="79980-107">示例</span><span class="sxs-lookup"><span data-stu-id="79980-107">EXAMPLES</span></span>

### <span data-ttu-id="79980-108">範例1</span><span class="sxs-lookup"><span data-stu-id="79980-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="79980-109">這個命令會在每個星期一、星期三，建立每個09:00 的群集自動縮放至5個工作節點的情況。</span><span class="sxs-lookup"><span data-stu-id="79980-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="79980-110">範例2：使用自動縮放條件啟用群集的以排程為基礎的自動縮放。</span><span class="sxs-lookup"><span data-stu-id="79980-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="79980-111">這個命令會在每個星期一、星期三，建立每個09:00 的群集自動縮放至5個工作節點的情況。</span><span class="sxs-lookup"><span data-stu-id="79980-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="79980-112">參數</span><span class="sxs-lookup"><span data-stu-id="79980-112">PARAMETERS</span></span>

### <span data-ttu-id="79980-113">日</span><span class="sxs-lookup"><span data-stu-id="79980-113">-Day</span></span>
<span data-ttu-id="79980-114">取得或設定自動縮放排程條件的天數。</span><span class="sxs-lookup"><span data-stu-id="79980-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79980-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79980-115">-DefaultProfile</span></span>
<span data-ttu-id="79980-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79980-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79980-117">時間</span><span class="sxs-lookup"><span data-stu-id="79980-117">-Time</span></span>
<span data-ttu-id="79980-118">取得或設定自動縮放排程條件的時間。</span><span class="sxs-lookup"><span data-stu-id="79980-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79980-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="79980-119">-WorkerNodeCount</span></span>
<span data-ttu-id="79980-120">取得或設定自動縮放排程條件的排程 workernode 計數。</span><span class="sxs-lookup"><span data-stu-id="79980-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79980-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79980-121">CommonParameters</span></span>
<span data-ttu-id="79980-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79980-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79980-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79980-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79980-124">輸入</span><span class="sxs-lookup"><span data-stu-id="79980-124">INPUTS</span></span>

### <span data-ttu-id="79980-125">所有</span><span class="sxs-lookup"><span data-stu-id="79980-125">None</span></span>

## <span data-ttu-id="79980-126">輸出</span><span class="sxs-lookup"><span data-stu-id="79980-126">OUTPUTS</span></span>

### <span data-ttu-id="79980-127">AzureHDInsightAutoscaleCondition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="79980-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="79980-128">筆記</span><span class="sxs-lookup"><span data-stu-id="79980-128">NOTES</span></span>

## <span data-ttu-id="79980-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="79980-129">RELATED LINKS</span></span>

<span data-ttu-id="79980-130">[新-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="79980-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
