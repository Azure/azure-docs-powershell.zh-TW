---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284483"
---
# <span data-ttu-id="7623c-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7623c-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="7623c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7623c-102">SYNOPSIS</span></span>
<span data-ttu-id="7623c-103">建立網路規則。</span><span class="sxs-lookup"><span data-stu-id="7623c-103">Create a network rule.</span></span>

## <span data-ttu-id="7623c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7623c-104">SYNTAX</span></span>

### <span data-ttu-id="7623c-105">ByVirtualNetworkRule (預設) </span><span class="sxs-lookup"><span data-stu-id="7623c-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7623c-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="7623c-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7623c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7623c-107">DESCRIPTION</span></span>
<span data-ttu-id="7623c-108">在目前的 powershell 會話中建立網路規則物件。</span><span class="sxs-lookup"><span data-stu-id="7623c-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="7623c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7623c-109">EXAMPLES</span></span>

### <span data-ttu-id="7623c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7623c-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="7623c-111">建立 virtualnetwork 規則集。</span><span class="sxs-lookup"><span data-stu-id="7623c-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="7623c-112">參數</span><span class="sxs-lookup"><span data-stu-id="7623c-112">PARAMETERS</span></span>

### <span data-ttu-id="7623c-113">-動作</span><span class="sxs-lookup"><span data-stu-id="7623c-113">-Action</span></span>
<span data-ttu-id="7623c-114">網路規則的動作。</span><span class="sxs-lookup"><span data-stu-id="7623c-114">The action of network rule.</span></span>

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

### <span data-ttu-id="7623c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7623c-115">-DefaultProfile</span></span>
<span data-ttu-id="7623c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7623c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7623c-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7623c-117">-IPAddressOrRange</span></span>
<span data-ttu-id="7623c-118">以 CIDR 格式指定 IP 或 IP 範圍。</span><span class="sxs-lookup"><span data-stu-id="7623c-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="7623c-119">只允許 IPV4 位址。</span><span class="sxs-lookup"><span data-stu-id="7623c-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="7623c-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="7623c-120">-IPRule</span></span>
<span data-ttu-id="7623c-121">指示建立 IPRule。</span><span class="sxs-lookup"><span data-stu-id="7623c-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="7623c-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="7623c-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="7623c-123">子網的資源識別碼，例如：/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}。</span><span class="sxs-lookup"><span data-stu-id="7623c-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="7623c-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7623c-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="7623c-125">指示建立 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="7623c-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="7623c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7623c-126">CommonParameters</span></span>
<span data-ttu-id="7623c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7623c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7623c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7623c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7623c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7623c-129">INPUTS</span></span>

### <span data-ttu-id="7623c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="7623c-130">System.String</span></span>

## <span data-ttu-id="7623c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7623c-131">OUTPUTS</span></span>

### <span data-ttu-id="7623c-132">IPSNetworkRule 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="7623c-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="7623c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7623c-133">NOTES</span></span>

## <span data-ttu-id="7623c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7623c-134">RELATED LINKS</span></span>
