---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50f3c3a02410adda37b26c88cd5196c4ae232f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906898"
---
# <span data-ttu-id="89fa4-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89fa4-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="89fa4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="89fa4-103">為負載平衡器建立外發規則組式。</span><span class="sxs-lookup"><span data-stu-id="89fa4-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="89fa4-104">語法</span><span class="sxs-lookup"><span data-stu-id="89fa4-104">SYNTAX</span></span>

### <span data-ttu-id="89fa4-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="89fa4-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89fa4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="89fa4-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89fa4-107">描述</span><span class="sxs-lookup"><span data-stu-id="89fa4-107">DESCRIPTION</span></span>
<span data-ttu-id="89fa4-108">**New-AzLoadBalancerOutboundRuleConfig** Cmdlet 會為 Azure 負載平衡器建立輸出規則組式。</span><span class="sxs-lookup"><span data-stu-id="89fa4-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="89fa4-109">例子</span><span class="sxs-lookup"><span data-stu-id="89fa4-109">EXAMPLES</span></span>

### <span data-ttu-id="89fa4-110">範例 1：建立負載平衡器外發規則組</span><span class="sxs-lookup"><span data-stu-id="89fa4-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="89fa4-111">第一個命令在名為 MyResourceGroup 的資源群組中建立名為 MyPublicIP 的公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="89fa4-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="89fa4-112">第二個命令會使用 $publicip 中的公用 IP 位址建立名為 FrontendIpConfig01 的前端 IP 組$frontend變數。</span><span class="sxs-lookup"><span data-stu-id="89fa4-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="89fa4-113">第三個命令會建立名為 BackAddressPool01 的後端位址資料庫組，然後將它儲存在$backend變數中。</span><span class="sxs-lookup"><span data-stu-id="89fa4-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="89fa4-114">第四個命令會使用 $frontend 和 $backend 中的前端和後端物件，建立名為 MyOutboundRule 的輸出規則$backend。</span><span class="sxs-lookup"><span data-stu-id="89fa4-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="89fa4-115">建立 *外* 發規則設定時，需要通訊協定 *、FrontendIPConfiguration* 和 *後端AddressPool* 參數。</span><span class="sxs-lookup"><span data-stu-id="89fa4-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="89fa4-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="89fa4-116">Example 2</span></span>

<span data-ttu-id="89fa4-117">為負載平衡器建立外發規則組式。</span><span class="sxs-lookup"><span data-stu-id="89fa4-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="89fa4-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="89fa4-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="89fa4-119">參數</span><span class="sxs-lookup"><span data-stu-id="89fa4-119">PARAMETERS</span></span>

### <span data-ttu-id="89fa4-120">-已配置OutboundPort</span><span class="sxs-lookup"><span data-stu-id="89fa4-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="89fa4-121">NAT 的外發端口數量。</span><span class="sxs-lookup"><span data-stu-id="89fa4-121">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-122">-後端AddressPool</span><span class="sxs-lookup"><span data-stu-id="89fa4-122">-BackendAddressPool</span></span>
<span data-ttu-id="89fa4-123">一組 DIP 的參照。</span><span class="sxs-lookup"><span data-stu-id="89fa4-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="89fa4-124">外發流量會隨機負載平衡于後端 IP 中的 IP。</span><span class="sxs-lookup"><span data-stu-id="89fa4-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-125">-後端AddressPoolId</span><span class="sxs-lookup"><span data-stu-id="89fa4-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="89fa4-126">一組 DIP 的參照。</span><span class="sxs-lookup"><span data-stu-id="89fa4-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="89fa4-127">外發流量會隨機負載平衡于後端 IP 中的 IP。</span><span class="sxs-lookup"><span data-stu-id="89fa4-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fa4-128">-DefaultProfile</span></span>
<span data-ttu-id="89fa4-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="89fa4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="89fa4-130">-EnableTcpReset</span></span>
<span data-ttu-id="89fa4-131">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="89fa4-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="89fa4-132">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="89fa4-132">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="89fa4-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="89fa4-134">負載平衡器的前一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="89fa4-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="89fa4-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="89fa4-136">TCP 閒置連接的超時</span><span class="sxs-lookup"><span data-stu-id="89fa4-136">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="89fa4-137">-Name</span></span>
<span data-ttu-id="89fa4-138">外發規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="89fa4-138">Name of the outbound rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-139">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="89fa4-139">-Protocol</span></span>
<span data-ttu-id="89fa4-140">通訊協定 - TCP、UDP 或全部</span><span class="sxs-lookup"><span data-stu-id="89fa4-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="89fa4-141">-確認</span><span class="sxs-lookup"><span data-stu-id="89fa4-141">-Confirm</span></span>
<span data-ttu-id="89fa4-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="89fa4-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89fa4-143">-WhatIf</span></span>
<span data-ttu-id="89fa4-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89fa4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89fa4-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89fa4-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fa4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fa4-146">CommonParameters</span></span>
<span data-ttu-id="89fa4-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89fa4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fa4-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="89fa4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fa4-149">輸入</span><span class="sxs-lookup"><span data-stu-id="89fa4-149">INPUTS</span></span>

### <span data-ttu-id="89fa4-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="89fa4-150">System.Int32</span></span>

### <span data-ttu-id="89fa4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="89fa4-151">System.String</span></span>

### <span data-ttu-id="89fa4-152">Microsoft.Azure.Commands.Network.models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="89fa4-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="89fa4-153">Microsoft.Azure.Commands.Network.models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="89fa4-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="89fa4-154">輸出</span><span class="sxs-lookup"><span data-stu-id="89fa4-154">OUTPUTS</span></span>

### <span data-ttu-id="89fa4-155">Microsoft.Azure.Commands.Network.models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="89fa4-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="89fa4-156">筆記</span><span class="sxs-lookup"><span data-stu-id="89fa4-156">NOTES</span></span>

## <span data-ttu-id="89fa4-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="89fa4-157">RELATED LINKS</span></span>

[<span data-ttu-id="89fa4-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89fa4-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="89fa4-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89fa4-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="89fa4-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89fa4-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="89fa4-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89fa4-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
