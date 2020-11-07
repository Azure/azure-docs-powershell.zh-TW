---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794384"
---
# <span data-ttu-id="4f75f-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f75f-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="4f75f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f75f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f75f-103">取得資料包捕獲資源的資訊和屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="4f75f-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="4f75f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f75f-104">SYNTAX</span></span>

### <span data-ttu-id="4f75f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="4f75f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f75f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4f75f-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f75f-107">說明</span><span class="sxs-lookup"><span data-stu-id="4f75f-107">DESCRIPTION</span></span>
<span data-ttu-id="4f75f-108">Get-AzNetworkWatcherPacketCapture 會取得資料包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="4f75f-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="4f75f-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f75f-109">EXAMPLES</span></span>

### <span data-ttu-id="4f75f-110">---範例1：使用多個篩選建立資料包捕獲並檢索其狀態---</span><span class="sxs-lookup"><span data-stu-id="4f75f-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="4f75f-111">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="4f75f-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="4f75f-112">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f75f-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="4f75f-113">接著，我們會呼叫 Get-AzNetworkWatcherPacketCapture 來取得捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="4f75f-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="4f75f-114">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="4f75f-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="4f75f-115">參數</span><span class="sxs-lookup"><span data-stu-id="4f75f-115">PARAMETERS</span></span>

### <span data-ttu-id="4f75f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f75f-116">-AsJob</span></span>
<span data-ttu-id="4f75f-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f75f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f75f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f75f-118">-DefaultProfile</span></span>
<span data-ttu-id="4f75f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f75f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f75f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f75f-120">-NetworkWatcher</span></span>
<span data-ttu-id="4f75f-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="4f75f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="4f75f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4f75f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="4f75f-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f75f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="4f75f-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="4f75f-124">-PacketCaptureName</span></span>
<span data-ttu-id="4f75f-125">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="4f75f-125">The packet capture name.</span></span>

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

### <span data-ttu-id="4f75f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f75f-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f75f-127">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f75f-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4f75f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f75f-128">CommonParameters</span></span>
<span data-ttu-id="4f75f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f75f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f75f-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f75f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f75f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4f75f-131">INPUTS</span></span>

### <span data-ttu-id="4f75f-132">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f75f-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4f75f-133">System.object</span><span class="sxs-lookup"><span data-stu-id="4f75f-133">System.String</span></span>

## <span data-ttu-id="4f75f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4f75f-134">OUTPUTS</span></span>

### <span data-ttu-id="4f75f-135">PSGetPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f75f-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="4f75f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4f75f-136">NOTES</span></span>
<span data-ttu-id="4f75f-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="4f75f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="4f75f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f75f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4f75f-139">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f75f-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f75f-140">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4f75f-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4f75f-141">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f75f-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f75f-142">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f75f-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f75f-143">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f75f-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4f75f-144">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f75f-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4f75f-145">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f75f-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4f75f-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4f75f-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4f75f-147">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4f75f-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4f75f-148">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4f75f-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4f75f-149">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4f75f-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4f75f-150">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4f75f-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

