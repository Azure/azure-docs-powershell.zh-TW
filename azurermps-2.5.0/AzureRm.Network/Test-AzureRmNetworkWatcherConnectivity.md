---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
ms.openlocfilehash: 55dc2682c4c3e62b42a6a23ac12f93991e4873fc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800317"
---
# <span data-ttu-id="c9d23-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c9d23-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="c9d23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9d23-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d23-103">傳回指定來源 VM 與目的地的連線資訊。</span><span class="sxs-lookup"><span data-stu-id="c9d23-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d23-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9d23-104">SYNTAX</span></span>

### <span data-ttu-id="c9d23-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c9d23-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9d23-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c9d23-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d23-107">說明</span><span class="sxs-lookup"><span data-stu-id="c9d23-107">DESCRIPTION</span></span>
<span data-ttu-id="c9d23-108">Test-AzureRmNetworkWatcherConnectivity Cmdlet 會傳回指定來源 VM 與目的地的連線資訊。</span><span class="sxs-lookup"><span data-stu-id="c9d23-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="c9d23-109">如果無法建立來源與目的地之間的連線，此 Cmdlet 會傳回問題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c9d23-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="c9d23-110">示例</span><span class="sxs-lookup"><span data-stu-id="c9d23-110">EXAMPLES</span></span>

### <span data-ttu-id="c9d23-111">---------------範例1：測試從 VM 到網站---------------的網路觀察程式連線能力</span><span class="sxs-lookup"><span data-stu-id="c9d23-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


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

<span data-ttu-id="c9d23-112">在這個範例中，我們會測試 Azure 中 VM 的連線性與 www.bing.com。</span><span class="sxs-lookup"><span data-stu-id="c9d23-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="c9d23-113">參數</span><span class="sxs-lookup"><span data-stu-id="c9d23-113">PARAMETERS</span></span>

### <span data-ttu-id="c9d23-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9d23-114">-AsJob</span></span>
<span data-ttu-id="c9d23-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c9d23-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9d23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d23-116">-DefaultProfile</span></span>
<span data-ttu-id="c9d23-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9d23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d23-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c9d23-118">-DestinationAddress</span></span>
<span data-ttu-id="c9d23-119">要建立連線之資源的 IP 位址或 URI。</span><span class="sxs-lookup"><span data-stu-id="c9d23-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="c9d23-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="c9d23-120">-DestinationId</span></span>
<span data-ttu-id="c9d23-121">要進行連線嘗試的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9d23-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="c9d23-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c9d23-122">-DestinationPort</span></span>
<span data-ttu-id="c9d23-123">將在其上執行檢查連線的埠。</span><span class="sxs-lookup"><span data-stu-id="c9d23-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d23-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c9d23-124">-NetworkWatcher</span></span>
<span data-ttu-id="c9d23-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="c9d23-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="c9d23-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c9d23-126">-NetworkWatcherName</span></span>
<span data-ttu-id="c9d23-127">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9d23-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d23-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d23-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9d23-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9d23-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c9d23-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="c9d23-130">-SourceId</span></span>
<span data-ttu-id="c9d23-131">將啟動連線檢查的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9d23-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="c9d23-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="c9d23-132">-SourcePort</span></span>
<span data-ttu-id="c9d23-133">將執行連線檢查的來源埠。</span><span class="sxs-lookup"><span data-stu-id="c9d23-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d23-134">CommonParameters</span></span>
<span data-ttu-id="c9d23-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9d23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d23-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9d23-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d23-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c9d23-137">INPUTS</span></span>

### <span data-ttu-id="c9d23-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c9d23-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c9d23-139">字串 System.object （system.object）</span><span class="sxs-lookup"><span data-stu-id="c9d23-139">System.String System.Int32</span></span>

## <span data-ttu-id="c9d23-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c9d23-140">OUTPUTS</span></span>

### <span data-ttu-id="c9d23-141">PSConnectivityInformation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c9d23-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="c9d23-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c9d23-142">NOTES</span></span>
<span data-ttu-id="c9d23-143">關鍵字： azure、azurerm、arm、資源、連線性、管理、管理員、網路、網路、網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="c9d23-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c9d23-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9d23-144">RELATED LINKS</span></span>

<span data-ttu-id="c9d23-145">[新-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
[AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
[移除-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="c9d23-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="c9d23-146">[AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
[AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
[AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
[AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="c9d23-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="c9d23-147">[新-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
[新-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
[AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
[移除-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
[停止 AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="c9d23-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
