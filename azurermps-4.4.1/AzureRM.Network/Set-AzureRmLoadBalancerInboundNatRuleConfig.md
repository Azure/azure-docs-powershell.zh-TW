---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 004180f2369616654741df960a56a9f9c5bb6047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448125"
---
# <span data-ttu-id="fceae-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fceae-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="fceae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fceae-102">SYNOPSIS</span></span>
<span data-ttu-id="fceae-103">為負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="fceae-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fceae-104">句法</span><span class="sxs-lookup"><span data-stu-id="fceae-104">SYNTAX</span></span>

### <span data-ttu-id="fceae-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fceae-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fceae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fceae-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fceae-107">說明</span><span class="sxs-lookup"><span data-stu-id="fceae-107">DESCRIPTION</span></span>
<span data-ttu-id="fceae-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器設定入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="fceae-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="fceae-109">示例</span><span class="sxs-lookup"><span data-stu-id="fceae-109">EXAMPLES</span></span>

### <span data-ttu-id="fceae-110">範例1：修改負載平衡器上的輸入 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="fceae-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="fceae-111">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="fceae-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="fceae-112">第二個命令使用管線運算子，將負載平衡器 $slb 至 Add-AzureRmLoadBalancerInboundNatRuleConfig，這會將輸入的 NAT 規則設定新增到其中。</span><span class="sxs-lookup"><span data-stu-id="fceae-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="fceae-113">第三個命令會將負載平衡器傳到 **AzureRmLoadBalancerInboundNatRuleConfig** ，這會儲存並更新入站 NAT 規則設定。</span><span class="sxs-lookup"><span data-stu-id="fceae-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="fceae-114">請注意，規則設定沒有啟用浮動 IP，而是由前一個命令所啟用。</span><span class="sxs-lookup"><span data-stu-id="fceae-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="fceae-115">參數</span><span class="sxs-lookup"><span data-stu-id="fceae-115">PARAMETERS</span></span>

### <span data-ttu-id="fceae-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fceae-116">-BackendPort</span></span>
<span data-ttu-id="fceae-117">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="fceae-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="fceae-118">-EnableFloatingIP</span></span>
<span data-ttu-id="fceae-119">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fceae-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="fceae-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fceae-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="fceae-121">指定要與入站 NAT 規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="fceae-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fceae-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="fceae-123">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="fceae-123">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="fceae-124">-FrontendPort</span></span>
<span data-ttu-id="fceae-125">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="fceae-125">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fceae-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fceae-127">指定在負載平衡器中維護交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="fceae-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fceae-128">-LoadBalancer</span></span>
<span data-ttu-id="fceae-129">指定負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="fceae-129">Specifies a load balancer.</span></span>
<span data-ttu-id="fceae-130">這個 Cmdlet 為此參數指定的負載平衡器設定入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="fceae-130">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="fceae-131">-Name</span></span>
<span data-ttu-id="fceae-132">指定入站 NAT 規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="fceae-132">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="fceae-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="fceae-133">-Protocol</span></span>
<span data-ttu-id="fceae-134">指定與入站 NAT 規則配置相符的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fceae-134">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="fceae-135">此參數可接受的值為： Tcp 或 Udp。</span><span class="sxs-lookup"><span data-stu-id="fceae-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fceae-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fceae-136">-DefaultProfile</span></span>
<span data-ttu-id="fceae-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fceae-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fceae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fceae-138">CommonParameters</span></span>
<span data-ttu-id="fceae-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fceae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fceae-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fceae-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fceae-141">輸入</span><span class="sxs-lookup"><span data-stu-id="fceae-141">INPUTS</span></span>

### <span data-ttu-id="fceae-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fceae-142">PSLoadBalancer</span></span>
<span data-ttu-id="fceae-143">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fceae-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fceae-144">輸出</span><span class="sxs-lookup"><span data-stu-id="fceae-144">OUTPUTS</span></span>

### <span data-ttu-id="fceae-145">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fceae-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fceae-146">筆記</span><span class="sxs-lookup"><span data-stu-id="fceae-146">NOTES</span></span>

## <span data-ttu-id="fceae-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="fceae-147">RELATED LINKS</span></span>

[<span data-ttu-id="fceae-148">附加 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fceae-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fceae-149">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fceae-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fceae-150">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fceae-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fceae-151">新-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fceae-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fceae-152">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fceae-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


