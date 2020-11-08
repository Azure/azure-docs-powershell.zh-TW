---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126463"
---
# <span data-ttu-id="73720-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73720-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="73720-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73720-102">SYNOPSIS</span></span>
<span data-ttu-id="73720-103">為負載平衡器建立入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="73720-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="73720-104">句法</span><span class="sxs-lookup"><span data-stu-id="73720-104">SYNTAX</span></span>

### <span data-ttu-id="73720-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="73720-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73720-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73720-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73720-107">說明</span><span class="sxs-lookup"><span data-stu-id="73720-107">DESCRIPTION</span></span>
<span data-ttu-id="73720-108">**新的 AzLoadBalancerInboundNatPoolConfig** Cmdlet 會為負載平衡器建立入站 NAT 池配置。</span><span class="sxs-lookup"><span data-stu-id="73720-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="73720-109">示例</span><span class="sxs-lookup"><span data-stu-id="73720-109">EXAMPLES</span></span>

### <span data-ttu-id="73720-110">範例1：新增</span><span class="sxs-lookup"><span data-stu-id="73720-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="73720-111">參數</span><span class="sxs-lookup"><span data-stu-id="73720-111">PARAMETERS</span></span>

### <span data-ttu-id="73720-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="73720-112">-BackendPort</span></span>
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

### <span data-ttu-id="73720-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73720-113">-DefaultProfile</span></span>
<span data-ttu-id="73720-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73720-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73720-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="73720-115">-EnableFloatingIP</span></span>
<span data-ttu-id="73720-116">針對設定 SQL AlwaysOn 可用性群組所需的浮動 IP 功能，配置虛擬機器的端點。</span><span class="sxs-lookup"><span data-stu-id="73720-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="73720-117">使用 SQL server 中的 SQL AlwaysOn 可用性群組時，此設定是必要的。</span><span class="sxs-lookup"><span data-stu-id="73720-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="73720-118">在您建立端點之後，就無法變更此設定。</span><span class="sxs-lookup"><span data-stu-id="73720-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="73720-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="73720-119">-EnableTcpReset</span></span>
<span data-ttu-id="73720-120">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="73720-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="73720-121">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="73720-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="73720-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="73720-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="73720-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="73720-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="73720-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="73720-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="73720-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="73720-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="73720-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="73720-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="73720-127">TCP 空閒連線的超時時間。</span><span class="sxs-lookup"><span data-stu-id="73720-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="73720-128">此值可設定為4到30分鐘。</span><span class="sxs-lookup"><span data-stu-id="73720-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="73720-129">預設值為4分鐘。</span><span class="sxs-lookup"><span data-stu-id="73720-129">The default value is 4 minutes.</span></span> <span data-ttu-id="73720-130">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="73720-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="73720-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="73720-131">-Name</span></span>
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

### <span data-ttu-id="73720-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="73720-132">-Protocol</span></span>
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

### <span data-ttu-id="73720-133">-確認</span><span class="sxs-lookup"><span data-stu-id="73720-133">-Confirm</span></span>
<span data-ttu-id="73720-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73720-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73720-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73720-135">-WhatIf</span></span>
<span data-ttu-id="73720-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73720-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73720-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73720-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73720-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73720-138">CommonParameters</span></span>
<span data-ttu-id="73720-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73720-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73720-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73720-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73720-141">輸入</span><span class="sxs-lookup"><span data-stu-id="73720-141">INPUTS</span></span>

### <span data-ttu-id="73720-142">System.object</span><span class="sxs-lookup"><span data-stu-id="73720-142">System.String</span></span>

### <span data-ttu-id="73720-143">System.object</span><span class="sxs-lookup"><span data-stu-id="73720-143">System.Int32</span></span>

### <span data-ttu-id="73720-144">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="73720-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="73720-145">輸出</span><span class="sxs-lookup"><span data-stu-id="73720-145">OUTPUTS</span></span>

### <span data-ttu-id="73720-146">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="73720-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="73720-147">筆記</span><span class="sxs-lookup"><span data-stu-id="73720-147">NOTES</span></span>

## <span data-ttu-id="73720-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="73720-148">RELATED LINKS</span></span>

[<span data-ttu-id="73720-149">附加 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73720-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="73720-150">AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73720-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="73720-151">移除-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73720-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="73720-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="73720-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
