---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612308"
---
# Get-AzHDInsightOperationsManagementSuite

## 摘要
取得群集上 (OMS) 安裝的 Operations Management Suite 狀態。

## 句法

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzHDInsightOperationsManagementSuite** Cmdlet 會取得 Azure HDInsight 群集中的 OMS 安裝狀態。 如果已啟用 OMS，則也會傳回 OMS 工作區識別碼。

## 示例

### 範例1
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled 屬性為 true，因此已在群集上啟用 Operations Management Suite (OMS) 。 記錄流入位置的 OMS 工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd

### 範例2
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled 屬性為 true，因此已在群集上啟用 Operations Management Suite (OMS) 。 記錄流入位置的 OMS 工作區識別碼是1d364e89-bb71-4503-aa3d-a23535aea7bd

### 範例3
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

因為 ClusterMonitoringEnabled 屬性為 false，所以在群集上停用運營管理套件 (OMS) 。

### 範例4
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

因為 ClusterMonitoringEnabled 屬性為 false，所以在群集上停用運營管理套件 (OMS) 。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
要取得作業管理套件狀態的群集名稱 (OMS) 。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
群集的 [資源] 群組。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### AzureHDInsightOMS 中的 [.]

## 筆記

## 相關連結
