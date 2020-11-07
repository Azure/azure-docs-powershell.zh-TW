---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795502"
---
# <span data-ttu-id="e354c-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e354c-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="e354c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e354c-102">SYNOPSIS</span></span>
<span data-ttu-id="e354c-103">移除網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="e354c-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="e354c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e354c-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e354c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e354c-105">DESCRIPTION</span></span>
<span data-ttu-id="e354c-106">Remove-AzNetworkWatcher Cmdlet 會移除網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="e354c-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="e354c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e354c-107">EXAMPLES</span></span>

### <span data-ttu-id="e354c-108">--------------------------範例1：建立和刪除網路監視程式--------------------------</span><span class="sxs-lookup"><span data-stu-id="e354c-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="e354c-109">這個範例會在資源群組中建立網路觀察程式，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="e354c-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e354c-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="e354c-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="e354c-111">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="e354c-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e354c-112">參數</span><span class="sxs-lookup"><span data-stu-id="e354c-112">PARAMETERS</span></span>

### <span data-ttu-id="e354c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e354c-113">-AsJob</span></span>
<span data-ttu-id="e354c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e354c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e354c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e354c-115">-DefaultProfile</span></span>
<span data-ttu-id="e354c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e354c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e354c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e354c-117">-Name</span></span>
<span data-ttu-id="e354c-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e354c-118">The resource name.</span></span>

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

### <span data-ttu-id="e354c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e354c-119">-PassThru</span></span>
<span data-ttu-id="e354c-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="e354c-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e354c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e354c-121">-ResourceGroupName</span></span>
<span data-ttu-id="e354c-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e354c-122">The resource group name.</span></span>

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

### <span data-ttu-id="e354c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e354c-123">-Confirm</span></span>
<span data-ttu-id="e354c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e354c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e354c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e354c-125">-WhatIf</span></span>
<span data-ttu-id="e354c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e354c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e354c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e354c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e354c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e354c-128">CommonParameters</span></span>
<span data-ttu-id="e354c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e354c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e354c-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e354c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e354c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e354c-131">INPUTS</span></span>

### <span data-ttu-id="e354c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e354c-132">System.String</span></span>

## <span data-ttu-id="e354c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e354c-133">OUTPUTS</span></span>

### <span data-ttu-id="e354c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e354c-134">System.Object</span></span>

## <span data-ttu-id="e354c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e354c-135">NOTES</span></span>
<span data-ttu-id="e354c-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="e354c-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e354c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e354c-137">RELATED LINKS</span></span>

[<span data-ttu-id="e354c-138">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e354c-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e354c-139">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e354c-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e354c-140">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e354c-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e354c-141">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e354c-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e354c-142">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e354c-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e354c-143">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e354c-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e354c-144">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e354c-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e354c-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e354c-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e354c-146">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e354c-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e354c-147">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e354c-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e354c-148">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e354c-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e354c-149">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e354c-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
