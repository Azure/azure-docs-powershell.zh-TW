---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 6ae660eae9e597d92e162529ff244431d4720418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447489"
---
# Enable-AzureRmBackupContainerReregistration

## 摘要
Reregisters 要連線至備份保存庫的伺服器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Enable-AzureRmBackupContainerReregistration** Cmdlet 會 reregisters 伺服器以連線至 Azure 備份電子倉庫，並繼續備份復原點鏈。
如果您銷毀伺服器，其所有雲端備份點都會保留在備份保存庫中。
如果您建立替換伺服器並指派相同的完整功能變數名稱，您可以將伺服器連線到相同的電子倉庫。
這個 Cmdlet 可讓備份進行備份，並將新的備份點新增到現有集合。
新的伺服器會在備份鏈中繼續。

## 示例

## 參數

### -容器
指定此 Cmdlet reregisters 的容器。
若要取得 **AzureRmBackupContainer** ，請使用 Get-AzureRmBackupContainer Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRMBackupContainer 中的 AzureBackup。
參數：容器 (ByValue) 

## 輸出

### System.void

## 筆記

## 相關連結

[AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


