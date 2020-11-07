---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794399"
---
# <span data-ttu-id="7a5a8-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a5a8-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="7a5a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5a8-103">取得網路觀察程式的屬性</span><span class="sxs-lookup"><span data-stu-id="7a5a8-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="7a5a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a5a8-104">SYNTAX</span></span>

### <span data-ttu-id="7a5a8-105">獲取</span><span class="sxs-lookup"><span data-stu-id="7a5a8-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a5a8-106">清單</span><span class="sxs-lookup"><span data-stu-id="7a5a8-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a5a8-107">說明</span><span class="sxs-lookup"><span data-stu-id="7a5a8-107">DESCRIPTION</span></span>
<span data-ttu-id="7a5a8-108">Get-AzNetworkWatcher Cmdlet 會取得一或多個 Azure 網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="7a5a8-109">示例</span><span class="sxs-lookup"><span data-stu-id="7a5a8-109">EXAMPLES</span></span>

### <span data-ttu-id="7a5a8-110">--------------------------範例1：取得網路觀察程式--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a5a8-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="7a5a8-111">在 [資源群組 NetworkWatcherRG] 中取得名為 NetworkWatcher_westcentralus 的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="7a5a8-112">參數</span><span class="sxs-lookup"><span data-stu-id="7a5a8-112">PARAMETERS</span></span>

### <span data-ttu-id="7a5a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5a8-113">-DefaultProfile</span></span>
<span data-ttu-id="7a5a8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a5a8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a5a8-115">-Name</span></span>
<span data-ttu-id="7a5a8-116">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a5a8-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5a8-119">CommonParameters</span></span>
<span data-ttu-id="7a5a8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5a8-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a5a8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5a8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7a5a8-122">INPUTS</span></span>

### <span data-ttu-id="7a5a8-123">所有</span><span class="sxs-lookup"><span data-stu-id="7a5a8-123">None</span></span>

## <span data-ttu-id="7a5a8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7a5a8-124">OUTPUTS</span></span>

### <span data-ttu-id="7a5a8-125">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7a5a8-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="7a5a8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7a5a8-126">NOTES</span></span>
<span data-ttu-id="7a5a8-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="7a5a8-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="7a5a8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a5a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="7a5a8-129">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a5a8-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7a5a8-130">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a5a8-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7a5a8-131">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a5a8-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a5a8-132">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7a5a8-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7a5a8-133">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a5a8-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a5a8-134">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a5a8-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a5a8-135">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a5a8-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a5a8-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7a5a8-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7a5a8-137">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7a5a8-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7a5a8-138">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7a5a8-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7a5a8-139">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7a5a8-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7a5a8-140">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7a5a8-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
