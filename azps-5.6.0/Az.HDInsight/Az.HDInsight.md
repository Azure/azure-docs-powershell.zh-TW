---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: ec924f7424d2b522e6bbd9ce1db51e8c920ec663
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911661"
---
# <span data-ttu-id="a50cd-101">Az.HDInsight 模組</span><span class="sxs-lookup"><span data-stu-id="a50cd-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="a50cd-102">描述</span><span class="sxs-lookup"><span data-stu-id="a50cd-102">Description</span></span>
<span data-ttu-id="a50cd-103">本節主題將說明 Azure Resource Manager (ARM) 架構中的 Microsoft Azure HDInsight Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a50cd-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="a50cd-104">這些 Cmdlet 可用來管理 HDInsight 組群及其上執行的工作。</span><span class="sxs-lookup"><span data-stu-id="a50cd-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="a50cd-105">Cmdlet 存在於 Microsoft.Azure.Commands.HDInsight 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="a50cd-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="a50cd-106">Az.HDInsight Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a50cd-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="a50cd-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="a50cd-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="a50cd-108">新增組群身分識別至組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="a50cd-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="a50cd-110">新增在一組組集中執行之服務的版本至組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="a50cd-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="a50cd-112">新增 Hadoop 組配置值自訂和/或 Hive 共用文件庫自訂至組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="a50cd-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="a50cd-114">新增 SQL 資料庫做為病毒或 Oozie 元庫至組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="a50cd-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="a50cd-116">新增腳本動作至組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="a50cd-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="a50cd-118">新增安全性設定檔至組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a50cd-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="a50cd-120">新增 Azure 儲存體金鑰至組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a50cd-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="a50cd-122">停用 HDInsight 群集中的監控，相關記錄會停止流向啟用期間指定的監控工作區。</span><span class="sxs-lookup"><span data-stu-id="a50cd-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="a50cd-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a50cd-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="a50cd-124">啟用 HDInsight 群集中的監控功能，相關記錄將會送到啟用期間指定的監控工作區。</span><span class="sxs-lookup"><span data-stu-id="a50cd-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="a50cd-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a50cd-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="a50cd-126">獲取並列出與目前訂閱或指定資源群組相關聯的所有 Azure HDInsight 群組，或取回特定的群組。</span><span class="sxs-lookup"><span data-stu-id="a50cd-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="a50cd-127">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a50cd-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a50cd-128">獲得 HDInsight 簇的自動縮放組式組式。</span><span class="sxs-lookup"><span data-stu-id="a50cd-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-129">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="a50cd-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="a50cd-130">列出 HDInsight 集區主機。</span><span class="sxs-lookup"><span data-stu-id="a50cd-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a50cd-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="a50cd-132">從一個工作組獲得工作清單，然後以反時間順序列出工作，或取回特定工作。</span><span class="sxs-lookup"><span data-stu-id="a50cd-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="a50cd-133">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="a50cd-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="a50cd-134">從與指定組群相關聯的儲存空間帳戶，獲得工作的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="a50cd-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="a50cd-135">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a50cd-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="a50cd-136">在組集中獲得監控安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="a50cd-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="a50cd-137">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a50cd-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="a50cd-138">為一個組獲取持續執行腳本動作，並按時間順序列出這些動作，或獲得指定的持續腳本動作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a50cd-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="a50cd-139">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="a50cd-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="a50cd-140">獲得 HDInsight 服務的屬性，例如可用位置和容量。</span><span class="sxs-lookup"><span data-stu-id="a50cd-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="a50cd-141">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="a50cd-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="a50cd-142">獲得該組群的腳本動作歷程記錄，並以反向時間順序列出，或獲得先前執行的腳本動作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a50cd-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="a50cd-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="a50cd-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="a50cd-144">將病毒查詢提交至 HDInsight 集區，並一次作業中取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="a50cd-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="a50cd-145">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a50cd-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="a50cd-146">在目前訂閱的指定資源群組中建立 Azure HDInsight 群組。</span><span class="sxs-lookup"><span data-stu-id="a50cd-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="a50cd-147">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a50cd-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a50cd-148">建立描述 Azure HDInsight 集區之自動縮放設置的非持續物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="a50cd-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="a50cd-150">建立以排程為基礎的自動縮放條件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="a50cd-151">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a50cd-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="a50cd-152">建立描述 Azure HDInsight 集區組配置的非持續型集組組物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="a50cd-153">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a50cd-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="a50cd-154">建立一個病毒工作物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="a50cd-155">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a50cd-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="a50cd-156">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="a50cd-157">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a50cd-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="a50cd-158">建立一個小豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="a50cd-159">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a50cd-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="a50cd-160">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="a50cd-161">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a50cd-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="a50cd-162">建立串流 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="a50cd-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="a50cd-163">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a50cd-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="a50cd-164">從目前的訂閱移除指定的 HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="a50cd-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="a50cd-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a50cd-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a50cd-166">移除 HDInsight 簇的自動縮放組式組式。</span><span class="sxs-lookup"><span data-stu-id="a50cd-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-167">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a50cd-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="a50cd-168">從 HDInsight 集區移除持續腳本動作。</span><span class="sxs-lookup"><span data-stu-id="a50cd-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-169">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="a50cd-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="a50cd-170">重新開機 HDInsight 集區的特定主機。</span><span class="sxs-lookup"><span data-stu-id="a50cd-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a50cd-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="a50cd-172">設定 Azure HDInsight 套件的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a50cd-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-173">Set-AzHDInsightClusterCryptEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a50cd-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="a50cd-174">旋轉指定 HDInsight 集的磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a50cd-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="a50cd-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="a50cd-176">設定指定組集中的工作者節點數目。</span><span class="sxs-lookup"><span data-stu-id="a50cd-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="a50cd-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="a50cd-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="a50cd-178">設定組組設定物件中的預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="a50cd-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="a50cd-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="a50cd-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="a50cd-180">設定 Azure HDInsight 套件的閘道 HTTP 認證。</span><span class="sxs-lookup"><span data-stu-id="a50cd-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a50cd-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="a50cd-182">將先前執行的腳本動作設定為可保存的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="a50cd-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="a50cd-183">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a50cd-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="a50cd-184">在指定的組集中開始已定義的 Azure HDInsight 工作。</span><span class="sxs-lookup"><span data-stu-id="a50cd-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="a50cd-185">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a50cd-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="a50cd-186">停止在一個組上指定的執行中工作。</span><span class="sxs-lookup"><span data-stu-id="a50cd-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="a50cd-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="a50cd-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="a50cd-188">將新的腳本動作提交至 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="a50cd-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="a50cd-189">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a50cd-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="a50cd-190">選取要與 Cmdlet Invoke-RmAzureHDInsightHiveJob組。</span><span class="sxs-lookup"><span data-stu-id="a50cd-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="a50cd-191">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a50cd-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="a50cd-192">等待指定工作的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="a50cd-192">Waits for the completion or failure of a specified job.</span></span>

