---
Module Name: AzureRM.HDInsight
Module Guid: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: fba8b9d96666a3a7d625e8f2af7274a6c086f94d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442240"
---
# AzureRM （HDInsight）模組
## 說明
本節中的主題檔在 Azure 資源管理器中，將 Microsoft Azure HDInsight 的 Azure PowerShell Cmdlet 記錄在 (ARM) 架構中。 這些 Cmdlet 可用來管理 HDInsight 群集以及在其上執行的作業。 Cmdlet 存在於 Microsoft Azure. 命令命名空間中。

## AzureRM （HDInsight） Cmdlet
### [附加 AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
將群集身分識別新增至群集設定物件。

### [附加 AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
將在群集中執行的服務的版本新增至群集設定物件。

### [附加 AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。

### [附加 AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。

### [附加 AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
在群集設定物件中加入腳本動作。

### [附加 AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
在群集設定物件中新增安全性 profileto。

### [附加 AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
將 Azure 儲存空間金鑰新增至群集設定物件。

### [AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
取得並列出與目前的訂閱或指定的資源群組相關聯的所有 Azure HDInsight 群集，或檢索特定的群集。

### [AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。

### [AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。

### [AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
取得群集的持續式腳本動作並依時間順序列出它們，或取得指定的持久化腳本動作的詳細資料。

### [AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
取得 HDInsight 服務的相關屬性，例如可用的位置和容量。

### [AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
取得群集的腳本動作歷程記錄，並以逆序的時間順序列出它，或是取得先前執行的腳本動作的詳細資料。

### [授與 AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
授權 HTTP 存取群集。

### [授與 AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
授與 Windows 群集的 RDP 存取權。

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。

### [新-AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。

### [新-AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。

### [新-AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
建立 Hive 工作物件。

### [新-AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
建立 MapReduce 工作物件。

### [新-AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
建立豬工作物件。

### [新-AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
建立 Sqoop 工作物件。

### [新-AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
建立流式處理 MapReduce 工作物件。

### [移除-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
從目前的訂閱中移除指定的 HDInsight 群集。

### [移除-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
從 HDInsight 群集移除持久的腳本動作。

### [吊銷-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
停用 HTTP 對群集的存取權。

### [吊銷-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
停用 RDP 對 Windows 群集的存取權。

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
設定指定群集中的工作人員節點數。

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
在群集設定物件中設定預設儲存空間帳戶設定。

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
將先前執行的腳本動作設為持久化的腳本動作。

### [開始-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
在指定的群集上啟動已定義的 Azure HDInsight 作業。

### [停止 AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
在群集上停止指定的執行作業。

### [Submit-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
將新的腳本指令提交至 Azure HDInsight 群集。

### [使用-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
選取要與 Invoke-RmAzureHDInsightHiveJob Cmdlet 搭配使用的群集。

### [稍候-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
等待指定作業的完成或失敗。

