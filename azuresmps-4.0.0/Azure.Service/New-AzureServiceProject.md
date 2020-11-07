---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967664"
---
# New-AzureServiceProject

## 摘要
為新的服務建立所需的檔案和配置。

## 句法

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**新的-AzureServiceProject** Cmdlet 會針對目前目錄中的新 Azure 服務建立所需的檔案和配置。

## 示例

### 範例1：建立服務的基架
```
PS C:\> New-AzureServiceProject MyService1
```

這個範例會為目前目錄中名為 MyService1 的新 Azure 服務建立基架。

## 參數

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -ServiceName
指定服務的名稱。
它會決定您服務的主機名稱的第一個區段 (例如，name.cloudapp.net) ，以及將包含您服務的目錄。
名稱只能包含字母、數位和短劃線字元 ( ) 。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[附加 AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[發佈-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


