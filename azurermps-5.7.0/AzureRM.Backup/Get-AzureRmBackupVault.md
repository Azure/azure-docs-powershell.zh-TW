---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625938"
---
# Get-AzureRmBackupVault

## 摘要
取得備份保存庫。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmBackupVault** Cmdlet 會取得 Azure 備份保存庫。
這個 Cmdlet 會傳回 **AzureRmBackupVault** 物件，以與其他 Cmdlet 搭配使用。

## 示例

### 範例1：查看所有備份電子倉庫
```
PS C:\>Get-AzureRmBackupVault
```

這個命令會取得所有的 Azure 備份保存庫。

### 範例2：查看在美國西部中建立的所有電子倉庫
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

這個命令會取得所有備份保存庫。
透過使用管線運算子，命令會將它們傳遞到 Where-Object Cmdlet。
該 Cmdlet 會根據 **Region** 屬性來篩選結果。
如需詳細資訊，請輸入 `Get-Help Where-Object` 。

### 範例3：取得特定的電子倉庫
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

這個命令會取得名為 Vault03 的保存庫。

### 範例4：計算擁有本機冗余儲存空間的電子倉庫數
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

這個命令會取得所有的 Azure 備份保存庫。
該命令會將它們傳遞到物件，而 **物件** 會根據 [ **儲存空間** ] 屬性來篩選結果。
命令會將具有 LocallyRedundant 值的專案傳遞給 Measure-Object Cmdlet，以計算結果。
如需詳細資訊，請輸入 `Get-Help Measure-Object` 。

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

### -名稱
指定此 Cmdlet 取得的備份保存庫的名稱。
如果有多個備份保存庫具有相同名稱，此 Cmdlet 會將它們全部返回。
指定 *ResourceGroupName* 參數以取得唯一的保存庫。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 取得備份保存庫的 Azure 資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### AzureRmBackupVault

## 筆記
* 所有

## 相關連結

[AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[新-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[移除-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


