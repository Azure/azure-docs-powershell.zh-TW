---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 4f60445dc22c2e2b0f8c0c5291691f4d7456db2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916953"
---
# <span data-ttu-id="0072f-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0072f-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="0072f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0072f-102">SYNOPSIS</span></span>
<span data-ttu-id="0072f-103">獲得 HDInsight 簇的自動縮放組式組式。</span><span class="sxs-lookup"><span data-stu-id="0072f-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="0072f-104">語法</span><span class="sxs-lookup"><span data-stu-id="0072f-104">SYNTAX</span></span>

### <span data-ttu-id="0072f-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0072f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0072f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0072f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0072f-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0072f-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0072f-108">描述</span><span class="sxs-lookup"><span data-stu-id="0072f-108">DESCRIPTION</span></span>
<span data-ttu-id="0072f-109">**Get-AzHDInsightClusterAutoscaleConfiguration** Cmdlet 取得 HDInsight 叢集的自動縮放組式組。</span><span class="sxs-lookup"><span data-stu-id="0072f-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="0072f-110">例子</span><span class="sxs-lookup"><span data-stu-id="0072f-110">EXAMPLES</span></span>

### <span data-ttu-id="0072f-111">範例 1：取得 HDInsight cluster 的自動縮放組式。</span><span class="sxs-lookup"><span data-stu-id="0072f-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="0072f-112">此命令會獲得 HDInsight 集區自動縮放組式組。</span><span class="sxs-lookup"><span data-stu-id="0072f-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="0072f-113">參數</span><span class="sxs-lookup"><span data-stu-id="0072f-113">PARAMETERS</span></span>

### <span data-ttu-id="0072f-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0072f-114">-ClusterName</span></span>
<span data-ttu-id="0072f-115">獲取或設定組名。</span><span class="sxs-lookup"><span data-stu-id="0072f-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0072f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0072f-116">-DefaultProfile</span></span>
<span data-ttu-id="0072f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0072f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0072f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0072f-118">-InputObject</span></span>
<span data-ttu-id="0072f-119">獲取或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0072f-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0072f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0072f-120">-ResourceGroupName</span></span>
<span data-ttu-id="0072f-121">獲取或設定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0072f-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0072f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0072f-122">-ResourceId</span></span>
<span data-ttu-id="0072f-123">獲取或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0072f-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0072f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0072f-124">CommonParameters</span></span>
<span data-ttu-id="0072f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0072f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0072f-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0072f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0072f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0072f-127">INPUTS</span></span>

### <span data-ttu-id="0072f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0072f-128">System.String</span></span>

### <span data-ttu-id="0072f-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0072f-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="0072f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0072f-130">OUTPUTS</span></span>

### <span data-ttu-id="0072f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="0072f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="0072f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0072f-132">NOTES</span></span>

## <span data-ttu-id="0072f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0072f-133">RELATED LINKS</span></span>

<span data-ttu-id="0072f-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0072f-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
