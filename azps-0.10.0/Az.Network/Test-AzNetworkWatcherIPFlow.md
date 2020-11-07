---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795357"
---
# <span data-ttu-id="95aa1-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="95aa1-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="95aa1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="95aa1-103">傳回是否允許或拒絕來自特定目的地的資料包。</span><span class="sxs-lookup"><span data-stu-id="95aa1-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="95aa1-104">句法</span><span class="sxs-lookup"><span data-stu-id="95aa1-104">SYNTAX</span></span>

### <span data-ttu-id="95aa1-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="95aa1-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95aa1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="95aa1-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95aa1-107">說明</span><span class="sxs-lookup"><span data-stu-id="95aa1-107">DESCRIPTION</span></span>
<span data-ttu-id="95aa1-108">針對特定 VM 資源的 Test-AzNetworkWatcherIPFlow Cmdlet，以及使用本機和遠端、IP 位址和埠的指定方向的資料包，會傳回是否允許或拒絕該資料包。</span><span class="sxs-lookup"><span data-stu-id="95aa1-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="95aa1-109">示例</span><span class="sxs-lookup"><span data-stu-id="95aa1-109">EXAMPLES</span></span>

### <span data-ttu-id="95aa1-110">---範例1：執行 Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="95aa1-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="95aa1-111">取得此訂閱之西部中心的網路觀察程式，然後取得 VM 及其相關的網路介面。</span><span class="sxs-lookup"><span data-stu-id="95aa1-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="95aa1-112">接著，在第一個網路介面上執行 Test-AzNetworkWatcherIPFlow 使用第一個網路介面的第一個 IP，以取得網際網路上 IP 的輸出連線。</span><span class="sxs-lookup"><span data-stu-id="95aa1-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="95aa1-113">參數</span><span class="sxs-lookup"><span data-stu-id="95aa1-113">PARAMETERS</span></span>

### <span data-ttu-id="95aa1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95aa1-114">-AsJob</span></span>
<span data-ttu-id="95aa1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="95aa1-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95aa1-116">-DefaultProfile</span></span>
<span data-ttu-id="95aa1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95aa1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95aa1-118">方向</span><span class="sxs-lookup"><span data-stu-id="95aa1-118">-Direction</span></span>
<span data-ttu-id="95aa1-119">發展.</span><span class="sxs-lookup"><span data-stu-id="95aa1-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="95aa1-120">-LocalIPAddress</span></span>
<span data-ttu-id="95aa1-121">[本機 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="95aa1-121">Local IP Address.</span></span>

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

### <span data-ttu-id="95aa1-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="95aa1-122">-LocalPort</span></span>
<span data-ttu-id="95aa1-123">本機埠。</span><span class="sxs-lookup"><span data-stu-id="95aa1-123">Local Port.</span></span>

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

### <span data-ttu-id="95aa1-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95aa1-124">-NetworkWatcher</span></span>
<span data-ttu-id="95aa1-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="95aa1-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="95aa1-126">-NetworkWatcherName</span></span>
<span data-ttu-id="95aa1-127">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="95aa1-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-128">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="95aa1-128">-Protocol</span></span>
<span data-ttu-id="95aa1-129">通訊協定.</span><span class="sxs-lookup"><span data-stu-id="95aa1-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="95aa1-130">-RemoteIPAddress</span></span>
<span data-ttu-id="95aa1-131">[遠端 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="95aa1-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="95aa1-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="95aa1-132">-RemotePort</span></span>
<span data-ttu-id="95aa1-133">遠端埠。</span><span class="sxs-lookup"><span data-stu-id="95aa1-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95aa1-134">-ResourceGroupName</span></span>
<span data-ttu-id="95aa1-135">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95aa1-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95aa1-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="95aa1-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="95aa1-137">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="95aa1-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="95aa1-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="95aa1-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="95aa1-139">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="95aa1-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="95aa1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95aa1-140">CommonParameters</span></span>
<span data-ttu-id="95aa1-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95aa1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95aa1-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95aa1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95aa1-143">輸入</span><span class="sxs-lookup"><span data-stu-id="95aa1-143">INPUTS</span></span>

### <span data-ttu-id="95aa1-144">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="95aa1-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="95aa1-145">System.object</span><span class="sxs-lookup"><span data-stu-id="95aa1-145">System.String</span></span>

## <span data-ttu-id="95aa1-146">輸出</span><span class="sxs-lookup"><span data-stu-id="95aa1-146">OUTPUTS</span></span>

### <span data-ttu-id="95aa1-147">PSIPFlowVerifyResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="95aa1-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="95aa1-148">筆記</span><span class="sxs-lookup"><span data-stu-id="95aa1-148">NOTES</span></span>
<span data-ttu-id="95aa1-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="95aa1-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="95aa1-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="95aa1-150">RELATED LINKS</span></span>

[<span data-ttu-id="95aa1-151">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95aa1-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="95aa1-152">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95aa1-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="95aa1-153">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95aa1-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="95aa1-154">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="95aa1-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="95aa1-155">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="95aa1-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="95aa1-156">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="95aa1-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="95aa1-157">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="95aa1-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="95aa1-158">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95aa1-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95aa1-159">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="95aa1-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="95aa1-160">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95aa1-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95aa1-161">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95aa1-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95aa1-162">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95aa1-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
