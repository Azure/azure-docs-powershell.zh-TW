---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: b3732167d26f35b0e3e8ac6c29f187138cde0b18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902401"
---
# <span data-ttu-id="ae6e7-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae6e7-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="ae6e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6e7-103">建立新封包捕獲篩選物件。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="ae6e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae6e7-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="ae6e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6e7-106">Cmdlet New-AzPacketCaptureFilterConfig建立一個新的封包捕獲篩選物件。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="ae6e7-107">此物件用來限制使用指定準則在封包捕獲會話期間所捕獲的封包類型。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="ae6e7-108">Cmdlet New-AzNetworkWatcherPacketCapture接受多個篩選物件，以啟用可撰寫的捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="ae6e7-109">例子</span><span class="sxs-lookup"><span data-stu-id="ae6e7-109">EXAMPLES</span></span>

### <span data-ttu-id="ae6e7-110">範例 1：建立包含多個篩選的封包捕獲</span><span class="sxs-lookup"><span data-stu-id="ae6e7-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="ae6e7-111">在此範例中，我們建立名為「PacketCaptureTest」的封包捕獲，具有多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="ae6e7-112">會話完成之後，就會儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="ae6e7-113">注意：Azure 網路監視程式擴充功能必須安裝在目標虛擬機器上，以建立封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="ae6e7-114">參數</span><span class="sxs-lookup"><span data-stu-id="ae6e7-114">PARAMETERS</span></span>

### <span data-ttu-id="ae6e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6e7-115">-DefaultProfile</span></span>
<span data-ttu-id="ae6e7-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae6e7-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="ae6e7-117">-LocalIPAddress</span></span>
<span data-ttu-id="ae6e7-118">指定要篩選的當地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="ae6e7-119">輸入範例：單一位址專案輸入"127.0.0.1"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="ae6e7-120">範圍為"127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="ae6e7-121">多個專案為「127.0.0.1;127.0.0.5;」。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="ae6e7-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="ae6e7-122">-LocalPort</span></span>
<span data-ttu-id="ae6e7-123">指定要篩選的當地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="ae6e7-124">輸入範例：單一位址專案輸入"127.0.0.1"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="ae6e7-125">範圍為"127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="ae6e7-126">多個專案為「127.0.0.1;127.0.0.5;」。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="ae6e7-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ae6e7-127">-Protocol</span></span>
<span data-ttu-id="ae6e7-128">指定要篩選的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="ae6e7-129">可接受的值 "TCP"，"UDP"，"Any"</span><span class="sxs-lookup"><span data-stu-id="ae6e7-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="ae6e7-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="ae6e7-130">-RemoteIPAddress</span></span>
<span data-ttu-id="ae6e7-131">指定要篩選的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="ae6e7-132">輸入範例：單一位址專案輸入"127.0.0.1"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="ae6e7-133">範圍為"127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="ae6e7-134">多個專案為「127.0.0.1;127.0.0.5;」。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="ae6e7-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="ae6e7-135">-RemotePort</span></span>
<span data-ttu-id="ae6e7-136">指定要篩選的遠端埠。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="ae6e7-137">遠端埠範例輸入：「80」表示單一端口專案。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="ae6e7-138">範圍為"80-85"。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-138">"80-85" for range.</span></span>
<span data-ttu-id="ae6e7-139">多個專案為 「80;443;」。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="ae6e7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6e7-140">CommonParameters</span></span>
<span data-ttu-id="ae6e7-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6e7-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ae6e7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6e7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ae6e7-143">INPUTS</span></span>

### <span data-ttu-id="ae6e7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ae6e7-144">System.String</span></span>

## <span data-ttu-id="ae6e7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ae6e7-145">OUTPUTS</span></span>

### <span data-ttu-id="ae6e7-146">Microsoft.Azure.Commands.Network.models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="ae6e7-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="ae6e7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ae6e7-147">NOTES</span></span>
<span data-ttu-id="ae6e7-148">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、監視者、封包、捕獲、流量、篩選</span><span class="sxs-lookup"><span data-stu-id="ae6e7-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="ae6e7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae6e7-149">RELATED LINKS</span></span>

[<span data-ttu-id="ae6e7-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae6e7-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ae6e7-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae6e7-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ae6e7-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae6e7-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ae6e7-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae6e7-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ae6e7-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae6e7-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ae6e7-155">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="ae6e7-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ae6e7-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ae6e7-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ae6e7-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae6e7-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae6e7-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae6e7-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ae6e7-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae6e7-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae6e7-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae6e7-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae6e7-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae6e7-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae6e7-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae6e7-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ae6e7-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ae6e7-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ae6e7-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ae6e7-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ae6e7-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae6e7-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae6e7-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae6e7-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae6e7-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae6e7-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae6e7-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ae6e7-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ae6e7-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae6e7-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae6e7-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae6e7-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae6e7-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ae6e7-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ae6e7-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ae6e7-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ae6e7-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ae6e7-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ae6e7-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ae6e7-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ae6e7-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ae6e7-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ae6e7-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae6e7-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
