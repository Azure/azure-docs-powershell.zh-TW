---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: a6415d941646f335ba7cae4fc2aab39d75000ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450043"
---
# New-AzureRmBackupVault

## 摘要
建立備份電子倉庫。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmBackupVault** Cmdlet 會建立 Azure 備份電子倉庫。
這個 Cmdlet 會傳回 **AzureRmBackupVault** 物件，該物件充當 vault 實體的參照。

## 示例

### 範例1：建立備份電子倉庫
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

這個命令會建立名為 Vault03 的 Azure 備份電子倉庫。
Vault 位於 [西部美國] 地區名為 [ResourceGroup01] 的資源群組中。
Vault 會使用預設的 GeoRedundant 儲存類型。

### 範例2：建立使用本機冗余儲存空間的備份電子倉庫
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

這個命令會建立名為 Vault03 的 Azure 備份電子倉庫。
Vault 位於 [西部美國] 地區名為 [ResourceGroup02] 的資源群組中。
Vault 會使用 LocallyRedundant 儲存類型。

## 參數

### -名稱
指定 Azure 備份保存庫的名稱。
名稱在資源群組中必須是唯一的。

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

### -Region
指定備份保存庫所在的 Azure 區域。
針對混合式備份案例，建議您在接近內部部署伺服器的區域中建立電子倉庫，以減少延遲。
若要將 Azure 基礎結構的備份做為服務 (IaaS) 虛擬機器，該保存庫就會成為本機虛擬機器的探索點。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 建立備份電子倉庫之現有 Azure 資源群組的名稱。
若要建立資源群組，請使用 New-AzureRMResourceGroup Cmdlet。
[資源] 群組和 [Azure 備份] 電子倉庫不需要位於同一個區域中。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 儲存空間
指定備份資料的儲存類型。
此參數可接受的值為： LocallyRedundant 和 GeoRedundant。
預設值為 GeoRedundant。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
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

### 所有

## 輸出

### AzureRmBackupVault

## 筆記
* 所有

## 相關連結

[AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[移除-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


