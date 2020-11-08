---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136735"
---
# Remove-AzManagedHsmKey

## 摘要
刪除受管理的 HSM 中的金鑰。

## 句法

### RemoveByKeyNameParameterSet (預設) 
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByInputObjectParameterSet
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
Remove-AzManagedHsmKey Cmdlet 會刪除受管理的 HSM 中的金鑰。
如果不小心刪除了金鑰，則可以使用具有特殊「復原」許可權的使用者 Undo-AzManagedHsmKeyRemoval 來復原金鑰。
這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。

## 示例

### 範例1：從受管理的 HSM 移除金鑰
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

這個命令會從受管理的 HSM （名為 testmhsm）移除名為 testkey 的索引鍵。

### 範例2：在未確認使用者的情況下移除金鑰
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

這個命令會從受管理的 HSM （名為 testmhsm）移除名為 testkey 的索引鍵。
此命令會指定 *Force* 參數，因此 Cmdlet 不會提示您進行確認。

### 範例3：永久清除受管理的 HSM 中的已刪除金鑰
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

這個命令會將名為 testkey 的金鑰從已 testmhsm 的 managed HSM 中永久移除。
執行此 Cmdlet 需要「清除」許可權，此許可權必須事先已明確地授予此受管理 HSM 的使用者。

### 範例4：使用管線運算子移除按鍵
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

這個命令會取得名為 testmhsm 的受管理 HSM 中的所有金鑰，並使用管線運算子將它們傳遞到 **物件** Cmdlet。
這個 Cmdlet 會將已 **啟用** 屬性的值 $False 的金鑰傳遞給目前的 Cmdlet。
該 Cmdlet 會移除這些索引鍵。

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

### -Force
不要要求確認。

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

### -HsmName
HSM 名稱。 Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
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
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
永久移除先前刪除的金鑰。

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

### -名稱
索引鍵名稱。
Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Cmdlet 預設不會傳回物件。
如果指定此開關，則 Cmdlet 會傳回已刪除的金鑰組象。

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

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## 筆記

## 相關連結

[附加 AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[備份-AzManagedHsmKey](./Backup-AzManagedHsmKey.md)

[AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[復原-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[更新-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)