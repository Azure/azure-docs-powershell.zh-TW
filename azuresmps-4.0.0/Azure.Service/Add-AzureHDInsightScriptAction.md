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
# Add-AzureHDInsightScriptAction

## 摘要
新增 HDInsight 腳本動作。

## 句法

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
此版本的 Azure PowerShell HDInsight 已被否決。
這些 Cmdlet 將會在2017年1月1日移除。
請使用較新版本的 Azure PowerShell HDInsight。

如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。
如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。
如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。

**AzureHDInsightScriptAction** Cmdlet 提供 Azure HDInsight 功能，可用於安裝其他軟體，或使用 Windows PowerShell 腳本來變更在 Hadoop 群集上執行的應用程式設定。

部署 HDInsight 群集時，腳本動作會在叢集節點上執行，而且會在群集中的節點完成 HDInsight 設定之後執行。
[腳本] 動作會以系統管理員帳戶許可權執行，並提供叢集節點的完整存取權。
您可以為每個群集提供一個腳本指令清單，以指定的循序執行。

## 示例

### 範例1：在群集中加入腳本動作
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

第一個命令使用 **新的 AzureHDInsightClusterConfig** Cmdlet 來建立 HDInsight 群集設定，然後將它儲存在 $Config 變數中。

第二個命令使用 **AzureHDInsightScriptAction** Cmdlet，以將名為 TestScriptAction 的腳本動作新增至 $Config。

最後一個命令會使用 **AzureHDInsightCluster** Cmdlet 來建立新的 HDInsight 群集，該群集會執行儲存在 $Config 中的腳本動作。

### 範例2：在群集中新增多個腳本動作
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

第一個命令使用 **新的 AzureHDInsightClusterConfig** Cmdlet 來建立 HDInsight 群集設定，然後將它儲存在 $Config 變數中。

第二個命令會使用 **AzureHDInsightScriptAction** Cmdlet，將指定的腳本動作新增至 $Config，然後使用管線 $Config 運算子，將第二個 **腳本動作新增** 至 $Config。

最終命令會使用 **AzureHDInsightCluster** Cmdlet 來建立在 $Config 中執行腳本動作的群集。

## 參數

### -ClusterRoleCollection
指定要執行腳本的節點。
此參數可接受的值為： [頭節點] 或 [DataNode]。

您可以指定一個值或兩個值。

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

### -Config
指定 [配置] 物件。
這個 Cmdlet 會將腳本動作資訊新增至此參數指定的物件。

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

### -名稱
指定腳本動作的名稱。

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

### -參數
指定腳本動作所需的參數。

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

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -Uri
指定要執行的腳本的 URI 位置。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[新-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[新-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


