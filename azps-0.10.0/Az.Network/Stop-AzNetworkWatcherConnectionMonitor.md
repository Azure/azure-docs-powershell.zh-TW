---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795364"
---
# <span data-ttu-id="b98e5-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b98e5-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b98e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b98e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b98e5-103">停止連線監視器</span><span class="sxs-lookup"><span data-stu-id="b98e5-103">Stop a connection monitor</span></span>

## <span data-ttu-id="b98e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="b98e5-104">SYNTAX</span></span>

### <span data-ttu-id="b98e5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b98e5-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b98e5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b98e5-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b98e5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b98e5-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b98e5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b98e5-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b98e5-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b98e5-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b98e5-110">說明</span><span class="sxs-lookup"><span data-stu-id="b98e5-110">DESCRIPTION</span></span>
<span data-ttu-id="b98e5-111">Stop-AzNetworkWatcherConnectionMonitor Cmdlet 會停止指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="b98e5-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="b98e5-112">示例</span><span class="sxs-lookup"><span data-stu-id="b98e5-112">EXAMPLES</span></span>

### <span data-ttu-id="b98e5-113">---------------範例1：停止連接監視器---------------</span><span class="sxs-lookup"><span data-stu-id="b98e5-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="b98e5-114">在這個範例中，我們會停止由名稱和網路觀察程式指定的連線監視器</span><span class="sxs-lookup"><span data-stu-id="b98e5-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="b98e5-115">參數</span><span class="sxs-lookup"><span data-stu-id="b98e5-115">PARAMETERS</span></span>

### <span data-ttu-id="b98e5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b98e5-116">-AsJob</span></span>
<span data-ttu-id="b98e5-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b98e5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b98e5-118">-確認</span><span class="sxs-lookup"><span data-stu-id="b98e5-118">-Confirm</span></span>
<span data-ttu-id="b98e5-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b98e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b98e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b98e5-120">-DefaultProfile</span></span>
<span data-ttu-id="b98e5-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b98e5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b98e5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b98e5-122">-InputObject</span></span>
<span data-ttu-id="b98e5-123">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="b98e5-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b98e5-124">-位置</span><span class="sxs-lookup"><span data-stu-id="b98e5-124">-Location</span></span>
<span data-ttu-id="b98e5-125">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="b98e5-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b98e5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b98e5-126">-Name</span></span>
<span data-ttu-id="b98e5-127">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="b98e5-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b98e5-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b98e5-128">-NetworkWatcher</span></span>
<span data-ttu-id="b98e5-129">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="b98e5-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="b98e5-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b98e5-130">-NetworkWatcherName</span></span>
<span data-ttu-id="b98e5-131">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b98e5-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="b98e5-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b98e5-132">-PassThru</span></span>
<span data-ttu-id="b98e5-133">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="b98e5-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b98e5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b98e5-134">-ResourceGroupName</span></span>
<span data-ttu-id="b98e5-135">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b98e5-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b98e5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b98e5-136">-ResourceId</span></span>
<span data-ttu-id="b98e5-137">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b98e5-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b98e5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b98e5-138">-WhatIf</span></span>
<span data-ttu-id="b98e5-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b98e5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b98e5-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b98e5-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="b98e5-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b98e5-141">INPUTS</span></span>

### <span data-ttu-id="b98e5-142">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b98e5-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b98e5-143">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="b98e5-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="b98e5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b98e5-144">OUTPUTS</span></span>

### <span data-ttu-id="b98e5-145">System.object</span><span class="sxs-lookup"><span data-stu-id="b98e5-145">System.Boolean</span></span>


## <span data-ttu-id="b98e5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b98e5-146">NOTES</span></span>
<span data-ttu-id="b98e5-147">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="b98e5-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b98e5-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b98e5-148">RELATED LINKS</span></span>
<span data-ttu-id="b98e5-149">[新-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="b98e5-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="b98e5-150">[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="b98e5-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="b98e5-151">[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="b98e5-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="b98e5-152">[新-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
[移除-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
[開始-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="b98e5-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>