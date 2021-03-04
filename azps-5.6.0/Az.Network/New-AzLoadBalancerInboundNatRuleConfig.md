---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a6bec76345df188ca58e8b790637e35606de1f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914729"
---
# <span data-ttu-id="ab049-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab049-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ab049-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab049-102">SYNOPSIS</span></span>
<span data-ttu-id="ab049-103">為負載平衡器建立內入 NAT 規則組。</span><span class="sxs-lookup"><span data-stu-id="ab049-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ab049-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab049-104">SYNTAX</span></span>

### <span data-ttu-id="ab049-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ab049-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab049-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab049-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab049-107">描述</span><span class="sxs-lookup"><span data-stu-id="ab049-107">DESCRIPTION</span></span>
<span data-ttu-id="ab049-108">**New-AzLoadBalancerInboundNatRuleConfig** Cmdlet 會為 Azure 負載平衡器建立輸入網路位址轉譯 (NAT) 規則組式。</span><span class="sxs-lookup"><span data-stu-id="ab049-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ab049-109">例子</span><span class="sxs-lookup"><span data-stu-id="ab049-109">EXAMPLES</span></span>

### <span data-ttu-id="ab049-110">範例 1：為負載平衡器建立內入 NAT 規則組</span><span class="sxs-lookup"><span data-stu-id="ab049-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="ab049-111">第一個命令在名為 MyResourceGroup 的資源群組中建立名為 MyPublicIP 的公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="ab049-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="ab049-112">第二個命令會使用 $publicip 中的公用 IP 位址建立名為 FrontendIpConfig01 的前端 IP 組$frontend變數。</span><span class="sxs-lookup"><span data-stu-id="ab049-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="ab049-113">第三個命令會使用 $frontend 中的前端物件，建立名為 MyInboundNatRule 的輸入 NAT 規則$frontend。</span><span class="sxs-lookup"><span data-stu-id="ab049-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="ab049-114">已指定 TCP 通訊協定，且前端埠為 3389，與這種情況中的後端埠相同。</span><span class="sxs-lookup"><span data-stu-id="ab049-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="ab049-115">若要 *建立輸入 NAT 規則設定，需要 FrontendIpConfiguration、Protocol、FrontendPort* 和 *後端Port* 參數。  </span><span class="sxs-lookup"><span data-stu-id="ab049-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="ab049-116">參數</span><span class="sxs-lookup"><span data-stu-id="ab049-116">PARAMETERS</span></span>

### <span data-ttu-id="ab049-117">-後端埠</span><span class="sxs-lookup"><span data-stu-id="ab049-117">-BackendPort</span></span>
<span data-ttu-id="ab049-118">指定符合此規則組配置的流量後端埠。</span><span class="sxs-lookup"><span data-stu-id="ab049-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="ab049-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab049-119">-DefaultProfile</span></span>
<span data-ttu-id="ab049-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab049-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab049-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ab049-121">-EnableFloatingIP</span></span>
<span data-ttu-id="ab049-122">表示此 Cmdlet 啟用規則配置的浮動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ab049-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ab049-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ab049-123">-EnableTcpReset</span></span>
<span data-ttu-id="ab049-124">在 TCP 流程閒置超時或非預期的連接終止時接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="ab049-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ab049-125">只有在通訊協定設定為 TCP 時，才能使用此元素。</span><span class="sxs-lookup"><span data-stu-id="ab049-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ab049-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab049-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ab049-127">指定要與負載平衡器規則群組原則關聯的前端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="ab049-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ab049-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ab049-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ab049-129">指定前端 IP 位址配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab049-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ab049-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ab049-130">-FrontendPort</span></span>
<span data-ttu-id="ab049-131">指定與負載平衡器規則組配置相符的前端埠。</span><span class="sxs-lookup"><span data-stu-id="ab049-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ab049-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ab049-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ab049-133">指定在負載平衡器中維護交談狀態的時間長度 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="ab049-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ab049-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab049-134">-Name</span></span>
<span data-ttu-id="ab049-135">指定此 Cmdlet 所建立的規則組組名稱。</span><span class="sxs-lookup"><span data-stu-id="ab049-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ab049-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ab049-136">-Protocol</span></span>
<span data-ttu-id="ab049-137">指定通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ab049-137">Specifies a protocol.</span></span>
<span data-ttu-id="ab049-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab049-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab049-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="ab049-139">Tcp</span></span>
- <span data-ttu-id="ab049-140">Udp</span><span class="sxs-lookup"><span data-stu-id="ab049-140">Udp</span></span>

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

### <span data-ttu-id="ab049-141">-確認</span><span class="sxs-lookup"><span data-stu-id="ab049-141">-Confirm</span></span>
<span data-ttu-id="ab049-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ab049-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab049-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab049-143">-WhatIf</span></span>
<span data-ttu-id="ab049-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab049-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab049-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab049-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab049-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab049-146">CommonParameters</span></span>
<span data-ttu-id="ab049-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab049-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab049-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ab049-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab049-149">輸入</span><span class="sxs-lookup"><span data-stu-id="ab049-149">INPUTS</span></span>

### <span data-ttu-id="ab049-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ab049-150">System.String</span></span>

### <span data-ttu-id="ab049-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ab049-151">System.Int32</span></span>

### <span data-ttu-id="ab049-152">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab049-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ab049-153">輸出</span><span class="sxs-lookup"><span data-stu-id="ab049-153">OUTPUTS</span></span>

### <span data-ttu-id="ab049-154">Microsoft.Azure.Commands.Network.models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ab049-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="ab049-155">筆記</span><span class="sxs-lookup"><span data-stu-id="ab049-155">NOTES</span></span>

## <span data-ttu-id="ab049-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab049-156">RELATED LINKS</span></span>

[<span data-ttu-id="ab049-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab049-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ab049-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab049-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ab049-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab049-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ab049-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ab049-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ab049-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab049-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ab049-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab049-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


