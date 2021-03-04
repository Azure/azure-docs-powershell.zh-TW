---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 608be77335c0201b8ae1d17b34057025392f1072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908485"
---
# <span data-ttu-id="f3e52-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3e52-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="f3e52-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3e52-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e52-103">建立 Azure VirtualRouter。</span><span class="sxs-lookup"><span data-stu-id="f3e52-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="f3e52-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3e52-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3e52-105">描述</span><span class="sxs-lookup"><span data-stu-id="f3e52-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e52-106">**New-AzVirtualRouter** Cmdlet 會建立 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3e52-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="f3e52-107">例子</span><span class="sxs-lookup"><span data-stu-id="f3e52-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e52-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f3e52-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="f3e52-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3e52-109">PARAMETERS</span></span>

### <span data-ttu-id="f3e52-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3e52-110">-AsJob</span></span>
<span data-ttu-id="f3e52-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f3e52-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3e52-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e52-112">-DefaultProfile</span></span>
<span data-ttu-id="f3e52-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3e52-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3e52-114">-強制</span><span class="sxs-lookup"><span data-stu-id="f3e52-114">-Force</span></span>
<span data-ttu-id="f3e52-115">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="f3e52-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f3e52-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="f3e52-116">-HostedSubnet</span></span>
<span data-ttu-id="f3e52-117">虛擬路由器託管的子網。</span><span class="sxs-lookup"><span data-stu-id="f3e52-117">The subnet where the virtual router is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e52-118">-位置</span><span class="sxs-lookup"><span data-stu-id="f3e52-118">-Location</span></span>
<span data-ttu-id="f3e52-119">位置。</span><span class="sxs-lookup"><span data-stu-id="f3e52-119">The location.</span></span>

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

### <span data-ttu-id="f3e52-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3e52-120">-Name</span></span>
<span data-ttu-id="f3e52-121">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e52-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e52-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3e52-123">虛擬路由器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f3e52-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="f3e52-124">-標記</span><span class="sxs-lookup"><span data-stu-id="f3e52-124">-Tag</span></span>
<span data-ttu-id="f3e52-125">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3e52-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f3e52-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f3e52-126">-Confirm</span></span>
<span data-ttu-id="f3e52-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3e52-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3e52-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e52-128">-WhatIf</span></span>
<span data-ttu-id="f3e52-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3e52-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3e52-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3e52-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3e52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e52-131">CommonParameters</span></span>
<span data-ttu-id="f3e52-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3e52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e52-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3e52-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e52-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f3e52-134">INPUTS</span></span>

### <span data-ttu-id="f3e52-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f3e52-135">System.String</span></span>

### <span data-ttu-id="f3e52-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3e52-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f3e52-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f3e52-137">OUTPUTS</span></span>

### <span data-ttu-id="f3e52-138">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3e52-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="f3e52-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f3e52-139">NOTES</span></span>

## <span data-ttu-id="f3e52-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3e52-140">RELATED LINKS</span></span>
