---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 790a0f0383796728b4754c4d64d98ef2ca7ed3c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447877"
---
# Start-AzureRmAutomationDscCompilationJob

## 摘要
在自動化中編譯 DSC 設定。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**Start-AzureRmAutomationDscCompilationJob** Cmdlet 會在 Azure 自動化中編譯 (DSC) 設定的 Ap 所需狀態設定。

## 示例

### 範例1：在自動化中編譯 Azure DSC 設定
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

第一個命令會建立參數字典，並將它們儲存在 $Params 變數中。

第二個命令會編譯名為 Config01 的 DSC 配置。
此命令包括 DSC 設定參數 $Params 中的值。

### 範例2：使用新的節點配置組建版本，在自動化中編譯 Azure DSC 設定。
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

與第一個範例類似，第一個命令會建立一個參數字典，並將它們儲存在 $Params 變數中。

第二個命令會編譯名為 Config01 的 DSC 配置。
此命令包括 DSC 設定參數 $Params 中的值。

它不會以名稱 Config01 [<2>]」建立新的節點設定，來覆寫較舊的現有節點 <NodeName> 設定。 版本號碼會根據已存在的現有版本編號增加。

## 參數

### -AutomationAccountName
指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationData
指定 DSC 設定的配置資料字典。

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigurationName
指定此 Cmdlet 編譯的 DSC 配置名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -IncrementNodeConfigurationBuild
建立新的節點配置組建版本。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -參數
指定此 Cmdlet 用來編譯 DSC 設定的參數字典。

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 在其中編譯配置的資源群組的名稱。

```yaml
Type: String
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

### CompilationJob 中的 [.]

## 筆記

## 相關連結

[AzureRmAutomationDscCompilationJob](./Get-AzureRmAutomationDscCompilationJob.md)

[AzureRmAutomationDscCompilationJobOutput](./Get-AzureRmAutomationDscCompilationJobOutput.md)


