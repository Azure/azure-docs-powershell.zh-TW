---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 3a78dd91879082c39ae8d7d737484d532ff63f7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452252"
---
# Disable-AzureRmActivityLogAlert

## 摘要
停用活動記錄通知並設定其標記。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### DisableByNameAndResourceGroup
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisableByInputObject
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisableByResourceId
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**Disable AzureRmActivityLogAlert** Cmdlet 會停用和活動記錄通知，並允許您設定其標記。
這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。

## 示例

### 範例1：停用活動記錄通知
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

這個命令會停用資源群組預設-ActivityLogsAlerts 中稱為 alert1 的活動記錄提醒。

這個命令會變更名為 alert1 的活動記錄提醒的 tags 屬性並停用。

### 範例2：使用 PSActivityLogAlertResource 物件做為輸入來停用活動記錄提醒
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

這個命令會停用稱為 alert1 的活動記錄提醒。 針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。

### 範例3：使用 ResourceId 參數停用 ActivityLogAlert
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

這個命令會使用管道中的 ResourceId 參數停用 ActivityLogAlert。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標籤屬性。

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
活動記錄通知的名稱。

```yaml
Type: String
Parameter Sets: DisableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
要在其中存在預警資源之資源群組的名稱。

```yaml
Type: String
Parameter Sets: DisableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。

```yaml
Type: String
Parameter Sets: DisableByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSActivityLogAlertResource 中的 OutputClasses。

## 筆記

## 相關連結

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[AzureRmActivityLogAlert](./Get-AzureRmActivityLogAlert.md)

[移除-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[新-AzureRmActionGroup](./New-AzureRmActionGroup.md)

[新-AzureRmActivityLogAlertCondition](./Get-AzureRmActivityLogAlertCondition.md)

[Enable-AzureRmActivityLogAlert](./Enable-AzureRmActivityLogAlert.md)
