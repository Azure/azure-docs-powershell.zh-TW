---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: 87f269042b6d0f660f621a865dda7619afd9be5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625036"
---
# Enable-AzureRmBackupProtection

## 摘要
將專案與 Azure 備份保護原則建立關聯。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Enable-AzureRmBackupProtection** Cmdlet 會將專案與 Azure 備份保護原則建立關聯。
若要啟用保護原則，您必須先擁有現有的備份專案和現有的原則。
兩者必須屬於相同的備份保存庫。
[備份排程] 會針對專案及後續備份的增量複本進行完整的初始複本。

## 示例

### 範例1：在 Azure 虛擬機器上啟用保護
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。

第二個命令會針對 $Vault 中的電子倉庫，取得名為 DefaultPolicy 的備份保護原則。
該命令會將該物件儲存在 $Policy 變數中。

最後一個命令會使用管線運算子，將一個 Cmdlet 的值傳遞到下一個 Cmdlet。
它會使用 Get-AzureRmBackupContainer Cmdlet 來取得容器。
命令會使用 Get-AzureRmBackupItem Cmdlet 從該容器中取得備份專案。
目前的 Cmdlet 會針對命令傳遞到該 Cmdlet 的專案啟用 $Policy 中儲存的原則。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -專案
指定此 Cmdlet 針對其啟用保護的備份專案。
若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。

```yaml
Type: AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -原則
指定此 Cmdlet 與專案相關聯的保護原則。
若要取得 **AzureRmBackupProtectionPolicy** 物件，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet。

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
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

### AzureRmBackupItem

## 輸出

### AzureRmBackupJob

## 筆記

## 相關連結

[備份-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


