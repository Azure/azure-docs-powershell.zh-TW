---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: f406ddbf3e975e6caa3d9e9164673ec95a311e76
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400173"
---
# <span data-ttu-id="c40e1-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="c40e1-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="c40e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c40e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c40e1-103">建立新的網路組配置診斷設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="c40e1-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="c40e1-104">此物件會使用指定的準則，在診斷會話期間限制網路問題。</span><span class="sxs-lookup"><span data-stu-id="c40e1-104">This object is used to restrict the network confiuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="c40e1-105">語法</span><span class="sxs-lookup"><span data-stu-id="c40e1-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c40e1-106">描述</span><span class="sxs-lookup"><span data-stu-id="c40e1-106">DESCRIPTION</span></span>
<span data-ttu-id="c40e1-107">Cmdlet New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile會建立一個新的診斷設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="c40e1-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="c40e1-108">此物件用於使用指定準則在網路組配置診斷會話期間限制網路問題。</span><span class="sxs-lookup"><span data-stu-id="c40e1-108">This object is used to restrict the network confiuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="c40e1-109">例子</span><span class="sxs-lookup"><span data-stu-id="c40e1-109">EXAMPLES</span></span>

### <span data-ttu-id="c40e1-110">範例 1：針對 VM 和指定的網路設定檔啟動網路組配置診斷會話</span><span class="sxs-lookup"><span data-stu-id="c40e1-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="c40e1-111">參數</span><span class="sxs-lookup"><span data-stu-id="c40e1-111">PARAMETERS</span></span>

### <span data-ttu-id="c40e1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40e1-112">-DefaultProfile</span></span>
<span data-ttu-id="c40e1-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c40e1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c40e1-114">-目的地</span><span class="sxs-lookup"><span data-stu-id="c40e1-114">-Destination</span></span>
<span data-ttu-id="c40e1-115">流量目的地。</span><span class="sxs-lookup"><span data-stu-id="c40e1-115">Traffic destination.</span></span>
<span data-ttu-id="c40e1-116">接受的值為：'\*'、IP 位址/CIDR、服務標記。</span><span class="sxs-lookup"><span data-stu-id="c40e1-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e1-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c40e1-117">-DestinationPort</span></span>
<span data-ttu-id="c40e1-118">流量目的地埠。</span><span class="sxs-lookup"><span data-stu-id="c40e1-118">Traffic destination port.</span></span>
<span data-ttu-id="c40e1-119">接受的值為 '\*'、埠 (例如 3389) 和埠範圍 (例如 80-100) 。</span><span class="sxs-lookup"><span data-stu-id="c40e1-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e1-120">-方向</span><span class="sxs-lookup"><span data-stu-id="c40e1-120">-Direction</span></span>
<span data-ttu-id="c40e1-121">交通路線。</span><span class="sxs-lookup"><span data-stu-id="c40e1-121">The direction of the traffic.</span></span>
<span data-ttu-id="c40e1-122">接受的值為 '輸入'和 'Outbound'</span><span class="sxs-lookup"><span data-stu-id="c40e1-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e1-123">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="c40e1-123">-Protocol</span></span>
<span data-ttu-id="c40e1-124">要驗證的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c40e1-124">Protocol to be verified on.</span></span>
<span data-ttu-id="c40e1-125">接受的值為'\*'、TCP、UDP。</span><span class="sxs-lookup"><span data-stu-id="c40e1-125">Accepted values are '\*', TCP, UDP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e1-126">-來源</span><span class="sxs-lookup"><span data-stu-id="c40e1-126">-Source</span></span>
<span data-ttu-id="c40e1-127">流量來源。</span><span class="sxs-lookup"><span data-stu-id="c40e1-127">Traffic source.</span></span>
<span data-ttu-id="c40e1-128">接受的值為'\*'、IP 位址/CIDR、服務標記。</span><span class="sxs-lookup"><span data-stu-id="c40e1-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40e1-129">CommonParameters</span></span>
<span data-ttu-id="c40e1-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c40e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40e1-131">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c40e1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40e1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c40e1-132">INPUTS</span></span>

### <span data-ttu-id="c40e1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c40e1-133">System.String</span></span>

## <span data-ttu-id="c40e1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c40e1-134">OUTPUTS</span></span>

### <span data-ttu-id="c40e1-135">Microsoft.Azure.Commands.Network.models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="c40e1-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="c40e1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c40e1-136">NOTES</span></span>
<span data-ttu-id="c40e1-137">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、監視者、診斷、設定檔</span><span class="sxs-lookup"><span data-stu-id="c40e1-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="c40e1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c40e1-138">RELATED LINKS</span></span>

[<span data-ttu-id="c40e1-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c40e1-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c40e1-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c40e1-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c40e1-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c40e1-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c40e1-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c40e1-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c40e1-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c40e1-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c40e1-144">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="c40e1-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c40e1-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c40e1-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c40e1-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c40e1-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c40e1-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c40e1-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c40e1-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c40e1-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c40e1-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c40e1-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c40e1-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c40e1-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c40e1-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c40e1-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c40e1-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c40e1-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c40e1-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c40e1-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c40e1-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c40e1-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c40e1-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c40e1-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c40e1-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c40e1-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c40e1-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c40e1-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c40e1-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c40e1-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c40e1-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c40e1-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c40e1-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c40e1-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c40e1-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c40e1-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c40e1-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c40e1-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c40e1-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c40e1-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c40e1-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c40e1-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c40e1-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c40e1-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
