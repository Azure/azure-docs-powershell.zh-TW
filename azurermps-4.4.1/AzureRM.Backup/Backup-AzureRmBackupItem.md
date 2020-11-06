---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446891"
---
# Backup-AzureRmBackupItem

## 摘要
啟動備份專案的備份。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmBackupItem** Cmdlet 會針對受保護的 Azure 備份專案（未與備份排程關聯）啟動備份。
您可以在啟用保護後立即執行初始備份，或在排程備份失敗後啟動備份。

如果現有的備份作業正在執行，此 Cmdlet 會失敗。

## 示例

### 範例1：開始備份虛擬機器
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。

第二個命令會在 $Vault 中使用 Get-AzureRmBackupContainer Cmdlet，透過電子倉庫中的指定名稱來取得容器。
該命令會將該物件儲存在 $Container 變數中。

最後一個命令會使用 Get-AzureRmBackupItem Cmdlet，在 $Container 中取得備份專案。
命令會使用管線運算子將專案傳遞至目前的 Cmdlet。
目前的 Cmdlet 會開始備份容器中的虛擬機器。

## 參數

### -專案
指定此 Cmdlet 啟動備份操作的備份專案。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRMBackupItem

## 輸出

### AzureRmBackupJob

## 筆記

## 相關連結

[AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Restore-AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


