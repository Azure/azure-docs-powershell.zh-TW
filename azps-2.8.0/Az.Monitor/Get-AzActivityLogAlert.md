---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 50ffa5beb8ab79d3c903ec5b7e6a21c9b08116db
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406395"
---
# Get-AzActivityLogAlert

## 簡介
獲得一或多個活動記錄提醒資源。

## 語法

### GetByNameAndResourceGroup
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-AzActivityLogAlert** Cmdlet 會取得一或多個活動記錄提醒資源。

## 例子

### 範例 1：根據訂閱識別碼取得活動記錄提醒
```
PS C:\>Get-AzActivityLogAlert
```

此命令會列出目前訂閱的所有活動記錄通知。

### 範例 2：取得給定資源群組的活動記錄提醒
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

此命令會列出給定資源群組的活動記錄通知。

### 範例 3：取得活動記錄提醒。
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

此命令會列出一 (活動記錄提醒的單一) 清單。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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
活動記錄提醒的名稱。

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
警示資源存在之資源組的名稱。
如果 Name 不是 Null 或空值，此參數必須包含非空字串。

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource

## 筆記

## 相關連結

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Remove-AzActivityLogAlert](./Remove-AzActivityLogAlert.md)

[New-AzActionGroup](./New-AzActionGroup.md)
