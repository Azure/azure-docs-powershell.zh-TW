---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456495"
---
# <span data-ttu-id="0aaeb-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0aaeb-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="0aaeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0aaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="0aaeb-103">從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aaeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="0aaeb-104">SYNTAX</span></span>

### <span data-ttu-id="0aaeb-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="0aaeb-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aaeb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0aaeb-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aaeb-107">說明</span><span class="sxs-lookup"><span data-stu-id="0aaeb-107">DESCRIPTION</span></span>
<span data-ttu-id="0aaeb-108">Get-AzureRmNetworkWatcherNextHop Cmdlet 會從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="0aaeb-109">下一個躍點可讓您查看 Azure 資源類型、該資源的關聯 IP 位址，以及負責路由的路由表規則。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="0aaeb-110">示例</span><span class="sxs-lookup"><span data-stu-id="0aaeb-110">EXAMPLES</span></span>

### <span data-ttu-id="0aaeb-111">--範例1：在與網際網路 IP 通訊時取得下一個躍點</span><span class="sxs-lookup"><span data-stu-id="0aaeb-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="0aaeb-112">取得從指定虛擬 Vachine 的主要網路介面到 204.79.197.200 (www.bing.com 的下一個從外寄通訊的躍點) </span><span class="sxs-lookup"><span data-stu-id="0aaeb-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="0aaeb-113">參數</span><span class="sxs-lookup"><span data-stu-id="0aaeb-113">PARAMETERS</span></span>

### <span data-ttu-id="0aaeb-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="0aaeb-114">-DestinationIPAddress</span></span>
<span data-ttu-id="0aaeb-115">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-115">Destination IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aaeb-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0aaeb-116">-NetworkWatcher</span></span>
<span data-ttu-id="0aaeb-117">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="0aaeb-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0aaeb-118">-NetworkWatcherName</span></span>
<span data-ttu-id="0aaeb-119">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="0aaeb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aaeb-120">-ResourceGroupName</span></span>
<span data-ttu-id="0aaeb-121">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0aaeb-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="0aaeb-122">-SourceIPAddress</span></span>
<span data-ttu-id="0aaeb-123">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-123">Source IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aaeb-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="0aaeb-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="0aaeb-125">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="0aaeb-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0aaeb-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0aaeb-127">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0aaeb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aaeb-128">-DefaultProfile</span></span>
<span data-ttu-id="0aaeb-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aaeb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aaeb-130">CommonParameters</span></span>
<span data-ttu-id="0aaeb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aaeb-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0aaeb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aaeb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0aaeb-133">INPUTS</span></span>

### <span data-ttu-id="0aaeb-134">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0aaeb-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0aaeb-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0aaeb-135">System.String</span></span>

## <span data-ttu-id="0aaeb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0aaeb-136">OUTPUTS</span></span>

### <span data-ttu-id="0aaeb-137">PSNextHopResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0aaeb-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="0aaeb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0aaeb-138">NOTES</span></span>
<span data-ttu-id="0aaeb-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="0aaeb-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="0aaeb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aaeb-140">RELATED LINKS</span></span>

[<span data-ttu-id="0aaeb-141">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0aaeb-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0aaeb-142">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0aaeb-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0aaeb-143">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0aaeb-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0aaeb-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0aaeb-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0aaeb-145">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0aaeb-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0aaeb-146">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0aaeb-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0aaeb-147">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0aaeb-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0aaeb-148">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0aaeb-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0aaeb-149">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0aaeb-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0aaeb-150">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0aaeb-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0aaeb-151">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0aaeb-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0aaeb-152">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0aaeb-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

