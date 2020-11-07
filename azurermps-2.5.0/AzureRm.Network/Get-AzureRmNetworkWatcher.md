---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802350"
---
# <span data-ttu-id="2dd74-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dd74-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="2dd74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2dd74-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd74-103">取得網路觀察程式的屬性</span><span class="sxs-lookup"><span data-stu-id="2dd74-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dd74-104">句法</span><span class="sxs-lookup"><span data-stu-id="2dd74-104">SYNTAX</span></span>

### <span data-ttu-id="2dd74-105">獲取</span><span class="sxs-lookup"><span data-stu-id="2dd74-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd74-106">清單</span><span class="sxs-lookup"><span data-stu-id="2dd74-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dd74-107">說明</span><span class="sxs-lookup"><span data-stu-id="2dd74-107">DESCRIPTION</span></span>
<span data-ttu-id="2dd74-108">Get-AzureRmNetworkWatcher Cmdlet 會取得一或多個 Azure 網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2dd74-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="2dd74-109">示例</span><span class="sxs-lookup"><span data-stu-id="2dd74-109">EXAMPLES</span></span>

### <span data-ttu-id="2dd74-110">--------------------------範例1：取得網路觀察程式--------------------------</span><span class="sxs-lookup"><span data-stu-id="2dd74-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="2dd74-111">在 [資源群組 NetworkWatcherRG] 中取得名為 NetworkWatcher_westcentralus 的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2dd74-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="2dd74-112">參數</span><span class="sxs-lookup"><span data-stu-id="2dd74-112">PARAMETERS</span></span>

### <span data-ttu-id="2dd74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd74-113">-DefaultProfile</span></span>
<span data-ttu-id="2dd74-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2dd74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dd74-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2dd74-115">-Name</span></span>
<span data-ttu-id="2dd74-116">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2dd74-116">The network watcher name.</span></span>

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

### <span data-ttu-id="2dd74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd74-117">-ResourceGroupName</span></span>
<span data-ttu-id="2dd74-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dd74-118">The resource group name.</span></span>

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

### <span data-ttu-id="2dd74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd74-119">CommonParameters</span></span>
<span data-ttu-id="2dd74-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2dd74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd74-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2dd74-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd74-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2dd74-122">INPUTS</span></span>

### <span data-ttu-id="2dd74-123">所有</span><span class="sxs-lookup"><span data-stu-id="2dd74-123">None</span></span>

## <span data-ttu-id="2dd74-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2dd74-124">OUTPUTS</span></span>

### <span data-ttu-id="2dd74-125">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2dd74-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="2dd74-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2dd74-126">NOTES</span></span>
<span data-ttu-id="2dd74-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2dd74-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="2dd74-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dd74-128">RELATED LINKS</span></span>

[<span data-ttu-id="2dd74-129">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dd74-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2dd74-130">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dd74-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2dd74-131">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dd74-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dd74-132">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2dd74-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2dd74-133">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dd74-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dd74-134">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dd74-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dd74-135">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dd74-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dd74-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2dd74-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2dd74-137">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2dd74-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2dd74-138">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2dd74-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2dd74-139">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2dd74-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2dd74-140">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2dd74-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
