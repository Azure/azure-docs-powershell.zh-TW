---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282703"
---
# Get-AzServiceEndpointPolicy

## 摘要
取得服務端點原則。

## 句法

### ListParameterSet (預設) 
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzServiceEndpointPolicy** Cmdlet 會取得服務端點原則。

## 示例

### 範例1
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

這個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 ServiceEndpointPolicy1 的服務端點原則，並將它儲存在 $policy 變數中。

### 範例2
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

這個命令會在名為 ResourceGroup01 的資源群組中取得所有服務端點原則的清單，並將它儲存在 $policyList 變數中。

### 範例3
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

這個命令會取得以 "ServiceEndpointPolicy" 開頭的所有服務端點原則的清單。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
服務端點原則的名稱

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceId
服務端點原則的識別碼。

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSServiceEndpointPolicy 中的 [.]

## 筆記

## 相關連結

[新-AzServiceEndpointPolicy](./New-AzServiceEndpointPolicy.md)

[移除-AzServiceEndpointPolicy](./Remove-AzServiceEndpointPolicy.md)

[Set-AzServiceEndpointPolicy](./Set-AzServiceEndpointPolicy.md)
