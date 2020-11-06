---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446203"
---
# <span data-ttu-id="ecaed-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ecaed-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="ecaed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecaed-102">SYNOPSIS</span></span>
<span data-ttu-id="ecaed-103">從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="ecaed-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecaed-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecaed-104">SYNTAX</span></span>

### <span data-ttu-id="ecaed-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ecaed-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecaed-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ecaed-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecaed-107">說明</span><span class="sxs-lookup"><span data-stu-id="ecaed-107">DESCRIPTION</span></span>
<span data-ttu-id="ecaed-108">Get-AzureRmNetworkWatcherNextHop Cmdlet 會從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="ecaed-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="ecaed-109">下一個躍點可讓您查看 Azure 資源類型、該資源的關聯 IP 位址，以及負責路由的路由表規則。</span><span class="sxs-lookup"><span data-stu-id="ecaed-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="ecaed-110">示例</span><span class="sxs-lookup"><span data-stu-id="ecaed-110">EXAMPLES</span></span>

### <span data-ttu-id="ecaed-111">--範例1：在與網際網路 IP 通訊時取得下一個躍點</span><span class="sxs-lookup"><span data-stu-id="ecaed-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="ecaed-112">取得從指定虛擬 Vachine 的主要網路介面到 204.79.197.200 (www.bing.com 的下一個從外寄通訊的躍點) </span><span class="sxs-lookup"><span data-stu-id="ecaed-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="ecaed-113">參數</span><span class="sxs-lookup"><span data-stu-id="ecaed-113">PARAMETERS</span></span>

### <span data-ttu-id="ecaed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecaed-114">-AsJob</span></span>
<span data-ttu-id="ecaed-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ecaed-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecaed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecaed-116">-DefaultProfile</span></span>
<span data-ttu-id="ecaed-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecaed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecaed-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="ecaed-118">-DestinationIPAddress</span></span>
<span data-ttu-id="ecaed-119">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ecaed-119">Destination IP address.</span></span>

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

### <span data-ttu-id="ecaed-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecaed-120">-NetworkWatcher</span></span>
<span data-ttu-id="ecaed-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ecaed-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="ecaed-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ecaed-122">-NetworkWatcherName</span></span>
<span data-ttu-id="ecaed-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecaed-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="ecaed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecaed-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecaed-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecaed-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ecaed-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="ecaed-126">-SourceIPAddress</span></span>
<span data-ttu-id="ecaed-127">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ecaed-127">Source IP address.</span></span>

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

### <span data-ttu-id="ecaed-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="ecaed-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="ecaed-129">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="ecaed-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="ecaed-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ecaed-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ecaed-131">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="ecaed-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="ecaed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecaed-132">CommonParameters</span></span>
<span data-ttu-id="ecaed-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecaed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecaed-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ecaed-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecaed-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ecaed-135">INPUTS</span></span>

### <span data-ttu-id="ecaed-136">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ecaed-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ecaed-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ecaed-137">System.String</span></span>

## <span data-ttu-id="ecaed-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ecaed-138">OUTPUTS</span></span>

### <span data-ttu-id="ecaed-139">PSNextHopResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ecaed-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="ecaed-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ecaed-140">NOTES</span></span>
<span data-ttu-id="ecaed-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="ecaed-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="ecaed-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecaed-142">RELATED LINKS</span></span>

[<span data-ttu-id="ecaed-143">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecaed-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ecaed-144">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecaed-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ecaed-145">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecaed-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ecaed-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ecaed-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ecaed-147">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ecaed-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ecaed-148">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ecaed-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ecaed-149">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ecaed-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ecaed-150">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecaed-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecaed-151">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ecaed-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ecaed-152">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecaed-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecaed-153">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecaed-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecaed-154">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecaed-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

