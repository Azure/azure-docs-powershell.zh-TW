---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: f0fc298ba92b7e9dc0f0bf5ed4f8cbdba5b8091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903009"
---
# <span data-ttu-id="0544d-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0544d-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="0544d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0544d-102">SYNOPSIS</span></span>
<span data-ttu-id="0544d-103">建立或更新網路規則集。</span><span class="sxs-lookup"><span data-stu-id="0544d-103">Create or update a network rule set.</span></span> <span data-ttu-id="0544d-104">規則集只能套用至「進級」註冊表。</span><span class="sxs-lookup"><span data-stu-id="0544d-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="0544d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0544d-105">SYNTAX</span></span>

### <span data-ttu-id="0544d-106">AddAddNetworkRuleWithoutInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="0544d-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0544d-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="0544d-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0544d-108">描述</span><span class="sxs-lookup"><span data-stu-id="0544d-108">DESCRIPTION</span></span>
<span data-ttu-id="0544d-109">建立或更新網路規則集</span><span class="sxs-lookup"><span data-stu-id="0544d-109">Create or update a network rule set</span></span>

## <span data-ttu-id="0544d-110">例子</span><span class="sxs-lookup"><span data-stu-id="0544d-110">EXAMPLES</span></span>

### <span data-ttu-id="0544d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0544d-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="0544d-112">建立新網路規則集。</span><span class="sxs-lookup"><span data-stu-id="0544d-112">Create a new network rule set.</span></span>

## <span data-ttu-id="0544d-113">參數</span><span class="sxs-lookup"><span data-stu-id="0544d-113">PARAMETERS</span></span>

### <span data-ttu-id="0544d-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="0544d-114">-DefaultAction</span></span>
<span data-ttu-id="0544d-115">預設動作，可以是 'Allow' 或 'Deny'</span><span class="sxs-lookup"><span data-stu-id="0544d-115">Default action, could be 'Allow' or 'Deny'</span></span>

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

### <span data-ttu-id="0544d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0544d-116">-DefaultProfile</span></span>
<span data-ttu-id="0544d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0544d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0544d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0544d-118">-InputObject</span></span>
<span data-ttu-id="0544d-119">Input PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0544d-119">Input PSNetworkRuleSet</span></span>

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

### <span data-ttu-id="0544d-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="0544d-120">-NetworkRule</span></span>
<span data-ttu-id="0544d-121">網路規則清單</span><span class="sxs-lookup"><span data-stu-id="0544d-121">List of Network rules</span></span>

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

### <span data-ttu-id="0544d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0544d-122">CommonParameters</span></span>
<span data-ttu-id="0544d-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0544d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0544d-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0544d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0544d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0544d-125">INPUTS</span></span>

### <span data-ttu-id="0544d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0544d-126">System.String</span></span>

### <span data-ttu-id="0544d-127">Microsoft.Azure.Commands.ContainerRegistry.models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0544d-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="0544d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0544d-128">OUTPUTS</span></span>

### <span data-ttu-id="0544d-129">Microsoft.Azure.Commands.ContainerRegistry.models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0544d-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="0544d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0544d-130">NOTES</span></span>

## <span data-ttu-id="0544d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0544d-131">RELATED LINKS</span></span>
