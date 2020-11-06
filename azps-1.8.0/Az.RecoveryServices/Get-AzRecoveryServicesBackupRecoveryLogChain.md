---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: d06cae4fc13151d8b1c5c2b0fb4dd7803606fe49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621142"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## 摘要
這個命令會列出所指定備份專案的連續記錄鏈起點和終點。 使用它來判斷使用者想要還原資料庫的時間點是否有效或不正確。

## 句法

### NoFilterParameterSet (預設) 
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzRecoveryServicesBackupRecoveryLogChain** Cmdlet 會取得備份的 Azure 備份專案在時間範圍內的復原點。
在專案已備份之後， **AzRecoveryServicesBackupRecoveryLogChain** 物件有一個或多個還原時間範圍。

## 示例

### 範例1
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

第一個命令會從七天前取得日期，然後將它儲存在 $StartDate 變數中。
第二個命令會取得今天的日期，然後將它儲存在 $EndDate 變數中。
第三個命令會取得 AzureWorkload 備份容器，並將它們儲存在 $Containers 變數中。
第四個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。
最後一個命令會針對 $BackupItem 中的專案取得復原點時間範圍陣列，然後將它們儲存在 $RP 變數中。

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

### -結束日期
需要回遷復原點之時間範圍的結束時間

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -專案
需要取得復原點的受保護的專案物件

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -開始日期
需要回遷復原點之時間範圍的開始時間

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### ItemBase 中的 RecoveryServices，然後再
System.object

## 輸出

### RecoveryPointBase 中的 RecoveryServices，然後再

## 筆記

## 相關連結