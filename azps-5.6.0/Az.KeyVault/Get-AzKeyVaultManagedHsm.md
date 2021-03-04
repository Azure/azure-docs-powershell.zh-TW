---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: b65fed5670f34072504c736283ba12e51086d3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913189"
---
# Get-AzKeyVaultManagedHsm

## 簡介
取得受管理的 HSMS。

## 語法

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzKeyVaultManagedPvm** Cmdlet 會取得訂閱中受管理的 HSMS 相關資訊。 您可以查看訂閱中所有受管理的 HSMS 實例，或根據資源群組或特定受管理的 HSM 篩選結果。
請注意，雖然當您取得單一受管理的 HSM 時，此 Cmdlet 可選擇性指定資源群組，但您應這麼做以提升績效。

## 例子

### 範例 1：取得目前訂閱中所有受管理的 HSMS
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

此命令會獲得您目前訂閱中所有受管理的 HSMS。

### 範例 2：取得特定的受管理 HSM
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

此命令會獲得您目前訂閱中名為 mym 的受管理 HSM。

### 範例 3：在資源群組中取得受管理的 HSMS
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

此命令會獲得資源群組中名為 myrg1 的所有受管理的 HSMS。

### 範例 4：使用篩選取得受管理的 HSMS
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

此命令會獲得訂閱中以 "mydm" 做為開始的所有受管理的 HSM。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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
HSM 名稱。 Cmdlet 會根據名稱和目前選取的環境來建構 HSM 的 FQDN。

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
指定與所查詢受管理的 HSM 相關聯的資源組名。

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

### -標記
指定指定標記的金鑰和選擇性值，以篩選受管理的 HSMS 清單。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.Collections.Hashtable

## 輸出

### Microsoft.Azure.Commands.KeyVault.models.PSManagedPvm

### Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultIdentityItem

## 筆記

## 相關連結

[New-AzKeyVaultManagedPvm](./New-AzKeyVaultManagedHsm.md)

[Remove-AzKeyVaultManagedPvm](./Remove-AzKeyVaultManagedHsm.md)

[Update-AzKeyVaultManagedPvm](./Update-AzKeyVaultManagedHsm.md)