---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6f724cb7208afb1a5f9474048b5e2dc46c17f5af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790826"
---
# <span data-ttu-id="a7cd1-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7cd1-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a7cd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cd1-103">為負載平衡器建立入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a7cd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7cd1-104">SYNTAX</span></span>

### <span data-ttu-id="a7cd1-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a7cd1-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7cd1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7cd1-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7cd1-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7cd1-107">DESCRIPTION</span></span>
<span data-ttu-id="a7cd1-108">**新的-AzLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器建立入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a7cd1-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7cd1-109">EXAMPLES</span></span>

### <span data-ttu-id="a7cd1-110">範例1：為負載平衡器建立入站 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="a7cd1-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="a7cd1-111">第一個命令會在名為 MyResourceGroup 的資源群組中建立名為 MyPublicIP 的公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="a7cd1-112">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定，然後將其儲存在 $frontend 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="a7cd1-113">第三個命令會在 $frontend 中使用前端物件來建立名為 MyInboundNatRule 的輸入 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="a7cd1-114">已指定 TCP 通訊協定，而前端埠是3389，這種情況與後端埠相同。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="a7cd1-115">必須有 *FrontendIpConfiguration* 、 *Protocol* 、 *FrontendPort* 和 *BACKENDPORT* 參數，才能建立入站 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="a7cd1-116">參數</span><span class="sxs-lookup"><span data-stu-id="a7cd1-116">PARAMETERS</span></span>

### <span data-ttu-id="a7cd1-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a7cd1-117">-BackendPort</span></span>
<span data-ttu-id="a7cd1-118">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="a7cd1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cd1-119">-DefaultProfile</span></span>
<span data-ttu-id="a7cd1-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7cd1-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a7cd1-121">-EnableFloatingIP</span></span>
<span data-ttu-id="a7cd1-122">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a7cd1-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a7cd1-123">-EnableTcpReset</span></span>
<span data-ttu-id="a7cd1-124">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a7cd1-125">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a7cd1-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7cd1-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a7cd1-127">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a7cd1-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a7cd1-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a7cd1-129">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a7cd1-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a7cd1-130">-FrontendPort</span></span>
<span data-ttu-id="a7cd1-131">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a7cd1-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a7cd1-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a7cd1-133">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a7cd1-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7cd1-134">-Name</span></span>
<span data-ttu-id="a7cd1-135">指定此 Cmdlet 所建立之規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a7cd1-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a7cd1-136">-Protocol</span></span>
<span data-ttu-id="a7cd1-137">指定通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-137">Specifies a protocol.</span></span>
<span data-ttu-id="a7cd1-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a7cd1-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a7cd1-139">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="a7cd1-139">Tcp</span></span>
- <span data-ttu-id="a7cd1-140">Udp-in</span><span class="sxs-lookup"><span data-stu-id="a7cd1-140">Udp</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cd1-141">-確認</span><span class="sxs-lookup"><span data-stu-id="a7cd1-141">-Confirm</span></span>
<span data-ttu-id="a7cd1-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7cd1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7cd1-143">-WhatIf</span></span>
<span data-ttu-id="a7cd1-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7cd1-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7cd1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cd1-146">CommonParameters</span></span>
<span data-ttu-id="a7cd1-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cd1-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cd1-149">輸入</span><span class="sxs-lookup"><span data-stu-id="a7cd1-149">INPUTS</span></span>

### <span data-ttu-id="a7cd1-150">System.object</span><span class="sxs-lookup"><span data-stu-id="a7cd1-150">System.String</span></span>

### <span data-ttu-id="a7cd1-151">System.object</span><span class="sxs-lookup"><span data-stu-id="a7cd1-151">System.Int32</span></span>

### <span data-ttu-id="a7cd1-152">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7cd1-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a7cd1-153">輸出</span><span class="sxs-lookup"><span data-stu-id="a7cd1-153">OUTPUTS</span></span>

### <span data-ttu-id="a7cd1-154">PSInboundNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7cd1-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="a7cd1-155">筆記</span><span class="sxs-lookup"><span data-stu-id="a7cd1-155">NOTES</span></span>

## <span data-ttu-id="a7cd1-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7cd1-156">RELATED LINKS</span></span>

[<span data-ttu-id="a7cd1-157">附加 AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7cd1-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a7cd1-158">AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7cd1-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a7cd1-159">新-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7cd1-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a7cd1-160">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7cd1-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a7cd1-161">移除-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7cd1-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a7cd1-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7cd1-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


