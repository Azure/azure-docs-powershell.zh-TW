---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 402235f4d98b39ec78ffdc67bd0a01ab16e0400a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446961"
---
# <span data-ttu-id="bbe0c-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbe0c-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="bbe0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbe0c-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe0c-103">將入站 NAT 規則配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbe0c-104">SYNTAX</span></span>

### <span data-ttu-id="bbe0c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="bbe0c-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe0c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe0c-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe0c-107">說明</span><span class="sxs-lookup"><span data-stu-id="bbe0c-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe0c-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會將入站網路位址轉譯 (NAT) 規則設定新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="bbe0c-109">示例</span><span class="sxs-lookup"><span data-stu-id="bbe0c-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe0c-110">範例1：將入站 NAT 規則配置新增至負載平衡器</span><span class="sxs-lookup"><span data-stu-id="bbe0c-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="bbe0c-111">第一個命令會取得名為 MyloadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="bbe0c-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 **Add-AzureRmLoadBalancerInboundNatRuleConfig** ，這會將輸入的 NAT 規則設定新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="bbe0c-113">參數</span><span class="sxs-lookup"><span data-stu-id="bbe0c-113">PARAMETERS</span></span>

### <span data-ttu-id="bbe0c-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bbe0c-114">-BackendPort</span></span>
<span data-ttu-id="bbe0c-115">指定規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="bbe0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe0c-116">-DefaultProfile</span></span>
<span data-ttu-id="bbe0c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbe0c-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bbe0c-118">-EnableFloatingIP</span></span>
<span data-ttu-id="bbe0c-119">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="bbe0c-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="bbe0c-120">-EnableTcpReset</span></span>
<span data-ttu-id="bbe0c-121">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="bbe0c-122">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="bbe0c-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbe0c-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bbe0c-124">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="bbe0c-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bbe0c-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bbe0c-126">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="bbe0c-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bbe0c-127">-FrontendPort</span></span>
<span data-ttu-id="bbe0c-128">指定與規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="bbe0c-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bbe0c-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bbe0c-130">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="bbe0c-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbe0c-131">-LoadBalancer</span></span>
<span data-ttu-id="bbe0c-132">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="bbe0c-133">這個 Cmdlet 會將入站 NAT 規則配置新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbe0c-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbe0c-134">-Name</span></span>
<span data-ttu-id="bbe0c-135">指定要新增的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="bbe0c-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="bbe0c-136">-Protocol</span></span>
<span data-ttu-id="bbe0c-137">指定與入站 NAT 規則相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="bbe0c-138">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="bbe0c-139">-確認</span><span class="sxs-lookup"><span data-stu-id="bbe0c-139">-Confirm</span></span>
<span data-ttu-id="bbe0c-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbe0c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe0c-141">-WhatIf</span></span>
<span data-ttu-id="bbe0c-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbe0c-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbe0c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe0c-144">CommonParameters</span></span>
<span data-ttu-id="bbe0c-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe0c-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbe0c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe0c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="bbe0c-147">INPUTS</span></span>

### <span data-ttu-id="bbe0c-148">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbe0c-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="bbe0c-149">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bbe0c-149">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="bbe0c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="bbe0c-150">OUTPUTS</span></span>

### <span data-ttu-id="bbe0c-151">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbe0c-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bbe0c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="bbe0c-152">NOTES</span></span>

## <span data-ttu-id="bbe0c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbe0c-153">RELATED LINKS</span></span>

[<span data-ttu-id="bbe0c-154">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbe0c-154">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bbe0c-155">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbe0c-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bbe0c-156">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbe0c-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bbe0c-157">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbe0c-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bbe0c-158">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbe0c-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="bbe0c-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbe0c-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


