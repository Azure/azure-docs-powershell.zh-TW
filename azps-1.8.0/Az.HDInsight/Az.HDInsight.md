---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 78153558764d12a63d6c1b599da2067338969628
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611342"
---
# <span data-ttu-id="29047-101">Az （HDInsight）模組</span><span class="sxs-lookup"><span data-stu-id="29047-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="29047-102">說明</span><span class="sxs-lookup"><span data-stu-id="29047-102">Description</span></span>
<span data-ttu-id="29047-103">本節中的主題檔在 Azure 資源管理器中，將 Microsoft Azure HDInsight 的 Azure PowerShell Cmdlet 記錄在 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="29047-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="29047-104">這些 Cmdlet 可用來管理 HDInsight 群集以及在其上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="29047-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="29047-105">Cmdlet 存在於 Microsoft Azure. 命令命名空間中。</span><span class="sxs-lookup"><span data-stu-id="29047-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="29047-106">Az （HDInsight） Cmdlet</span><span class="sxs-lookup"><span data-stu-id="29047-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="29047-107">附加 AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="29047-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="29047-108">將群集身分識別新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="29047-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-109">附加 AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="29047-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="29047-110">將在群集中執行的服務的版本新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="29047-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-111">附加 AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="29047-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="29047-112">將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="29047-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-113">附加 AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="29047-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="29047-114">新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="29047-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-115">附加 AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="29047-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="29047-116">在群集設定物件中加入腳本動作。</span><span class="sxs-lookup"><span data-stu-id="29047-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-117">附加 AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="29047-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="29047-118">在群集設定物件中新增安全性 profileto。</span><span class="sxs-lookup"><span data-stu-id="29047-118">Adds a security profileto a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-119">附加 AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="29047-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="29047-120">將 Azure 儲存空間金鑰新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="29047-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-121">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="29047-121">Disable-AzHDInsightOperationsManagementSuite</span></span>](Disable-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="29047-122">在 HDInsight 群集中停用作業管理套件 (OMS) ，而相關的記錄將停止流入在啟用期間指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="29047-122">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="29047-123">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="29047-123">Enable-AzHDInsightOperationsManagementSuite</span></span>](Enable-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="29047-124">在 HDInsight 群集中啟用操作管理套件 (OMS) ，而相關的記錄將會傳送到 enable 中指定的 OMS 工作區。</span><span class="sxs-lookup"><span data-stu-id="29047-124">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="29047-125">AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29047-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="29047-126">取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。</span><span class="sxs-lookup"><span data-stu-id="29047-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="29047-127">AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="29047-127">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="29047-128">從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。</span><span class="sxs-lookup"><span data-stu-id="29047-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="29047-129">AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="29047-129">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="29047-130">從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="29047-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="29047-131">AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="29047-131">Get-AzHDInsightOperationsManagementSuite</span></span>](Get-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="29047-132">取得群集上 (OMS) 安裝的 Operations Management Suite 狀態。</span><span class="sxs-lookup"><span data-stu-id="29047-132">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

### [<span data-ttu-id="29047-133">AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="29047-133">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="29047-134">取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="29047-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="29047-135">AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="29047-135">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="29047-136">取得 HDInsight 服務的相關屬性，例如可用的位置和容量。</span><span class="sxs-lookup"><span data-stu-id="29047-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="29047-137">AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="29047-137">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="29047-138">取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="29047-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="29047-139">授與 AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="29047-139">Grant-AzHDInsightHttpServicesAccess</span></span>](Grant-AzHDInsightHttpServicesAccess.md)
<span data-ttu-id="29047-140">授權 HTTP 存取群集。</span><span class="sxs-lookup"><span data-stu-id="29047-140">Grants HTTP access to the cluster.</span></span>

### [<span data-ttu-id="29047-141">授與 AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="29047-141">Grant-AzHDInsightRdpServicesAccess</span></span>](Grant-AzHDInsightRdpServicesAccess.md)
<span data-ttu-id="29047-142">授與 Windows 群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="29047-142">Grants RDP access to the Windows cluster.</span></span>

### [<span data-ttu-id="29047-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="29047-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="29047-144">將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。</span><span class="sxs-lookup"><span data-stu-id="29047-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="29047-145">新-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29047-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="29047-146">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="29047-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="29047-147">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="29047-147">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="29047-148">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="29047-148">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="29047-149">新-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="29047-149">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="29047-150">建立 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="29047-150">Creates a Hive job object.</span></span>

### [<span data-ttu-id="29047-151">新-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="29047-151">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="29047-152">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="29047-152">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="29047-153">新-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="29047-153">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="29047-154">建立豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="29047-154">Creates a Pig job object.</span></span>

### [<span data-ttu-id="29047-155">新-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="29047-155">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="29047-156">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="29047-156">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="29047-157">新-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="29047-157">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="29047-158">建立流式處理 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="29047-158">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="29047-159">移除-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29047-159">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="29047-160">從目前的訂閱中移除指定的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="29047-160">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="29047-161">移除-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="29047-161">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="29047-162">從 HDInsight 群集移除持久的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="29047-162">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="29047-163">吊銷-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="29047-163">Revoke-AzHDInsightHttpServicesAccess</span></span>](Revoke-AzHDInsightHttpServicesAccess.md)
<span data-ttu-id="29047-164">停用 HTTP 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="29047-164">Disables HTTP access to the cluster.</span></span>

### [<span data-ttu-id="29047-165">吊銷-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="29047-165">Revoke-AzHDInsightRdpServicesAccess</span></span>](Revoke-AzHDInsightRdpServicesAccess.md)
<span data-ttu-id="29047-166">停用 RDP 對 Windows 群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="29047-166">Disables RDP access to a Windows cluster.</span></span>

### [<span data-ttu-id="29047-167">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="29047-167">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="29047-168">設定指定群集中的工作人員節點數。</span><span class="sxs-lookup"><span data-stu-id="29047-168">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="29047-169">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="29047-169">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="29047-170">在群集設定物件中設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="29047-170">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="29047-171">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="29047-171">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="29047-172">將先前執行的腳本動作設為持久化的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="29047-172">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="29047-173">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="29047-173">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="29047-174">在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="29047-174">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="29047-175">停止 AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="29047-175">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="29047-176">在群集上停止指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="29047-176">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="29047-177">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="29047-177">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="29047-178">將新的腳本指令提交至 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="29047-178">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="29047-179">使用-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29047-179">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="29047-180">選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。</span><span class="sxs-lookup"><span data-stu-id="29047-180">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="29047-181">稍候-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="29047-181">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="29047-182">等待指定作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="29047-182">Waits for the completion or failure of a specified job.</span></span>

