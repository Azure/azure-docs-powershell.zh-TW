---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916502"
---
# New-AzResourceGroup

## 簡介
建立 Azure 資源群組。

## 語法

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**New-AzResourceGroup** Cmdlet 會建立 Azure 資源群組。
您可以只使用名稱和位置來建立資源群組，然後使用 New-AzResource Cmdlet 來建立資源以新增到資源群組。
若要新增部署至現有的資源群組，請使用 New-AzResourceGroupDeployment Cmdlet。 若要將資源新增到現有的資源群組，請使用 **New-AzResource** Cmdlet。 Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。 Azure 資源群組是部署為一個單位的 Azure 資源集合。

## 例子

### 範例 1：建立空白資源群組
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

此命令會建立一個沒有資源的資源群組。 您可以使用 **New-AzResource** 或 **New-AzResourceGroupDeployment** Cmdlet 來新增資源與部署至此資源群組。

### 範例 2：使用位置參數建立空白資源群組
```
PS> New-AzResourceGroup RG01 "South Central US"
```

此命令會建立一個沒有資源的資源群組。

### 範例 3：建立具有標記的資源群組
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

此命令會建立空白資源群組。 此命令與範例 1 中的命令相同，但它會指派標記給資源群組。 第一個稱為 Empty 的標記可用來識別沒有資源的資源群組。 第二個標記名為部門，且具有行銷值。 您可以使用這個標記來將資源群組分類，以便管理或預算。

## 參數

### -ApiVersion
指定資源提供者支援的 API 版本。
您可以指定與預設版本不同的版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -強制
強制執行命令，但不要求使用者確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定資源群組的位置。 指定 Azure 資料中心位置，例如美國西部或東南亞。 您可以將資源群組放在任何位置。 資源群組不一定位於 Azure 訂閱的相同位置，也不一定位於與資源相同的位置。
若要判斷哪個位置支援每種資源類型，請使用Get-AzResourceProvider ProviderNamespace 參數的 *Cmdlet。*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定資源組的名稱。 資源名稱在訂閱中必須是唯一的。 如果具有該名稱的資源群組已存在，命令會提示您確認，然後再取代現有的資源群組。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -標記
以雜湊表格形式建立索引鍵值組。 例如：@{key0="value0";key1=$null;key2="value2"} 若要新增或變更標記，您必須取代資源群組的標記集合。
將標記指派給資源和群組後，您可以使用 Get-AzResource 和Get-AzResourceGroup 的 Tag 參數，以標記名稱或名稱和值來搜尋資源和群組。 您可以使用標記來分類資源，例如按照部門或成本中心，或追蹤資源的附注或批註。
若要取得預先定義的標籤，請使用 Get-AzTag Cmdlet。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.Collections.Hashtable

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## 筆記

## 相關連結

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
