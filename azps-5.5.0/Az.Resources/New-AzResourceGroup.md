---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135379"
---
# New-AzResourceGroup

## 摘要
建立 Azure 資源群組。

## 句法

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzResourceGroup** Cmdlet 會建立 Azure 資源群組。
您可以只使用名稱和位置來建立資源群組，然後使用 New-AzResource Cmdlet 來建立要新增至資源群組的資源。
若要將部署新增至現有的資源群組，請使用 New-AzResourceGroupDeployment Cmdlet。 若要新增資源至現有的資源群組，請使用 **AzResource** Cmdlet。 Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。 Azure 資源群組是一個以單位形式部署的 Azure 資源集合。

## 示例

### 範例1：建立空白的資源群組
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

這個命令會建立沒有資源的資源群組。 您可以使用 **新的-AzResource** 或 **AzResourceGroupDeployment** Cmdlet，將資源和部署新增至此資源群組。

### 範例2：使用位置參數建立空白的資源群組
```
PS> New-AzResourceGroup RG01 "South Central US"
```

這個命令會建立沒有資源的資源群組。

### 範例3：使用標籤建立資源群組
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

這個命令會建立空白的資源群組。 這個命令與範例1中的命令一樣，只不過它會將標記指派給資源群組。 名為 Empty 的第一個標籤可以用來找出沒有資源的資源群組。 第二個標記為「部門」，且具有 [行銷] 的值。 您可以使用像這樣的標記，將資源群組分類以進行管理或編制預算。

## 參數

### -ApiVersion
指定資源提供者支援的 API 版本。
您可以指定不同于預設版本的版本。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -Force
強制執行命令，而不要求使用者確認。

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
指定資源群組的位置。 指定 Azure 資料中心位置，例如 [西部] 或 [東南部]。 您可以將資源群組放在任何位置。 資源群組不必須位於與您的 Azure 訂閱相同的位置，或與其資源位於相同的位置。
若要判斷哪個位置支援每個資源類型，請使用 Get-AzResourceProvider Cmdlet 與 *ProviderNamespace* 參數。

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
指定資源群組的名稱。 資源名稱在訂閱中必須是唯一的。 如果已經存在該名稱的資源群組，該命令會在您替換現有的資源群組之前提示您進行確認。

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

### -預先
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。

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

### -Tag
雜湊資料表形式的索引鍵/值對。 例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"} 若要新增或變更標記，您必須取代資源群組的標記集合。
在您指派標籤至資源和群組之後，您可以使用 Get-AzResource 和 Get-AzResourceGroup 的 *tag* 參數，依標記名稱或名稱和值來搜尋資源和群組。 您可以使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。
若要取得預先定義的標記，請使用 Get-AzTag Cmdlet。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

## 輸出

### PSResourceGroup 中的 SdkModels （）

## 筆記

## 相關連結

[AzResourceProvider](./Get-AzResourceProvider.md)

[AzResourceGroup](./Get-AzResourceGroup.md)

[新-AzResource](./New-AzResource.md)

[新-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[移除-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
