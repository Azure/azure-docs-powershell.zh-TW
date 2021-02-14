---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134659"
---
# Set-AzRecoveryServicesVaultProperty

## 摘要
更新電子倉庫的屬性。

## 句法

### AzureRSVaultSoftDelteParameterSet (預設) 
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureRSVaultCMKParameterSet
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzRecoveryServicesVaultProperty** Cmdlet 會更新恢復服務保存庫的屬性。 這個 Cmdlet 可用來啟用/停用虛刪除，或針對具有兩個不同參數集的保存庫設定 CMK 加密。 
只有在保存庫中沒有已註冊的容器，才能停用保存庫的 **SoftDeleteFeatureState** 屬性。 只有在使用者第一次更新 CMK 保存庫時，才能設定 InfrastructurEncryption。

## 示例

### 範例1：更新電子倉庫的 SoftDeleteFeatureState
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

第一個命令會取得 Vault 物件，然後將它儲存在 $vault 變數中。
第二個命令會將保存庫的 SoftDeleteFeatureState 屬性更新為「已啟用」狀態。

### 範例2：更新電子倉庫的 CMK 加密

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

第一個 Cmdlet 會取得更新加密屬性的 RSVault。 第二個 Cmdlet 會取得 azure 金鑰保存庫。 第三個 Cmdlet 會從金鑰保存庫取得金鑰。
第四個 Cmdlet 會在 RSVault 中更新客戶管理的加密金鑰。 使用-InfrastructureEncryption param 可在第一次更新時啟用基礎結構加密。 

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -SoftDeleteFeatureState
[復原服務] 保存庫的 SoftDeleteFeatureState。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyId
要用於 CMK 的加密金鑰的 KeyId。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultSubscriptionId
主要電子倉庫的訂閱 Id。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InfrastructureEncryption
在此電子倉庫上啟用基礎結構加密。 配置加密時，必須啟用基礎結構加密。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
[恢復服務] 保存庫的 ARM ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### System.object

### VaultSoftDeleteFeatureState 中的 RecoveryServices，然後再

## 輸出

### BackupResourceVaultConfigResource 中的 RecoveryServices 備份。

## 筆記

## 相關連結

[AzRecoveryServicesVault](./Get-AzRecoveryServicesVault.md)

[AzRecoveryServicesVaultProperty](./Get-AzRecoveryServicesVaultProperty.md)
