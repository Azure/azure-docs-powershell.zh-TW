---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9a6999dc379a5a39acea9b17107cabf2cae5ee25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448120"
---
# Set-AzureRmLoadBalancerProbeConfig

## 摘要
設定探測器配置的目標狀態。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmLoadBalancerProbeConfig** Cmdlet 會設定探針設定的目標狀態。

## 示例

### 範例1：修改負載平衡器上的探測設定
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

第一個命令會取得名為 MyLoadBalancer 的 loadbalancer，然後將它儲存在 $slb 變數中。

第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerProbeConfig，這會將新的探針設定新增到其中。

第三個命令會將負載平衡器傳遞給 AzureRmLoadBalancerProbeConfig，以 **設定** 新的配置。
請注意，您必須指定前面命令中指定的數個相同參數，因為目前的 Cmdlet 需要它們。

## 參數

### -IntervalInSeconds
指定探測到負載平衡服務每個實例之間的間隔（以秒為單位）。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancer
指定負載平衡器。
這個 Cmdlet 會針對此參數指定的負載平衡器設定探測配置的目標狀態。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所設定的探測配置名稱。

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

### -埠
指定探測器應連接到負載平衡服務的埠。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeCount
指定實例被視為不健康的每個實例連續失敗數。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
指定要用於探測的通訊協定。
此參數可接受的值為： Tcp 或 Http。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestPath
指定負載平衡服務中要探測以判斷健康情況的路徑。

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

### PSLoadBalancer
形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值

## 輸出

### PSLoadBalancer 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmLoadBalancerProbeConfig](./Add-AzureRmLoadBalancerProbeConfig.md)

[AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[AzureRmLoadBalancerProbeConfig](./Get-AzureRmLoadBalancerProbeConfig.md)

[新-AzureRmLoadBalancerProbeConfig](./New-AzureRmLoadBalancerProbeConfig.md)

[移除-AzureRmLoadBalancerProbeConfig](./Remove-AzureRmLoadBalancerProbeConfig.md)


