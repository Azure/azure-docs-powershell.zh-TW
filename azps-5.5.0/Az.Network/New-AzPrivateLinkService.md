---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131203"
---
# <span data-ttu-id="07827-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07827-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="07827-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07827-102">SYNOPSIS</span></span>
<span data-ttu-id="07827-103">建立私人連結服務</span><span class="sxs-lookup"><span data-stu-id="07827-103">Creates a private link service</span></span>

## <span data-ttu-id="07827-104">句法</span><span class="sxs-lookup"><span data-stu-id="07827-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07827-105">說明</span><span class="sxs-lookup"><span data-stu-id="07827-105">DESCRIPTION</span></span>
<span data-ttu-id="07827-106">**新的-AzPrivateLinkService** Cmdlet 會建立私人連結服務</span><span class="sxs-lookup"><span data-stu-id="07827-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="07827-107">示例</span><span class="sxs-lookup"><span data-stu-id="07827-107">EXAMPLES</span></span>

### <span data-ttu-id="07827-108">範例1</span><span class="sxs-lookup"><span data-stu-id="07827-108">Example 1</span></span>

<span data-ttu-id="07827-109">下列範例會建立私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="07827-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="07827-110">參數</span><span class="sxs-lookup"><span data-stu-id="07827-110">PARAMETERS</span></span>

### <span data-ttu-id="07827-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07827-111">-AsJob</span></span>
<span data-ttu-id="07827-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07827-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07827-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="07827-113">-AutoApproval</span></span>
<span data-ttu-id="07827-114">私人連結服務的自動核准訂閱</span><span class="sxs-lookup"><span data-stu-id="07827-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="07827-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07827-115">-DefaultProfile</span></span>
<span data-ttu-id="07827-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07827-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07827-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="07827-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="07827-118">針對私人連結服務啟用 proxy 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="07827-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="07827-119">-Force</span><span class="sxs-lookup"><span data-stu-id="07827-119">-Force</span></span>
<span data-ttu-id="07827-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="07827-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="07827-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="07827-121">-IpConfiguration</span></span>
<span data-ttu-id="07827-122">Ip 配置</span><span class="sxs-lookup"><span data-stu-id="07827-122">The ip configurations</span></span>

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

### <span data-ttu-id="07827-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="07827-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="07827-124">前端 ip 配置</span><span class="sxs-lookup"><span data-stu-id="07827-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="07827-125">-位置</span><span class="sxs-lookup"><span data-stu-id="07827-125">-Location</span></span>
<span data-ttu-id="07827-126">位於.</span><span class="sxs-lookup"><span data-stu-id="07827-126">location.</span></span>

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

### <span data-ttu-id="07827-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="07827-127">-Name</span></span>
<span data-ttu-id="07827-128">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="07827-128">The name of the service.</span></span>

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

### <span data-ttu-id="07827-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07827-129">-ResourceGroupName</span></span>
<span data-ttu-id="07827-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07827-130">The resource group name.</span></span>

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

### <span data-ttu-id="07827-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="07827-131">-Tag</span></span>
<span data-ttu-id="07827-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="07827-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07827-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="07827-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="07827-134">-可見度</span><span class="sxs-lookup"><span data-stu-id="07827-134">-Visibility</span></span>
<span data-ttu-id="07827-135">私人連結服務的可見度訂閱</span><span class="sxs-lookup"><span data-stu-id="07827-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="07827-136">-確認</span><span class="sxs-lookup"><span data-stu-id="07827-136">-Confirm</span></span>
<span data-ttu-id="07827-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07827-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07827-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07827-138">-WhatIf</span></span>
<span data-ttu-id="07827-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07827-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07827-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07827-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07827-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07827-141">CommonParameters</span></span>
<span data-ttu-id="07827-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07827-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07827-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="07827-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07827-144">輸入</span><span class="sxs-lookup"><span data-stu-id="07827-144">INPUTS</span></span>

### <span data-ttu-id="07827-145">System.object</span><span class="sxs-lookup"><span data-stu-id="07827-145">System.String</span></span>

### <span data-ttu-id="07827-146">PSFrontendIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="07827-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="07827-147">PSPrivateLinkServiceIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="07827-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="07827-148">輸出</span><span class="sxs-lookup"><span data-stu-id="07827-148">OUTPUTS</span></span>

### <span data-ttu-id="07827-149">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07827-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="07827-150">筆記</span><span class="sxs-lookup"><span data-stu-id="07827-150">NOTES</span></span>

## <span data-ttu-id="07827-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="07827-151">RELATED LINKS</span></span>

[<span data-ttu-id="07827-152">AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07827-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="07827-153">移除-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="07827-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="07827-154">新-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="07827-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
