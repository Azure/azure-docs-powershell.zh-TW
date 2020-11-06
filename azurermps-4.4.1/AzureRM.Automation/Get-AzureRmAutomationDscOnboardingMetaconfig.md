---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 58d15476921005b6da674d6a16441eb2e4f82865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450080"
---
# Get-AzureRmAutomationDscOnboardingMetaconfig

## 摘要
建立元設定. mof 檔案。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmAutomationDscOnboardingMetaconfig** Cmdlet 會建立 Ap 所需的狀態設定 (DSC) 元設定管理物件格式 (MOF) 檔案。
這個 Cmdlet 會針對您指定的每個電腦名稱稱建立一個 mof 檔案。
這個 Cmdlet 會為 mof 檔案建立一個資料夾。
您可以執行此資料夾的 Set-DscLocalConfigurationManager Cmdlet，以將這些電腦作為 DSC 節點的 Azure 自動化帳戶。

## 示例

### 範例1：自動化 DSC 的板載伺服器
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

第一個命令會針對自動帳戶（名為 Contoso17）的兩個伺服器建立 DSC 元配置檔案。
該命令會將這些檔案儲存在桌面上。

第二個命令使用 **DscLocalConfigurationManager** Cmdlet，將元設定套用至指定的電腦，以將其作為 DSC 節點。

## 參數

### -AutomationAccountName
指定自動化帳戶的名稱。
您可以將 *ComputerName* 參數指定的電腦上建到此參數指定的帳號。

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

### -ComputerName
指定此 Cmdlet 產生的電腦名稱稱的陣列。 mof 檔案。
如果您沒有指定此參數，則 Cmdlet 會為目前電腦 (localhost) 產生一個 mof 檔案。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
強制執行命令，不會提示您確認，以及取代現有的、具有相同名稱的 mof 檔案。

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

### -OutputFolder
指定此 Cmdlet 儲存. mof 檔案的資料夾名稱。

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

### -ResourceGroupName
指定資源群組的名稱。
這個 Cmdlet 會在此參數指定的資源群組中，將 mof 檔案建立給板載電腦。

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

### DscOnboardingMetaconfig 中的 [.]

## 筆記

## 相關連結

