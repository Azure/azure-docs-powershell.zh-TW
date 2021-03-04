---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bfc14e0fba2b384766495dde9e3ef11fafd4653c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916556"
---
# <span data-ttu-id="57e5e-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e5e-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="57e5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="57e5e-103">建立描述 Azure HDInsight 集區之自動縮放設置的非持續物件。</span><span class="sxs-lookup"><span data-stu-id="57e5e-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="57e5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="57e5e-104">SYNTAX</span></span>

### <span data-ttu-id="57e5e-105">LoadAutoscaleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57e5e-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e5e-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="57e5e-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e5e-107">描述</span><span class="sxs-lookup"><span data-stu-id="57e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="57e5e-108">Cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** 會建立描述 Azure HDInsight 叢集自動縮放組式配置的非持續物件。</span><span class="sxs-lookup"><span data-stu-id="57e5e-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="57e5e-109">例子</span><span class="sxs-lookup"><span data-stu-id="57e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="57e5e-110">範例 1：建立描述載入型自動縮放設置的物件</span><span class="sxs-lookup"><span data-stu-id="57e5e-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="57e5e-111">此命令會建立描述載入型自動縮放配置的物件。</span><span class="sxs-lookup"><span data-stu-id="57e5e-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="57e5e-112">範例 2：建立描述以排程為基礎的自動縮放設置的物件</span><span class="sxs-lookup"><span data-stu-id="57e5e-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="57e5e-113">此命令會建立描述排程型自動縮放配置的物件。</span><span class="sxs-lookup"><span data-stu-id="57e5e-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="57e5e-114">參數</span><span class="sxs-lookup"><span data-stu-id="57e5e-114">PARAMETERS</span></span>

### <span data-ttu-id="57e5e-115">-條件</span><span class="sxs-lookup"><span data-stu-id="57e5e-115">-Condition</span></span>
<span data-ttu-id="57e5e-116">獲得或設定以排程為基礎的自動縮放的條件。</span><span class="sxs-lookup"><span data-stu-id="57e5e-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e5e-117">-DefaultProfile</span></span>
<span data-ttu-id="57e5e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57e5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57e5e-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="57e5e-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="57e5e-120">獲得或設定負載型自動縮放的最大工作節點計數。</span><span class="sxs-lookup"><span data-stu-id="57e5e-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e5e-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="57e5e-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="57e5e-122">獲得或設定負載型自動縮放的最少工作節點計數。</span><span class="sxs-lookup"><span data-stu-id="57e5e-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e5e-123">-時區</span><span class="sxs-lookup"><span data-stu-id="57e5e-123">-TimeZone</span></span>
<span data-ttu-id="57e5e-124">獲取或設定以排程為基礎的自動縮放的時區。</span><span class="sxs-lookup"><span data-stu-id="57e5e-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e5e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e5e-125">CommonParameters</span></span>
<span data-ttu-id="57e5e-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57e5e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e5e-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57e5e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e5e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="57e5e-128">INPUTS</span></span>

### <span data-ttu-id="57e5e-129">沒有</span><span class="sxs-lookup"><span data-stu-id="57e5e-129">None</span></span>

## <span data-ttu-id="57e5e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="57e5e-130">OUTPUTS</span></span>

### <span data-ttu-id="57e5e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="57e5e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="57e5e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="57e5e-132">NOTES</span></span>

## <span data-ttu-id="57e5e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="57e5e-133">RELATED LINKS</span></span>

<span data-ttu-id="57e5e-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="57e5e-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
