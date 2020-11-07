---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b02b2abec8138170d574492c8429f463fc6a28a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624241"
---
# <span data-ttu-id="4121c-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4121c-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4121c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4121c-102">SYNOPSIS</span></span>
<span data-ttu-id="4121c-103">為負載平衡器建立入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="4121c-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4121c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4121c-104">SYNTAX</span></span>

### <span data-ttu-id="4121c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="4121c-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4121c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4121c-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4121c-107">說明</span><span class="sxs-lookup"><span data-stu-id="4121c-107">DESCRIPTION</span></span>
<span data-ttu-id="4121c-108">**新的-AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet 會針對 Azure 負載平衡器建立入站網路位址轉譯 (NAT) 規則配置。</span><span class="sxs-lookup"><span data-stu-id="4121c-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4121c-109">示例</span><span class="sxs-lookup"><span data-stu-id="4121c-109">EXAMPLES</span></span>

### <span data-ttu-id="4121c-110">範例1：為負載平衡器建立入站 NAT 規則配置</span><span class="sxs-lookup"><span data-stu-id="4121c-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="4121c-111">第一個命令會在名為 MyResourceGroup 的資源群組中建立名為 MyPublicIP 的公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="4121c-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="4121c-112">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定，然後將其儲存在 $frontend 變數中。</span><span class="sxs-lookup"><span data-stu-id="4121c-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="4121c-113">第三個命令會在 $frontend 中使用前端物件來建立名為 MyInboundNatRule 的輸入 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="4121c-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="4121c-114">已指定 TCP 通訊協定，而前端埠是3389，這種情況與後端埠相同。</span><span class="sxs-lookup"><span data-stu-id="4121c-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="4121c-115">*FrontendIpConfiguration* 、 *Procotol* 、 *FrontendPort* 和 *BACKENDPORT* 參數都是建立入站 NAT 規則設定所必需的。</span><span class="sxs-lookup"><span data-stu-id="4121c-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="4121c-116">參數</span><span class="sxs-lookup"><span data-stu-id="4121c-116">PARAMETERS</span></span>

### <span data-ttu-id="4121c-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4121c-117">-BackendPort</span></span>
<span data-ttu-id="4121c-118">指定此規則設定所相符之流量的後端埠。</span><span class="sxs-lookup"><span data-stu-id="4121c-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="4121c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4121c-119">-DefaultProfile</span></span>
<span data-ttu-id="4121c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4121c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4121c-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4121c-121">-EnableFloatingIP</span></span>
<span data-ttu-id="4121c-122">表示此 Cmdlet 為規則設定啟用浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4121c-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4121c-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4121c-123">-EnableTcpReset</span></span>
<span data-ttu-id="4121c-124">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="4121c-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4121c-125">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="4121c-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4121c-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4121c-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4121c-127">指定要與負載平衡器規則配置相關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="4121c-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4121c-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4121c-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4121c-129">指定前端 IP 位址設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="4121c-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="4121c-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4121c-130">-FrontendPort</span></span>
<span data-ttu-id="4121c-131">指定與負載平衡器規則配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="4121c-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4121c-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4121c-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4121c-133">指定在負載平衡器中維持交談狀態的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="4121c-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="4121c-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="4121c-134">-Name</span></span>
<span data-ttu-id="4121c-135">指定此 Cmdlet 所建立之規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4121c-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4121c-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4121c-136">-Protocol</span></span>
<span data-ttu-id="4121c-137">指定通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4121c-137">Specifies a protocol.</span></span>
<span data-ttu-id="4121c-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4121c-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4121c-139">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="4121c-139">Tcp</span></span>
- <span data-ttu-id="4121c-140">Udp-in</span><span class="sxs-lookup"><span data-stu-id="4121c-140">Udp</span></span>

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

### <span data-ttu-id="4121c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="4121c-141">-Confirm</span></span>
<span data-ttu-id="4121c-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4121c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4121c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4121c-143">-WhatIf</span></span>
<span data-ttu-id="4121c-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4121c-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4121c-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4121c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4121c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4121c-146">CommonParameters</span></span>
<span data-ttu-id="4121c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4121c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4121c-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4121c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4121c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="4121c-149">INPUTS</span></span>

### <span data-ttu-id="4121c-150">所有</span><span class="sxs-lookup"><span data-stu-id="4121c-150">None</span></span>

## <span data-ttu-id="4121c-151">輸出</span><span class="sxs-lookup"><span data-stu-id="4121c-151">OUTPUTS</span></span>

### <span data-ttu-id="4121c-152">PSInboundNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4121c-152">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="4121c-153">筆記</span><span class="sxs-lookup"><span data-stu-id="4121c-153">NOTES</span></span>

## <span data-ttu-id="4121c-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="4121c-154">RELATED LINKS</span></span>

[<span data-ttu-id="4121c-155">附加 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4121c-155">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4121c-156">AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4121c-156">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4121c-157">新-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4121c-157">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4121c-158">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4121c-158">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="4121c-159">移除-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4121c-159">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4121c-160">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4121c-160">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


