---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 9c3fd17454381cf17604eb430588255b4889b3cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450064"
---
# Import-AzureRmAutomationDscNodeConfiguration

## 摘要
在自動化中將 MOF 檔案匯入為 DSC 節點配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
匯 **入-AzureRmAutomationDscConfiguration** Cmdlet 會將受管理的物件格式（ (MOF) 設定檔）匯入到 Azure 自動化中，做為所需的狀態設定 (DSC) 節點設定。
指定 mof 檔案的路徑。

## 示例

### 範例1：將 DSC 節點設定匯入自動化
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。
命令會指定 *Force* 參數。
如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會將它取代。

### 範例2：將 DSC 節點設定匯入自動化，然後建立新的組建版本，而不會覆寫現有的 NodeConfiguration。
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。
命令會指定 *Force* 參數。
如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會新增名稱為 ContosoConfiguration [2] 的新組建版本。

## 參數

### -AutomationAccountName
指定此 Cmdlet 匯入 DSC 節點配置的自動化帳戶名稱。

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

### -ConfigurationName
指定自動化中的 DSC 設定名稱，以做為要匯入之節點配置的命名空間和容器。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
表示此 Cmdlet 會取代自動化中現有的 DSC 節點設定。

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

### -IncrementNodeConfigurationBuild
建立新的節點配置組建版本。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
指定此 Cmdlet 所匯入的 MOF 設定檔路徑。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 匯入 DSC 節點設定的資源群組的名稱。

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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

### NodeConfiguration 中的 [.]

## 筆記

## 相關連結

[Export-AzureRmAutomationDscConfiguration](./Export-AzureRmAutomationDscConfiguration.md)

[AzureRmAutomationDscConfiguration](./Get-AzureRmAutomationDscConfiguration.md)


