---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 61b23db6cfc634b318aa0070b5f784ad7067a234
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795371"
---
# <span data-ttu-id="01812-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="01812-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="01812-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01812-102">SYNOPSIS</span></span>
<span data-ttu-id="01812-103">啟動連線監視器</span><span class="sxs-lookup"><span data-stu-id="01812-103">Start a connection monitor</span></span>

## <span data-ttu-id="01812-104">句法</span><span class="sxs-lookup"><span data-stu-id="01812-104">SYNTAX</span></span>

### <span data-ttu-id="01812-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="01812-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01812-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="01812-106">SetByName</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01812-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="01812-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01812-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="01812-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01812-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="01812-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="01812-110">說明</span><span class="sxs-lookup"><span data-stu-id="01812-110">DESCRIPTION</span></span>
<span data-ttu-id="01812-111">Start-AzNetworkWatcherConnectionMonitor Cmdlet 會啟動指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="01812-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="01812-112">示例</span><span class="sxs-lookup"><span data-stu-id="01812-112">EXAMPLES</span></span>

### <span data-ttu-id="01812-113">---------------範例1：啟動連線監視器---------------</span><span class="sxs-lookup"><span data-stu-id="01812-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="01812-114">在這個範例中，我們會啟動由名稱和網路監視程式指定的連線監視器</span><span class="sxs-lookup"><span data-stu-id="01812-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="01812-115">參數</span><span class="sxs-lookup"><span data-stu-id="01812-115">PARAMETERS</span></span>

### <span data-ttu-id="01812-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01812-116">-AsJob</span></span>
<span data-ttu-id="01812-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="01812-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01812-118">-確認</span><span class="sxs-lookup"><span data-stu-id="01812-118">-Confirm</span></span>
<span data-ttu-id="01812-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01812-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01812-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01812-120">-DefaultProfile</span></span>
<span data-ttu-id="01812-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01812-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01812-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01812-122">-InputObject</span></span>
<span data-ttu-id="01812-123">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="01812-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="01812-124">-位置</span><span class="sxs-lookup"><span data-stu-id="01812-124">-Location</span></span>
<span data-ttu-id="01812-125">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="01812-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="01812-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="01812-126">-Name</span></span>
<span data-ttu-id="01812-127">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="01812-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="01812-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="01812-128">-NetworkWatcher</span></span>
<span data-ttu-id="01812-129">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="01812-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="01812-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="01812-130">-NetworkWatcherName</span></span>
<span data-ttu-id="01812-131">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="01812-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="01812-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01812-132">-PassThru</span></span>
<span data-ttu-id="01812-133">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="01812-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="01812-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01812-134">-ResourceGroupName</span></span>
<span data-ttu-id="01812-135">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="01812-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="01812-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01812-136">-ResourceId</span></span>
<span data-ttu-id="01812-137">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="01812-137">Resource ID.</span></span>

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

### <span data-ttu-id="01812-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01812-138">-WhatIf</span></span>
<span data-ttu-id="01812-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01812-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01812-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01812-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="01812-141">輸入</span><span class="sxs-lookup"><span data-stu-id="01812-141">INPUTS</span></span>

### <span data-ttu-id="01812-142">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="01812-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="01812-143">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="01812-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="01812-144">輸出</span><span class="sxs-lookup"><span data-stu-id="01812-144">OUTPUTS</span></span>

### <span data-ttu-id="01812-145">System.object</span><span class="sxs-lookup"><span data-stu-id="01812-145">System.Boolean</span></span>


## <span data-ttu-id="01812-146">筆記</span><span class="sxs-lookup"><span data-stu-id="01812-146">NOTES</span></span>
<span data-ttu-id="01812-147">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="01812-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="01812-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="01812-148">RELATED LINKS</span></span>
<span data-ttu-id="01812-149">[新-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="01812-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="01812-150">[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="01812-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="01812-151">[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="01812-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="01812-152">[AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
[移除-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
[停止 AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="01812-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span></span>