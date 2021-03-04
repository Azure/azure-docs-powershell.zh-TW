---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: c9b95a1f16c90eb3c6e057707dbf63d431b9a1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917310"
---
# <span data-ttu-id="f03c5-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f03c5-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="f03c5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f03c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f03c5-103">選取要與 Cmdlet Invoke-RmAzureHDInsightHiveJob組。</span><span class="sxs-lookup"><span data-stu-id="f03c5-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="f03c5-104">語法</span><span class="sxs-lookup"><span data-stu-id="f03c5-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f03c5-105">描述</span><span class="sxs-lookup"><span data-stu-id="f03c5-105">DESCRIPTION</span></span>
<span data-ttu-id="f03c5-106">**Use-AzHDInsightCluster** Cmdlet 會選取 Invoke-AzHDInsightHiveJob Cmdlet 的 Azure HDInsight 叢集，以用於提交 Hive 工作。</span><span class="sxs-lookup"><span data-stu-id="f03c5-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="f03c5-107">例子</span><span class="sxs-lookup"><span data-stu-id="f03c5-107">EXAMPLES</span></span>

### <span data-ttu-id="f03c5-108">範例 1：選取適用于 Hive 查詢提交的組</span><span class="sxs-lookup"><span data-stu-id="f03c5-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f03c5-109">此命令會選取要提交病毒查詢的一個組。</span><span class="sxs-lookup"><span data-stu-id="f03c5-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="f03c5-110">參數</span><span class="sxs-lookup"><span data-stu-id="f03c5-110">PARAMETERS</span></span>

### <span data-ttu-id="f03c5-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f03c5-111">-ClusterName</span></span>
<span data-ttu-id="f03c5-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="f03c5-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03c5-113">-DefaultProfile</span></span>
<span data-ttu-id="f03c5-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f03c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f03c5-115">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="f03c5-115">-HttpCredential</span></span>
<span data-ttu-id="f03c5-116">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="f03c5-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="f03c5-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f03c5-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03c5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03c5-119">CommonParameters</span></span>
<span data-ttu-id="f03c5-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f03c5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03c5-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f03c5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03c5-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f03c5-122">INPUTS</span></span>

### <span data-ttu-id="f03c5-123">沒有</span><span class="sxs-lookup"><span data-stu-id="f03c5-123">None</span></span>

## <span data-ttu-id="f03c5-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f03c5-124">OUTPUTS</span></span>

### <span data-ttu-id="f03c5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f03c5-125">System.String</span></span>

## <span data-ttu-id="f03c5-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f03c5-126">NOTES</span></span>

## <span data-ttu-id="f03c5-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f03c5-127">RELATED LINKS</span></span>

[<span data-ttu-id="f03c5-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f03c5-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="f03c5-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f03c5-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


