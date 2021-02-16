---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: e717c32b817dc86de2bfa1b9de09b95121609f28
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416153"
---
# <span data-ttu-id="e7e10-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e7e10-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="e7e10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7e10-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e10-103">會針對指定的來源 VM 和目的地，返回連接資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e10-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="e7e10-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7e10-104">SYNTAX</span></span>

### <span data-ttu-id="e7e10-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e7e10-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7e10-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e7e10-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7e10-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e7e10-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e10-108">描述</span><span class="sxs-lookup"><span data-stu-id="e7e10-108">DESCRIPTION</span></span>
<span data-ttu-id="e7e10-109">Cmdlet Test-AzNetworkWatcherConnectivity會針對指定的來源 VM 和目的地，會返回連接資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e10-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="e7e10-110">如果來源和目的地之間無法建立連接，Cmdlet 會返回問題的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e10-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="e7e10-111">例子</span><span class="sxs-lookup"><span data-stu-id="e7e10-111">EXAMPLES</span></span>

### <span data-ttu-id="e7e10-112">範例 1：測試從 VM 到網站的網路監視程式連接</span><span class="sxs-lookup"><span data-stu-id="e7e10-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="e7e10-113">在此範例中，我們會測試從 Azure 中的 VM 到 www.bing.com。</span><span class="sxs-lookup"><span data-stu-id="e7e10-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="e7e10-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="e7e10-114">Example 2</span></span>

<span data-ttu-id="e7e10-115">會針對指定的來源 VM 和目的地，返回連接資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e10-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="e7e10-116"> (自動) </span><span class="sxs-lookup"><span data-stu-id="e7e10-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="e7e10-117">參數</span><span class="sxs-lookup"><span data-stu-id="e7e10-117">PARAMETERS</span></span>

### <span data-ttu-id="e7e10-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7e10-118">-AsJob</span></span>
<span data-ttu-id="e7e10-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e7e10-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7e10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e10-120">-DefaultProfile</span></span>
<span data-ttu-id="e7e10-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7e10-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7e10-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e7e10-122">-DestinationAddress</span></span>
<span data-ttu-id="e7e10-123">嘗試進行連接之資源的 IP 位址或 URI。</span><span class="sxs-lookup"><span data-stu-id="e7e10-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="e7e10-124">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="e7e10-124">-DestinationId</span></span>
<span data-ttu-id="e7e10-125">嘗試進行連接之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7e10-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="e7e10-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e7e10-126">-DestinationPort</span></span>
<span data-ttu-id="e7e10-127">執行檢查連接之埠。</span><span class="sxs-lookup"><span data-stu-id="e7e10-127">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="e7e10-128">-位置</span><span class="sxs-lookup"><span data-stu-id="e7e10-128">-Location</span></span>
<span data-ttu-id="e7e10-129">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="e7e10-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e7e10-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e7e10-130">-NetworkWatcher</span></span>
<span data-ttu-id="e7e10-131">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="e7e10-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="e7e10-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e7e10-132">-NetworkWatcherName</span></span>
<span data-ttu-id="e7e10-133">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7e10-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e10-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7e10-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="e7e10-135">將執行檢查連接之通訊協定組。</span><span class="sxs-lookup"><span data-stu-id="e7e10-135">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e10-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e10-136">-ResourceGroupName</span></span>
<span data-ttu-id="e7e10-137">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7e10-137">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e10-138">-SourceId</span><span class="sxs-lookup"><span data-stu-id="e7e10-138">-SourceId</span></span>
<span data-ttu-id="e7e10-139">將啟動連接檢查的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7e10-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="e7e10-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e7e10-140">-SourcePort</span></span>
<span data-ttu-id="e7e10-141">將執行連接檢查的來源埠。</span><span class="sxs-lookup"><span data-stu-id="e7e10-141">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e10-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e10-142">CommonParameters</span></span>
<span data-ttu-id="e7e10-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7e10-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e10-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e7e10-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e10-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e7e10-145">INPUTS</span></span>

### <span data-ttu-id="e7e10-146">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e7e10-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e7e10-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e7e10-147">System.String</span></span>

### <span data-ttu-id="e7e10-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e7e10-148">System.Int32</span></span>

## <span data-ttu-id="e7e10-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e7e10-149">OUTPUTS</span></span>

### <span data-ttu-id="e7e10-150">Microsoft.Azure.Commands.Network.models.PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="e7e10-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="e7e10-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e7e10-151">NOTES</span></span>
<span data-ttu-id="e7e10-152">關鍵字：azure、azurerm、arm、資源、連接、管理、管理員、網路、網路、網路監視者</span><span class="sxs-lookup"><span data-stu-id="e7e10-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e7e10-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7e10-153">RELATED LINKS</span></span>

<span data-ttu-id="e7e10-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="e7e10-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="e7e10-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[Get-AzNetworkWatcherTopwork](./Get-AzNetworkWatcherTopology.md) 
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="e7e10-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="e7e10-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="e7e10-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="e7e10-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="e7e10-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>
