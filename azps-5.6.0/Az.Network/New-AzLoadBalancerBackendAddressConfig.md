---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 980b16d373f17101266908c0a24443764d96561f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902873"
---
# <span data-ttu-id="81282-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="81282-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="81282-102">簡介</span><span class="sxs-lookup"><span data-stu-id="81282-102">SYNOPSIS</span></span>
<span data-ttu-id="81282-103">會返回負載平衡器後端位址設定檔。</span><span class="sxs-lookup"><span data-stu-id="81282-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="81282-104">語法</span><span class="sxs-lookup"><span data-stu-id="81282-104">SYNTAX</span></span>

### <span data-ttu-id="81282-105">SetByResourcePublicIpAddress (預設) </span><span class="sxs-lookup"><span data-stu-id="81282-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81282-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="81282-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81282-107">描述</span><span class="sxs-lookup"><span data-stu-id="81282-107">DESCRIPTION</span></span>
<span data-ttu-id="81282-108">會返回負載平衡器後端位址設定檔。</span><span class="sxs-lookup"><span data-stu-id="81282-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="81282-109">例子</span><span class="sxs-lookup"><span data-stu-id="81282-109">EXAMPLES</span></span>

### <span data-ttu-id="81282-110">範例 1：新的 loadbalancer address config with virtual network reference</span><span class="sxs-lookup"><span data-stu-id="81282-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="81282-111">範例 2：New loadbalancer address config with loadbalancer frontend ip configuration reference</span><span class="sxs-lookup"><span data-stu-id="81282-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="81282-112">參數</span><span class="sxs-lookup"><span data-stu-id="81282-112">PARAMETERS</span></span>

### <span data-ttu-id="81282-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81282-113">-DefaultProfile</span></span>
<span data-ttu-id="81282-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="81282-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81282-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="81282-115">-IpAddress</span></span>
<span data-ttu-id="81282-116">要新增到後端資料庫的 IPAddress</span><span class="sxs-lookup"><span data-stu-id="81282-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81282-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="81282-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="81282-118">與後端位址設定檔相關聯的負載平衡器前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="81282-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81282-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="81282-119">-Name</span></span>
<span data-ttu-id="81282-120">後端位址組名</span><span class="sxs-lookup"><span data-stu-id="81282-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="81282-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="81282-121">-VirtualNetworkId</span></span>
<span data-ttu-id="81282-122">與後端位址設定檔相關聯的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="81282-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81282-123">-確認</span><span class="sxs-lookup"><span data-stu-id="81282-123">-Confirm</span></span>
<span data-ttu-id="81282-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="81282-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81282-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81282-125">-WhatIf</span></span>
<span data-ttu-id="81282-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81282-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81282-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81282-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81282-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81282-128">CommonParameters</span></span>
<span data-ttu-id="81282-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="81282-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81282-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81282-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81282-131">輸入</span><span class="sxs-lookup"><span data-stu-id="81282-131">INPUTS</span></span>

### <span data-ttu-id="81282-132">System.String</span><span class="sxs-lookup"><span data-stu-id="81282-132">System.String</span></span>

### <span data-ttu-id="81282-133">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81282-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="81282-134">輸出</span><span class="sxs-lookup"><span data-stu-id="81282-134">OUTPUTS</span></span>

### <span data-ttu-id="81282-135">Microsoft.Azure.Commands.Network.models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="81282-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="81282-136">筆記</span><span class="sxs-lookup"><span data-stu-id="81282-136">NOTES</span></span>

## <span data-ttu-id="81282-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="81282-137">RELATED LINKS</span></span>
