---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967416"
---
# New-AzureSqlDatabaseServerContext

## 摘要
建立伺服器連接內容。

## 句法

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

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSqlDatabaseServerCoNtext** Cmdlet 會建立 Azure SQL Database server 連接內容。
使用 [SQL Server 驗證]，透過指定的認證，建立 SQL 資料庫伺服器的線上內容。
您可以依名稱、完全限定名稱或 URL 來指定 SQL 資料庫伺服器。
若要取得認證，請使用 Get-Credential 的 Cmdlet，提示您指定使用者名稱和密碼。

使用 **新的 AzureSqlDatabaseServerCoNtext** Cmdlet 與憑證的驗證，以使用指定的 Azure 訂閱資料來建立指定 SQL 資料庫伺服器的線上內容。
您可以依名稱或完全限定的名稱來指定 SQL 資料庫伺服器。
您可以指定訂閱資料做為參數，也可以從目前的 Azure 訂閱中進行檢索。
使用 AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Cmdlet 選取目前的 Azure 訂閱。

## 示例

### 範例1：使用 SQL Server 驗證建立內容
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

這個範例使用 SQL Server 驗證。

第一個命令會提示您輸入伺服器管理員認證，並將認證儲存在 $Credential 變數中。

第二個命令會使用 $Credential 連接到名為 lpqd0zbr8y 的 SQL 資料庫伺服器。

最後一個命令會在伺服器上建立一個名為 Database17 的資料庫，該資料庫是 $CoNtext 中之內容的一部分。

### 範例2：使用憑證的驗證建立內容
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

這個範例使用的是以憑證為基礎的驗證。

前兩個命令會將值指派給 $SubscriptionId，並 $Thumbprint 變數。

第三個命令會在 $Thumbprint 中取得指紋所識別的憑證，並將它儲存在 $Certificate 中。

第四個命令會將訂閱設定為 Subscription07，而第五個命令則會選取該訂閱。

最後一個命令會在目前訂閱中建立名為 lpqd0zbr8y 的伺服器的內容。

## 參數

### -認證
指定認證物件，為您提供用於存取伺服器的 SQL Server 驗證。

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
指定 Azure SQL 資料庫伺服器 (FQDN) 名稱的完整功能變數名稱。
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
指定此 Cmdlet 用來建立連接內容之 Azure 訂閱的名稱。
如果您沒有指定此參數的值，該 Cmdlet 會使用目前的訂閱。
執行 Select-AzureSubscription Cmdlet 來變更目前的訂閱。

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
表示此 Cmdlet 使用 Azure 訂閱建立線上內容。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### SqlDatabase. IServerDataServiceCoNtext （WindowsAzure）

## 筆記
* 如果您在未指定網域的情況下進行驗證，而您使用的是 Windows PowerShell 2.0，則 Get-Credential Cmdlet 會傳回 () 前的反斜線 \\ ，例如 \user。 Windows PowerShell 3.0 不會加上反斜線。 **AzureSqlDatabaseServerCoNtext** Cmdlet 的 *Credential* 參數無法辨識此反斜線。 若要移除它，請使用類似下列的命令：

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## 相關連結

[Azure SQL 資料庫 Cmdlet](./Azure.SQLDatabase.md)

[AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[新-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[移除-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


