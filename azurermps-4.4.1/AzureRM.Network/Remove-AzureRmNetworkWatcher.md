---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444900"
---
# <span data-ttu-id="c56bd-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c56bd-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="c56bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c56bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c56bd-103">移除網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="c56bd-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c56bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="c56bd-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="c56bd-105">DESCRIPTION</span></span>
<span data-ttu-id="c56bd-106">Remove-AzureRmNetworkWatcher Cmdlet 會移除網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="c56bd-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="c56bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="c56bd-107">EXAMPLES</span></span>

### <span data-ttu-id="c56bd-108">--------------------------範例1：建立和刪除網路監視程式--------------------------</span><span class="sxs-lookup"><span data-stu-id="c56bd-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="c56bd-109">這個範例會在資源群組中建立網路觀察程式，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="c56bd-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c56bd-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="c56bd-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="c56bd-111">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="c56bd-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="c56bd-112">參數</span><span class="sxs-lookup"><span data-stu-id="c56bd-112">PARAMETERS</span></span>

### <span data-ttu-id="c56bd-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c56bd-113">-Name</span></span>
<span data-ttu-id="c56bd-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c56bd-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56bd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c56bd-115">-PassThru</span></span>
<span data-ttu-id="c56bd-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="c56bd-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="c56bd-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c56bd-118">The resource group name.</span></span>

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

### <span data-ttu-id="c56bd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c56bd-119">-Confirm</span></span>
<span data-ttu-id="c56bd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c56bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56bd-121">-WhatIf</span></span>
<span data-ttu-id="c56bd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c56bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56bd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c56bd-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56bd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56bd-124">-DefaultProfile</span></span>
<span data-ttu-id="c56bd-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c56bd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56bd-126">CommonParameters</span></span>
<span data-ttu-id="c56bd-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c56bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56bd-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c56bd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56bd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c56bd-129">INPUTS</span></span>

### <span data-ttu-id="c56bd-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c56bd-130">System.String</span></span>

## <span data-ttu-id="c56bd-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c56bd-131">OUTPUTS</span></span>

### <span data-ttu-id="c56bd-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c56bd-132">System.Object</span></span>

## <span data-ttu-id="c56bd-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c56bd-133">NOTES</span></span>
<span data-ttu-id="c56bd-134">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="c56bd-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c56bd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c56bd-135">RELATED LINKS</span></span>

[<span data-ttu-id="c56bd-136">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c56bd-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c56bd-137">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c56bd-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c56bd-138">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c56bd-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c56bd-139">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c56bd-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c56bd-140">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c56bd-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c56bd-141">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c56bd-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c56bd-142">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c56bd-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c56bd-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c56bd-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c56bd-144">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c56bd-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c56bd-145">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c56bd-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c56bd-146">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c56bd-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c56bd-147">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c56bd-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
