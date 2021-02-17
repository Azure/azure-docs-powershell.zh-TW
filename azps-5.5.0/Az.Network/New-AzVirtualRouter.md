---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140318"
---
# <span data-ttu-id="c909f-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c909f-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="c909f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c909f-102">SYNOPSIS</span></span>
<span data-ttu-id="c909f-103">建立 Azure VirtualRouter。</span><span class="sxs-lookup"><span data-stu-id="c909f-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="c909f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c909f-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c909f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c909f-105">DESCRIPTION</span></span>
<span data-ttu-id="c909f-106">**新的-AzVirtualRouter** Cmdlet 會建立 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c909f-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="c909f-107">示例</span><span class="sxs-lookup"><span data-stu-id="c909f-107">EXAMPLES</span></span>

### <span data-ttu-id="c909f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c909f-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="c909f-109">參數</span><span class="sxs-lookup"><span data-stu-id="c909f-109">PARAMETERS</span></span>

### <span data-ttu-id="c909f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c909f-110">-AsJob</span></span>
<span data-ttu-id="c909f-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c909f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c909f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c909f-112">-DefaultProfile</span></span>
<span data-ttu-id="c909f-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c909f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c909f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c909f-114">-Force</span></span>
<span data-ttu-id="c909f-115">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="c909f-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c909f-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="c909f-116">-HostedSubnet</span></span>
<span data-ttu-id="c909f-117">託管虛擬路由器的子網。</span><span class="sxs-lookup"><span data-stu-id="c909f-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="c909f-118">-位置</span><span class="sxs-lookup"><span data-stu-id="c909f-118">-Location</span></span>
<span data-ttu-id="c909f-119">位置。</span><span class="sxs-lookup"><span data-stu-id="c909f-119">The location.</span></span>

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

### <span data-ttu-id="c909f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c909f-120">-Name</span></span>
<span data-ttu-id="c909f-121">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c909f-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="c909f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c909f-122">-ResourceGroupName</span></span>
<span data-ttu-id="c909f-123">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c909f-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="c909f-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="c909f-124">-Tag</span></span>
<span data-ttu-id="c909f-125">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="c909f-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c909f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c909f-126">-Confirm</span></span>
<span data-ttu-id="c909f-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c909f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c909f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c909f-128">-WhatIf</span></span>
<span data-ttu-id="c909f-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c909f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c909f-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c909f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c909f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c909f-131">CommonParameters</span></span>
<span data-ttu-id="c909f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c909f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c909f-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c909f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c909f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c909f-134">INPUTS</span></span>

### <span data-ttu-id="c909f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="c909f-135">System.String</span></span>

### <span data-ttu-id="c909f-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c909f-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c909f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c909f-137">OUTPUTS</span></span>

### <span data-ttu-id="c909f-138">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c909f-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="c909f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c909f-139">NOTES</span></span>

## <span data-ttu-id="c909f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c909f-140">RELATED LINKS</span></span>
