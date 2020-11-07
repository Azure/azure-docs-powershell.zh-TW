---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795402"
---
# <span data-ttu-id="1ccbf-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ccbf-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="1ccbf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ccbf-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccbf-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="1ccbf-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ccbf-104">SYNTAX</span></span>

### <span data-ttu-id="1ccbf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1ccbf-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ccbf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1ccbf-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ccbf-107">說明</span><span class="sxs-lookup"><span data-stu-id="1ccbf-107">DESCRIPTION</span></span>
<span data-ttu-id="1ccbf-108">Set-AzNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="1ccbf-109">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="1ccbf-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="1ccbf-111">示例</span><span class="sxs-lookup"><span data-stu-id="1ccbf-111">EXAMPLES</span></span>

### <span data-ttu-id="1ccbf-112">---範例1：針對指定的 NSG 設定流程記錄---</span><span class="sxs-lookup"><span data-stu-id="1ccbf-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="1ccbf-113">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="1ccbf-114">在回應中，我們會看到指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="1ccbf-115">參數</span><span class="sxs-lookup"><span data-stu-id="1ccbf-115">PARAMETERS</span></span>

### <span data-ttu-id="1ccbf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ccbf-116">-AsJob</span></span>
<span data-ttu-id="1ccbf-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1ccbf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ccbf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccbf-118">-DefaultProfile</span></span>
<span data-ttu-id="1ccbf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ccbf-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ccbf-120">-EnableFlowLog</span></span>
<span data-ttu-id="1ccbf-121">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccbf-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="1ccbf-122">-EnableRetention</span></span>
<span data-ttu-id="1ccbf-123">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccbf-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ccbf-124">-NetworkWatcher</span></span>
<span data-ttu-id="1ccbf-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="1ccbf-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1ccbf-126">-NetworkWatcherName</span></span>
<span data-ttu-id="1ccbf-127">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccbf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ccbf-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ccbf-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1ccbf-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1ccbf-130">-RetentionInDays</span></span>
<span data-ttu-id="1ccbf-131">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="1ccbf-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1ccbf-132">-StorageAccountId</span></span>
<span data-ttu-id="1ccbf-133">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="1ccbf-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1ccbf-134">-TargetResourceId</span></span>
<span data-ttu-id="1ccbf-135">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-135">The target resource ID.</span></span>

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

### <span data-ttu-id="1ccbf-136">-確認</span><span class="sxs-lookup"><span data-stu-id="1ccbf-136">-Confirm</span></span>
<span data-ttu-id="1ccbf-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccbf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ccbf-138">-WhatIf</span></span>
<span data-ttu-id="1ccbf-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ccbf-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccbf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccbf-141">CommonParameters</span></span>
<span data-ttu-id="1ccbf-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccbf-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ccbf-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccbf-144">輸入</span><span class="sxs-lookup"><span data-stu-id="1ccbf-144">INPUTS</span></span>

### <span data-ttu-id="1ccbf-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ccbf-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1ccbf-146">System.object （系統字串） Int32</span><span class="sxs-lookup"><span data-stu-id="1ccbf-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="1ccbf-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1ccbf-147">OUTPUTS</span></span>

### <span data-ttu-id="1ccbf-148">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ccbf-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="1ccbf-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1ccbf-149">NOTES</span></span>
<span data-ttu-id="1ccbf-150">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="1ccbf-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="1ccbf-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ccbf-151">RELATED LINKS</span></span>

[<span data-ttu-id="1ccbf-152">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1ccbf-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1ccbf-153">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ccbf-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1ccbf-154">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ccbf-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1ccbf-155">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ccbf-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1ccbf-156">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ccbf-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ccbf-157">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1ccbf-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1ccbf-158">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ccbf-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ccbf-159">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ccbf-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ccbf-160">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ccbf-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ccbf-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1ccbf-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1ccbf-162">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1ccbf-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1ccbf-163">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1ccbf-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1ccbf-164">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1ccbf-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1ccbf-165">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1ccbf-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1ccbf-166">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1ccbf-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
