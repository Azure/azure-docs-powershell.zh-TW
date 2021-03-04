---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: f80ac8dda086910cf83e1d010f2878b6e4ba9362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911669"
---
# <span data-ttu-id="3cb83-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="3cb83-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="3cb83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3cb83-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb83-103">新增腳本動作至組組物件。</span><span class="sxs-lookup"><span data-stu-id="3cb83-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="3cb83-104">語法</span><span class="sxs-lookup"><span data-stu-id="3cb83-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cb83-105">描述</span><span class="sxs-lookup"><span data-stu-id="3cb83-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb83-106">**Add-AzHDInsightScriptAction** Cmdlet 會新增腳本動作至由 New-AzHDInsightClusterConfig 建立 HDInsight 組組物件。</span><span class="sxs-lookup"><span data-stu-id="3cb83-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="3cb83-107">腳本動作提供的功能可用來安裝其他軟體，或變更在 Hadoop cluster 上執行的應用程式組式，其使用 Windows PowerShell 或 Bash 腳本 (分別適用于 Windows 或 Linux) 。</span><span class="sxs-lookup"><span data-stu-id="3cb83-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="3cb83-108">部署 HDInsight 組組時，腳本動作會于該組節點上執行，而且會以完成 HDInsight 配置的節點執行。</span><span class="sxs-lookup"><span data-stu-id="3cb83-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="3cb83-109">腳本動作會以系統管理員帳戶許可權執行，並提供組節點的完整存取權限。</span><span class="sxs-lookup"><span data-stu-id="3cb83-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="3cb83-110">您可以提供每一組腳本動作清單，以指定的循序執行。</span><span class="sxs-lookup"><span data-stu-id="3cb83-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="3cb83-111">例子</span><span class="sxs-lookup"><span data-stu-id="3cb83-111">EXAMPLES</span></span>

### <span data-ttu-id="3cb83-112">範例 1：新增腳本動作至組組物件</span><span class="sxs-lookup"><span data-stu-id="3cb83-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="3cb83-113">此命令會為您的 hadoop-001 集的 Head 和 Worker 節點新增腳本動作，以在建立集區結束時執行。</span><span class="sxs-lookup"><span data-stu-id="3cb83-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="3cb83-114">參數</span><span class="sxs-lookup"><span data-stu-id="3cb83-114">PARAMETERS</span></span>

### <span data-ttu-id="3cb83-115">-Config</span><span class="sxs-lookup"><span data-stu-id="3cb83-115">-Config</span></span>
<span data-ttu-id="3cb83-116">指定此 Cmdlet 修改的 HDInsight 集區組物件。</span><span class="sxs-lookup"><span data-stu-id="3cb83-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3cb83-117">此物件是由 **New-AzHDInsightClusterConfig** Cmdlet 所建立。</span><span class="sxs-lookup"><span data-stu-id="3cb83-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb83-118">-DefaultProfile</span></span>
<span data-ttu-id="3cb83-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb83-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cb83-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cb83-120">-Name</span></span>
<span data-ttu-id="3cb83-121">指定腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cb83-121">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb83-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="3cb83-122">-NodeType</span></span>
<span data-ttu-id="3cb83-123">指定執行腳本動作的節點類型。</span><span class="sxs-lookup"><span data-stu-id="3cb83-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="3cb83-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3cb83-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3cb83-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="3cb83-125">HeadNode</span></span>
- <span data-ttu-id="3cb83-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="3cb83-126">WorkerNode</span></span>
- <span data-ttu-id="3cb83-127">KeeperkeeperNode</span><span class="sxs-lookup"><span data-stu-id="3cb83-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb83-128">-參數</span><span class="sxs-lookup"><span data-stu-id="3cb83-128">-Parameters</span></span>
<span data-ttu-id="3cb83-129">指定腳本動作的參數。</span><span class="sxs-lookup"><span data-stu-id="3cb83-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb83-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="3cb83-130">-Uri</span></span>
<span data-ttu-id="3cb83-131">指定 PowerShell 或 Bash 腳本 (腳本動作的公用 URI) 。</span><span class="sxs-lookup"><span data-stu-id="3cb83-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb83-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb83-132">CommonParameters</span></span>
<span data-ttu-id="3cb83-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3cb83-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb83-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cb83-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb83-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3cb83-135">INPUTS</span></span>

### <span data-ttu-id="3cb83-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3cb83-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3cb83-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3cb83-137">OUTPUTS</span></span>

### <span data-ttu-id="3cb83-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3cb83-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3cb83-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3cb83-139">NOTES</span></span>

## <span data-ttu-id="3cb83-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cb83-140">RELATED LINKS</span></span>

[<span data-ttu-id="3cb83-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3cb83-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


