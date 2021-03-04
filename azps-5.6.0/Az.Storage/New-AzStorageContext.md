---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915077"
---
# New-AzStorageContext

## 簡介
建立 Azure 儲存內容。

## 語法

### OAuthAccount (預設) 
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### Local一級
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## 描述
**New-AzStorageCoNtext** Cmdlet 會建立 Azure 儲存內容。
儲存內容的預設驗證為 OAuth (Azure AD) 輸入儲存帳戶名稱。
請參閱 中的儲存服務驗證詳細資料 https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services 。

## 例子

### 範例 1：指定儲存帳戶名稱和金鑰以建立上下文
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

此命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文。

### 範例 2：指定連接字串以建立上下文
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

此命令會根據帳戶 ContosoGeneral 的指定連接字串建立上下文。

### 範例 3：建立匿名儲存帳戶的上下文
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

此命令會為名為 ContosoGeneral 的帳戶建立匿名使用上下文。
命令會指定 HTTP 做為連接通訊協定。

### 範例 4：使用本地開發儲存空間帳戶建立上下文
```
PS C:\>New-AzStorageContext -Local
```

此命令會使用本地開發儲存帳戶建立上下文。
命令會指定 *Local* 參數。

### 範例 5：取得本地開發人員儲存帳戶的容器
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

此命令會使用本地開發儲存帳戶建立上下文，然後使用管線運算子將新內容傳遞給 **Get-AzStorageContainer** Cmdlet。
該命令會為本地開發人員儲存帳戶獲得 Azure 儲存容器。

### 範例 6：取得多個容器
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

第一個命令會使用本地開發儲存空間帳戶建立上下文，然後將該上下文儲存在 $CoNtext 01 變數中。
第二個命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文，然後將該上下文儲存在 $CoNtext 02 變數中。
最後一個命令會使用 **Get-AzStorageContainer** 取得儲存在 $CoNtext 01 和 $CoNtext 02 之上下文的容器。

### 範例 7：使用端點建立上下文
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

此命令會建立具有指定儲存端點的 Azure 儲存體上下文。
該命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文。

### 範例 8：使用指定的環境建立上下文
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

此命令會建立具有指定 Azure 環境的 Azure 儲存上下文。
該命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文。

### 範例 9：使用 SAS 權杖建立上下文
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

第一個命令會針對名為 ContosoMain 的容器使用 **New-AzStorageContainerSASToken** Cmdlet 來產生 SAS 權杖，然後將該權杖儲存在 $SasToken 變數中。
該權杖適用于讀取、新增、更新及刪除許可權。
第二個命令會針對名為 ContosoGeneral 的帳戶建立上下文，該帳戶使用儲存在 $SasToken 中的 SAS 權杖，然後將該上下文儲存在 $CoNtext 變數中。
最後一個命令會使用儲存在其中上下文，列出與名為 ContosoMain 之容器相關聯的所有$CoNtext。

### 範例 10：使用 OAuth 驗證建立上下文
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

此命令會使用 OAuth (Azure AD) 內容。

## 參數

### -匿名
表示此 Cmdlet 會建立匿名登入的 Azure 儲存內容。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
指定 Azure 儲存體上下文的連接字串。

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -端點
指定 Azure 儲存體上下文的端點。

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -環境
指定 Azure 環境。
此參數可接受的值為：AzureCloud 和 AzureChinaCloud。
如需要詳細資訊，請鍵入 `Get-Help Get-AzEnvironment` 。

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -本地
表示此 Cmdlet 是使用本地開發儲存帳戶建立內容。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
傳輸通訊協定 (HTTPs/HTTP) 。

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
指定一個共用存取簽名 (SAS) 為上下文的權杖。

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
指定 Azure 儲存體帳戶金鑰。
此 Cmdlet 會為此參數指定的金鑰建立上下文。

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
指定 Azure 儲存體帳戶名稱。
此 Cmdlet 會為此參數指定的帳號建立上下文。

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -使用ConnectedAccount
表示此 Cmdlet 會使用 OAuth (Azure AD) Azure 儲存內容。
當未指定其他驗證時，Cmdlet 預設會使用 OAuth 驗證。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.WindowsAzure.Commands.storage.AzureStorageCoNtext

## 筆記

## 相關連結

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


