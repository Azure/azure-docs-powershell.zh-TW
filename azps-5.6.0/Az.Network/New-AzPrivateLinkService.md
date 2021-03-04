---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 9ed82247ff0b1813293059a7608557184bdb18ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903486"
---
# <span data-ttu-id="c52b4-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c52b4-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="c52b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c52b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c52b4-103">建立私人連結服務</span><span class="sxs-lookup"><span data-stu-id="c52b4-103">Creates a private link service</span></span>

## <span data-ttu-id="c52b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="c52b4-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c52b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="c52b4-105">DESCRIPTION</span></span>
<span data-ttu-id="c52b4-106">**New-AzPrivateLinkService** Cmdlet 會建立私人連結服務</span><span class="sxs-lookup"><span data-stu-id="c52b4-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="c52b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="c52b4-107">EXAMPLES</span></span>

### <span data-ttu-id="c52b4-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c52b4-108">Example 1</span></span>

<span data-ttu-id="c52b4-109">下列範例會建立私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="c52b4-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="c52b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="c52b4-110">PARAMETERS</span></span>

### <span data-ttu-id="c52b4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c52b4-111">-AsJob</span></span>
<span data-ttu-id="c52b4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c52b4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c52b4-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="c52b4-113">-AutoApproval</span></span>
<span data-ttu-id="c52b4-114">私人連結服務的自動核准訂閱</span><span class="sxs-lookup"><span data-stu-id="c52b4-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52b4-115">-DefaultProfile</span></span>
<span data-ttu-id="c52b4-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c52b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c52b4-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="c52b4-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="c52b4-118">啟用私人連結服務的 Proxy 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c52b4-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="c52b4-119">-強制</span><span class="sxs-lookup"><span data-stu-id="c52b4-119">-Force</span></span>
<span data-ttu-id="c52b4-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="c52b4-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c52b4-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c52b4-121">-IpConfiguration</span></span>
<span data-ttu-id="c52b4-122">IP 組配置</span><span class="sxs-lookup"><span data-stu-id="c52b4-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52b4-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c52b4-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="c52b4-124">前端 IP 組配置</span><span class="sxs-lookup"><span data-stu-id="c52b4-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52b4-125">-位置</span><span class="sxs-lookup"><span data-stu-id="c52b4-125">-Location</span></span>
<span data-ttu-id="c52b4-126">位置。</span><span class="sxs-lookup"><span data-stu-id="c52b4-126">location.</span></span>

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

### <span data-ttu-id="c52b4-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c52b4-127">-Name</span></span>
<span data-ttu-id="c52b4-128">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c52b4-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="c52b4-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c52b4-130">The resource group name.</span></span>

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

### <span data-ttu-id="c52b4-131">-標記</span><span class="sxs-lookup"><span data-stu-id="c52b4-131">-Tag</span></span>
<span data-ttu-id="c52b4-132">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="c52b4-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c52b4-133">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c52b4-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52b4-134">-可見度</span><span class="sxs-lookup"><span data-stu-id="c52b4-134">-Visibility</span></span>
<span data-ttu-id="c52b4-135">私人連結服務的可見度訂閱</span><span class="sxs-lookup"><span data-stu-id="c52b4-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c52b4-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c52b4-136">-Confirm</span></span>
<span data-ttu-id="c52b4-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c52b4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c52b4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c52b4-138">-WhatIf</span></span>
<span data-ttu-id="c52b4-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c52b4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c52b4-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c52b4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c52b4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52b4-141">CommonParameters</span></span>
<span data-ttu-id="c52b4-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c52b4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52b4-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c52b4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52b4-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c52b4-144">INPUTS</span></span>

### <span data-ttu-id="c52b4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c52b4-145">System.String</span></span>

### <span data-ttu-id="c52b4-146">Microsoft.Azure.Commands.Network.models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c52b4-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="c52b4-147">Microsoft.Azure.Commands.Network.models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c52b4-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="c52b4-148">輸出</span><span class="sxs-lookup"><span data-stu-id="c52b4-148">OUTPUTS</span></span>

### <span data-ttu-id="c52b4-149">Microsoft.Azure.Commands.Network.models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c52b4-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="c52b4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="c52b4-150">NOTES</span></span>

## <span data-ttu-id="c52b4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="c52b4-151">RELATED LINKS</span></span>

[<span data-ttu-id="c52b4-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c52b4-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="c52b4-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c52b4-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="c52b4-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c52b4-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
