---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: a5de80561ee0b80c2ce825db26e1de5c6f46b80b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447473"
---
# Wait-AzureRmBackupJob

## 摘要
等待備份作業完成。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmBackupJob** Cmdlet 會等待 Azure 備份作業完成。
備份作業可能需要花很長的時間。
如果您執行的是腳本的一部份備份作業，您可能會想要強制腳本在作業完成後再繼續其他工作。
包含此 Cmdlet 的腳本可能比輪詢備份服務的作業狀態更簡單。

## 示例

## 參數

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

### -工作
指定此 Cmdlet 取消的作業。
若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -超時
指定此 Cmdlet 等候作業完成所需的最長時間（以秒為單位）。
我們建議您指定一個超時值。

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object
參數：作業 (ByValue) 

## 輸出

### AzureRMBackupJob 中的 AzureBackup。

## 筆記

## 相關連結

[AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[停止 AzureRmBackupJob](./Stop-AzureRmBackupJob.md)


