---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 912c2a424cda533dd5d576ab6744476b689d2ae1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626649"
---
# <span data-ttu-id="452a9-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="452a9-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="452a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="452a9-102">SYNOPSIS</span></span>
<span data-ttu-id="452a9-103">取得資料包捕獲資源的資訊和屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="452a9-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="452a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="452a9-104">SYNTAX</span></span>

### <span data-ttu-id="452a9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="452a9-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="452a9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="452a9-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="452a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="452a9-107">DESCRIPTION</span></span>
<span data-ttu-id="452a9-108">Get-AzureRmNetworkWatcherPacketCapture 會取得資料包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="452a9-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="452a9-109">示例</span><span class="sxs-lookup"><span data-stu-id="452a9-109">EXAMPLES</span></span>

### <span data-ttu-id="452a9-110">---範例1：使用多個篩選建立資料包捕獲並檢索其狀態---</span><span class="sxs-lookup"><span data-stu-id="452a9-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="452a9-111">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="452a9-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="452a9-112">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="452a9-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="452a9-113">接著，我們會呼叫 Get-AzureRmNetworkWatcherPacketCapture 來取得捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="452a9-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="452a9-114">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="452a9-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="452a9-115">參數</span><span class="sxs-lookup"><span data-stu-id="452a9-115">PARAMETERS</span></span>

### <span data-ttu-id="452a9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="452a9-116">-AsJob</span></span>
<span data-ttu-id="452a9-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="452a9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="452a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452a9-118">-DefaultProfile</span></span>
<span data-ttu-id="452a9-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="452a9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="452a9-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="452a9-120">-NetworkWatcher</span></span>
<span data-ttu-id="452a9-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="452a9-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="452a9-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="452a9-122">-NetworkWatcherName</span></span>
<span data-ttu-id="452a9-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="452a9-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="452a9-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="452a9-124">-PacketCaptureName</span></span>
<span data-ttu-id="452a9-125">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="452a9-125">The packet capture name.</span></span>

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

### <span data-ttu-id="452a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="452a9-127">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="452a9-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="452a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452a9-128">CommonParameters</span></span>
<span data-ttu-id="452a9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="452a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452a9-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="452a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452a9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="452a9-131">INPUTS</span></span>

### <span data-ttu-id="452a9-132">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="452a9-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="452a9-133">System.object</span><span class="sxs-lookup"><span data-stu-id="452a9-133">System.String</span></span>

## <span data-ttu-id="452a9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="452a9-134">OUTPUTS</span></span>

### <span data-ttu-id="452a9-135">PSGetPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="452a9-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="452a9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="452a9-136">NOTES</span></span>
<span data-ttu-id="452a9-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="452a9-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="452a9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="452a9-138">RELATED LINKS</span></span>

[<span data-ttu-id="452a9-139">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="452a9-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="452a9-140">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="452a9-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="452a9-141">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="452a9-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="452a9-142">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="452a9-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="452a9-143">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="452a9-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="452a9-144">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="452a9-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="452a9-145">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="452a9-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="452a9-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="452a9-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="452a9-147">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="452a9-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="452a9-148">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="452a9-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="452a9-149">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="452a9-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="452a9-150">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="452a9-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

