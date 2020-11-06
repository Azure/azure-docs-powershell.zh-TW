---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451907"
---
# Get-AzureRmCognitiveServicesAccountSkus

## 摘要
取得帳戶可用的 Sku。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### GetSkusWithAccount (預設) 
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetSkusWithFilter
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmCognitiveServicesAccountSkus** Cmdlet 會針對認知服務帳戶取得可用的 sku。
[SKU] 是帳戶的層級方案。
它會定義該帳戶的價格、通話限制及工資率。
F0 SKU 是免費的層級。
支付的層級包括 S0、S1、S2 等。

## 示例

### 範例1
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

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

### -位置
認知服務帳戶位置。

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定帳戶的名稱。

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定將帳戶指派給哪個資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -類型
認知服務帳戶類型。

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSCognitiveServicesSkus （CognitiveServices.）。

## 筆記

## 相關連結
