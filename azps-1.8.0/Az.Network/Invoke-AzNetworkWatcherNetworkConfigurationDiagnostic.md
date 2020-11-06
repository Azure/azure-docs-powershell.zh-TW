---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: a79de3beadefefd3de65b830f42e4728ca6b6b82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621884"
---
# <span data-ttu-id="4bd93-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4bd93-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="4bd93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bd93-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd93-103">針對目標資源的指定網路設定檔，喚醒呼叫網路設定診斷會話。</span><span class="sxs-lookup"><span data-stu-id="4bd93-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="4bd93-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bd93-104">SYNTAX</span></span>

### <span data-ttu-id="4bd93-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="4bd93-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd93-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4bd93-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd93-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4bd93-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd93-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd93-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd93-109">說明</span><span class="sxs-lookup"><span data-stu-id="4bd93-109">DESCRIPTION</span></span>
<span data-ttu-id="4bd93-110">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic Cmdlet 會針對目標資源的指定網路設定檔呼叫網路設定診斷會話。</span><span class="sxs-lookup"><span data-stu-id="4bd93-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="4bd93-111">示例</span><span class="sxs-lookup"><span data-stu-id="4bd93-111">EXAMPLES</span></span>

### <span data-ttu-id="4bd93-112">範例1：針對 VM 與指定的網路設定檔喚醒呼叫網路設定診斷會話</span><span class="sxs-lookup"><span data-stu-id="4bd93-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="4bd93-113">參數</span><span class="sxs-lookup"><span data-stu-id="4bd93-113">PARAMETERS</span></span>

### <span data-ttu-id="4bd93-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bd93-114">-AsJob</span></span>
<span data-ttu-id="4bd93-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bd93-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bd93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd93-116">-DefaultProfile</span></span>
<span data-ttu-id="4bd93-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bd93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd93-118">-位置</span><span class="sxs-lookup"><span data-stu-id="4bd93-118">-Location</span></span>
<span data-ttu-id="4bd93-119">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="4bd93-119">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd93-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bd93-120">-NetworkWatcher</span></span>
<span data-ttu-id="4bd93-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="4bd93-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd93-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4bd93-122">-NetworkWatcherName</span></span>
<span data-ttu-id="4bd93-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd93-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd93-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4bd93-124">-Profile</span></span>
<span data-ttu-id="4bd93-125">網路設定診斷配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="4bd93-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd93-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bd93-127">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd93-127">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd93-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd93-128">-ResourceId</span></span>
<span data-ttu-id="4bd93-129">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4bd93-129">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd93-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd93-130">-TargetResourceId</span></span>
<span data-ttu-id="4bd93-131">要執行網路設定診斷的目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4bd93-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="4bd93-132">有效的選項為 VM、NetworkInterface、VMSS/NetworkInterface 及應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4bd93-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="4bd93-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="4bd93-133">-VerbosityLevel</span></span>
<span data-ttu-id="4bd93-134">詳細等級。</span><span class="sxs-lookup"><span data-stu-id="4bd93-134">Verbosity level.</span></span>
<span data-ttu-id="4bd93-135">已接受的值為「標準」、「最小」、' 完整」。</span><span class="sxs-lookup"><span data-stu-id="4bd93-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

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

### <span data-ttu-id="4bd93-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd93-136">CommonParameters</span></span>
<span data-ttu-id="4bd93-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bd93-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd93-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bd93-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd93-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4bd93-139">INPUTS</span></span>

### <span data-ttu-id="4bd93-140">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bd93-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4bd93-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4bd93-141">System.String</span></span>

## <span data-ttu-id="4bd93-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4bd93-142">OUTPUTS</span></span>

### <span data-ttu-id="4bd93-143">PSNetworkConfigurationDiagnosticResponse 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bd93-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="4bd93-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4bd93-144">NOTES</span></span>
<span data-ttu-id="4bd93-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，診斷，設定檔</span><span class="sxs-lookup"><span data-stu-id="4bd93-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="4bd93-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bd93-146">RELATED LINKS</span></span>

[<span data-ttu-id="4bd93-147">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bd93-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4bd93-148">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bd93-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4bd93-149">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4bd93-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4bd93-150">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4bd93-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4bd93-151">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4bd93-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4bd93-152">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4bd93-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4bd93-153">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4bd93-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4bd93-154">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bd93-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bd93-155">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4bd93-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4bd93-156">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bd93-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bd93-157">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bd93-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bd93-158">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4bd93-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4bd93-159">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd93-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4bd93-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4bd93-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4bd93-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4bd93-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4bd93-162">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bd93-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4bd93-163">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bd93-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4bd93-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bd93-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4bd93-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4bd93-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4bd93-166">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bd93-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4bd93-167">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bd93-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4bd93-168">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4bd93-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4bd93-169">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4bd93-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4bd93-170">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4bd93-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4bd93-171">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4bd93-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4bd93-172">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4bd93-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4bd93-173">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4bd93-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
