---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 9a0e40716623b4d0b11f661ce859a0ee8787e685
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612059"
---
# Update-AzKeyVaultSecret

## 摘要
更新金鑰保存庫中密碼的屬性。

## 句法

### 預設 (預設) 
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzKeyVaultSecret** Cmdlet 會更新金鑰保存庫中的秘密可編輯屬性。

## 示例

### 範例1：修改密碼的屬性
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

前四個命令會定義到期日期、NotBefore 日期、標籤和內容類型的屬性，並將屬性儲存在變數中。
最後一個命令會使用儲存的變數，在名為 ContosoVault 的金鑰保存庫中修改名為 HR 的密碼的屬性。

### 範例2：刪除機密的標記與內容類型
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

這個命令會在名為 [Contoso] 的 [主要電子倉庫] 中，刪除名為「HR」之指定版本之密碼的標記和內容類型。

### 範例3：停用其名稱以其開頭的最新版本密碼
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

第一個命令會將字串值 Contoso 儲存在 $Vault 變數中。
第二個命令會將字串值儲存在 $Prefix 變數中。
第三個命令使用 Get-AzKeyVaultSecret Cmdlet 在指定的金鑰保存庫中取得機密，然後將這些機密傳遞到 **物件** Cmdlet。 **物件** Cmdlet 會篩選以字元開頭的名稱的密碼。 命令會將與篩選器相符的秘訣加入 Update-AzKeyVaultSecret Cmdlet，從而停用。

### 範例4：為所有版本的機密設定 ContentType
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

前三個命令會定義要用於 *VaultName* 、 *名稱* 和 *ContentType* 參數的字串變數。 第四個命令使用 Get-AzKeyVaultKey Cmdlet 來取得指定的金鑰，並將這些金鑰管道到 Update-AzKeyVaultSecret Cmdlet，以將其內容類型設為 XML。

## 參數

### -ContentType
密碼的內容類型。
如果沒有指定，則秘密內容類型的現有值會保持不變。
透過指定空字串來移除現有的內容類型值。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -啟用
如果有的話，請在值為 true 時啟用密碼。
如果值為 false，則停用密碼。
如果未指定，則機密的啟用/停用狀態的現有值會保持不變。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -到期
以 UTC 時程表示的密碼到期時間。
如果未指定，密碼到期時間的現有值會保持不變。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
秘密物件

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
[秘密名稱]。
Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
無法使用密碼前的 UTC 時間。
如果沒有指定，則密碼的 NotBefore 屬性的現有值會保持不變。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Cmdlet 預設不會傳回物件。
如果已指定此開關，請傳回機密物件。

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

### -Tag
代表秘密標記的 hashtable。
如果沒有指定，則機密的現有標記會保持不變。
指定空的 Hashtable 來移除標記。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
保存庫名稱。
Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -版本
秘密版本。
Cmdlet 會從保存庫名稱、目前已選取的環境、秘密名稱和密碼版本構造秘密的 FQDN。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSKeyVaultSecretIdentityItem 中的 KeyVault。

## 輸出

### PSKeyVaultSecret 中的 KeyVault。

## 筆記

## 相關連結
