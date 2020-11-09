---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284696"
---
# Backup-AzManagedHsmKey

## 摘要
備份受管理的 HSM 中的金鑰。

## 句法

### ByKeyName (預設) 
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzManagedHsmKey** Cmdlet 會將指定的金鑰下載並儲存在檔案中，以備份受管理 HSM 中的金鑰。
如果有多個版本的金鑰，所有版本都包含在備份中。
因為下載的內容是經過加密的，所以無法在 Azure Managed HSM 之外使用。
您可以將備份的金鑰還原到其備份之訂閱中的任何受管理 HSM。
使用此 Cmdlet 的常見原因如下： 
- 您想要保管金鑰複本，以便您在受管理的 HSM 中不小心刪除金鑰時擁有離線複本。
 
- 您使用受管理的 HSM 建立了金鑰，現在想要將該金鑰克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。
使用 **AzManagedHsmKey** Cmdlet 以加密格式來檢索金鑰，然後使用 Restore-AzManagedHsmKey Cmdlet，並在第二個區域中指定受管理的 HSM。

## 示例

### 範例1：使用自動產生的檔案名備份金鑰
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

這個命令會從受管理的 HSM （名為 testmhsm）中檢索名為 testkey 的索引鍵，並將該金鑰的備份儲存到自動為您命名的檔案，並顯示檔案名。

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
覆寫指定的檔案（如果有的話）

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
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要備份的主要捆綁，從檢索呼叫的輸出中流水線。

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
索引鍵名稱。
Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
輸出檔案。
儲存已備份之金鑰 blob 的輸出檔案。
如果不存在，則會選取預設的檔案名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

### System.object

## 筆記

## 相關連結

[附加 AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[移除-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[復原-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[更新-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)