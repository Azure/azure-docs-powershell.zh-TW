---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800102"
---
# <span data-ttu-id="ba6dd-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ba6dd-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="ba6dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6dd-103">在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba6dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba6dd-104">SYNTAX</span></span>

### <span data-ttu-id="ba6dd-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ba6dd-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6dd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ba6dd-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba6dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="ba6dd-107">DESCRIPTION</span></span>
<span data-ttu-id="ba6dd-108">Get-AzureRmNetworkWatcherSecurityGroupView 可讓您在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="ba6dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba6dd-109">EXAMPLES</span></span>

### <span data-ttu-id="ba6dd-110">---範例1：在 VM 上進行安全性群組視圖呼叫---</span><span class="sxs-lookup"><span data-stu-id="ba6dd-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="ba6dd-111">在上述範例中，我們會先取得地區網路觀察程式，然後再取得區域中的 VM。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="ba6dd-112">接著，我們會在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="ba6dd-113">參數</span><span class="sxs-lookup"><span data-stu-id="ba6dd-113">PARAMETERS</span></span>

### <span data-ttu-id="ba6dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba6dd-114">-AsJob</span></span>
<span data-ttu-id="ba6dd-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ba6dd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba6dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6dd-116">-DefaultProfile</span></span>
<span data-ttu-id="ba6dd-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba6dd-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba6dd-118">-NetworkWatcher</span></span>
<span data-ttu-id="ba6dd-119">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="ba6dd-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ba6dd-120">-NetworkWatcherName</span></span>
<span data-ttu-id="ba6dd-121">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="ba6dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba6dd-123">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ba6dd-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ba6dd-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ba6dd-125">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="ba6dd-125">The target VM Id</span></span>

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

### <span data-ttu-id="ba6dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6dd-126">CommonParameters</span></span>
<span data-ttu-id="ba6dd-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6dd-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba6dd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6dd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ba6dd-129">INPUTS</span></span>

### <span data-ttu-id="ba6dd-130">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ba6dd-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ba6dd-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ba6dd-131">System.String</span></span>

## <span data-ttu-id="ba6dd-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ba6dd-132">OUTPUTS</span></span>

### <span data-ttu-id="ba6dd-133">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ba6dd-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="ba6dd-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ba6dd-134">NOTES</span></span>
<span data-ttu-id="ba6dd-135">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="ba6dd-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="ba6dd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba6dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba6dd-137">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba6dd-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ba6dd-138">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba6dd-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ba6dd-139">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba6dd-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ba6dd-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ba6dd-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ba6dd-141">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ba6dd-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ba6dd-142">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ba6dd-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ba6dd-143">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ba6dd-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ba6dd-144">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba6dd-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba6dd-145">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ba6dd-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ba6dd-146">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba6dd-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba6dd-147">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba6dd-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba6dd-148">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba6dd-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

