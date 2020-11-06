---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1a9eb2ef731e7ce555fbac1a08cd8468de83ebc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453631"
---
# New-AzureRmRecoveryServicesBackupProtectionPolicy

## 摘要
建立備份保護原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 會在電子倉庫中建立備份保護原則。
保護原則與至少一個保留原則相關聯。
保留原則定義了在 Azure 備份中保留復原點的時間長度。
您可以使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet 來取得預設的保留原則。
您也可以使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject Cmdlet 來取得預設的排程原則。
**SchedulePolicy** 和 **RetentionPolicy** 物件是用來做為 **新的 AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 的輸入。
使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。

## 示例

### 範例1：建立備份保護原則
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

第一個命令會取得基底 **SchedulePolicyObject** ，然後將它儲存在 $SchPol 變數中。
第二個命令會從 $SchPol 的排程原則中移除所有排程的執行時間。
第三個命令使用 Get-Date Cmdlet 來取得目前的日期和時間。
第四個命令會將目前的日期和時間 $Dt 為排程原則的排程執行時間。
第五個命令會取得基底 **RetentionPolicy** 物件，然後將它儲存在 $RetPol 變數中。
第六個命令會將 [保留期間] 原則設定為365天。
最終命令會根據先前命令建立的排程和保留原則，建立 **BackupProtectionPolicy** 物件。

## 參數

### -BackupManagementType
指定備份管理類型。
此參數可接受的值為：
- Add-azurevm 
- AzureSQLDatabase

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -名稱
指定原則的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
指定基底 **RetentionPolicy** 物件。
您可以使用 Get-AzureRmRecoveryServicesBackupRetentionPolicyObject Cmdlet 來取得 **RetentionPolicy** 物件。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
指定基底 **SchedulePolicy** 物件。
您可以使用 Get-AzureRmRecoveryServicesBackupSchedulePolicyObject Cmdlet 來取得 **SchedulePolicy** 物件。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -WorkloadType
指定工作負荷類型。
此參數可接受的值為：
- Add-azurevm 
- AzureSQLDatabase

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### WorkloadType 中的 RecoveryServices，然後再

### "RecoveryServices" 1 [[BackupManagementType]、[RecoveryServices]、[]、[Version = 4.3.1.0]、[Culture = 中立]、[PublicKeyToken = null]]

### RetentionPolicyBase 中的 RecoveryServices，然後再

### SchedulePolicyBase 中的 RecoveryServices，然後再

### System.object
參數： VaultId (ByValue) 

## 輸出

### PolicyBase 中的 RecoveryServices，然後再

## 筆記

## 相關連結

[Enable-AzureRmRecoveryServicesBackupProtection](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[AzureRmRecoveryServicesBackupSchedulePolicyObject](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[移除-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


