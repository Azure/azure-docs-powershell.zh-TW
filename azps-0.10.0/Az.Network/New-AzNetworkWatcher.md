---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794251"
---
# <span data-ttu-id="5ef22-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ef22-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="5ef22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ef22-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef22-103">建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="5ef22-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="5ef22-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ef22-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef22-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ef22-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef22-106">New-AzNetworkWatcher Cmdlet 會建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="5ef22-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="5ef22-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ef22-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef22-108">範例1：建立網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="5ef22-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="5ef22-109">這個範例會在新建立的資源群組內建立新的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="5ef22-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="5ef22-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="5ef22-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="5ef22-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ef22-111">PARAMETERS</span></span>

### <span data-ttu-id="5ef22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef22-112">-DefaultProfile</span></span>
<span data-ttu-id="5ef22-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ef22-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ef22-114">-位置</span><span class="sxs-lookup"><span data-stu-id="5ef22-114">-Location</span></span>
<span data-ttu-id="5ef22-115">位於.</span><span class="sxs-lookup"><span data-stu-id="5ef22-115">Location.</span></span>

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

### <span data-ttu-id="5ef22-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ef22-116">-Name</span></span>
<span data-ttu-id="5ef22-117">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="5ef22-117">The network watcher name.</span></span>

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

### <span data-ttu-id="5ef22-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef22-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ef22-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ef22-119">The resource group name.</span></span>

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

### <span data-ttu-id="5ef22-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ef22-120">-Tag</span></span>
<span data-ttu-id="5ef22-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="5ef22-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5ef22-122">例如：</span><span class="sxs-lookup"><span data-stu-id="5ef22-122">For example:</span></span>

<span data-ttu-id="5ef22-123">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5ef22-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5ef22-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5ef22-124">-Confirm</span></span>
<span data-ttu-id="5ef22-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ef22-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef22-126">-WhatIf</span></span>
<span data-ttu-id="5ef22-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ef22-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef22-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ef22-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef22-129">CommonParameters</span></span>
<span data-ttu-id="5ef22-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ef22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef22-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ef22-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef22-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5ef22-132">INPUTS</span></span>

### <span data-ttu-id="5ef22-133">System.object</span><span class="sxs-lookup"><span data-stu-id="5ef22-133">System.String</span></span>
<span data-ttu-id="5ef22-134">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ef22-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5ef22-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5ef22-135">OUTPUTS</span></span>

### <span data-ttu-id="5ef22-136">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ef22-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="5ef22-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5ef22-137">NOTES</span></span>
<span data-ttu-id="5ef22-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="5ef22-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="5ef22-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ef22-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ef22-140">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ef22-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5ef22-141">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ef22-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5ef22-142">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ef22-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ef22-143">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5ef22-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5ef22-144">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ef22-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ef22-145">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ef22-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ef22-146">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ef22-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5ef22-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5ef22-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5ef22-148">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5ef22-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5ef22-149">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5ef22-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5ef22-150">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5ef22-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5ef22-151">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5ef22-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
