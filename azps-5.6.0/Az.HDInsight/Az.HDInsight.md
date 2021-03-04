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
# Az.HDInsight 模組
## 描述
本節主題將說明 Azure Resource Manager (ARM) 架構中的 Microsoft Azure HDInsight Cmdlet。 這些 Cmdlet 可用來管理 HDInsight 組群及其上執行的工作。 Cmdlet 存在於 Microsoft.Azure.Commands.HDInsight 命名空間中。

## Az.HDInsight Cmdlet
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
新增組群身分識別至組組物件。

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
新增在一組組集中執行之服務的版本至組組物件。

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
新增 Hadoop 組配置值自訂和/或 Hive 共用文件庫自訂至組組物件。

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
新增 SQL 資料庫做為病毒或 Oozie 元庫至組物件。

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
新增腳本動作至組組物件。

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
新增安全性設定檔至組組物件。

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
新增 Azure 儲存體金鑰至組組物件。

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
停用 HDInsight 群集中的監控，相關記錄會停止流向啟用期間指定的監控工作區。

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
啟用 HDInsight 群集中的監控功能，相關記錄將會送到啟用期間指定的監控工作區。

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
獲取並列出與目前訂閱或指定資源群組相關聯的所有 Azure HDInsight 群組，或取回特定的群組。

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
獲得 HDInsight 簇的自動縮放組式組式。

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
列出 HDInsight 集區主機。

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
從一個工作組獲得工作清單，然後以反時間順序列出工作，或取回特定工作。

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
從與指定組群相關聯的儲存空間帳戶，獲得工作的記錄輸出。

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
在組集中獲得監控安裝的狀態。

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
為一個組獲取持續執行腳本動作，並按時間順序列出這些動作，或獲得指定的持續腳本動作詳細資料。

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
獲得 HDInsight 服務的屬性，例如可用位置和容量。

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
獲得該組群的腳本動作歷程記錄，並以反向時間順序列出，或獲得先前執行的腳本動作詳細資料。

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
將病毒查詢提交至 HDInsight 集區，並一次作業中取得查詢結果。

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
在目前訂閱的指定資源群組中建立 Azure HDInsight 群組。

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
建立描述 Azure HDInsight 集區之自動縮放設置的非持續物件。

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
建立以排程為基礎的自動縮放條件。

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
建立描述 Azure HDInsight 集區組配置的非持續型集組組物件。

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
建立一個病毒工作物件。

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
建立 MapReduce 工作物件。

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
建立一個小豬工作物件。

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
建立 Sqoop 工作物件。

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
建立串流 MapReduce 工作物件。

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
從目前的訂閱移除指定的 HDInsight 集區。

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
移除 HDInsight 簇的自動縮放組式組式。

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
從 HDInsight 集區移除持續腳本動作。

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
重新開機 HDInsight 集區的特定主機。

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
設定 Azure HDInsight 套件的自動縮放設定。

### [Set-AzHDInsightClusterCryptEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
旋轉指定 HDInsight 集的磁片加密金鑰。

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
設定指定組集中的工作者節點數目。

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
設定組組設定物件中的預設儲存空間帳戶設定。

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
設定 Azure HDInsight 套件的閘道 HTTP 認證。

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
將先前執行的腳本動作設定為可保存的腳本動作。

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
在指定的組集中開始已定義的 Azure HDInsight 工作。

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
停止在一個組上指定的執行中工作。

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
將新的腳本動作提交至 Azure HDInsight 集區。

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
選取要與 Cmdlet Invoke-RmAzureHDInsightHiveJob組。

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
等待指定工作的完成或失敗。

