---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452776"
---
# Get-AzureRmDelegation

## 摘要
在指定的子網上取得委派 (或所有委派) 。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmDelegation** Cmdlet 會從子網上取得命名委派。 如果沒有命名委派，它會在所提供的子網上傳回所有委派。

## 示例

### 1：檢索特定委派
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

第一行會檢索感興趣的子網。 第二行顯示名為「myDelegation」的委派的委派資訊。

### 2：檢索所有子網委派
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

第一行會檢索感興趣的子網。 第二行儲存 $delegations 變數中 _mySubnet_ 的所有委派清單。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -名稱
委派的名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -子網
子網上

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。
如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSSubnet 中的 [.]

## 輸出

### Microsoft.Azure.Commands.Network.Models.PSDelegation

## 筆記

## 相關連結
[附加 AzureRmDelegation](./Add-AzureRmDelegation.md) 
[新-AzureRmDelegation](./New-AzureRmDelegation.md) 
[移除-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
[AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
