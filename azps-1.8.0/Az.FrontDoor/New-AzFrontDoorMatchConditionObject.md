---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787789"
---
# New-AzFrontDoorMatchConditionObject

## 摘要
建立 WAF 原則建立的 MatchCondition 物件

## 句法

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
建立 WAF 原則建立的 MatchCondition 物件

## 示例

### 範例1
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

建立 MatchCondition 物件

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

### -MatchValue
[相符] 值。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MatchVariable
[相符] 變數。
可能的值包括： "RemoteAddr"、"RequestMethod"、"QueryString"、"PostArgs"、"RequestUri"、"RequestHeader"、"RequestBody"

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NegateCondition
描述此情況是否為 [否定] 條件，或 [非預設值] 為 false

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatorProperty
描述要相符的運算子。
可能的值包括： [Any]、"IPMatch"、"GeoMatch"、"等於"、"Contains"、"小於"、"GreaterThan"、"LessThanOrEqual"、"GreaterThanOrEqual"、"BeginsWith"、"EndsWith"、""、"" "

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -選取器
要相符的 RequestHeader 或 RequestBody 中的選擇器名稱

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### PSMatchCondition 中的 FrontDoor。

## 筆記

## 相關連結

[新-AzFrontDoorCustomRuleObject](./New-AzFrontDoorCustomRuleObject.md)
