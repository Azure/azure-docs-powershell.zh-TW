---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452096"
---
# Remove-AzureRmRecoveryServicesVault

## 摘要
刪除恢復服務電子倉庫。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesVault** Cmdlet 會刪除 [恢復服務] 保存庫。

## 示例

### 範例1
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

刪除恢復服務電子倉庫。

## 參數

### -保存庫
指定 Azure Site Recovery 保存庫物件。

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### ARSVault
參數 "Vault" 接受來自管線的 "ARSVault" 類型值

## 輸出

### VaultOperationOutput 中的 RecoveryServices

## 筆記

## 相關連結

[AzureRmRecoveryServicesVault](./Get-AzureRmRecoveryServicesVault.md)

[AzureRmRecoveryServicesVaultSettingsFile](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[新-AzureRmRecoveryServicesVault](./New-AzureRmRecoveryServicesVault.md)


