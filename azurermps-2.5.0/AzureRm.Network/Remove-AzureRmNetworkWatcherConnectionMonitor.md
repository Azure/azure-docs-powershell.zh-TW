---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 046a2ee4591eb345efd71163d27140799cb229e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801213"
---
# <span data-ttu-id="38e1e-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e1e-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="38e1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="38e1e-103">移除 [連接監視器]。</span><span class="sxs-lookup"><span data-stu-id="38e1e-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38e1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="38e1e-104">SYNTAX</span></span>

### <span data-ttu-id="38e1e-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="38e1e-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="38e1e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="38e1e-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="38e1e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="38e1e-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="38e1e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="38e1e-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="38e1e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="38e1e-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="38e1e-110">說明</span><span class="sxs-lookup"><span data-stu-id="38e1e-110">DESCRIPTION</span></span>
<span data-ttu-id="38e1e-111">AzureRmNetworkWatcherConnectionMonitor Cmdlet 會移除指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="38e1e-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="38e1e-112">示例</span><span class="sxs-lookup"><span data-stu-id="38e1e-112">EXAMPLES</span></span>

### <span data-ttu-id="38e1e-113">---------------範例1：移除指定的連接監視器---------------</span><span class="sxs-lookup"><span data-stu-id="38e1e-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="38e1e-114">在這個範例中，我們會刪除由位置和名稱指定的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="38e1e-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="38e1e-115">參數</span><span class="sxs-lookup"><span data-stu-id="38e1e-115">PARAMETERS</span></span>

### <span data-ttu-id="38e1e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38e1e-116">-AsJob</span></span>
<span data-ttu-id="38e1e-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38e1e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38e1e-118">-確認</span><span class="sxs-lookup"><span data-stu-id="38e1e-118">-Confirm</span></span>
<span data-ttu-id="38e1e-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38e1e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e1e-120">-DefaultProfile</span></span>
<span data-ttu-id="38e1e-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38e1e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38e1e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38e1e-122">-InputObject</span></span>
<span data-ttu-id="38e1e-123">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="38e1e-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="38e1e-124">-位置</span><span class="sxs-lookup"><span data-stu-id="38e1e-124">-Location</span></span>
<span data-ttu-id="38e1e-125">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="38e1e-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="38e1e-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="38e1e-126">-Name</span></span>
<span data-ttu-id="38e1e-127">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="38e1e-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="38e1e-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="38e1e-128">-NetworkWatcher</span></span>
<span data-ttu-id="38e1e-129">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="38e1e-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="38e1e-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="38e1e-130">-NetworkWatcherName</span></span>
<span data-ttu-id="38e1e-131">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="38e1e-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="38e1e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38e1e-132">-PassThru</span></span>
<span data-ttu-id="38e1e-133">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="38e1e-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="38e1e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e1e-134">-ResourceGroupName</span></span>
<span data-ttu-id="38e1e-135">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38e1e-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="38e1e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38e1e-136">-ResourceId</span></span>
<span data-ttu-id="38e1e-137">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="38e1e-137">Resource ID.</span></span>

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

### <span data-ttu-id="38e1e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e1e-138">-WhatIf</span></span>
<span data-ttu-id="38e1e-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38e1e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38e1e-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38e1e-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="38e1e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="38e1e-141">INPUTS</span></span>

### <span data-ttu-id="38e1e-142">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="38e1e-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="38e1e-143">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="38e1e-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="38e1e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="38e1e-144">OUTPUTS</span></span>

### <span data-ttu-id="38e1e-145">System.object</span><span class="sxs-lookup"><span data-stu-id="38e1e-145">System.Boolean</span></span>


## <span data-ttu-id="38e1e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="38e1e-146">NOTES</span></span>
<span data-ttu-id="38e1e-147">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="38e1e-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="38e1e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="38e1e-148">RELATED LINKS</span></span>
<span data-ttu-id="38e1e-149">[新-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
[AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
[移除-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="38e1e-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="38e1e-150">[AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
[AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
[AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
[AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="38e1e-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="38e1e-151">[新-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
[新-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
[AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
[移除-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
[停止 AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="38e1e-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="38e1e-152">[新-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
[AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
[AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="38e1e-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>

