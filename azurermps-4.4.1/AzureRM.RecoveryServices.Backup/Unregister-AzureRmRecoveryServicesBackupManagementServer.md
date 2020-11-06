---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453343"
---
# Unregister-AzureRmRecoveryServicesBackupManagementServer

## 摘要
從保存庫登出 SCDPM 服務器或備份伺服器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
[ **登出 AzureRmRecoveryServicesBackupManagementServer** ] Cmdlet 會從保存庫中登出) 伺服器或 Azure 備份伺服器的系統中心資料保護管理員 (SCDPM。
這個 Cmdlet 會移除未從保存庫中登出之伺服器的參考。

在您可以取消註冊容器之前，您必須刪除所有與該容器相關聯的受保護資料。

使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。

## 示例

### 範例1：從保存庫登出 SCDPM 服務器
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

第一個命令會取得名為 dpmserver01.contoso.com 的備份管理伺服器，然後將它儲存在 $BMS 變數中。

第二個命令會從保存庫登出 SCDPM 服務器。

## 參數

### -AzureRmBackupManagementServer
指定要取消註冊的 SCDPM 服務器物件。
若要取得 **BackupManagementServer** 物件，請使用 Get-AzureRmRecoveryServicesBackupManagementServer Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
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

## 輸出

## 筆記

## 相關連結

[AzureRmRecoveryServicesBackupManagementServer](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


