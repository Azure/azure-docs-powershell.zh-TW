---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789290"
---
# <span data-ttu-id="d44a7-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d44a7-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="d44a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d44a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d44a7-103">建立私人連結服務</span><span class="sxs-lookup"><span data-stu-id="d44a7-103">Creates a private link service</span></span>

## <span data-ttu-id="d44a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d44a7-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d44a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="d44a7-105">DESCRIPTION</span></span>
<span data-ttu-id="d44a7-106">**新的-AzPrivateLinkService** Cmdlet 會建立私人連結服務</span><span class="sxs-lookup"><span data-stu-id="d44a7-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="d44a7-107">示例</span><span class="sxs-lookup"><span data-stu-id="d44a7-107">EXAMPLES</span></span>

### <span data-ttu-id="d44a7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d44a7-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="d44a7-109">這個範例會建立私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="d44a7-109">This example creates a private link service.</span></span>

## <span data-ttu-id="d44a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="d44a7-110">PARAMETERS</span></span>

### <span data-ttu-id="d44a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d44a7-111">-AsJob</span></span>
<span data-ttu-id="d44a7-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d44a7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d44a7-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="d44a7-113">-AutoApproval</span></span>
<span data-ttu-id="d44a7-114">私人連結服務的自動核准訂閱</span><span class="sxs-lookup"><span data-stu-id="d44a7-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="d44a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44a7-115">-DefaultProfile</span></span>
<span data-ttu-id="d44a7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d44a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d44a7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d44a7-117">-Force</span></span>
<span data-ttu-id="d44a7-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="d44a7-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d44a7-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d44a7-119">-IpConfiguration</span></span>
<span data-ttu-id="d44a7-120">Ip 配置</span><span class="sxs-lookup"><span data-stu-id="d44a7-120">The ip configurations</span></span>

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

### <span data-ttu-id="d44a7-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d44a7-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="d44a7-122">前端 ip 配置</span><span class="sxs-lookup"><span data-stu-id="d44a7-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="d44a7-123">-位置</span><span class="sxs-lookup"><span data-stu-id="d44a7-123">-Location</span></span>
<span data-ttu-id="d44a7-124">位於.</span><span class="sxs-lookup"><span data-stu-id="d44a7-124">location.</span></span>

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

### <span data-ttu-id="d44a7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d44a7-125">-Name</span></span>
<span data-ttu-id="d44a7-126">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="d44a7-126">The name of the service.</span></span>

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

### <span data-ttu-id="d44a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="d44a7-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d44a7-128">The resource group name.</span></span>

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

### <span data-ttu-id="d44a7-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="d44a7-129">-Tag</span></span>
<span data-ttu-id="d44a7-130">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d44a7-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d44a7-131">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d44a7-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d44a7-132">-可見度</span><span class="sxs-lookup"><span data-stu-id="d44a7-132">-Visibility</span></span>
<span data-ttu-id="d44a7-133">私人連結服務的可見度訂閱</span><span class="sxs-lookup"><span data-stu-id="d44a7-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="d44a7-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d44a7-134">-Confirm</span></span>
<span data-ttu-id="d44a7-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d44a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d44a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d44a7-136">-WhatIf</span></span>
<span data-ttu-id="d44a7-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d44a7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d44a7-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d44a7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d44a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44a7-139">CommonParameters</span></span>
<span data-ttu-id="d44a7-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d44a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44a7-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d44a7-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44a7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d44a7-142">INPUTS</span></span>

### <span data-ttu-id="d44a7-143">System.object</span><span class="sxs-lookup"><span data-stu-id="d44a7-143">System.String</span></span>

### <span data-ttu-id="d44a7-144">PSFrontendIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="d44a7-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="d44a7-145">PSPrivateLinkServiceIpConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="d44a7-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="d44a7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d44a7-146">OUTPUTS</span></span>

### <span data-ttu-id="d44a7-147">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d44a7-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d44a7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d44a7-148">NOTES</span></span>

## <span data-ttu-id="d44a7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d44a7-149">RELATED LINKS</span></span>

[<span data-ttu-id="d44a7-150">AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d44a7-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="d44a7-151">移除-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d44a7-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="d44a7-152">新-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d44a7-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
