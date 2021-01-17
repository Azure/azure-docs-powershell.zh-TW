---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448756"
---
# Get-AzIotSecurityAnalytics

## 摘要
取得 IoT 安全分析

## 句法

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzIotSecurityAnalytics Cmdlet 會傳回特定 iot 安全解決方案的一組安全分析

## 示例

### 範例1
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

在 reasource 群組 "MyResourceGroup" 中取得安全性解決方案 "MySolution" 的 deafult IoT Security Analytics

## 參數

### -預設值
如果有的話，請取得預設分析集，否則請取得所有分析集的清單。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -解決方案名稱
方案名稱

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### PSIotSecuritySolutionAnalytics 中的 IotSecuritySolutionAnalytics （Security..。

## 筆記

## 相關連結
