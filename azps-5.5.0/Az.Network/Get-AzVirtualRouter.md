---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131322"
---
# Get-AzVirtualRouter

## 摘要
取得 Azure VirtualRouter

## 句法

### VirtualRouterSubscriptionIdParameterSet (預設) 
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VirtualRouterNameParameterSet
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VirtualRouterResourceIdParameterSet
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzVirtualRouter** Cmdlet 會取得 Azure VirtualRouter

## 示例

### 範例1
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### 範例2
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

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

### -ResourceGroupName
虛擬路由器的資源組名稱。

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
虛擬路由器的 ResourceId。

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouterName
虛擬路由器的名稱。

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

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

## 輸出

### PSVirtualRouter 中的 [.]

## 筆記

## 相關連結
