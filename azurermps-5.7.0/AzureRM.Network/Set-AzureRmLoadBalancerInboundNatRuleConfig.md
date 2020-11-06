---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 98f7052ab0fa326789242cdebaf34f188684993e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447754"
---
# <span data-ttu-id="9fb4b-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fb4b-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9fb4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fb4b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb4b-103">為負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fb4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fb4b-104">SYNTAX</span></span>

### <span data-ttu-id="9fb4b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fb4b-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb4b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9fb4b-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fb4b-107">說明</span><span class="sxs-lookup"><span data-stu-id="9fb4b-107">DESCRIPTION</span></span>
<span data-ttu-id="9fb4b-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9fb4b-109">示例</span><span class="sxs-lookup"><span data-stu-id="9fb4b-109">EXAMPLES</span></span>

### <span data-ttu-id="9fb4b-110">範例1：修改負載平衡器上的輸入 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="9fb4b-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="9fb4b-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="9fb4b-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerInboundNatRuleConfig，這會將輸入的 NAT 規則設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="9fb4b-113">第三個命令會將負載平衡器傳到 **AzureRmLoadBalancerInboundNatRuleConfig** ，這會儲存並更新入站 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="9fb4b-114">請注意，規則設定沒有啟用浮動 IP，而是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="9fb4b-115">參數</span><span class="sxs-lookup"><span data-stu-id="9fb4b-115">PARAMETERS</span></span>

### <span data-ttu-id="9fb4b-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9fb4b-116">-BackendPort</span></span>
<span data-ttu-id="9fb4b-117">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb4b-118">-DefaultProfile</span></span>
<span data-ttu-id="9fb4b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fb4b-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9fb4b-120">-EnableFloatingIP</span></span>
<span data-ttu-id="9fb4b-121">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9fb4b-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fb4b-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9fb4b-123">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9fb4b-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9fb4b-125">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-125">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fb4b-126">-FrontendPort</span></span>
<span data-ttu-id="9fb4b-127">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9fb4b-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9fb4b-129">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fb4b-130">-LoadBalancer</span></span>
<span data-ttu-id="9fb4b-131">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-131">Specifies a load balancer.</span></span>
<span data-ttu-id="9fb4b-132">這個 Cmdlet 為此參數指定的負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fb4b-133">-Name</span></span>
<span data-ttu-id="9fb4b-134">指定入站 NAT 規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-134">Specifies the name of an inbound NAT rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-135">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9fb4b-135">-Protocol</span></span>
<span data-ttu-id="9fb4b-136">指定與入站 NAT 規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="9fb4b-137">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb4b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb4b-138">CommonParameters</span></span>
<span data-ttu-id="9fb4b-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb4b-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9fb4b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb4b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9fb4b-141">INPUTS</span></span>

### <span data-ttu-id="9fb4b-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fb4b-142">PSLoadBalancer</span></span>
<span data-ttu-id="9fb4b-143">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9fb4b-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9fb4b-144">輸出</span><span class="sxs-lookup"><span data-stu-id="9fb4b-144">OUTPUTS</span></span>

### <span data-ttu-id="9fb4b-145">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9fb4b-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9fb4b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="9fb4b-146">NOTES</span></span>

## <span data-ttu-id="9fb4b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fb4b-147">RELATED LINKS</span></span>

[<span data-ttu-id="9fb4b-148">附加 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fb4b-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9fb4b-149">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fb4b-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9fb4b-150">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fb4b-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9fb4b-151">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fb4b-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9fb4b-152">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fb4b-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


