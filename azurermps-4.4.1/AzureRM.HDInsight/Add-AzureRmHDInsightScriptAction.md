---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 51bfee17e33afcb93b90c36198e9352c3fca5fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623668"
---
# <span data-ttu-id="7b66e-101">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="7b66e-101">Add-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="7b66e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b66e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b66e-103">在群集設定物件中加入腳本動作。</span><span class="sxs-lookup"><span data-stu-id="7b66e-103">Adds a script action to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b66e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b66e-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b66e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7b66e-105">DESCRIPTION</span></span>
<span data-ttu-id="7b66e-106">**AzureRmHDInsightScriptAction** Cmdlet 會將腳本動作新增至由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="7b66e-106">The **Add-AzureRmHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

<span data-ttu-id="7b66e-107">[腳本動作] 提供的功能可讓您安裝其他軟體或變更在 Hadoop 群集上執行的應用程式的設定，方法是使用 Windows PowerShell 或 Windows 或 Linux 群集 (的 Bash 腳本分別) 。</span><span class="sxs-lookup"><span data-stu-id="7b66e-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>

<span data-ttu-id="7b66e-108">部署 HDInsight 群集時，腳本動作會在叢集節點上執行，而且會在群集中的節點完成 HDInsight 設定之後執行。</span><span class="sxs-lookup"><span data-stu-id="7b66e-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="7b66e-109">[腳本] 動作會以系統管理員帳戶許可權執行，並提供叢集節點的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="7b66e-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="7b66e-110">您可以為每個群集提供一個腳本指令清單，以指定的循序執行。</span><span class="sxs-lookup"><span data-stu-id="7b66e-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="7b66e-111">示例</span><span class="sxs-lookup"><span data-stu-id="7b66e-111">EXAMPLES</span></span>

### <span data-ttu-id="7b66e-112">範例1：將腳本動作新增至群集設定物件</span><span class="sxs-lookup"><span data-stu-id="7b66e-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


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
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="7b66e-113">這個命令會針對您的 hadoop-001 群集的 Head 和 Worker 節點新增一個腳本動作，以便在群集建立結束時執行。</span><span class="sxs-lookup"><span data-stu-id="7b66e-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="7b66e-114">參數</span><span class="sxs-lookup"><span data-stu-id="7b66e-114">PARAMETERS</span></span>

### <span data-ttu-id="7b66e-115">-Config</span><span class="sxs-lookup"><span data-stu-id="7b66e-115">-Config</span></span>
<span data-ttu-id="7b66e-116">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="7b66e-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="7b66e-117">這個物件是由 **新的-AzureRmHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="7b66e-117">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="7b66e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b66e-118">-Name</span></span>
<span data-ttu-id="7b66e-119">指定腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b66e-119">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="7b66e-120">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7b66e-120">-NodeType</span></span>
<span data-ttu-id="7b66e-121">指定要在其上執行腳本動作的節點類型。</span><span class="sxs-lookup"><span data-stu-id="7b66e-121">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="7b66e-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7b66e-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b66e-123">節點</span><span class="sxs-lookup"><span data-stu-id="7b66e-123">HeadNode</span></span>
- <span data-ttu-id="7b66e-124">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="7b66e-124">WorkerNode</span></span>
- <span data-ttu-id="7b66e-125">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="7b66e-125">ZookeeperNode</span></span>

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

### <span data-ttu-id="7b66e-126">-參數</span><span class="sxs-lookup"><span data-stu-id="7b66e-126">-Parameters</span></span>
<span data-ttu-id="7b66e-127">指定腳本動作的參數。</span><span class="sxs-lookup"><span data-stu-id="7b66e-127">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="7b66e-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="7b66e-128">-Uri</span></span>
<span data-ttu-id="7b66e-129">指定 PowerShell 或 Bash 腳本)  (腳本操作的公用 URI。</span><span class="sxs-lookup"><span data-stu-id="7b66e-129">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="7b66e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b66e-130">-DefaultProfile</span></span>
<span data-ttu-id="7b66e-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b66e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b66e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b66e-132">CommonParameters</span></span>
<span data-ttu-id="7b66e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b66e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b66e-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b66e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b66e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7b66e-135">INPUTS</span></span>

### <span data-ttu-id="7b66e-136">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="7b66e-136">AzureHDInsightConfig</span></span>
<span data-ttu-id="7b66e-137">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7b66e-137">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="7b66e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7b66e-138">OUTPUTS</span></span>

### <span data-ttu-id="7b66e-139">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="7b66e-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="7b66e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7b66e-140">NOTES</span></span>

## <span data-ttu-id="7b66e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b66e-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b66e-142">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7b66e-142">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


