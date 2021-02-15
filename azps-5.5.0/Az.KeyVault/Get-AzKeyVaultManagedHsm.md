---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129238"
---
# Get-AzKeyVaultManagedHsm

## 摘要
取得受管理的 Hsm。

## 句法

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzKeyVaultManagedHsm** Cmdlet 會取得訂閱中受管理的 hsm 的相關資訊。 您可以在訂閱中查看所有受管理的 Hsm 實例，或依據資源群組或特定受管理的 HSM 來篩選結果。
請注意，雖然在您取得單一受管理的 HSM 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做以取得較佳的效能。

## 示例

### 範例1：在您目前的訂閱中取得所有受管理的 Hsm
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

這個命令會在您目前的訂閱中取得所有受管理的 Hsm。

### 範例2：取得特定的受管理 HSM
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

這個命令會在您目前的訂閱中取得名為 myhsm 的受管理 HSM。

### 範例3：在資源群組中取得受管理的 Hsm
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

這個命令會取得名為 myrg1 的資源群組中的所有受管理的 Hsm。

### 範例4：使用篩選來取得受管理的 Hsm
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

這個命令會取得訂閱中以 "myhsm" 為開頭的所有 managed Hsm。

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

### -名稱
HSM 名稱。 Cmdlet 根據名稱和目前所選的環境來構造 HSM 的 FQDN。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
指定與被查詢之受管理的 HSM 相關聯的資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Tag
指定指定標記的索引鍵和選用值，以篩選受管理的 Hsm 清單。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

## 輸出

### PSManagedHsm 中的 KeyVault。

### PSKeyVaultIdentityItem 中的 KeyVault。

## 筆記

## 相關連結

[新-AzKeyVaultManagedHsm](./New-AzKeyVaultManagedHsm.md)

[移除-AzKeyVaultManagedHsm](./Remove-AzKeyVaultManagedHsm.md)

[更新-AzKeyVaultManagedHsm](./Update-AzKeyVaultManagedHsm.md)