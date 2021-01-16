---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283952"
---
# Az （HDInsight）模組
## 說明
本節中的主題檔在 Azure 資源管理器中，將 Microsoft Azure HDInsight 的 Azure PowerShell Cmdlet 記錄在 (ARM) 架構中。 這些 Cmdlet 可用來管理 HDInsight 群集以及在其上執行的作業。 Cmdlet 存在於 Microsoft Azure. 命令命名空間中。

## Az （HDInsight） Cmdlet
### [附加 AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
將群集身分識別新增至群集設定物件。

### [附加 AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
將在群集中執行的服務的版本新增至群集設定物件。

### [附加 AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。

### [附加 AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。

### [附加 AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
在群集設定物件中加入腳本動作。

### [附加 AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
新增安全設定檔至群集設定物件。

### [附加 AzHDInsightStorage](Add-AzHDInsightStorage.md)
將 Azure 儲存空間金鑰新增至群集設定物件。

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
在 HDInsight 群集中停用監視，相關記錄將停止流入至啟用期間指定的監視工作區。

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
在 HDInsight 群集中啟用監視，並將相關的記錄傳送到 [啟用期間] 指定的監視工作區。

### [AzHDInsightCluster](Get-AzHDInsightCluster.md)
取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。

### [AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
取得 HDInsight 群集的自動縮放設定。

### [AzHDInsightHost](Get-AzHDInsightHost.md)
列出 HDInsight 群集的主機。

### [AzHDInsightJob](Get-AzHDInsightJob.md)
從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。

### [AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。

### [AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
取得群集上的監視安裝狀態。

### [AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。

### [AzHDInsightProperty](Get-AzHDInsightProperty.md)
取得 HDInsight 服務的相關屬性，例如可用的位置和容量。

### [AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。

### [新-AzHDInsightCluster](New-AzHDInsightCluster.md)
在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。

### [新-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
建立一個描述 Azure HDInsight 群集的自動縮放設定的非持久化物件。

### [新-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
建立以排程為基礎的自動縮放條件。

### [新-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。

### [新-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
建立 Hive 工作物件。

### [新-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
建立 MapReduce 工作物件。

### [新-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
建立豬工作物件。

### [新-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
建立 Sqoop 工作物件。

### [新-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
建立流式處理 MapReduce 工作物件。

### [移除-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
從目前的訂閱中移除指定的 HDInsight 群集。

### [移除-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
移除 HDInsight 群集的自動縮放設定。

### [移除-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
從 HDInsight 群集移除持久的腳本動作。

### [重新開機-AzHDInsightHost](Restart-AzHDInsightHost.md)
重新開機 HDInsight 群集的特定主機。

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
設定 Azure HDInsight 群集的自動縮放設定。

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
旋轉指定 HDInsight 群集的磁片加密金鑰。

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
設定指定群集中的工作人員節點數。

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
在群集設定物件中設定預設儲存空間帳戶設定。

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
設定 Azure HDInsight 群集的閘道 HTTP 認證。

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
將先前執行的腳本動作設為持久化的腳本動作。

### [開始-AzHDInsightJob](Start-AzHDInsightJob.md)
在指定的群集上啟動已定義的 Azure HDInsight 作業。

### [停止 AzHDInsightJob](Stop-AzHDInsightJob.md)
在群集上停止指定的執行作業。

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
將新的腳本指令提交至 Azure HDInsight 群集。

### [使用-AzHDInsightCluster](Use-AzHDInsightCluster.md)
選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。

### [稍候-AzHDInsightJob](Wait-AzHDInsightJob.md)
等待指定作業的完成或失敗。

