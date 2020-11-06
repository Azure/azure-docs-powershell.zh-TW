---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447186"
---
# Set-AzureRmAutomationRunbook

## 摘要
修改 runbook。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzureRmAutomationRunbook Cmdlet 會修改 AP 中 Azure 自動化 runbook 的 **設定** 。

## 示例

### 範例1：針對 runbook 啟用詳細記錄
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

這個命令會針對在名為 Contoso17 的 Azure 自動化帳戶中指定的 runbook 啟用詳細記錄。

## 參數

### -AutomationAccountName
指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -描述
指定 runbook 的描述。

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

### -LogProgress
指定 runbook 是否要記錄進度。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogVerbose
指定記錄是否包含詳細資訊。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 修改的 runbook 名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 修改 runbook 之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -標記
指定要取代已修改之 runbook 之目前標記的標記字典。

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### [-Azure. 命令介面]。

## 筆記

## 相關連結

[Export-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[AzureRmAutomationRunbook](./Get-AzureRMAutomationRunbook.md)

[匯入-AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[新-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[新-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[發佈-AzureRmAutomationRunbook](./Publish-AzureRMAutomationRunbook.md)

[移除-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[開始-AzureRmAutomationRunbook](./Start-AzureRMAutomationRunbook.md)


