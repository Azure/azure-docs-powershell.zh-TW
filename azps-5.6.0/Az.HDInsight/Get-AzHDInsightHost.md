---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916950"
---
# <span data-ttu-id="bd904-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="bd904-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="bd904-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd904-102">SYNOPSIS</span></span>
<span data-ttu-id="bd904-103">列出 HDInsight 集區主機。</span><span class="sxs-lookup"><span data-stu-id="bd904-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="bd904-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd904-104">SYNTAX</span></span>

### <span data-ttu-id="bd904-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd904-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd904-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd904-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd904-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd904-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd904-108">描述</span><span class="sxs-lookup"><span data-stu-id="bd904-108">DESCRIPTION</span></span>
<span data-ttu-id="bd904-109">**Get-AzHDInsightHost** Cmdlet 會列出 HDInsight 組群的主機。</span><span class="sxs-lookup"><span data-stu-id="bd904-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="bd904-110">例子</span><span class="sxs-lookup"><span data-stu-id="bd904-110">EXAMPLES</span></span>

### <span data-ttu-id="bd904-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bd904-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="bd904-112">此命令清單包含組名的組主機。</span><span class="sxs-lookup"><span data-stu-id="bd904-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="bd904-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bd904-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="bd904-114">此命令清單列出具有管線的集區主機。</span><span class="sxs-lookup"><span data-stu-id="bd904-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="bd904-115">參數</span><span class="sxs-lookup"><span data-stu-id="bd904-115">PARAMETERS</span></span>

### <span data-ttu-id="bd904-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bd904-116">-ClusterName</span></span>
<span data-ttu-id="bd904-117">獲取或設定組名。</span><span class="sxs-lookup"><span data-stu-id="bd904-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd904-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd904-118">-DefaultProfile</span></span>
<span data-ttu-id="bd904-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd904-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd904-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd904-120">-InputObject</span></span>
<span data-ttu-id="bd904-121">獲取或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="bd904-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd904-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd904-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd904-123">獲取或設定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd904-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd904-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd904-124">-ResourceId</span></span>
<span data-ttu-id="bd904-125">獲取或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd904-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd904-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd904-126">CommonParameters</span></span>
<span data-ttu-id="bd904-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd904-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd904-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd904-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd904-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bd904-129">INPUTS</span></span>

### <span data-ttu-id="bd904-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bd904-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="bd904-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bd904-131">OUTPUTS</span></span>

### <span data-ttu-id="bd904-132">Microsoft.Azure.Commands.HDInsight.models.management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="bd904-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="bd904-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bd904-133">NOTES</span></span>

## <span data-ttu-id="bd904-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd904-134">RELATED LINKS</span></span>
