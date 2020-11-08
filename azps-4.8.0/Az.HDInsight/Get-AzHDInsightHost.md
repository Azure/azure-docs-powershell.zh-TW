---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969701"
---
# <span data-ttu-id="dec64-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="dec64-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="dec64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dec64-102">SYNOPSIS</span></span>
<span data-ttu-id="dec64-103">列出 HDInsight 群集的主機。</span><span class="sxs-lookup"><span data-stu-id="dec64-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="dec64-104">句法</span><span class="sxs-lookup"><span data-stu-id="dec64-104">SYNTAX</span></span>

### <span data-ttu-id="dec64-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dec64-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec64-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dec64-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec64-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dec64-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dec64-108">說明</span><span class="sxs-lookup"><span data-stu-id="dec64-108">DESCRIPTION</span></span>
<span data-ttu-id="dec64-109">**AzHDInsightHost** Cmdlet 會列出 HDInsight 群集的主機。</span><span class="sxs-lookup"><span data-stu-id="dec64-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="dec64-110">示例</span><span class="sxs-lookup"><span data-stu-id="dec64-110">EXAMPLES</span></span>

### <span data-ttu-id="dec64-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dec64-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="dec64-112">這個命令清單包含群集名稱的群集主機。</span><span class="sxs-lookup"><span data-stu-id="dec64-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="dec64-113">範例2</span><span class="sxs-lookup"><span data-stu-id="dec64-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="dec64-114">此命令會列出包含管線的群集主機。</span><span class="sxs-lookup"><span data-stu-id="dec64-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="dec64-115">參數</span><span class="sxs-lookup"><span data-stu-id="dec64-115">PARAMETERS</span></span>

### <span data-ttu-id="dec64-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dec64-116">-ClusterName</span></span>
<span data-ttu-id="dec64-117">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="dec64-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="dec64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec64-118">-DefaultProfile</span></span>
<span data-ttu-id="dec64-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dec64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dec64-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dec64-120">-InputObject</span></span>
<span data-ttu-id="dec64-121">取得或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="dec64-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="dec64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec64-122">-ResourceGroupName</span></span>
<span data-ttu-id="dec64-123">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dec64-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="dec64-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dec64-124">-ResourceId</span></span>
<span data-ttu-id="dec64-125">取得或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dec64-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="dec64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec64-126">CommonParameters</span></span>
<span data-ttu-id="dec64-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dec64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec64-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dec64-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec64-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dec64-129">INPUTS</span></span>

### <span data-ttu-id="dec64-130">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="dec64-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="dec64-131">輸出</span><span class="sxs-lookup"><span data-stu-id="dec64-131">OUTPUTS</span></span>

### <span data-ttu-id="dec64-132">AzureHDInsightHostInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dec64-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="dec64-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dec64-133">NOTES</span></span>

## <span data-ttu-id="dec64-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dec64-134">RELATED LINKS</span></span>
