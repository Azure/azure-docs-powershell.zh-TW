---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: 10cc869bf6e0ac194ce5e2e77c69885a8e0a0d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448144"
---
# <span data-ttu-id="ae22d-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae22d-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="ae22d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae22d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae22d-103">建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ae22d-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae22d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae22d-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae22d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae22d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae22d-106">New-AzureRmNetworkWatcher Cmdlet 會建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ae22d-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="ae22d-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae22d-107">EXAMPLES</span></span>

### <span data-ttu-id="ae22d-108">範例1：建立網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="ae22d-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="ae22d-109">這個範例會在新建立的資源群組內建立新的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="ae22d-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="ae22d-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="ae22d-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="ae22d-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae22d-111">PARAMETERS</span></span>

### <span data-ttu-id="ae22d-112">-位置</span><span class="sxs-lookup"><span data-stu-id="ae22d-112">-Location</span></span>
<span data-ttu-id="ae22d-113">位於.</span><span class="sxs-lookup"><span data-stu-id="ae22d-113">Location.</span></span>

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

### <span data-ttu-id="ae22d-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae22d-114">-Name</span></span>
<span data-ttu-id="ae22d-115">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ae22d-115">The network watcher name.</span></span>

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

### <span data-ttu-id="ae22d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae22d-116">-ResourceGroupName</span></span>
<span data-ttu-id="ae22d-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae22d-117">The resource group name.</span></span>

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

### <span data-ttu-id="ae22d-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae22d-118">-Tag</span></span>
<span data-ttu-id="ae22d-119">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ae22d-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae22d-120">例如：</span><span class="sxs-lookup"><span data-stu-id="ae22d-120">For example:</span></span>

<span data-ttu-id="ae22d-121">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ae22d-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae22d-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ae22d-122">-Confirm</span></span>
<span data-ttu-id="ae22d-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae22d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae22d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae22d-124">-WhatIf</span></span>
<span data-ttu-id="ae22d-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae22d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae22d-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae22d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae22d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae22d-127">-DefaultProfile</span></span>
<span data-ttu-id="ae22d-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae22d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae22d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae22d-129">CommonParameters</span></span>
<span data-ttu-id="ae22d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae22d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae22d-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae22d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae22d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ae22d-132">INPUTS</span></span>

### <span data-ttu-id="ae22d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ae22d-133">System.String</span></span>
<span data-ttu-id="ae22d-134">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae22d-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae22d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ae22d-135">OUTPUTS</span></span>

### <span data-ttu-id="ae22d-136">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae22d-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ae22d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ae22d-137">NOTES</span></span>
<span data-ttu-id="ae22d-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="ae22d-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="ae22d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae22d-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae22d-140">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae22d-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae22d-141">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae22d-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae22d-142">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae22d-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae22d-143">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae22d-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ae22d-144">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae22d-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae22d-145">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae22d-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae22d-146">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae22d-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae22d-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ae22d-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ae22d-148">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae22d-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ae22d-149">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae22d-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ae22d-150">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ae22d-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ae22d-151">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ae22d-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
