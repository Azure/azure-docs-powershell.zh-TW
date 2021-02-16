---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139114"
---
# <span data-ttu-id="b23ba-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b23ba-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="b23ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b23ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b23ba-103">設定 Azure HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b23ba-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b23ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="b23ba-104">SYNTAX</span></span>

### <span data-ttu-id="b23ba-105">LoadAutoscaleByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b23ba-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b23ba-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23ba-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b23ba-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b23ba-114">說明</span><span class="sxs-lookup"><span data-stu-id="b23ba-114">DESCRIPTION</span></span>
<span data-ttu-id="b23ba-115">這個 Cmdlet **集合 AzHDInsightClusterAutoscaleConfiguration** 會設定 Azure HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b23ba-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b23ba-116">示例</span><span class="sxs-lookup"><span data-stu-id="b23ba-116">EXAMPLES</span></span>

### <span data-ttu-id="b23ba-117">範例1：設定 HDInsight 群集的負載自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="b23ba-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="b23ba-118">這個命令會設定 Azure HDInsight 群集的負載自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b23ba-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="b23ba-119">範例2：設定 HDInsight 群集的以排程為基礎的自動縮放</span><span class="sxs-lookup"><span data-stu-id="b23ba-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="b23ba-120">這個命令會設定 HDInsight 群集的以排程為基礎的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b23ba-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="b23ba-121">範例3：根據已設定自動縮放設定的其他群集，設定 HDInsight 群集的自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="b23ba-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="b23ba-122">這個命令會根據另一個群集來設定 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b23ba-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="b23ba-123">參數</span><span class="sxs-lookup"><span data-stu-id="b23ba-123">PARAMETERS</span></span>

### <span data-ttu-id="b23ba-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b23ba-124">-AsJob</span></span>
<span data-ttu-id="b23ba-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b23ba-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b23ba-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="b23ba-127">取得或設定自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="b23ba-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b23ba-128">-ClusterName</span></span>
<span data-ttu-id="b23ba-129">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b23ba-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-130">-條件</span><span class="sxs-lookup"><span data-stu-id="b23ba-130">-Condition</span></span>
<span data-ttu-id="b23ba-131">取得或設定以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="b23ba-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23ba-132">-DefaultProfile</span></span>
<span data-ttu-id="b23ba-133">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b23ba-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b23ba-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b23ba-134">-InputObject</span></span>
<span data-ttu-id="b23ba-135">取得或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b23ba-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="b23ba-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="b23ba-137">取得或設定載入基於負載自動縮放的最大 workernode 計數。</span><span class="sxs-lookup"><span data-stu-id="b23ba-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="b23ba-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="b23ba-139">取得或設定載入基於負載自動縮放的最小 workernode 計數。</span><span class="sxs-lookup"><span data-stu-id="b23ba-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b23ba-140">-ResourceGroupName</span></span>
<span data-ttu-id="b23ba-141">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b23ba-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b23ba-142">-ResourceId</span></span>
<span data-ttu-id="b23ba-143">取得或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b23ba-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-144">-排程</span><span class="sxs-lookup"><span data-stu-id="b23ba-144">-Schedule</span></span>
<span data-ttu-id="b23ba-145">設定排程式參數</span><span class="sxs-lookup"><span data-stu-id="b23ba-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-146">-時區</span><span class="sxs-lookup"><span data-stu-id="b23ba-146">-TimeZone</span></span>
<span data-ttu-id="b23ba-147">取得或設定以排程為基礎的自動縮放時間時區。</span><span class="sxs-lookup"><span data-stu-id="b23ba-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-148">-確認</span><span class="sxs-lookup"><span data-stu-id="b23ba-148">-Confirm</span></span>
<span data-ttu-id="b23ba-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b23ba-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b23ba-150">-WhatIf</span></span>
<span data-ttu-id="b23ba-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b23ba-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b23ba-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b23ba-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23ba-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23ba-153">CommonParameters</span></span>
<span data-ttu-id="b23ba-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b23ba-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23ba-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b23ba-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23ba-156">輸入</span><span class="sxs-lookup"><span data-stu-id="b23ba-156">INPUTS</span></span>

### <span data-ttu-id="b23ba-157">System.object</span><span class="sxs-lookup"><span data-stu-id="b23ba-157">System.String</span></span>

### <span data-ttu-id="b23ba-158">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b23ba-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="b23ba-159">輸出</span><span class="sxs-lookup"><span data-stu-id="b23ba-159">OUTPUTS</span></span>

### <span data-ttu-id="b23ba-160">AzureHDInsightAutoscale （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b23ba-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="b23ba-161">筆記</span><span class="sxs-lookup"><span data-stu-id="b23ba-161">NOTES</span></span>

## <span data-ttu-id="b23ba-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="b23ba-162">RELATED LINKS</span></span>

<span data-ttu-id="b23ba-163">[新-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
[移除-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b23ba-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
