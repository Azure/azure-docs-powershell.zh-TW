---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 0ba43a38763252275d7461f11cc4db574720ba5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450555"
---
# New-AzureRmOperationalInsightsWorkspace

## 摘要
建立工作區。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmOperationalInsightsWorkspace** Cmdlet 會在指定的資源群組和位置中建立一個工作區。

## 示例

### 範例1：依名稱建立工作區
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

這個命令會在名為 [ContosoResourceGroup] 的資源群組中，建立名為 MyWorkspace 的標準 SKU 工作區。

### 範例2：建立工作區並將其連結至現有的帳戶
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

第一個命令使用 Get-AzureRmOperationalInsightsLinkTargets Cmdlet 來取得 Operational Insights 帳戶連結目標，然後將它們儲存在 $OILinkTargets 變數中。

第二個命令會使用管線運算子，將 $OILinkTargets 中的第一個帳戶連結目標傳遞給 **AzureRmOperationalInsightsWorkspace** Cmdlet。
此命令會建立一個名為 MyWorkspace 的標準 SKU 工作區，該工作區已連結至 $OILinkTargets 中第一個 Operational Insights 帳戶。

## 參數

### -CustomerId
指定此工作區將連結到哪個帳戶。
您也可以使用 Get-AzureRmOperationalInsightsLinkTargets Cmdlet 來列出潛在的帳戶。

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定要建立工作區的位置，例如 [東美國] 或 [西部]。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定工作區的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源群組的名稱。
工作區是在此資源群組中建立。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
工作區資料保留天數（天）。 730 days 是所有其他 Sku 允許的上限

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
指定工作區的服務層級。
有效值為： 

- 空閒
- 標準
- 佳

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
工作區的資源標記。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSWorkspace 中的 OperationalInsights。

## 筆記

## 相關連結

[Azure Operational Insights Cmdlet](./AzureRM.OperationalInsights.md)

[AzureRmOperationalInsightsLinkTargets](./Get-AzureRmOperationalInsightsLinkTargets.md)


