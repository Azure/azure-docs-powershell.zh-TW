---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 8e055df66c0623fbddbed8379cb25f165efb7081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624481"
---
# <span data-ttu-id="56f6a-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56f6a-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="56f6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="56f6a-103">將入站 NAT 規則配置新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="56f6a-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56f6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="56f6a-104">SYNTAX</span></span>

### <span data-ttu-id="56f6a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="56f6a-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56f6a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="56f6a-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f6a-107">說明</span><span class="sxs-lookup"><span data-stu-id="56f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="56f6a-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會將入站網路位址轉譯 (NAT) 規則設定新增至 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="56f6a-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="56f6a-109">示例</span><span class="sxs-lookup"><span data-stu-id="56f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="56f6a-110">範例1：將入站 NAT 規則配置新增至負載平衡器</span><span class="sxs-lookup"><span data-stu-id="56f6a-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="56f6a-111">第一個命令會取得名為 MyloadBalancer 的負載平衡器，然後將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="56f6a-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="56f6a-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 **Add-AzureRmLoadBalancerInboundNatRuleConfig** ，這會將輸入的 NAT 規則設定新增到負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="56f6a-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="56f6a-113">參數</span><span class="sxs-lookup"><span data-stu-id="56f6a-113">PARAMETERS</span></span>

### <span data-ttu-id="56f6a-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="56f6a-114">-BackendPort</span></span>
<span data-ttu-id="56f6a-115">指定規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="56f6a-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="56f6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f6a-116">-DefaultProfile</span></span>
<span data-ttu-id="56f6a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56f6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f6a-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="56f6a-118">-EnableFloatingIP</span></span>
<span data-ttu-id="56f6a-119">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="56f6a-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="56f6a-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f6a-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="56f6a-121">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="56f6a-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="56f6a-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="56f6a-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="56f6a-123">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="56f6a-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="56f6a-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="56f6a-124">-FrontendPort</span></span>
<span data-ttu-id="56f6a-125">指定與規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="56f6a-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="56f6a-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="56f6a-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="56f6a-127">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="56f6a-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="56f6a-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56f6a-128">-LoadBalancer</span></span>
<span data-ttu-id="56f6a-129">指定 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="56f6a-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="56f6a-130">這個 Cmdlet 會將入站 NAT 規則配置新增到此參數指定的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="56f6a-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="56f6a-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="56f6a-131">-Name</span></span>
<span data-ttu-id="56f6a-132">指定要新增的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="56f6a-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="56f6a-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="56f6a-133">-Protocol</span></span>
<span data-ttu-id="56f6a-134">指定與入站 NAT 規則相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="56f6a-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="56f6a-135">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="56f6a-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="56f6a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f6a-136">CommonParameters</span></span>
<span data-ttu-id="56f6a-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56f6a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f6a-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56f6a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f6a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="56f6a-139">INPUTS</span></span>

### <span data-ttu-id="56f6a-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56f6a-140">PSLoadBalancer</span></span>
<span data-ttu-id="56f6a-141">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="56f6a-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="56f6a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="56f6a-142">OUTPUTS</span></span>

### <span data-ttu-id="56f6a-143">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="56f6a-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="56f6a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="56f6a-144">NOTES</span></span>

## <span data-ttu-id="56f6a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="56f6a-145">RELATED LINKS</span></span>

[<span data-ttu-id="56f6a-146">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56f6a-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="56f6a-147">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56f6a-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="56f6a-148">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56f6a-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="56f6a-149">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56f6a-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="56f6a-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56f6a-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="56f6a-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56f6a-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


