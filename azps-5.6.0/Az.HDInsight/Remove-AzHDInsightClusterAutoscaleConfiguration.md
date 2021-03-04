---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c18567cac6edbeb55b0f7442b45748bc3d62bc86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909025"
---
# <span data-ttu-id="a3999-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3999-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="a3999-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3999-102">SYNOPSIS</span></span>
<span data-ttu-id="a3999-103">移除 HDInsight 簇的自動縮放組式組式。</span><span class="sxs-lookup"><span data-stu-id="a3999-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a3999-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3999-104">SYNTAX</span></span>

### <span data-ttu-id="a3999-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a3999-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3999-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3999-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3999-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3999-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3999-108">描述</span><span class="sxs-lookup"><span data-stu-id="a3999-108">DESCRIPTION</span></span>
<span data-ttu-id="a3999-109">**Remove-AzHDInsightClusterAutoscaleConfiguration** Cmdlet 會移除 HDInsight 叢集的自動縮放組式組。</span><span class="sxs-lookup"><span data-stu-id="a3999-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a3999-110">例子</span><span class="sxs-lookup"><span data-stu-id="a3999-110">EXAMPLES</span></span>

### <span data-ttu-id="a3999-111">範例 1：移除 HDInsight cluster 的自動縮放組式。</span><span class="sxs-lookup"><span data-stu-id="a3999-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="a3999-112">此命令會移除 HDInsight 集區中的自動縮放組式組式。</span><span class="sxs-lookup"><span data-stu-id="a3999-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a3999-113">參數</span><span class="sxs-lookup"><span data-stu-id="a3999-113">PARAMETERS</span></span>

### <span data-ttu-id="a3999-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3999-114">-AsJob</span></span>
<span data-ttu-id="a3999-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a3999-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3999-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a3999-116">-ClusterName</span></span>
<span data-ttu-id="a3999-117">獲取或設定組名。</span><span class="sxs-lookup"><span data-stu-id="a3999-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3999-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3999-118">-DefaultProfile</span></span>
<span data-ttu-id="a3999-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3999-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3999-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3999-120">-InputObject</span></span>
<span data-ttu-id="a3999-121">獲取或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a3999-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3999-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3999-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3999-123">獲取或設定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3999-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3999-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3999-124">-ResourceId</span></span>
<span data-ttu-id="a3999-125">獲取或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3999-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3999-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a3999-126">-Confirm</span></span>
<span data-ttu-id="a3999-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a3999-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3999-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3999-128">-WhatIf</span></span>
<span data-ttu-id="a3999-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3999-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3999-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3999-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3999-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3999-131">CommonParameters</span></span>
<span data-ttu-id="a3999-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3999-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3999-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3999-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3999-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a3999-134">INPUTS</span></span>

### <span data-ttu-id="a3999-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a3999-135">System.String</span></span>

### <span data-ttu-id="a3999-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a3999-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="a3999-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a3999-137">OUTPUTS</span></span>

### <span data-ttu-id="a3999-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3999-138">System.Boolean</span></span>

## <span data-ttu-id="a3999-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a3999-139">NOTES</span></span>

## <span data-ttu-id="a3999-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3999-140">RELATED LINKS</span></span>

<span data-ttu-id="a3999-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a3999-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
