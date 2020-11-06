---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451844"
---
# New-AzureRmDelegation

## 摘要
建立服務委派。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**新的-AzureRmDelegation** Cmdlet 會建立可新增至子網的服務委派。

## 示例

### 範例1
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

第一個 Cmdlet 會建立可新增至子網的委派，並將它儲存在 $delegation 變數中。 第二個和第三個 Cmdlet 會檢索要委派的子網。 第四個 Cmdlet 會將建立的委派新增到感興趣的子網上，而最後的 Cmdlet 會將更新的設定傳送至伺服器。

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
應該委派子網之服務的名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。
如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### Microsoft.Azure.Commands.Network.Models.PSDelegation

## 筆記

## 相關連結
[附加 AzureRmDelegation](./Add-AzureRmDelegation.md) 
[AzureRmDelegation](./Get-AzureRmDelegation.md) 
[移除-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
[AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)
