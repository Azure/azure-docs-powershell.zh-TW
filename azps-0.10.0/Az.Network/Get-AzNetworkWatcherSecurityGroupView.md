---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794382"
---
# <span data-ttu-id="67f20-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="67f20-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="67f20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67f20-102">SYNOPSIS</span></span>
<span data-ttu-id="67f20-103">在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="67f20-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="67f20-104">句法</span><span class="sxs-lookup"><span data-stu-id="67f20-104">SYNTAX</span></span>

### <span data-ttu-id="67f20-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="67f20-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f20-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="67f20-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67f20-107">說明</span><span class="sxs-lookup"><span data-stu-id="67f20-107">DESCRIPTION</span></span>
<span data-ttu-id="67f20-108">Get-AzNetworkWatcherSecurityGroupView 可讓您在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="67f20-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="67f20-109">示例</span><span class="sxs-lookup"><span data-stu-id="67f20-109">EXAMPLES</span></span>

### <span data-ttu-id="67f20-110">---範例1：在 VM 上進行安全性群組視圖呼叫---</span><span class="sxs-lookup"><span data-stu-id="67f20-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="67f20-111">在上述範例中，我們會先取得地區網路觀察程式，然後再取得區域中的 VM。</span><span class="sxs-lookup"><span data-stu-id="67f20-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="67f20-112">接著，我們會在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="67f20-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="67f20-113">參數</span><span class="sxs-lookup"><span data-stu-id="67f20-113">PARAMETERS</span></span>

### <span data-ttu-id="67f20-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67f20-114">-AsJob</span></span>
<span data-ttu-id="67f20-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67f20-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67f20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f20-116">-DefaultProfile</span></span>
<span data-ttu-id="67f20-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67f20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67f20-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67f20-118">-NetworkWatcher</span></span>
<span data-ttu-id="67f20-119">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="67f20-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="67f20-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="67f20-120">-NetworkWatcherName</span></span>
<span data-ttu-id="67f20-121">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="67f20-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="67f20-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f20-122">-ResourceGroupName</span></span>
<span data-ttu-id="67f20-123">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67f20-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="67f20-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="67f20-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="67f20-125">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="67f20-125">The target VM Id</span></span>

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

### <span data-ttu-id="67f20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f20-126">CommonParameters</span></span>
<span data-ttu-id="67f20-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67f20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f20-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67f20-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f20-129">輸入</span><span class="sxs-lookup"><span data-stu-id="67f20-129">INPUTS</span></span>

### <span data-ttu-id="67f20-130">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="67f20-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="67f20-131">System.object</span><span class="sxs-lookup"><span data-stu-id="67f20-131">System.String</span></span>

## <span data-ttu-id="67f20-132">輸出</span><span class="sxs-lookup"><span data-stu-id="67f20-132">OUTPUTS</span></span>

### <span data-ttu-id="67f20-133">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="67f20-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="67f20-134">筆記</span><span class="sxs-lookup"><span data-stu-id="67f20-134">NOTES</span></span>
<span data-ttu-id="67f20-135">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="67f20-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="67f20-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="67f20-136">RELATED LINKS</span></span>

[<span data-ttu-id="67f20-137">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67f20-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="67f20-138">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67f20-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="67f20-139">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67f20-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="67f20-140">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="67f20-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="67f20-141">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="67f20-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="67f20-142">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="67f20-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="67f20-143">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="67f20-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="67f20-144">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67f20-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="67f20-145">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="67f20-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="67f20-146">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67f20-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="67f20-147">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67f20-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="67f20-148">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67f20-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

