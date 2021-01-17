---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436318"
---
# New-AzPacketCaptureFilterConfig

## 摘要
建立新的 [資料包捕獲篩選] 物件。

## 句法

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
New-AzPacketCaptureFilterConfig Cmdlet 會建立新的 [資料包捕獲] 篩選物件。 這個物件是用來限制在資料包捕獲會話期間使用指定準則捕獲的資料包類型。 New-AzNetworkWatcherPacketCapture Cmdlet 可以接受多個篩選物件，以啟用可撰寫的捕獲會話。

## 示例

### 範例1：使用多個篩選建立資料包捕獲
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。 會話完成後，就會將它儲存到指定的儲存空間帳戶。 注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。

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

### -LocalIPAddress
指定要篩選的本機 IP 位址。
[範例] 輸入： [127.0.0.1 "代表單一位址專案。
範圍的 "127.0.0.1-127.0.0.255"。
"127.0.0.1; 127.0.0.5;" 代表多個專案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalPort
指定要篩選的本機 IP 位址。
[範例] 輸入： [127.0.0.1 "代表單一位址專案。
範圍的 "127.0.0.1-127.0.0.255"。
"127.0.0.1; 127.0.0.5;" 代表多個專案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -通訊協定
指定要篩選的通訊協定。 可接受的值 "TCP"，"UDP"，"Any"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoteIPAddress
指定要篩選的遠端 IP 位址。
[範例] 輸入： [127.0.0.1 "代表單一位址專案。
範圍的 "127.0.0.1-127.0.0.255"。
"127.0.0.1; 127.0.0.5;" 代表多個專案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemotePort
指定要篩選的遠端埠。
遠端埠範例輸入：「80」（適用于單一端口專案）。
範圍的 "80-85"。
"80; 443;" （針對多個專案）。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSPacketCaptureFilter 中的 [.]

## 筆記
關鍵字： azure、azurerm、arm、資源、管理、管理員、網路、網路、觀察者、資料包、捕獲、流量、篩選器 

## 相關連結

[新-AzNetworkWatcher](./New-AzNetworkWatcher.md)

[AzNetworkWatcher](./Get-AzNetworkWatcher.md)

[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)

[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)

[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)

[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)

[開始-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)

[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)

[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)

[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)

[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)

[新-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)

[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)

[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)

[停止 AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)

[開始-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)

[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)

[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)

[移除-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)

[新-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)

[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)

[AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)

[AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)

[AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)
