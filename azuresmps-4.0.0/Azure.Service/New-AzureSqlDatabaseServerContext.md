---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404168"
---
# New-AzureSqlDatabaseServerContext

## 簡介
建立伺服器連接上下文。

## 語法

### ByServerNameWithSqlAuth (預設) 
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByfullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 描述
**New-AzureSqlDatabaseServerCoNtext** Cmdlet 會建立 Azure SQL Database 伺服器連接上下文。
使用 SQL Server 驗證，使用指定的認證建立 SQL Database 伺服器的連接上下文。
您可以根據名稱、完整名稱或 URL 來指定 SQL Database 伺服器。
若要取得認證，請使用Get-Credential指定使用者名稱和密碼的 Cmdlet。

使用 **New-AzureSqlDatabaseServerCoNtext** Cmdlet 與憑證式驗證，使用指定的 Azure 訂閱資料建立與指定的 SQL Database 伺服器之連結上下文。
您可以根據名稱或完整名稱指定 SQL Database 伺服器。
您可以將訂閱資料指定為參數，也可以從目前的 Azure 訂閱中取用。
使用 Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Cmdlet 選取目前的 Azure 訂閱。

## 例子

### 範例 1：使用 SQL Server 驗證建立上下文
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

此範例使用 SQL Server 驗證。

第一個命令會提示您輸入伺服器系統管理員認證，並且將認證儲存在 $Credential 變數中。

第二個命令會使用 $Credential 來連接到名為 lpqd0zbr8y 的 SQL Database $Credential。

最後一個命令會在伺服器上建立名為 Database17 的資料庫，該資料庫是 $CoNtext。

### 範例 2：使用憑證式驗證建立上下文
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

此範例使用憑證式驗證。

前兩個命令會指派值給$SubscriptionId$Thumbprint變數。

第三個命令會以指紋在 $Thumbprint 中識別憑證，並儲存在 $Certificate。

第四個命令將訂閱設定為 Subscription07，而第五個命令會選取該訂閱。

最後一個命令會針對名為 lpqd0zbr8y 的伺服器，于目前的訂閱中建立內容。

## 參數

### -認證
指定提供 SQL Server 驗證的認證物件，以存取伺服器。

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
指定 Azure SQL Database 伺服器 (FQDN) 功能變數名稱。
例如，Server02.database.windows.net。

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
指定此 Cmdlet 用來存取伺服器的 Azure SQL DatabaseManagement 入口網站的 URL。

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。

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

### -ServerName
指定資料庫伺服器的名稱。

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
指定此 Cmdlet 用來建立連接上下文的 Azure 訂閱名稱。
如果您沒有為此參數指定值，Cmdlet 會使用目前的訂閱。
執行 Select-AzureSubscription Cmdlet 以變更目前的訂閱。

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
表示此 Cmdlet 使用 Azure 訂閱建立連接上下文。

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

## 輸出

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceCoNtext

## 筆記
* 如果您驗證時沒有指定網域，而且如果您使用 Windows PowerShell 2.0，Get-Credential Cmdlet 會以使用者名稱為前 () 回反杠 () 例如 \\ \user。 Windows PowerShell 3.0 不會新增反杠。 **New-AzureSqlDatabaseServerCoNtext** Cmdlet 的認證參數無法識別此反杠。  若要移除它，請使用類似下列的命令：

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## 相關連結



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


