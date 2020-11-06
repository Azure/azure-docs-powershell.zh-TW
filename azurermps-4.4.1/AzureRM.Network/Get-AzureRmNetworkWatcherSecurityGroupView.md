---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451616"
---
# <span data-ttu-id="a7482-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a7482-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="a7482-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7482-102">SYNOPSIS</span></span>
<span data-ttu-id="a7482-103">在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="a7482-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7482-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7482-104">SYNTAX</span></span>

### <span data-ttu-id="a7482-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a7482-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7482-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a7482-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7482-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7482-107">DESCRIPTION</span></span>
<span data-ttu-id="a7482-108">Get-AzureRmNetworkWatcherSecurityGroupView 可讓您在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="a7482-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="a7482-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7482-109">EXAMPLES</span></span>

### <span data-ttu-id="a7482-110">---範例1：在 VM 上進行安全性群組視圖呼叫---</span><span class="sxs-lookup"><span data-stu-id="a7482-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="a7482-111">在上述範例中，我們會先取得地區網路觀察程式，然後再取得區域中的 VM。</span><span class="sxs-lookup"><span data-stu-id="a7482-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="a7482-112">接著，我們會在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="a7482-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="a7482-113">參數</span><span class="sxs-lookup"><span data-stu-id="a7482-113">PARAMETERS</span></span>

### <span data-ttu-id="a7482-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7482-114">-NetworkWatcher</span></span>
<span data-ttu-id="a7482-115">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a7482-115">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7482-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a7482-116">-NetworkWatcherName</span></span>
<span data-ttu-id="a7482-117">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7482-117">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7482-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7482-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7482-119">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7482-119">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7482-120">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a7482-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a7482-121">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="a7482-121">The target VM Id</span></span>

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

### <span data-ttu-id="a7482-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7482-122">-DefaultProfile</span></span>
<span data-ttu-id="a7482-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7482-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7482-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7482-124">CommonParameters</span></span>
<span data-ttu-id="a7482-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7482-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7482-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7482-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7482-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a7482-127">INPUTS</span></span>

### <span data-ttu-id="a7482-128">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7482-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a7482-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a7482-129">System.String</span></span>

## <span data-ttu-id="a7482-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a7482-130">OUTPUTS</span></span>

### <span data-ttu-id="a7482-131">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7482-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="a7482-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a7482-132">NOTES</span></span>
<span data-ttu-id="a7482-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="a7482-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="a7482-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7482-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7482-135">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7482-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a7482-136">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7482-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a7482-137">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7482-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a7482-138">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a7482-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a7482-139">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a7482-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a7482-140">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a7482-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a7482-141">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a7482-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a7482-142">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7482-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7482-143">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a7482-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a7482-144">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7482-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7482-145">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7482-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7482-146">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7482-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

