---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456559"
---
# <span data-ttu-id="f2064-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f2064-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="f2064-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2064-102">SYNOPSIS</span></span>
<span data-ttu-id="f2064-103">傳回是否允許或拒絕來自特定目的地的資料包。</span><span class="sxs-lookup"><span data-stu-id="f2064-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2064-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2064-104">SYNTAX</span></span>

### <span data-ttu-id="f2064-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f2064-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2064-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f2064-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2064-107">說明</span><span class="sxs-lookup"><span data-stu-id="f2064-107">DESCRIPTION</span></span>
<span data-ttu-id="f2064-108">針對特定 VM 資源的 Test-AzureRmNetworkWatcherIPFlow Cmdlet，以及使用本機和遠端、IP 位址和埠的指定方向的資料包，會傳回是否允許或拒絕該資料包。</span><span class="sxs-lookup"><span data-stu-id="f2064-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="f2064-109">示例</span><span class="sxs-lookup"><span data-stu-id="f2064-109">EXAMPLES</span></span>

### <span data-ttu-id="f2064-110">---範例1：執行 Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="f2064-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="f2064-111">取得此訂閱之西部中心的網路觀察程式，然後取得 VM 及其相關的網路介面。</span><span class="sxs-lookup"><span data-stu-id="f2064-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="f2064-112">接著，在第一個網路介面上執行 Test-AzureRmNetworkWatcherIPFlow 使用第一個網路介面的第一個 IP，以取得網際網路上 IP 的輸出連線。</span><span class="sxs-lookup"><span data-stu-id="f2064-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="f2064-113">參數</span><span class="sxs-lookup"><span data-stu-id="f2064-113">PARAMETERS</span></span>

### <span data-ttu-id="f2064-114">方向</span><span class="sxs-lookup"><span data-stu-id="f2064-114">-Direction</span></span>
<span data-ttu-id="f2064-115">發展.</span><span class="sxs-lookup"><span data-stu-id="f2064-115">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2064-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="f2064-116">-LocalIPAddress</span></span>
<span data-ttu-id="f2064-117">[本機 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="f2064-117">Local IP Address.</span></span>

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

### <span data-ttu-id="f2064-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="f2064-118">-LocalPort</span></span>
<span data-ttu-id="f2064-119">本機埠。</span><span class="sxs-lookup"><span data-stu-id="f2064-119">Local Port.</span></span>

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

### <span data-ttu-id="f2064-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2064-120">-NetworkWatcher</span></span>
<span data-ttu-id="f2064-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f2064-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f2064-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f2064-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f2064-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2064-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2064-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f2064-124">-Protocol</span></span>
<span data-ttu-id="f2064-125">通訊協定.</span><span class="sxs-lookup"><span data-stu-id="f2064-125">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2064-126">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="f2064-126">-RemoteIPAddress</span></span>
<span data-ttu-id="f2064-127">[遠端 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="f2064-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="f2064-128">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="f2064-128">-RemotePort</span></span>
<span data-ttu-id="f2064-129">遠端埠。</span><span class="sxs-lookup"><span data-stu-id="f2064-129">Remote port.</span></span>

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

### <span data-ttu-id="f2064-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2064-130">-ResourceGroupName</span></span>
<span data-ttu-id="f2064-131">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2064-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f2064-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f2064-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f2064-133">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="f2064-133">Target network interface Id.</span></span>

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

### <span data-ttu-id="f2064-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f2064-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f2064-135">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="f2064-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f2064-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2064-136">-DefaultProfile</span></span>
<span data-ttu-id="f2064-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2064-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2064-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2064-138">CommonParameters</span></span>
<span data-ttu-id="f2064-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2064-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2064-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2064-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2064-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f2064-141">INPUTS</span></span>

### <span data-ttu-id="f2064-142">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2064-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f2064-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f2064-143">System.String</span></span>

## <span data-ttu-id="f2064-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f2064-144">OUTPUTS</span></span>

### <span data-ttu-id="f2064-145">PSIPFlowVerifyResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2064-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="f2064-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f2064-146">NOTES</span></span>
<span data-ttu-id="f2064-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="f2064-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="f2064-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2064-148">RELATED LINKS</span></span>

[<span data-ttu-id="f2064-149">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2064-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f2064-150">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2064-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f2064-151">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2064-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f2064-152">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f2064-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f2064-153">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f2064-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f2064-154">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f2064-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f2064-155">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f2064-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f2064-156">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2064-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2064-157">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f2064-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f2064-158">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2064-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2064-159">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2064-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2064-160">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2064-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
