---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: fb0373e97d719535c87c01c0a4b53b029cc2a878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451799"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## 摘要
修改備份保護原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmBackupProtectionPolicy** Cmdlet 會修改現有的 Azure 備份保護原則。
您可以修改備份排程與保留原則的元件。
您所做的任何變更都會影響與原則相關的專案的備份與保留。
使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。

## 示例

### 範例1：修改備份保護原則
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

第一個命令會取得基 SchedulePolicy 物件，然後將它儲存在 $SchPol 變數中。
第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。
第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間，然後將它儲存在 $DT 變數中。
第四個命令會將 $DT 中的日期和時間新增至排程原則的排程執行時間。
第五個命令會取得基本保留原則物件，然後將它儲存在 $RetPol 變數中。
第六個命令會將保留期間設定為365天。
第七個命令會取得名為 NewPolicy 的備份保護原則，然後將它儲存在 $Pol 變數中。
最後一個命令會在 $Pol 中使用排程 $SchPol 原則，以及 $RetPol 中的保留原則來修改備份保護原則。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -原則
指定此 Cmdlet 修改的備份保護原則。
若要取得 **BackupProtectionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
指定基本保留原則。
若要取得 **RetentionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
指定基本排程原則物件。
若要取得 **SchedulePolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject 物件。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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

### PolicyBase 中的 RecoveryServices，然後再
參數：原則 (ByValue) 

### System.object
參數： VaultId (ByValue) 

## 輸出

### JobBase 中的 RecoveryServices，然後再

## 筆記

## 相關連結

[AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[新-AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[移除-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


