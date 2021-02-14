---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128955"
---
# <span data-ttu-id="c6a3b-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6a3b-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="c6a3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a3b-103">取得負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-103">Gets a load balancer.</span></span>

## <span data-ttu-id="c6a3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6a3b-104">SYNTAX</span></span>

### <span data-ttu-id="c6a3b-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="c6a3b-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6a3b-106">擴充</span><span class="sxs-lookup"><span data-stu-id="c6a3b-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a3b-107">說明</span><span class="sxs-lookup"><span data-stu-id="c6a3b-107">DESCRIPTION</span></span>
<span data-ttu-id="c6a3b-108">**AzLoadBalancer** Cmdlet 會取得包含在資源群組中的一個或多個 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="c6a3b-109">示例</span><span class="sxs-lookup"><span data-stu-id="c6a3b-109">EXAMPLES</span></span>

### <span data-ttu-id="c6a3b-110">範例1：取得負載平衡器</span><span class="sxs-lookup"><span data-stu-id="c6a3b-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="c6a3b-111">這個命令會取得名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="c6a3b-112">必須先存在負載平衡器，才能執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="c6a3b-113">範例2：使用篩選來列出負載平衡器</span><span class="sxs-lookup"><span data-stu-id="c6a3b-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="c6a3b-114">這個命令會取得名稱開頭為 "MyLoadBalancer" 的所有負載平衡器</span><span class="sxs-lookup"><span data-stu-id="c6a3b-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="c6a3b-115">參數</span><span class="sxs-lookup"><span data-stu-id="c6a3b-115">PARAMETERS</span></span>

### <span data-ttu-id="c6a3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a3b-116">-DefaultProfile</span></span>
<span data-ttu-id="c6a3b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a3b-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c6a3b-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a3b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6a3b-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c6a3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a3b-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c6a3b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a3b-121">CommonParameters</span></span>
<span data-ttu-id="c6a3b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a3b-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c6a3b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a3b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c6a3b-124">INPUTS</span></span>

### <span data-ttu-id="c6a3b-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c6a3b-125">System.String</span></span>

## <span data-ttu-id="c6a3b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c6a3b-126">OUTPUTS</span></span>

### <span data-ttu-id="c6a3b-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6a3b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c6a3b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c6a3b-128">NOTES</span></span>

## <span data-ttu-id="c6a3b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6a3b-129">RELATED LINKS</span></span>

[<span data-ttu-id="c6a3b-130">新-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6a3b-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="c6a3b-131">移除-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6a3b-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="c6a3b-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6a3b-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


