---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: ce4550d4b0b0206db3a28f11a58ac4384ecbac60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445743"
---
# New-AzureRmBackupProtectionPolicy

## 摘要
建立備份原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### NoScheduleParamSet (預設) 
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmBackupProtectionPolicy** Cmdlet 會建立 azure 備份原則做為 azure PowerShell 物件。
備份原則定義備份專案的時間和頻率。
Enable-AzureRmBackupProtection Cmdlet 使用備份原則。

## 示例

### 範例1：建立每日及每月保留的每日備份原則
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。
第二個命令會建立一個保留原則，每日保留30天，然後將它儲存在 $Daily 變數中。
第三個命令會建立保留原則，每個月的第10個和第二十個是12個月的備份。
該命令會將保留原則儲存在 $Monthly 變數中。
最後一個命令會在 $Vault 的每日備份時間為 3:00 PM 的電子倉庫中建立備份原則。
該命令會指派儲存在 $Daily 和 $Monthly 中的保留原則。
該命令會將結果儲存在 $ProtectionPolicy 變數中。

## 參數

### -BackupTime
指定當天的時間（作為 **DateTime** 物件），以進行備份操作。
若要取得 **DateTime** ，請使用 Get-Date Cmdlet。
如需 **DateTime** 物件的相關資訊，請輸入 `Get-Help Get-Date` 。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 每日
表示備份作業是在每日排程上執行。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
指定一周中的天數陣列。
此原則會在此參數指定的天數上執行備份。
此參數可接受的值為：
- 從 
- 星期二 
- 星期三 
- 星期四 
- 日 
- 星期六 
- 星期天如果您指定 [ *每週* ] 參數，請指定此參數。

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -名稱
指定備份原則的名稱。
選取在電子倉庫中唯一的名稱。

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
指定備份原則的保留原則陣列。
若要取得 **AzureRmBackupRetentionPolicy** ，請使用 New-AzureRmBackupRetentionPolicyObject Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -類型
指定原則所套用的備份專案類型。
目前唯一支援的值為 Add-azurevm。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -保存庫
指定備份原則所屬的 Azure 備份電子倉庫。
若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -每週
表示每週一個或多天觸發備份原則。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### System.object

### System.object []

### AzureRMBackupRetentionPolicy [] 的 AzureBackup []

### AzureRMBackupVault 中的 AzureBackup。
參數：保存庫 (ByValue) 

## 輸出

### AzureRMBackupProtectionPolicy 中的 AzureBackup。

## 筆記
* 所有

## 相關連結

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[新-AzureRmBackupRetentionPolicyObject](./New-AzureRmBackupRetentionPolicyObject.md)

[移除-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)

[Set-AzureRmBackupProtectionPolicy](./Set-AzureRmBackupProtectionPolicy.md)


