---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: d69c4b3a21849db14d53760c8796b91399e742b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456496"
---
# <span data-ttu-id="af003-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af003-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="af003-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af003-102">SYNOPSIS</span></span>
<span data-ttu-id="af003-103">取得網路觀察程式的屬性</span><span class="sxs-lookup"><span data-stu-id="af003-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af003-104">句法</span><span class="sxs-lookup"><span data-stu-id="af003-104">SYNTAX</span></span>

### <span data-ttu-id="af003-105">獲取</span><span class="sxs-lookup"><span data-stu-id="af003-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af003-106">清單</span><span class="sxs-lookup"><span data-stu-id="af003-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af003-107">說明</span><span class="sxs-lookup"><span data-stu-id="af003-107">DESCRIPTION</span></span>
<span data-ttu-id="af003-108">Get-AzureRmNetworkWatcher Cmdlet 會取得一或多個 Azure 網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="af003-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="af003-109">示例</span><span class="sxs-lookup"><span data-stu-id="af003-109">EXAMPLES</span></span>

### <span data-ttu-id="af003-110">--------------------------範例1：取得網路觀察程式--------------------------</span><span class="sxs-lookup"><span data-stu-id="af003-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="af003-111">在 [資源群組 NetworkWatcherRG] 中取得名為 NetworkWatcher_westcentralus 的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="af003-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="af003-112">參數</span><span class="sxs-lookup"><span data-stu-id="af003-112">PARAMETERS</span></span>

### <span data-ttu-id="af003-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="af003-113">-Name</span></span>
<span data-ttu-id="af003-114">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="af003-114">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af003-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af003-115">-ResourceGroupName</span></span>
<span data-ttu-id="af003-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af003-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af003-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af003-117">-DefaultProfile</span></span>
<span data-ttu-id="af003-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af003-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af003-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af003-119">CommonParameters</span></span>
<span data-ttu-id="af003-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af003-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af003-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af003-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af003-122">輸入</span><span class="sxs-lookup"><span data-stu-id="af003-122">INPUTS</span></span>

### <span data-ttu-id="af003-123">所有</span><span class="sxs-lookup"><span data-stu-id="af003-123">None</span></span>

## <span data-ttu-id="af003-124">輸出</span><span class="sxs-lookup"><span data-stu-id="af003-124">OUTPUTS</span></span>

### <span data-ttu-id="af003-125">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="af003-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="af003-126">筆記</span><span class="sxs-lookup"><span data-stu-id="af003-126">NOTES</span></span>
<span data-ttu-id="af003-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="af003-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="af003-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="af003-128">RELATED LINKS</span></span>

[<span data-ttu-id="af003-129">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af003-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="af003-130">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af003-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="af003-131">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af003-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af003-132">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="af003-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="af003-133">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af003-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af003-134">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af003-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af003-135">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af003-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af003-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="af003-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="af003-137">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="af003-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="af003-138">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="af003-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="af003-139">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="af003-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="af003-140">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="af003-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
