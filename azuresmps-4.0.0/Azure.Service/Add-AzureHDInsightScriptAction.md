---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967166"
---
# <span data-ttu-id="11300-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="11300-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="11300-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11300-102">SYNOPSIS</span></span>
<span data-ttu-id="11300-103">新增 HDInsight 腳本動作。</span><span class="sxs-lookup"><span data-stu-id="11300-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="11300-104">句法</span><span class="sxs-lookup"><span data-stu-id="11300-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="11300-105">說明</span><span class="sxs-lookup"><span data-stu-id="11300-105">DESCRIPTION</span></span>
<span data-ttu-id="11300-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="11300-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="11300-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="11300-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="11300-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="11300-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="11300-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="11300-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="11300-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="11300-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="11300-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="11300-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="11300-112">**AzureHDInsightScriptAction** Cmdlet 提供 Azure HDInsight 功能，可用於安裝其他軟體，或使用 Windows PowerShell 腳本來變更在 Hadoop 群集上執行的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="11300-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="11300-113">部署 HDInsight 群集時，腳本動作會在叢集節點上執行，而且會在群集中的節點完成 HDInsight 設定之後執行。</span><span class="sxs-lookup"><span data-stu-id="11300-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="11300-114">[腳本] 動作會以系統管理員帳戶許可權執行，並提供叢集節點的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="11300-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="11300-115">您可以為每個群集提供一個腳本指令清單，以指定的循序執行。</span><span class="sxs-lookup"><span data-stu-id="11300-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="11300-116">示例</span><span class="sxs-lookup"><span data-stu-id="11300-116">EXAMPLES</span></span>

### <span data-ttu-id="11300-117">範例1：在群集中加入腳本動作</span><span class="sxs-lookup"><span data-stu-id="11300-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="11300-118">第一個命令使用 **新的 AzureHDInsightClusterConfig** Cmdlet 來建立 HDInsight 群集設定，然後將它儲存在 $Config 變數中。</span><span class="sxs-lookup"><span data-stu-id="11300-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="11300-119">第二個命令使用 **AzureHDInsightScriptAction** Cmdlet，以將名為 TestScriptAction 的腳本動作新增至 $Config。</span><span class="sxs-lookup"><span data-stu-id="11300-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="11300-120">最後一個命令會使用 **AzureHDInsightCluster** Cmdlet 來建立新的 HDInsight 群集，該群集會執行儲存在 $Config 中的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="11300-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="11300-121">範例2：在群集中新增多個腳本動作</span><span class="sxs-lookup"><span data-stu-id="11300-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="11300-122">第一個命令使用 **新的 AzureHDInsightClusterConfig** Cmdlet 來建立 HDInsight 群集設定，然後將它儲存在 $Config 變數中。</span><span class="sxs-lookup"><span data-stu-id="11300-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="11300-123">第二個命令會使用 **AzureHDInsightScriptAction** Cmdlet，將指定的腳本動作新增至 $Config，然後使用管線 $Config 運算子，將第二個 **腳本動作新增** 至 $Config。</span><span class="sxs-lookup"><span data-stu-id="11300-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="11300-124">最終命令會使用 **AzureHDInsightCluster** Cmdlet 來建立在 $Config 中執行腳本動作的群集。</span><span class="sxs-lookup"><span data-stu-id="11300-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="11300-125">參數</span><span class="sxs-lookup"><span data-stu-id="11300-125">PARAMETERS</span></span>

### <span data-ttu-id="11300-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="11300-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="11300-127">指定要執行腳本的節點。</span><span class="sxs-lookup"><span data-stu-id="11300-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="11300-128">此參數可接受的值為： [頭節點] 或 [DataNode]。</span><span class="sxs-lookup"><span data-stu-id="11300-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="11300-129">您可以指定一個值或兩個值。</span><span class="sxs-lookup"><span data-stu-id="11300-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11300-130">-Config</span><span class="sxs-lookup"><span data-stu-id="11300-130">-Config</span></span>
<span data-ttu-id="11300-131">指定 [配置] 物件。</span><span class="sxs-lookup"><span data-stu-id="11300-131">Specifies a configuration object.</span></span>
<span data-ttu-id="11300-132">這個 Cmdlet 會將腳本動作資訊新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="11300-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11300-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="11300-133">-Name</span></span>
<span data-ttu-id="11300-134">指定腳本動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="11300-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11300-135">-參數</span><span class="sxs-lookup"><span data-stu-id="11300-135">-Parameters</span></span>
<span data-ttu-id="11300-136">指定腳本動作所需的參數。</span><span class="sxs-lookup"><span data-stu-id="11300-136">Specifies the parameters that are required by a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11300-137">-設定檔</span><span class="sxs-lookup"><span data-stu-id="11300-137">-Profile</span></span>
<span data-ttu-id="11300-138">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="11300-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11300-139">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="11300-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11300-140">-Uri</span><span class="sxs-lookup"><span data-stu-id="11300-140">-Uri</span></span>
<span data-ttu-id="11300-141">指定要執行的腳本的 URI 位置。</span><span class="sxs-lookup"><span data-stu-id="11300-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11300-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11300-142">CommonParameters</span></span>
<span data-ttu-id="11300-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11300-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11300-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11300-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11300-145">輸入</span><span class="sxs-lookup"><span data-stu-id="11300-145">INPUTS</span></span>

## <span data-ttu-id="11300-146">輸出</span><span class="sxs-lookup"><span data-stu-id="11300-146">OUTPUTS</span></span>

## <span data-ttu-id="11300-147">筆記</span><span class="sxs-lookup"><span data-stu-id="11300-147">NOTES</span></span>

## <span data-ttu-id="11300-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="11300-148">RELATED LINKS</span></span>

[<span data-ttu-id="11300-149">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="11300-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="11300-150">新-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="11300-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


