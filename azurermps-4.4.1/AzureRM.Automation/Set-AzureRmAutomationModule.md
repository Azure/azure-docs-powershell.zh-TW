---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447177"
---
# Set-AzureRmAutomationModule

## 摘要
更新自動化中的模組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmAutomationModule** Cmdlet 會更新 Azure 自動化中的模組。
這個命令會接受副檔名為 .zip 的壓縮檔案。
檔案包含的資料夾包含下列其中一種類型的檔案： 

- wps_2 模組，其副檔名為 psm1 或 .dll 
- wps_2 的模組資訊清單，副檔名為 psd1。

.Zip 檔案的名稱、資料夾的名稱，以及資料夾中的檔案名都必須是相同的名稱。

將 .zip 檔案指定為自動化服務可存取的 URL。

如果您使用這個 Cmdlet 或 New-AzureRmAutomationModule Cmdlet 將 wps_2 模組匯入自動化，該作業就是非同步作業。
不論匯入成功與否，命令都會完成。
若要檢查是否成功，請執行下列命令：

`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName

檢查 **ProvisioningState** 屬性的值是否為 Succeeded。

## 示例

### 範例1：更新模組
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

這個命令會將名為 ContosoModule 的現有模組更新版本，匯入到名為 Contoso17 的自動化帳戶中。

## 參數

### -AutomationAccountName
指定此 Cmdlet 更新模組的自動化帳戶名稱。

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
指定包含此 Cmdlet 所匯入之模組新版的 .zip 檔案的 URL。

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
指定此 Cmdlet 更新自動化的模組版本。

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

### -名稱
指定此 Cmdlet 所匯入的模組名稱。

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
指定此 Cmdlet 更新模組的資源群組的名稱。

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

### [-Azure. 命令. Model. Module]

## 筆記

## 相關連結

[AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[新-AzureRmAutomationModule](./New-AzureRmAutomationModule.md)

[移除-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)


