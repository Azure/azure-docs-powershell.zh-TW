---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: bbbb418a8e101fa1b806bc910132f44e40158190
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441860"
---
# <span data-ttu-id="9ea2f-101">AzureRM （HDInsight）模組</span><span class="sxs-lookup"><span data-stu-id="9ea2f-101">AzureRM.HDInsight Module</span></span>
## <span data-ttu-id="9ea2f-102">說明</span><span class="sxs-lookup"><span data-stu-id="9ea2f-102">Description</span></span>
<span data-ttu-id="9ea2f-103">本節中的主題檔在 Azure 資源管理器中，將 Microsoft Azure HDInsight 的 Azure PowerShell Cmdlet 記錄在 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="9ea2f-104">這些 Cmdlet 可用來管理 HDInsight 群集以及在其上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="9ea2f-105">Cmdlet 存在於 Microsoft Azure. 命令命名空間中。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="9ea2f-106">AzureRM （HDInsight） Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ea2f-106">AzureRM.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="9ea2f-107">附加 AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="9ea2f-107">Add-AzureRmHDInsightClusterIdentity</span></span>](Add-AzureRmHDInsightClusterIdentity.md)
<span data-ttu-id="9ea2f-108">將群集身分識別新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-109">附加 AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="9ea2f-109">Add-AzureRmHDInsightComponentVersion</span></span>](Add-AzureRmHDInsightComponentVersion.md)
<span data-ttu-id="9ea2f-110">將在群集中執行的服務的版本新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-111">附加 AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="9ea2f-111">Add-AzureRmHDInsightConfigValues</span></span>](Add-AzureRmHDInsightConfigValues.md)
<span data-ttu-id="9ea2f-112">將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-113">附加 AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="9ea2f-113">Add-AzureRmHDInsightMetastore</span></span>](Add-AzureRmHDInsightMetastore.md)
<span data-ttu-id="9ea2f-114">新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-115">附加 AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="9ea2f-115">Add-AzureRmHDInsightScriptAction</span></span>](Add-AzureRmHDInsightScriptAction.md)
<span data-ttu-id="9ea2f-116">在群集設定物件中加入腳本動作。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-117">附加 AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="9ea2f-117">Add-AzureRmHDInsightSecurityProfile</span></span>](Add-AzureRmHDInsightSecurityProfile.md)
<span data-ttu-id="9ea2f-118">在群集設定物件中新增安全性 profileto。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-118">Adds a security profileto a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-119">附加 AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="9ea2f-119">Add-AzureRmHDInsightStorage</span></span>](Add-AzureRmHDInsightStorage.md)
<span data-ttu-id="9ea2f-120">將 Azure 儲存空間金鑰新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-121">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9ea2f-121">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>](Disable-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="9ea2f-122">在 HDInsight 群集中停用作業管理套件 (OMS) ，而相關的記錄將停止流入在啟用期間指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-122">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="9ea2f-123">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9ea2f-123">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>](Enable-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="9ea2f-124">在 HDInsight 群集中啟用操作管理套件 (OMS) ，而相關的記錄將會傳送到 enable 中指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-124">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="9ea2f-125">AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9ea2f-125">Get-AzureRmHDInsightCluster</span></span>](Get-AzureRmHDInsightCluster.md)
<span data-ttu-id="9ea2f-126">取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="9ea2f-127">AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ea2f-127">Get-AzureRmHDInsightJob</span></span>](Get-AzureRmHDInsightJob.md)
<span data-ttu-id="9ea2f-128">從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="9ea2f-129">AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="9ea2f-129">Get-AzureRmHDInsightJobOutput</span></span>](Get-AzureRmHDInsightJobOutput.md)
<span data-ttu-id="9ea2f-130">從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="9ea2f-131">AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9ea2f-131">Get-AzureRmHDInsightOperationsManagementSuite</span></span>](Get-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="9ea2f-132">取得群集上 (OMS) 安裝的 Operations Management Suite 狀態。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-132">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

### [<span data-ttu-id="9ea2f-133">AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9ea2f-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](Get-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="9ea2f-134">取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="9ea2f-135">AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="9ea2f-135">Get-AzureRmHDInsightProperties</span></span>](Get-AzureRmHDInsightProperties.md)
<span data-ttu-id="9ea2f-136">取得 HDInsight 服務的相關屬性，例如可用的位置和容量。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="9ea2f-137">AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="9ea2f-137">Get-AzureRmHDInsightScriptActionHistory</span></span>](Get-AzureRmHDInsightScriptActionHistory.md)
<span data-ttu-id="9ea2f-138">取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="9ea2f-139">授與 AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9ea2f-139">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](Grant-AzureRmHDInsightHttpServicesAccess.md)
<span data-ttu-id="9ea2f-140">授權 HTTP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-140">Grants HTTP access to the cluster.</span></span>

### [<span data-ttu-id="9ea2f-141">授與 AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9ea2f-141">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](Grant-AzureRmHDInsightRdpServicesAccess.md)
<span data-ttu-id="9ea2f-142">授與 Windows 群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-142">Grants RDP access to the Windows cluster.</span></span>

### [<span data-ttu-id="9ea2f-143">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="9ea2f-143">Invoke-AzureRmHDInsightHiveJob</span></span>](Invoke-AzureRmHDInsightHiveJob.md)
<span data-ttu-id="9ea2f-144">將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="9ea2f-145">新-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9ea2f-145">New-AzureRmHDInsightCluster</span></span>](New-AzureRmHDInsightCluster.md)
<span data-ttu-id="9ea2f-146">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="9ea2f-147">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9ea2f-147">New-AzureRmHDInsightClusterConfig</span></span>](New-AzureRmHDInsightClusterConfig.md)
<span data-ttu-id="9ea2f-148">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-148">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="9ea2f-149">新-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9ea2f-149">New-AzureRmHDInsightHiveJobDefinition</span></span>](New-AzureRmHDInsightHiveJobDefinition.md)
<span data-ttu-id="9ea2f-150">建立 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-150">Creates a Hive job object.</span></span>

### [<span data-ttu-id="9ea2f-151">新-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9ea2f-151">New-AzureRmHDInsightMapReduceJobDefinition</span></span>](New-AzureRmHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="9ea2f-152">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-152">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="9ea2f-153">新-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9ea2f-153">New-AzureRmHDInsightPigJobDefinition</span></span>](New-AzureRmHDInsightPigJobDefinition.md)
<span data-ttu-id="9ea2f-154">建立豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-154">Creates a Pig job object.</span></span>

### [<span data-ttu-id="9ea2f-155">新-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9ea2f-155">New-AzureRmHDInsightSqoopJobDefinition</span></span>](New-AzureRmHDInsightSqoopJobDefinition.md)
<span data-ttu-id="9ea2f-156">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-156">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="9ea2f-157">新-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9ea2f-157">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="9ea2f-158">建立流式處理 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-158">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="9ea2f-159">移除-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9ea2f-159">Remove-AzureRmHDInsightCluster</span></span>](Remove-AzureRmHDInsightCluster.md)
<span data-ttu-id="9ea2f-160">從目前的訂閱中移除指定的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-160">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="9ea2f-161">移除-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9ea2f-161">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](Remove-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="9ea2f-162">從 HDInsight 群集移除持久的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-162">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="9ea2f-163">吊銷-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9ea2f-163">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](Revoke-AzureRmHDInsightHttpServicesAccess.md)
<span data-ttu-id="9ea2f-164">停用 HTTP 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-164">Disables HTTP access to the cluster.</span></span>

### [<span data-ttu-id="9ea2f-165">吊銷-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9ea2f-165">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](Revoke-AzureRmHDInsightRdpServicesAccess.md)
<span data-ttu-id="9ea2f-166">停用 RDP 對 Windows 群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-166">Disables RDP access to a Windows cluster.</span></span>

### [<span data-ttu-id="9ea2f-167">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="9ea2f-167">Set-AzureRmHDInsightClusterSize</span></span>](Set-AzureRmHDInsightClusterSize.md)
<span data-ttu-id="9ea2f-168">設定指定群集中的工作人員節點數。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-168">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="9ea2f-169">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="9ea2f-169">Set-AzureRmHDInsightDefaultStorage</span></span>](Set-AzureRmHDInsightDefaultStorage.md)
<span data-ttu-id="9ea2f-170">在群集設定物件中設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-170">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="9ea2f-171">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9ea2f-171">Set-AzureRmHDInsightPersistedScriptAction</span></span>](Set-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="9ea2f-172">將先前執行的腳本動作設為持久化的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-172">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="9ea2f-173">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ea2f-173">Start-AzureRmHDInsightJob</span></span>](Start-AzureRmHDInsightJob.md)
<span data-ttu-id="9ea2f-174">在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-174">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="9ea2f-175">停止 AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ea2f-175">Stop-AzureRmHDInsightJob</span></span>](Stop-AzureRmHDInsightJob.md)
<span data-ttu-id="9ea2f-176">在群集上停止指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-176">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="9ea2f-177">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="9ea2f-177">Submit-AzureRmHDInsightScriptAction</span></span>](Submit-AzureRmHDInsightScriptAction.md)
<span data-ttu-id="9ea2f-178">將新的腳本指令提交至 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-178">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="9ea2f-179">使用-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9ea2f-179">Use-AzureRmHDInsightCluster</span></span>](Use-AzureRmHDInsightCluster.md)
<span data-ttu-id="9ea2f-180">選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-180">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="9ea2f-181">稍候-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ea2f-181">Wait-AzureRmHDInsightJob</span></span>](Wait-AzureRmHDInsightJob.md)
<span data-ttu-id="9ea2f-182">等待指定作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="9ea2f-182">Waits for the completion or failure of a specified job.</span></span>

