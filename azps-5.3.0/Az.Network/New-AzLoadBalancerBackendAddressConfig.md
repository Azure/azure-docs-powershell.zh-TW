---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437604"
---
# <span data-ttu-id="895a4-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="895a4-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="895a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="895a4-102">SYNOPSIS</span></span>
<span data-ttu-id="895a4-103">傳回負載平衡器後端位址 config。</span><span class="sxs-lookup"><span data-stu-id="895a4-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="895a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="895a4-104">SYNTAX</span></span>

### <span data-ttu-id="895a4-105">SetByResourcePublicIpAddress (預設) </span><span class="sxs-lookup"><span data-stu-id="895a4-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="895a4-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="895a4-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="895a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="895a4-107">DESCRIPTION</span></span>
<span data-ttu-id="895a4-108">傳回負載平衡器後端位址 config。</span><span class="sxs-lookup"><span data-stu-id="895a4-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="895a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="895a4-109">EXAMPLES</span></span>

### <span data-ttu-id="895a4-110">範例1：使用虛擬網路參照的新 loadbalancer 位址配置</span><span class="sxs-lookup"><span data-stu-id="895a4-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="895a4-111">範例2：新的 loadbalancer 位址 config 與 loadbalancer 前端 ip 配置參考</span><span class="sxs-lookup"><span data-stu-id="895a4-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="895a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="895a4-112">PARAMETERS</span></span>

### <span data-ttu-id="895a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895a4-113">-DefaultProfile</span></span>
<span data-ttu-id="895a4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="895a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="895a4-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="895a4-115">-IpAddress</span></span>
<span data-ttu-id="895a4-116">要新增到後端池的 IPAddress</span><span class="sxs-lookup"><span data-stu-id="895a4-116">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="895a4-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="895a4-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="895a4-118">與後端位址 config 相關聯的負載平衡器前端 ip 配置</span><span class="sxs-lookup"><span data-stu-id="895a4-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

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

### <span data-ttu-id="895a4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="895a4-119">-Name</span></span>
<span data-ttu-id="895a4-120">後端位址 config 的名稱</span><span class="sxs-lookup"><span data-stu-id="895a4-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="895a4-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="895a4-121">-VirtualNetworkId</span></span>
<span data-ttu-id="895a4-122">與後端位址 config 相關聯的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="895a4-122">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="895a4-123">-確認</span><span class="sxs-lookup"><span data-stu-id="895a4-123">-Confirm</span></span>
<span data-ttu-id="895a4-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="895a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="895a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="895a4-125">-WhatIf</span></span>
<span data-ttu-id="895a4-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="895a4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="895a4-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="895a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="895a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895a4-128">CommonParameters</span></span>
<span data-ttu-id="895a4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="895a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895a4-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="895a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895a4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="895a4-131">INPUTS</span></span>

### <span data-ttu-id="895a4-132">System.object</span><span class="sxs-lookup"><span data-stu-id="895a4-132">System.String</span></span>

### <span data-ttu-id="895a4-133">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="895a4-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="895a4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="895a4-134">OUTPUTS</span></span>

### <span data-ttu-id="895a4-135">PSLoadBalancerBackendAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="895a4-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="895a4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="895a4-136">NOTES</span></span>

## <span data-ttu-id="895a4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="895a4-137">RELATED LINKS</span></span>
