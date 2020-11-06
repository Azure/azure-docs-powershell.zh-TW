---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: a203d125e4ff6d811a581b0713ca4a002e098ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453144"
---
# Restore-AzureRmBackupItem

## 摘要
將備份專案的資料和設定還原到復原點。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Restore-AzureRmBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。
這個 Cmdlet 會從備份電子倉庫開始還原到您的帳戶。

還原操作不會還原完整的虛擬機器。
它會復原磁碟資料和配置資訊。
還原作業完成後，您必須建立虛擬機器並啟動。

## 示例

### 範例1：將虛擬機器還原到復原點
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。

第二個命令會在 $Vault 中使用 **AzureRmBackupContainer** Cmdlet，透過電子倉庫中的指定名稱取得容器。
該命令會將該物件儲存在 $Container 變數中。

第三個命令會使用 **AzureRmBackupItem** Cmdlet，在 $Container 中取得容器中的備份專案。
該命令會將該物件儲存在 $BackupItem 變數中。

第四個命令會針對 $BackupItem 中的專案取得復原點。
該命令會將該物件儲存在 $RecoveryPoint 變數中。

最後一個命令會針對名為 DestinationAccount 的帳戶還原 $RecoveryPoint 中的復原點。

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

### -RecoveryPoint
指定要還原虛擬機器的復原點。
若要取得 **AzureRmBackupRecoveryPoint** ，請使用 Get-AzureRmBackupRecoveryPoint Cmdlet。

```yaml
Type: AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
指定訂閱中目標儲存空間帳戶的名稱。
在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRmBackupRecoveryPoint

## 輸出

### AzureRmBackupJob

## 筆記

## 相關連結

[備份-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[AzureRmBackupRecoveryPoint](./Get-AzureRmBackupRecoveryPoint.md)


