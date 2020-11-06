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
在群集設定物件中新增安全性 profileto。

### [附加 AzHDInsightStorage](Add-AzHDInsightStorage.md)
將 Azure 儲存空間金鑰新增至群集設定物件。

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
在 HDInsight 群集中停用作業管理套件 (OMS) ，而相關的記錄將停止流入在啟用期間指定的 OMS 工作區。

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
在 HDInsight 群集中啟用操作管理套件 (OMS) ，而相關的記錄將會傳送到 enable 中指定的 OMS 工作區。

### [AzHDInsightCluster](Get-AzHDInsightCluster.md)
取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。

### [AzHDInsightJob](Get-AzHDInsightJob.md)
從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。

### [AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。

### [AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
取得群集上 (OMS) 安裝的 Operations Management Suite 狀態。

### [AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。

### [AzHDInsightProperty](Get-AzHDInsightProperty.md)
取得 HDInsight 服務的相關屬性，例如可用的位置和容量。

### [AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。

### [授與 AzHDInsightHttpServicesAccess](Grant-AzHDInsightHttpServicesAccess.md)
授權 HTTP 存取群集。

### [授與 AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
授與 Windows 群集的 RDP 存取權。

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。

### [新-AzHDInsightCluster](New-AzHDInsightCluster.md)
在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。

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

### [移除-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
從 HDInsight 群集移除持久的腳本動作。

### [吊銷-AzHDInsightHttpServicesAccess](Revoke-AzHDInsightHttpServicesAccess.md)
停用 HTTP 對群集的存取權。

### [吊銷-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
停用 RDP 對 Windows 群集的存取權。

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
設定指定群集中的工作人員節點數。

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
在群集設定物件中設定預設儲存空間帳戶設定。

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

