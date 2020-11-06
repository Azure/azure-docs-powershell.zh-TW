---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 15775f23a205257505d812c5f0493f9f7c124c2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451603"
---
# New-AzureRmLoadBalancerInboundNatRuleConfig

## 摘要
為負載平衡器建立入站 NAT 規則配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### SetByResourceId
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器建立入站網路位址轉譯 (NAT) 規則配置。

## 示例

### 範例1：為負載平衡器建立入站 NAT 規則配置
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

第一個命令會在名為 MyResourceGroup 的資源群組中建立名為 MyPublicIP 的公用 IP 位址，然後將它儲存在 $publicip 變數中。

第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定，然後將其儲存在 $frontend 變數中。

第三個命令會在 $frontend 中使用前端物件來建立名為 MyInboundNatRule 的輸入 NAT 規則配置。
已指定 TCP 通訊協定，而前端埠是3389，這種情況與後端埠相同。
*FrontendIpConfiguration* 、 *Procotol* 、 *FrontendPort* 和 *BACKENDPORT* 參數都是建立入站 NAT 規則設定所必需的。

## 參數

### -BackendPort
指定此規則設定所相符之流量的後端埠。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableFloatingIP
表示此 Cmdlet 為規則設定啟用浮動 IP 位址。

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

### -FrontendIpConfiguration
指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendIpConfigurationId
指定前端 IP 位址設定的 ID。

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPort
指定與負載平衡器規則配置相符的前端埠。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所建立之規則配置的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
指定通訊協定。
此參數可接受的值為：

- Tcp-out
- Udp-in

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### PSInboundNatRule 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmLoadBalancerInboundNatRuleConfig](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[AzureRmLoadBalancerInboundNatRuleConfig](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[新-AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[新-AzureRmPublicIpAddress](./New-AzureRmPublicIpAddress.md)

[移除-AzureRmLoadBalancerInboundNatRuleConfig](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[Set-AzureRmLoadBalancerInboundNatRuleConfig](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


