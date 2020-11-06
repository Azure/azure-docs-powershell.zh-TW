---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447479"
---
# Set-AzureRmBackupProtectionPolicy

## 摘要
修改現有的保護原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### NoScheduleParamSet (預設) 
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmBackupProtectionPolicy** Cmdlet 會修改 Azure 備份中的現有保護原則。
您可以修改下列保護原則元件： 
- 列名
- 備份排程
- 保留原則任何變更都可能會影響與原則相關的專案的備份與保留。

## 示例

## 參數

### -BackupTime
為原則指定一天的新備份時間（作為 **DateTime** 物件）。
若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。
如需 **DateTime** 物件的相關資訊，請輸入 `Get-Help Get-Date` 。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 每日
表示備份作業是在每日排程上執行。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
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
- 日

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
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

### -NewName
指定原則的新名稱。
此名稱在電子倉庫中必須是唯一的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionPolicy
指定此 Cmdlet 修改的保護原則。
若要取得 **AzureRmBackupProtectionPolicy** 物件，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet。

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

### -RetentionPolicy
指定備份原則的保留原則陣列。
若要取得 **AzureRmBackupRetentionPolicy** 物件，請使用 New-AzureRmBackupRetentionPolicyObject Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -每週
表示備份作業是在每週排程上執行。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRMBackupProtectionPolicy 中的 AzureBackup。
參數： ProtectionPolicy (ByValue) 

## 輸出

### AzureRMBackupJob 中的 AzureBackup。

## 筆記

## 相關連結

[新-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


