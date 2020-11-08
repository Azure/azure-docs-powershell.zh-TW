---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140050"
---
# Get-AzAlertRule

## 摘要
取得警示規則。

## 句法

### GetByResourceGroup
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceUri
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzAlertRule Cmdlet 會根據其名稱或 URI，或從指定的資源群組取得所有警示規則，來 **取得** 警示規則。

## 示例

### 範例1：取得資源群組的警示規則
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

這個命令會取得名為 [預設-Web CentralUS] 的資源群組的所有通知規則。
輸出不會包含有關規則的詳細資料，因為未指定 *DetailedOutput* 參數。

### 範例2：依名稱取得警示規則
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。
因為未指定 *DetailedOutput* 參數，所以輸出只包含有關警示規則的基本資訊。

### 範例3：透過名稱取得警示規則及詳細的輸出
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。
已指定 *DetailedOutput* 參數，因此會詳細說明輸出。

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

### -DetailedOutput
顯示輸出中的完整詳細資料。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要取得之警示規則的名稱。

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
指定目標資源的識別碼。

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### SwitchParameter 的系統管理功能

## 輸出

### PSAlertRule 中的 OutputClasses。

## 筆記

## 相關連結

[附加 AzLogAlertRule](./Add-AzLogAlertRule.md)

[附加 AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[附加 AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[AzAlertHistory](./Get-AzAlertHistory.md)

[移除-AzAlertRule](./Remove-AzAlertRule.md)


