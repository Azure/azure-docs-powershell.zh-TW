---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447166"
---
# Get-AzureRmBackupRecoveryPoint

## 摘要
取得已備份專案的復原點。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmBackupRecoveryPoint** Cmdlet 會取得已備份之 Azure 備份專案的復原點。
備份專案之後，備份會儲存一或多個復原點。

## 示例

### 範例1：取得專案的復原點
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。

第二個命令會在 $Vault 中使用 **AzureRmBackupContainer** Cmdlet，透過電子倉庫中的指定名稱取得容器。
該命令會將該物件儲存在 $Container 變數中。

第三個命令會使用 **AzureRmBackupItem** Cmdlet，在 $Container 中取得容器中的備份專案。
該命令會將該物件儲存在 $BackupItem 變數中。

最終命令會在 $BackupItem 中取得專案的復原點。

## 參數

### -專案
指定此 Cmdlet 取得復原點的專案。
若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。

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

### -RecoveryPointId
指定此 Cmdlet 取得的復原點識別碼。

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

### AzureRmBackupItem

## 輸出

### AzureRmBackupRecoveryPoint

## 筆記

## 相關連結

[AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[AzureRmBackupVault](./Get-AzureRmBackupVault.md)


