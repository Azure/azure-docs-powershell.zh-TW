---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282089"
---
# <span data-ttu-id="55d53-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55d53-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="55d53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55d53-102">SYNOPSIS</span></span>
<span data-ttu-id="55d53-103">設定負載平衡器的入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="55d53-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="55d53-104">句法</span><span class="sxs-lookup"><span data-stu-id="55d53-104">SYNTAX</span></span>

### <span data-ttu-id="55d53-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="55d53-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55d53-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55d53-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55d53-107">說明</span><span class="sxs-lookup"><span data-stu-id="55d53-107">DESCRIPTION</span></span>
<span data-ttu-id="55d53-108">**AzLoadBalancerInboundNatPoolConfig** Cmdlet 會為負載平衡器設定入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="55d53-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="55d53-109">示例</span><span class="sxs-lookup"><span data-stu-id="55d53-109">EXAMPLES</span></span>

### <span data-ttu-id="55d53-110">範例1：設定</span><span class="sxs-lookup"><span data-stu-id="55d53-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="55d53-111">參數</span><span class="sxs-lookup"><span data-stu-id="55d53-111">PARAMETERS</span></span>

### <span data-ttu-id="55d53-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="55d53-112">-BackendPort</span></span>
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

### <span data-ttu-id="55d53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d53-113">-DefaultProfile</span></span>
<span data-ttu-id="55d53-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55d53-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55d53-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="55d53-115">-EnableFloatingIP</span></span>
<span data-ttu-id="55d53-116">針對設定 SQL AlwaysOn 可用性群組所需的浮動 IP 功能，配置虛擬機器的端點。</span><span class="sxs-lookup"><span data-stu-id="55d53-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="55d53-117">使用 SQL server 中的 SQL AlwaysOn 可用性群組時，此設定是必要的。</span><span class="sxs-lookup"><span data-stu-id="55d53-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="55d53-118">在您建立端點之後，就無法變更此設定。</span><span class="sxs-lookup"><span data-stu-id="55d53-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="55d53-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="55d53-119">-EnableTcpReset</span></span>
<span data-ttu-id="55d53-120">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="55d53-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="55d53-121">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="55d53-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="55d53-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="55d53-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="55d53-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="55d53-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="55d53-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="55d53-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="55d53-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="55d53-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="55d53-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="55d53-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="55d53-127">TCP 空閒連線的超時時間。</span><span class="sxs-lookup"><span data-stu-id="55d53-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="55d53-128">此值可設定為4到30分鐘。</span><span class="sxs-lookup"><span data-stu-id="55d53-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="55d53-129">預設值為4分鐘。</span><span class="sxs-lookup"><span data-stu-id="55d53-129">The default value is 4 minutes.</span></span> <span data-ttu-id="55d53-130">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="55d53-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="55d53-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55d53-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="55d53-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="55d53-132">-Name</span></span>
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

### <span data-ttu-id="55d53-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="55d53-133">-Protocol</span></span>
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

### <span data-ttu-id="55d53-134">-確認</span><span class="sxs-lookup"><span data-stu-id="55d53-134">-Confirm</span></span>
<span data-ttu-id="55d53-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55d53-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d53-136">-WhatIf</span></span>
<span data-ttu-id="55d53-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55d53-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55d53-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55d53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55d53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d53-139">CommonParameters</span></span>
<span data-ttu-id="55d53-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55d53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d53-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55d53-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d53-142">輸入</span><span class="sxs-lookup"><span data-stu-id="55d53-142">INPUTS</span></span>

### <span data-ttu-id="55d53-143">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55d53-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="55d53-144">System.object</span><span class="sxs-lookup"><span data-stu-id="55d53-144">System.String</span></span>

### <span data-ttu-id="55d53-145">System.object</span><span class="sxs-lookup"><span data-stu-id="55d53-145">System.Int32</span></span>

### <span data-ttu-id="55d53-146">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55d53-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="55d53-147">輸出</span><span class="sxs-lookup"><span data-stu-id="55d53-147">OUTPUTS</span></span>

### <span data-ttu-id="55d53-148">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55d53-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55d53-149">筆記</span><span class="sxs-lookup"><span data-stu-id="55d53-149">NOTES</span></span>

## <span data-ttu-id="55d53-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="55d53-150">RELATED LINKS</span></span>

[<span data-ttu-id="55d53-151">附加 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55d53-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="55d53-152">AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55d53-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="55d53-153">新-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55d53-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="55d53-154">移除-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="55d53-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
