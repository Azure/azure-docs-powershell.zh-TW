---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 58ee0531ea0671314e6f1e6d590b388c3f82ef34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909538"
---
# <span data-ttu-id="b272b-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b272b-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b272b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b272b-102">SYNOPSIS</span></span>
<span data-ttu-id="b272b-103">在負載平衡器中新增一個內入 NAT 區。</span><span class="sxs-lookup"><span data-stu-id="b272b-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="b272b-104">語法</span><span class="sxs-lookup"><span data-stu-id="b272b-104">SYNTAX</span></span>

### <span data-ttu-id="b272b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b272b-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b272b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b272b-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b272b-107">描述</span><span class="sxs-lookup"><span data-stu-id="b272b-107">DESCRIPTION</span></span>
<span data-ttu-id="b272b-108">**Add-AzLoadBalancerInboundNatPoolConfig** Cmdlet 會將內建 NAT 集區新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b272b-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="b272b-109">例子</span><span class="sxs-lookup"><span data-stu-id="b272b-109">EXAMPLES</span></span>

### <span data-ttu-id="b272b-110">範例 1：新增</span><span class="sxs-lookup"><span data-stu-id="b272b-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
PS C:\> $lb | Set-AzLoadBalancer
```

## <span data-ttu-id="b272b-111">參數</span><span class="sxs-lookup"><span data-stu-id="b272b-111">PARAMETERS</span></span>

### <span data-ttu-id="b272b-112">-後端埠</span><span class="sxs-lookup"><span data-stu-id="b272b-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b272b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b272b-113">-DefaultProfile</span></span>
<span data-ttu-id="b272b-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b272b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b272b-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b272b-115">-EnableFloatingIP</span></span>
<span data-ttu-id="b272b-116">針對設定 SQL AlwaysOn 可用性群組所需的浮動 IP 功能，設定虛擬機器的端點。</span><span class="sxs-lookup"><span data-stu-id="b272b-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="b272b-117">在 SQL Server 中使用 SQL AlwaysOn 可用性群組時，需要此設定。</span><span class="sxs-lookup"><span data-stu-id="b272b-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="b272b-118">建立端點之後，無法變更此設定。</span><span class="sxs-lookup"><span data-stu-id="b272b-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="b272b-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b272b-119">-EnableTcpReset</span></span>
<span data-ttu-id="b272b-120">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="b272b-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b272b-121">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="b272b-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b272b-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b272b-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b272b-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b272b-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b272b-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="b272b-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b272b-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="b272b-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b272b-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b272b-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b272b-127">TCP 閒置連接的超時。</span><span class="sxs-lookup"><span data-stu-id="b272b-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="b272b-128">該值可以在 4 到 30 分鐘之間設定。</span><span class="sxs-lookup"><span data-stu-id="b272b-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="b272b-129">預設值為 4 分鐘。</span><span class="sxs-lookup"><span data-stu-id="b272b-129">The default value is 4 minutes.</span></span> <span data-ttu-id="b272b-130">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="b272b-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b272b-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b272b-131">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b272b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="b272b-132">-Name</span></span>
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

### <span data-ttu-id="b272b-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b272b-133">-Protocol</span></span>
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

### <span data-ttu-id="b272b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b272b-134">-Confirm</span></span>
<span data-ttu-id="b272b-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b272b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b272b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b272b-136">-WhatIf</span></span>
<span data-ttu-id="b272b-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b272b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b272b-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b272b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b272b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b272b-139">CommonParameters</span></span>
<span data-ttu-id="b272b-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b272b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b272b-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b272b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b272b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b272b-142">INPUTS</span></span>

### <span data-ttu-id="b272b-143">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b272b-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b272b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b272b-144">System.String</span></span>

### <span data-ttu-id="b272b-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b272b-145">System.Int32</span></span>

### <span data-ttu-id="b272b-146">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b272b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b272b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b272b-147">OUTPUTS</span></span>

### <span data-ttu-id="b272b-148">Microsoft.Azure.Commands.Network.models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b272b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b272b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b272b-149">NOTES</span></span>

## <span data-ttu-id="b272b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b272b-150">RELATED LINKS</span></span>

[<span data-ttu-id="b272b-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b272b-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b272b-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b272b-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b272b-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b272b-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b272b-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b272b-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
