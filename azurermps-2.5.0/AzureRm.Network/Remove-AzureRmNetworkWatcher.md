---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 84b92468f4945cbe25404b81f4c6403254a23ad3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801214"
---
# <span data-ttu-id="41bf3-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41bf3-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="41bf3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="41bf3-103">移除網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="41bf3-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41bf3-104">句法</span><span class="sxs-lookup"><span data-stu-id="41bf3-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41bf3-105">說明</span><span class="sxs-lookup"><span data-stu-id="41bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="41bf3-106">Remove-AzureRmNetworkWatcher Cmdlet 會移除網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="41bf3-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="41bf3-107">示例</span><span class="sxs-lookup"><span data-stu-id="41bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="41bf3-108">--------------------------範例1：建立和刪除網路監視程式--------------------------</span><span class="sxs-lookup"><span data-stu-id="41bf3-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="41bf3-109">這個範例會在資源群組中建立網路觀察程式，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="41bf3-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="41bf3-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="41bf3-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="41bf3-111">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="41bf3-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="41bf3-112">參數</span><span class="sxs-lookup"><span data-stu-id="41bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="41bf3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41bf3-113">-AsJob</span></span>
<span data-ttu-id="41bf3-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41bf3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41bf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bf3-115">-DefaultProfile</span></span>
<span data-ttu-id="41bf3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41bf3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41bf3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="41bf3-117">-Name</span></span>
<span data-ttu-id="41bf3-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="41bf3-118">The resource name.</span></span>

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

### <span data-ttu-id="41bf3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41bf3-119">-PassThru</span></span>
<span data-ttu-id="41bf3-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="41bf3-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="41bf3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41bf3-121">-ResourceGroupName</span></span>
<span data-ttu-id="41bf3-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41bf3-122">The resource group name.</span></span>

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

### <span data-ttu-id="41bf3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="41bf3-123">-Confirm</span></span>
<span data-ttu-id="41bf3-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41bf3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41bf3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41bf3-125">-WhatIf</span></span>
<span data-ttu-id="41bf3-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41bf3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41bf3-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41bf3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41bf3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bf3-128">CommonParameters</span></span>
<span data-ttu-id="41bf3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41bf3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bf3-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41bf3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bf3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="41bf3-131">INPUTS</span></span>

### <span data-ttu-id="41bf3-132">System.object</span><span class="sxs-lookup"><span data-stu-id="41bf3-132">System.String</span></span>

## <span data-ttu-id="41bf3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="41bf3-133">OUTPUTS</span></span>

### <span data-ttu-id="41bf3-134">System.object</span><span class="sxs-lookup"><span data-stu-id="41bf3-134">System.Object</span></span>

## <span data-ttu-id="41bf3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="41bf3-135">NOTES</span></span>
<span data-ttu-id="41bf3-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="41bf3-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="41bf3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="41bf3-137">RELATED LINKS</span></span>

[<span data-ttu-id="41bf3-138">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41bf3-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41bf3-139">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41bf3-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41bf3-140">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41bf3-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41bf3-141">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="41bf3-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="41bf3-142">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41bf3-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41bf3-143">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41bf3-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41bf3-144">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41bf3-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41bf3-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="41bf3-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="41bf3-146">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="41bf3-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="41bf3-147">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="41bf3-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="41bf3-148">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="41bf3-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="41bf3-149">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="41bf3-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
