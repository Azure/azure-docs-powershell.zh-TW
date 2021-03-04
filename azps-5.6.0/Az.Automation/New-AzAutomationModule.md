---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917105"
---
# New-AzAutomationModule

## 簡介
將模組導入自動化。

## 語法

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzAutomationModule Cmdlet** 將模組導入 Azure Automation。
此命令接受副檔名為 .zip 的壓縮檔案。
檔案包含的資料夾包含下列其中一種類型的檔案： 
- Windows PowerShell 模組，副檔名為 .psm1 或 .dll 
- Windows PowerShell 模組清單，副檔名為 .psd1.ZIP 檔案名、資料夾名稱，以及資料夾中的檔案名必須相同。
將 .zip 檔案指定為自動化服務可存取的 URL。
如果您使用此 Cmdlet 或 Cmdlet 將 Windows PowerShell 模組Set-AzAutomationModule自動化，則作業是非同步。
無論成功或失敗，命令都完成。
若要檢查是否成功，請執行下列命令 `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ：ModuleName 檢查 **ProvisioningState** 屬性中的成功值。

## 例子

### 範例 1：匯出模組
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

此命令會將名為 ContosoModule 的模組，導入名為 Contoso17 的自動化帳戶。
模組會儲存在 Azure Blob 中名為 contosostorage 的儲存帳戶和名為模組的容器。

## 參數

### -AutomationAccountName
指定此 Cmdlet 所輸入模組的自動化帳戶名稱。

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

### -ContentLinkUri
模組 zip 封裝的 URL

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
指定此 Cmdlet 所導入模組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 所輸入模組的資源組名。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### System.Uri

## 輸出

### Microsoft.Azure.Commands.Automation.Model.Module

## 筆記

## 相關連結

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


