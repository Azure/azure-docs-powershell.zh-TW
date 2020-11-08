---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971450"
---
# <span data-ttu-id="de4a2-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="de4a2-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="de4a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="de4a2-103">取得 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="de4a2-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="de4a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="de4a2-104">SYNTAX</span></span>

### <span data-ttu-id="de4a2-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="de4a2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de4a2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4a2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de4a2-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4a2-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de4a2-108">說明</span><span class="sxs-lookup"><span data-stu-id="de4a2-108">DESCRIPTION</span></span>
<span data-ttu-id="de4a2-109">**AzHDInsightClusterAutoscaleConfiguration** Cmdlet 會取得 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="de4a2-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="de4a2-110">示例</span><span class="sxs-lookup"><span data-stu-id="de4a2-110">EXAMPLES</span></span>

### <span data-ttu-id="de4a2-111">範例1：取得 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="de4a2-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="de4a2-112">這個命令會取得 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="de4a2-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="de4a2-113">參數</span><span class="sxs-lookup"><span data-stu-id="de4a2-113">PARAMETERS</span></span>

### <span data-ttu-id="de4a2-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="de4a2-114">-ClusterName</span></span>
<span data-ttu-id="de4a2-115">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="de4a2-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="de4a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4a2-116">-DefaultProfile</span></span>
<span data-ttu-id="de4a2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de4a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de4a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de4a2-118">-InputObject</span></span>
<span data-ttu-id="de4a2-119">取得或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="de4a2-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="de4a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="de4a2-121">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de4a2-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="de4a2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de4a2-122">-ResourceId</span></span>
<span data-ttu-id="de4a2-123">取得或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="de4a2-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="de4a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4a2-124">CommonParameters</span></span>
<span data-ttu-id="de4a2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de4a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4a2-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de4a2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4a2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="de4a2-127">INPUTS</span></span>

### <span data-ttu-id="de4a2-128">System.object</span><span class="sxs-lookup"><span data-stu-id="de4a2-128">System.String</span></span>

### <span data-ttu-id="de4a2-129">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="de4a2-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="de4a2-130">輸出</span><span class="sxs-lookup"><span data-stu-id="de4a2-130">OUTPUTS</span></span>

### <span data-ttu-id="de4a2-131">AzureHDInsightAutoscale （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="de4a2-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="de4a2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="de4a2-132">NOTES</span></span>

## <span data-ttu-id="de4a2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="de4a2-133">RELATED LINKS</span></span>

<span data-ttu-id="de4a2-134">[新-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
[移除-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="de4a2-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
