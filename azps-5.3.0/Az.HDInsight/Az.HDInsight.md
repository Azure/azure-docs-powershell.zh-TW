---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438328"
---
# <span data-ttu-id="a124f-101">Az （HDInsight）模組</span><span class="sxs-lookup"><span data-stu-id="a124f-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="a124f-102">說明</span><span class="sxs-lookup"><span data-stu-id="a124f-102">Description</span></span>
<span data-ttu-id="a124f-103">本節中的主題檔在 Azure 資源管理器中，將 Microsoft Azure HDInsight 的 Azure PowerShell Cmdlet 記錄在 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="a124f-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="a124f-104">這些 Cmdlet 可用來管理 HDInsight 群集以及在其上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="a124f-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="a124f-105">Cmdlet 存在於 Microsoft Azure. 命令命名空間中。</span><span class="sxs-lookup"><span data-stu-id="a124f-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="a124f-106">Az （HDInsight） Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a124f-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="a124f-107">附加 AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="a124f-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="a124f-108">將群集身分識別新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-109">附加 AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="a124f-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="a124f-110">將在群集中執行的服務的版本新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-111">附加 AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="a124f-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="a124f-112">將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-113">附加 AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="a124f-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="a124f-114">新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-115">附加 AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="a124f-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="a124f-116">在群集設定物件中加入腳本動作。</span><span class="sxs-lookup"><span data-stu-id="a124f-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-117">附加 AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="a124f-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="a124f-118">新增安全設定檔至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-119">附加 AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a124f-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="a124f-120">將 Azure 儲存空間金鑰新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a124f-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="a124f-122">在 HDInsight 群集中停用監視，相關記錄將停止流入至啟用期間指定的監視工作區。</span><span class="sxs-lookup"><span data-stu-id="a124f-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="a124f-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a124f-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="a124f-124">在 HDInsight 群集中啟用監視，並將相關的記錄傳送到 [啟用期間] 指定的監視工作區。</span><span class="sxs-lookup"><span data-stu-id="a124f-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="a124f-125">AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a124f-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="a124f-126">取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。</span><span class="sxs-lookup"><span data-stu-id="a124f-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="a124f-127">AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a124f-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a124f-128">取得 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a124f-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-129">AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="a124f-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="a124f-130">列出 HDInsight 群集的主機。</span><span class="sxs-lookup"><span data-stu-id="a124f-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-131">AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a124f-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="a124f-132">從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。</span><span class="sxs-lookup"><span data-stu-id="a124f-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="a124f-133">AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="a124f-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="a124f-134">從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="a124f-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="a124f-135">AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a124f-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="a124f-136">取得群集上的監視安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="a124f-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="a124f-137">AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a124f-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="a124f-138">取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a124f-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="a124f-139">AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="a124f-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="a124f-140">取得 HDInsight 服務的相關屬性，例如可用的位置和容量。</span><span class="sxs-lookup"><span data-stu-id="a124f-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="a124f-141">AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="a124f-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="a124f-142">取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a124f-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="a124f-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="a124f-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="a124f-144">將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。</span><span class="sxs-lookup"><span data-stu-id="a124f-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="a124f-145">新-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a124f-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="a124f-146">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="a124f-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="a124f-147">新-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a124f-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a124f-148">建立一個描述 Azure HDInsight 群集的自動縮放設定的非持久化物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-149">新-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="a124f-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="a124f-150">建立以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="a124f-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="a124f-151">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a124f-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="a124f-152">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="a124f-153">新-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a124f-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="a124f-154">建立 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="a124f-155">新-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a124f-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="a124f-156">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="a124f-157">新-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a124f-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="a124f-158">建立豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="a124f-159">新-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a124f-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="a124f-160">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="a124f-161">新-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a124f-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="a124f-162">建立流式處理 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a124f-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="a124f-163">移除-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a124f-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="a124f-164">從目前的訂閱中移除指定的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="a124f-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="a124f-165">移除-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a124f-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a124f-166">移除 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a124f-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-167">移除-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a124f-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="a124f-168">從 HDInsight 群集移除持久的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="a124f-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-169">重新開機-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="a124f-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="a124f-170">重新開機 HDInsight 群集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="a124f-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a124f-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a124f-172">設定 Azure HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a124f-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-173">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a124f-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="a124f-174">旋轉指定 HDInsight 群集的磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a124f-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="a124f-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="a124f-176">設定指定群集中的工作人員節點數。</span><span class="sxs-lookup"><span data-stu-id="a124f-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="a124f-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="a124f-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="a124f-178">在群集設定物件中設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="a124f-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="a124f-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="a124f-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="a124f-180">設定 Azure HDInsight 群集的閘道 HTTP 認證。</span><span class="sxs-lookup"><span data-stu-id="a124f-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a124f-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="a124f-182">將先前執行的腳本動作設為持久化的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="a124f-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="a124f-183">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a124f-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="a124f-184">在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="a124f-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="a124f-185">停止 AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a124f-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="a124f-186">在群集上停止指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="a124f-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="a124f-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="a124f-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="a124f-188">將新的腳本指令提交至 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="a124f-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a124f-189">使用-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a124f-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="a124f-190">選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。</span><span class="sxs-lookup"><span data-stu-id="a124f-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="a124f-191">稍候-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a124f-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="a124f-192">等待指定作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="a124f-192">Waits for the completion or failure of a specified job.</span></span>

