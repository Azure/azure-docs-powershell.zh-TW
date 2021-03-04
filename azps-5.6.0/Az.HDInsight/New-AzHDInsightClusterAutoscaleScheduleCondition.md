---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: c2fcc4112bb2fb62b73531bd6bd580ba3bcd7648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916555"
---
# <span data-ttu-id="ddecc-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="ddecc-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="ddecc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddecc-102">SYNOPSIS</span></span>
<span data-ttu-id="ddecc-103">建立以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="ddecc-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="ddecc-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddecc-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddecc-105">描述</span><span class="sxs-lookup"><span data-stu-id="ddecc-105">DESCRIPTION</span></span>
<span data-ttu-id="ddecc-106">**New-AzHDInsightClusterAutoscaleScheduleCondition** Cmdlet 會建立以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="ddecc-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="ddecc-107">例子</span><span class="sxs-lookup"><span data-stu-id="ddecc-107">EXAMPLES</span></span>

### <span data-ttu-id="ddecc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ddecc-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="ddecc-109">此命令會建立一個條件，要求每週一、星期三上午 09：00，將工作節點自動縮放為 5 個工作節點。</span><span class="sxs-lookup"><span data-stu-id="ddecc-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="ddecc-110">範例 2：啟用具有自動縮放條件的一組以排程為基礎的自動縮放。</span><span class="sxs-lookup"><span data-stu-id="ddecc-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="ddecc-111">此命令會建立一個條件，要求每週一、星期三上午 09：00，將工作節點自動縮放為 5 個工作節點。</span><span class="sxs-lookup"><span data-stu-id="ddecc-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="ddecc-112">參數</span><span class="sxs-lookup"><span data-stu-id="ddecc-112">PARAMETERS</span></span>

### <span data-ttu-id="ddecc-113">-日</span><span class="sxs-lookup"><span data-stu-id="ddecc-113">-Day</span></span>
<span data-ttu-id="ddecc-114">獲得或設定自動縮放排程條件的天數。</span><span class="sxs-lookup"><span data-stu-id="ddecc-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="ddecc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddecc-115">-DefaultProfile</span></span>
<span data-ttu-id="ddecc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddecc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddecc-117">-時間</span><span class="sxs-lookup"><span data-stu-id="ddecc-117">-Time</span></span>
<span data-ttu-id="ddecc-118">獲得或設定自動縮放排程條件的時間。</span><span class="sxs-lookup"><span data-stu-id="ddecc-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="ddecc-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="ddecc-119">-WorkerNodeCount</span></span>
<span data-ttu-id="ddecc-120">獲取或設定自動縮放排程條件的排程工作程式計數。</span><span class="sxs-lookup"><span data-stu-id="ddecc-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="ddecc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddecc-121">CommonParameters</span></span>
<span data-ttu-id="ddecc-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddecc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddecc-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddecc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddecc-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ddecc-124">INPUTS</span></span>

### <span data-ttu-id="ddecc-125">沒有</span><span class="sxs-lookup"><span data-stu-id="ddecc-125">None</span></span>

## <span data-ttu-id="ddecc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ddecc-126">OUTPUTS</span></span>

### <span data-ttu-id="ddecc-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="ddecc-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="ddecc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ddecc-128">NOTES</span></span>

## <span data-ttu-id="ddecc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddecc-129">RELATED LINKS</span></span>

<span data-ttu-id="ddecc-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ddecc-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
