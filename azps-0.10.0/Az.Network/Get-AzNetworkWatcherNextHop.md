---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794386"
---
# <span data-ttu-id="1e0f6-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1e0f6-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="1e0f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0f6-103">從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="1e0f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e0f6-104">SYNTAX</span></span>

### <span data-ttu-id="1e0f6-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1e0f6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0f6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1e0f6-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e0f6-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e0f6-107">DESCRIPTION</span></span>
<span data-ttu-id="1e0f6-108">Get-AzNetworkWatcherNextHop Cmdlet 會從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="1e0f6-109">下一個躍點可讓您查看 Azure 資源類型、該資源的關聯 IP 位址，以及負責路由的路由表規則。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="1e0f6-110">示例</span><span class="sxs-lookup"><span data-stu-id="1e0f6-110">EXAMPLES</span></span>

### <span data-ttu-id="1e0f6-111">--範例1：在與網際網路 IP 通訊時取得下一個躍點</span><span class="sxs-lookup"><span data-stu-id="1e0f6-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="1e0f6-112">取得從指定虛擬 Vachine 的主要網路介面到 204.79.197.200 (www.bing.com 的下一個從外寄通訊的躍點) </span><span class="sxs-lookup"><span data-stu-id="1e0f6-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="1e0f6-113">參數</span><span class="sxs-lookup"><span data-stu-id="1e0f6-113">PARAMETERS</span></span>

### <span data-ttu-id="1e0f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e0f6-114">-AsJob</span></span>
<span data-ttu-id="1e0f6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e0f6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e0f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0f6-116">-DefaultProfile</span></span>
<span data-ttu-id="1e0f6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e0f6-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e0f6-118">-DestinationIPAddress</span></span>
<span data-ttu-id="1e0f6-119">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-119">Destination IP address.</span></span>

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

### <span data-ttu-id="1e0f6-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e0f6-120">-NetworkWatcher</span></span>
<span data-ttu-id="1e0f6-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="1e0f6-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1e0f6-122">-NetworkWatcherName</span></span>
<span data-ttu-id="1e0f6-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="1e0f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e0f6-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1e0f6-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e0f6-126">-SourceIPAddress</span></span>
<span data-ttu-id="1e0f6-127">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-127">Source IP address.</span></span>

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

### <span data-ttu-id="1e0f6-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="1e0f6-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="1e0f6-129">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="1e0f6-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1e0f6-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1e0f6-131">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="1e0f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0f6-132">CommonParameters</span></span>
<span data-ttu-id="1e0f6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0f6-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e0f6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0f6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1e0f6-135">INPUTS</span></span>

### <span data-ttu-id="1e0f6-136">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1e0f6-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1e0f6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1e0f6-137">System.String</span></span>

## <span data-ttu-id="1e0f6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1e0f6-138">OUTPUTS</span></span>

### <span data-ttu-id="1e0f6-139">PSNextHopResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1e0f6-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="1e0f6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1e0f6-140">NOTES</span></span>
<span data-ttu-id="1e0f6-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="1e0f6-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="1e0f6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e0f6-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e0f6-143">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e0f6-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1e0f6-144">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e0f6-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1e0f6-145">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e0f6-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1e0f6-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1e0f6-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1e0f6-147">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1e0f6-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1e0f6-148">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1e0f6-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1e0f6-149">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1e0f6-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1e0f6-150">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e0f6-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1e0f6-151">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1e0f6-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1e0f6-152">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e0f6-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1e0f6-153">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e0f6-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1e0f6-154">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e0f6-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

