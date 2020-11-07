---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967438"
---
# New-AzureRoleTemplate

## 摘要
建立網站和 worker 角色範本。

## 句法

### WebRole
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureRoleTemplate** Cmdlet 會建立網站和 worker 角色範本。

## 示例

### 範例1：建立網頁角色範本
```
PS C:\> New-AzureRoleTemplate -Web
```

這個範例會在目前目錄中名為 WebRoleTemplate 的資料夾中建立新的網頁角色範本。

### 範例2：建立 worker 角色範本
```
PS C:\> New-AzureRoleTemplate -Worker
```

這個範例會在目前目錄中名為 WebRoleTemplate 的資料夾中建立新的輔助角色範本。

### 範例3：在自訂目錄中建立角色範本
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

這個範例會在名為 MyWebRoleTemplate 的目錄中建立新的網頁角色範本，而不是在目前的目錄中。

## 參數

### -輸出
指定所產生範本的輸出路徑。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### 網頁
指定您要建立網頁角色範本。

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -員工
指定您要建立 worker 角色範本。

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
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

[附加 AzureWebRole](./Add-AzureWebRole.md)

[附加 AzureWorkerRole](./Add-AzureWorkerRole.md)


