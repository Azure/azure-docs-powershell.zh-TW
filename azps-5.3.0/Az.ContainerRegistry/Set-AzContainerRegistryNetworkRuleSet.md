---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446179"
---
# <span data-ttu-id="93aad-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93aad-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="93aad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93aad-102">SYNOPSIS</span></span>
<span data-ttu-id="93aad-103">建立或更新網路規則集。</span><span class="sxs-lookup"><span data-stu-id="93aad-103">Create or update a network rule set.</span></span> <span data-ttu-id="93aad-104">規則集只能套用到 "Premium" 註冊表。</span><span class="sxs-lookup"><span data-stu-id="93aad-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="93aad-105">句法</span><span class="sxs-lookup"><span data-stu-id="93aad-105">SYNTAX</span></span>

### <span data-ttu-id="93aad-106">AddAddNetworkRuleWithoutInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="93aad-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93aad-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="93aad-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93aad-108">說明</span><span class="sxs-lookup"><span data-stu-id="93aad-108">DESCRIPTION</span></span>
<span data-ttu-id="93aad-109">建立或更新網路規則集</span><span class="sxs-lookup"><span data-stu-id="93aad-109">Create or update a network rule set</span></span>

## <span data-ttu-id="93aad-110">示例</span><span class="sxs-lookup"><span data-stu-id="93aad-110">EXAMPLES</span></span>

### <span data-ttu-id="93aad-111">範例1</span><span class="sxs-lookup"><span data-stu-id="93aad-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="93aad-112">建立新的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="93aad-112">Create a new network rule set.</span></span>

## <span data-ttu-id="93aad-113">參數</span><span class="sxs-lookup"><span data-stu-id="93aad-113">PARAMETERS</span></span>

### <span data-ttu-id="93aad-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="93aad-114">-DefaultAction</span></span>
<span data-ttu-id="93aad-115">預設動作，可能是 "Allow" 或 "Deny"</span><span class="sxs-lookup"><span data-stu-id="93aad-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93aad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93aad-116">-DefaultProfile</span></span>
<span data-ttu-id="93aad-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93aad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93aad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93aad-118">-InputObject</span></span>
<span data-ttu-id="93aad-119">輸入 PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93aad-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93aad-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="93aad-120">-NetworkRule</span></span>
<span data-ttu-id="93aad-121">網路規則清單</span><span class="sxs-lookup"><span data-stu-id="93aad-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93aad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93aad-122">CommonParameters</span></span>
<span data-ttu-id="93aad-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93aad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93aad-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93aad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93aad-125">輸入</span><span class="sxs-lookup"><span data-stu-id="93aad-125">INPUTS</span></span>

### <span data-ttu-id="93aad-126">System.object</span><span class="sxs-lookup"><span data-stu-id="93aad-126">System.String</span></span>

### <span data-ttu-id="93aad-127">IPSNetworkRule 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="93aad-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="93aad-128">輸出</span><span class="sxs-lookup"><span data-stu-id="93aad-128">OUTPUTS</span></span>

### <span data-ttu-id="93aad-129">PSNetworkRuleSet 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="93aad-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="93aad-130">筆記</span><span class="sxs-lookup"><span data-stu-id="93aad-130">NOTES</span></span>

## <span data-ttu-id="93aad-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="93aad-131">RELATED LINKS</span></span>
