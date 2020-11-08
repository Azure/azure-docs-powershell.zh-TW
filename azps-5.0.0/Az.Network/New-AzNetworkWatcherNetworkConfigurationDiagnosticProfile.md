---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137420"
---
# <span data-ttu-id="f4f09-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="f4f09-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="f4f09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4f09-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f09-103">建立新的網路設定診斷設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="f4f09-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="f4f09-104">這個物件是用來在診斷會話期間使用指定準則來限制網路設定。</span><span class="sxs-lookup"><span data-stu-id="f4f09-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="f4f09-105">句法</span><span class="sxs-lookup"><span data-stu-id="f4f09-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4f09-106">說明</span><span class="sxs-lookup"><span data-stu-id="f4f09-106">DESCRIPTION</span></span>
<span data-ttu-id="f4f09-107">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile Cmdlet 會建立新的診斷設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="f4f09-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="f4f09-108">這個物件是用來在網路設定診斷會話期間使用指定準則來限制網路設定。</span><span class="sxs-lookup"><span data-stu-id="f4f09-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="f4f09-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4f09-109">EXAMPLES</span></span>

### <span data-ttu-id="f4f09-110">範例1：針對 VM 與指定的網路設定檔喚醒呼叫網路設定診斷會話</span><span class="sxs-lookup"><span data-stu-id="f4f09-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="f4f09-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4f09-111">PARAMETERS</span></span>

### <span data-ttu-id="f4f09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f09-112">-DefaultProfile</span></span>
<span data-ttu-id="f4f09-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4f09-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f09-114">-目的地</span><span class="sxs-lookup"><span data-stu-id="f4f09-114">-Destination</span></span>
<span data-ttu-id="f4f09-115">流量目的地。</span><span class="sxs-lookup"><span data-stu-id="f4f09-115">Traffic destination.</span></span>
<span data-ttu-id="f4f09-116">已接受的值為： ' \* '、IP 位址/CIDR、服務標記。</span><span class="sxs-lookup"><span data-stu-id="f4f09-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="f4f09-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f4f09-117">-DestinationPort</span></span>
<span data-ttu-id="f4f09-118">流量目的地埠。</span><span class="sxs-lookup"><span data-stu-id="f4f09-118">Traffic destination port.</span></span>
<span data-ttu-id="f4f09-119">已接受的值為 ' \* '、埠 (例如 3389) 和埠範圍 (例如 80-100) 。</span><span class="sxs-lookup"><span data-stu-id="f4f09-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="f4f09-120">方向</span><span class="sxs-lookup"><span data-stu-id="f4f09-120">-Direction</span></span>
<span data-ttu-id="f4f09-121">流量的方向。</span><span class="sxs-lookup"><span data-stu-id="f4f09-121">The direction of the traffic.</span></span>
<span data-ttu-id="f4f09-122">已接受的值為 "Inbound" 和 "呼出"</span><span class="sxs-lookup"><span data-stu-id="f4f09-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="f4f09-123">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f4f09-123">-Protocol</span></span>
<span data-ttu-id="f4f09-124">要驗證的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f4f09-124">Protocol to be verified on.</span></span>
<span data-ttu-id="f4f09-125">已接受的值為 ' \* '、TCP、UDP。</span><span class="sxs-lookup"><span data-stu-id="f4f09-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="f4f09-126">-來源</span><span class="sxs-lookup"><span data-stu-id="f4f09-126">-Source</span></span>
<span data-ttu-id="f4f09-127">[交通來源]。</span><span class="sxs-lookup"><span data-stu-id="f4f09-127">Traffic source.</span></span>
<span data-ttu-id="f4f09-128">已接受的值為 ' \* '、IP 位址/CIDR、服務標記。</span><span class="sxs-lookup"><span data-stu-id="f4f09-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="f4f09-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f09-129">CommonParameters</span></span>
<span data-ttu-id="f4f09-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4f09-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f09-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4f09-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f09-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f4f09-132">INPUTS</span></span>

### <span data-ttu-id="f4f09-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f4f09-133">System.String</span></span>

## <span data-ttu-id="f4f09-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f4f09-134">OUTPUTS</span></span>

### <span data-ttu-id="f4f09-135">PSNetworkConfigurationDiagnosticProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4f09-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="f4f09-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f4f09-136">NOTES</span></span>
<span data-ttu-id="f4f09-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，診斷，設定檔</span><span class="sxs-lookup"><span data-stu-id="f4f09-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="f4f09-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4f09-138">RELATED LINKS</span></span>

[<span data-ttu-id="f4f09-139">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4f09-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f4f09-140">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4f09-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f4f09-141">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4f09-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f4f09-142">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f4f09-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f4f09-143">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f4f09-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f4f09-144">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f4f09-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f4f09-145">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f4f09-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f4f09-146">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4f09-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4f09-147">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f4f09-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f4f09-148">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4f09-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4f09-149">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4f09-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4f09-150">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4f09-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4f09-151">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4f09-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f4f09-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f4f09-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f4f09-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f4f09-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f4f09-154">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4f09-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f4f09-155">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4f09-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f4f09-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4f09-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f4f09-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f4f09-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f4f09-158">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4f09-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f4f09-159">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4f09-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f4f09-160">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f4f09-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f4f09-161">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f4f09-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f4f09-162">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f4f09-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f4f09-163">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f4f09-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f4f09-164">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f4f09-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f4f09-165">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4f09-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
