---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140484"
---
# Update-AzManagedHsmKey

## 摘要
更新受管理的 HSM 中之金鑰的屬性。

## 句法

### 預設 (預設) 
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzManagedHsmKey** Cmdlet 會更新受管理 HSM 中之金鑰的可編輯屬性。

## 示例

### 範例1：修改金鑰以啟用它，並設定到期日和標籤
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。 該物件指定未來兩年的時間。 該命令會將該日期儲存在 $Expires 變數中。
如需詳細資訊，請輸入 `Get-Help Get-Date` 。
第二個命令會建立變數來儲存高嚴重性與會計的標記值。
最後一個命令會修改一個名為 testkey001 的金鑰。 該命令會啟用金鑰、將過期時間設定為儲存在 $Expires 的時間，並設定 $Tags 中儲存的標籤。

## 參數

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
True 的值會啟用索引鍵和 false 的值 disabless。
如果未指定，現有的啟用/停用狀態會保持不變。

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
以 UTC 時程表示之金鑰的到期時間。
如果沒有指定，則金鑰的現有到期時間會保持不變。

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

### -HsmName
HSM 名稱。 Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。

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

### -InputObject
主要物件

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyOps
可使用金鑰執行的作業。
如果沒有指定，則金鑰的現有按鍵動作會保持不變。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
索引鍵名稱。
Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
在無法使用 key 之前的 UTC 時間。
如果未指定，索引鍵的現有 NotBefore 屬性會保持不變。

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
如果已指定此開關，則會傳回更新的金鑰束物件。

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
Hashtable 代表主要標記。
如果未指定，索引鍵的 existings 標記會保持不變。

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

### -版本
金鑰版本。
Cmdlet 會從 managed HSM 名稱、目前已選取的環境、金鑰名稱和金鑰版本構造金鑰的 FQDN。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSKeyVaultKeyIdentityItem 中的 KeyVault。

## 輸出

### PSKeyVaultKey 中的 KeyVault。

## 筆記

## 相關連結

[附加 AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[備份-AzManagedHsmKey](./Backup-AzManagedHsmKey.md)

[移除-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[復原-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)