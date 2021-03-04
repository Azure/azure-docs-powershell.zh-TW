---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915558"
---
# Get-AzContainerRegistryManifest

## 簡介
取得或列出 ACR 清單。 

## 語法

### ListParameterSet (預設) 
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetParameterSet
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
取得或列出 ACR 清單。
若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`
第一。

## 例子

### 範例 1
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

在註冊表之下存放庫高山的清單清單。

### 範例 2
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

取得清單 sha256：a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.

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
清單參照。

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistryName
Azure 容器註冊表名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RepositoryName
存放庫名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.ContainerRegistry.models.PSManifestAttribute

### Microsoft.Azure.Commands.ContainerRegistry.models.PSAcrManifest

## 筆記

## 相關連結
