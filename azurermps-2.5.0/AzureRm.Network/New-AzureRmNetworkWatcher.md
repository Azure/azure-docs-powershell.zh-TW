---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: b096c87e588c48b609fe0a55be7344b39df98c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801233"
---
# <span data-ttu-id="2664a-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2664a-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="2664a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2664a-102">SYNOPSIS</span></span>
<span data-ttu-id="2664a-103">建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2664a-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2664a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2664a-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2664a-105">說明</span><span class="sxs-lookup"><span data-stu-id="2664a-105">DESCRIPTION</span></span>
<span data-ttu-id="2664a-106">New-AzureRmNetworkWatcher Cmdlet 會建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2664a-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="2664a-107">示例</span><span class="sxs-lookup"><span data-stu-id="2664a-107">EXAMPLES</span></span>

### <span data-ttu-id="2664a-108">範例1：建立網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2664a-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="2664a-109">這個範例會在新建立的資源群組內建立新的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2664a-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="2664a-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2664a-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="2664a-111">參數</span><span class="sxs-lookup"><span data-stu-id="2664a-111">PARAMETERS</span></span>

### <span data-ttu-id="2664a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2664a-112">-DefaultProfile</span></span>
<span data-ttu-id="2664a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2664a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2664a-114">-位置</span><span class="sxs-lookup"><span data-stu-id="2664a-114">-Location</span></span>
<span data-ttu-id="2664a-115">位於.</span><span class="sxs-lookup"><span data-stu-id="2664a-115">Location.</span></span>

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

### <span data-ttu-id="2664a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2664a-116">-Name</span></span>
<span data-ttu-id="2664a-117">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2664a-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2664a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2664a-118">-ResourceGroupName</span></span>
<span data-ttu-id="2664a-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2664a-119">The resource group name.</span></span>

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

### <span data-ttu-id="2664a-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2664a-120">-Tag</span></span>
<span data-ttu-id="2664a-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2664a-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2664a-122">例如：</span><span class="sxs-lookup"><span data-stu-id="2664a-122">For example:</span></span>

<span data-ttu-id="2664a-123">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2664a-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2664a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2664a-124">-Confirm</span></span>
<span data-ttu-id="2664a-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2664a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2664a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2664a-126">-WhatIf</span></span>
<span data-ttu-id="2664a-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2664a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2664a-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2664a-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2664a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2664a-129">CommonParameters</span></span>
<span data-ttu-id="2664a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2664a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2664a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2664a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2664a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2664a-132">INPUTS</span></span>

### <span data-ttu-id="2664a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2664a-133">System.String</span></span>
<span data-ttu-id="2664a-134">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2664a-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2664a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2664a-135">OUTPUTS</span></span>

### <span data-ttu-id="2664a-136">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2664a-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="2664a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2664a-137">NOTES</span></span>
<span data-ttu-id="2664a-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2664a-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2664a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2664a-139">RELATED LINKS</span></span>

[<span data-ttu-id="2664a-140">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2664a-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2664a-141">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2664a-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2664a-142">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2664a-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2664a-143">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2664a-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2664a-144">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2664a-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2664a-145">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2664a-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2664a-146">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2664a-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2664a-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2664a-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2664a-148">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2664a-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2664a-149">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2664a-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2664a-150">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2664a-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2664a-151">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2664a-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
