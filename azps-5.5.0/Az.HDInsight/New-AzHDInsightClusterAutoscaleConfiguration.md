---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129310"
---
# <span data-ttu-id="78cdc-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="78cdc-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="78cdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="78cdc-103">建立一個描述 Azure HDInsight 群集的自動縮放設定的非持久化物件。</span><span class="sxs-lookup"><span data-stu-id="78cdc-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="78cdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="78cdc-104">SYNTAX</span></span>

### <span data-ttu-id="78cdc-105">LoadAutoscaleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="78cdc-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78cdc-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="78cdc-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78cdc-107">說明</span><span class="sxs-lookup"><span data-stu-id="78cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="78cdc-108">Cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** 會建立一個描述 Azure HDInsight 群集的自動縮放設定的非持久化物件。</span><span class="sxs-lookup"><span data-stu-id="78cdc-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="78cdc-109">示例</span><span class="sxs-lookup"><span data-stu-id="78cdc-109">EXAMPLES</span></span>

### <span data-ttu-id="78cdc-110">範例1：建立描述載入型自動縮放設定的物件</span><span class="sxs-lookup"><span data-stu-id="78cdc-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="78cdc-111">這個命令會建立一個描述載入型自動縮放設定的物件。</span><span class="sxs-lookup"><span data-stu-id="78cdc-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="78cdc-112">範例2：建立描述以排程為基礎的自動縮放設定的物件</span><span class="sxs-lookup"><span data-stu-id="78cdc-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="78cdc-113">這個命令會建立一個描述以排程為基礎的自動縮放設定的物件。</span><span class="sxs-lookup"><span data-stu-id="78cdc-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="78cdc-114">參數</span><span class="sxs-lookup"><span data-stu-id="78cdc-114">PARAMETERS</span></span>

### <span data-ttu-id="78cdc-115">-條件</span><span class="sxs-lookup"><span data-stu-id="78cdc-115">-Condition</span></span>
<span data-ttu-id="78cdc-116">取得或設定以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="78cdc-116">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="78cdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cdc-117">-DefaultProfile</span></span>
<span data-ttu-id="78cdc-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78cdc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78cdc-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="78cdc-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="78cdc-120">取得或設定載入基於負載自動縮放的最大 workernode 計數。</span><span class="sxs-lookup"><span data-stu-id="78cdc-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="78cdc-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="78cdc-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="78cdc-122">取得或設定載入基於負載自動縮放的最小 workernode 計數。</span><span class="sxs-lookup"><span data-stu-id="78cdc-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="78cdc-123">-時區</span><span class="sxs-lookup"><span data-stu-id="78cdc-123">-TimeZone</span></span>
<span data-ttu-id="78cdc-124">取得或設定以排程為基礎的自動縮放時間時區。</span><span class="sxs-lookup"><span data-stu-id="78cdc-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="78cdc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cdc-125">CommonParameters</span></span>
<span data-ttu-id="78cdc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78cdc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cdc-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78cdc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cdc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="78cdc-128">INPUTS</span></span>

### <span data-ttu-id="78cdc-129">所有</span><span class="sxs-lookup"><span data-stu-id="78cdc-129">None</span></span>

## <span data-ttu-id="78cdc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="78cdc-130">OUTPUTS</span></span>

### <span data-ttu-id="78cdc-131">AzureHDInsightAutoscale （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="78cdc-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="78cdc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="78cdc-132">NOTES</span></span>

## <span data-ttu-id="78cdc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="78cdc-133">RELATED LINKS</span></span>

<span data-ttu-id="78cdc-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
[AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
[移除-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78cdc-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
