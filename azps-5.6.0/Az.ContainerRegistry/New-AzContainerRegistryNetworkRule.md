---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: 0fef46fb32c299a0d3117e8168e845777293d496
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904721"
---
# <span data-ttu-id="3b755-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b755-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="3b755-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b755-102">SYNOPSIS</span></span>
<span data-ttu-id="3b755-103">建立網路規則。</span><span class="sxs-lookup"><span data-stu-id="3b755-103">Create a network rule.</span></span>

## <span data-ttu-id="3b755-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b755-104">SYNTAX</span></span>

### <span data-ttu-id="3b755-105">ByVirtualNetworkRule (預設) </span><span class="sxs-lookup"><span data-stu-id="3b755-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b755-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="3b755-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b755-107">描述</span><span class="sxs-lookup"><span data-stu-id="3b755-107">DESCRIPTION</span></span>
<span data-ttu-id="3b755-108">在目前的 Powershell 會話中建立網路規則物件。</span><span class="sxs-lookup"><span data-stu-id="3b755-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="3b755-109">例子</span><span class="sxs-lookup"><span data-stu-id="3b755-109">EXAMPLES</span></span>

### <span data-ttu-id="3b755-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3b755-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="3b755-111">建立 virtualnetwork 規則集。</span><span class="sxs-lookup"><span data-stu-id="3b755-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="3b755-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b755-112">PARAMETERS</span></span>

### <span data-ttu-id="3b755-113">-動作</span><span class="sxs-lookup"><span data-stu-id="3b755-113">-Action</span></span>
<span data-ttu-id="3b755-114">網路規則的動作。</span><span class="sxs-lookup"><span data-stu-id="3b755-114">The action of network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b755-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b755-115">-DefaultProfile</span></span>
<span data-ttu-id="3b755-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b755-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b755-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3b755-117">-IPAddressOrRange</span></span>
<span data-ttu-id="3b755-118">以 CIDR 格式指定 IP 或 IP 範圍。</span><span class="sxs-lookup"><span data-stu-id="3b755-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="3b755-119">僅允許 IPV4 位址。</span><span class="sxs-lookup"><span data-stu-id="3b755-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b755-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3b755-120">-IPRule</span></span>
<span data-ttu-id="3b755-121">表示要建立 IPRule。</span><span class="sxs-lookup"><span data-stu-id="3b755-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b755-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3b755-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3b755-123">子網的資源識別碼，例如：/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/子網/{子網Name}。</span><span class="sxs-lookup"><span data-stu-id="3b755-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b755-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b755-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="3b755-125">表示要建立 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="3b755-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b755-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b755-126">CommonParameters</span></span>
<span data-ttu-id="3b755-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b755-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b755-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b755-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b755-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3b755-129">INPUTS</span></span>

### <span data-ttu-id="3b755-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3b755-130">System.String</span></span>

## <span data-ttu-id="3b755-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3b755-131">OUTPUTS</span></span>

### <span data-ttu-id="3b755-132">Microsoft.Azure.Commands.ContainerRegistry.models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b755-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="3b755-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3b755-133">NOTES</span></span>

## <span data-ttu-id="3b755-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b755-134">RELATED LINKS</span></span>
