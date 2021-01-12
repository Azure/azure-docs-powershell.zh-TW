---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110473"
---
# New-AzureWebsite

## 摘要
在 Azure 中建立要執行的新網站。

## 句法

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

這個 Cmdlet 會建立新的網站，以在 Azure 中執行，並準備透過 GitHub 進行部署。

## 示例

### 範例1：使用 Git 建立新的網站
```
PS C:\> New-AzureWebsite mySite -Git
```

這個範例會在 Azure 中建立新的網站，以及用來將檔案部署至新網站的本機 Git 儲存庫。

### 範例2：建立與 GitHub 整合的網站
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

這個範例會建立連結至 GitHub 知識庫的新網站，名為 [我的帳戶/myrepo]。
將提交至 GitHub 儲存庫的專案會推送至 Azure 中的網站。

## 參數

### -Git
設定本機 Git 儲存庫並將其連結至網站。
如果已指定，此參數會在本機目錄中設定 Git 儲存庫，並新增一個名為「azure ' 的遠端知識庫，並連結至 Azure 中的網站。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
表示此 Cmdlet 會將新的網站連結至現有的 GitHub 儲存庫。
提交至 Giuthub 知識庫的功能會推送至 Azure 中的網站。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubCredentials
指定要連線至 GitHub 的使用者名稱和密碼認證。

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubRepository
指定 GitHub 儲存庫的完整名稱以連結至此網站。
例如， `myaccount/myrepo` 。

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

### -Hostname
指定新網站的替代主機名稱。

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

### -位置
指定您要部署網站之資料中心的位置。

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

### -名稱
指定網站的名稱。

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

### -PublishingUsername
指定您在使用 Git 部署的 Azure 入口網站中指定的使用者名稱。

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

### -槽
指定網站的槽名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[Set-AzureWebsite](./Set-AzureWebsite.md)


