---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967923"
---
# Remove-AzureEnvironment

## 摘要
從 Windows PowerShell 刪除 Azure 環境。

## 句法

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureEnvironment** Cmdlet 會從您的漫遊設定檔中刪除 Azure 環境，讓 Windows PowerShell 找不到它。
這個 Cmdlet 不會從 Microsoft Azure 刪除環境，或以任何方式變更實際的環境。

Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。
您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。
如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。

## 示例

### 範例1：刪除環境
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

這個命令會從 Windows PowerShell 中刪除 ContosoEnv 環境。

### 範例2：刪除多個環境
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

這個命令會從 Windows PowerShell 中刪除名稱開頭為 "Contoso" 的環境。

## 參數

### -Force
取消確認提示。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要移除的環境名稱。
這個參數是必要的。
這個參數值區分大小寫。
不允許通配字元。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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
您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。

## 輸出

### None 或 System.object
如果您使用 *PassThru* 參數，這個 Cmdlet 會傳回布林值。
否則，它不會傳回任何輸出。

## 筆記

## 相關連結

[附加 AzureEnvironment](./Add-AzureEnvironment.md)

[AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


