---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: b7eaa3ef0c0379a0799e4091a4e808415b2f9fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447488"
---
# Remove-AzureRmBackupProtectionPolicy

## 摘要
從備份保存庫刪除原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmBackupProtectionPolicy** Cmdlet 會從 Azure 備份電子倉庫中刪除原則。
在您可以刪除備份保護原則之前，原則不能有任何相關聯的備份專案。
在您刪除原則之前，請確認每個相關專案都與其他原則相關聯。
若要將另一個原則與備份專案建立關聯，請使用 Enable-AzureRmBackupProtection Cmdlet。

## 示例

### 範例1：移除備份保護原則
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。
第二個命令會建立一個保留原則，每日保留30天，然後將它儲存在 $Daily 變數中。
第二個命令會使用 **AzureRmBackupProtectionPolicy** Cmdlet，在 $Vault 中的保存庫中，取得名為 DailyBackup 的保護原則。
該命令會將原則傳遞給目前的 Cmdlet。
該 Cmdlet 會移除原則。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

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

### -ProtectionPolicy
指定此 Cmdlet 移除的保護原則。
若要取得 **AzureRmBackupProtectionPolicy** ，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRMBackupProtectionPolicy 中的 AzureBackup。
參數： ProtectionPolicy (ByValue) 

## 輸出

### System.void

## 筆記

## 相關連結

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[新-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


