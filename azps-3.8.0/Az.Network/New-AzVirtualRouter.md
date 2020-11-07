---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959164"
---
# <span data-ttu-id="a79dd-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a79dd-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="a79dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a79dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a79dd-103">建立 Azure VirtualRouter。</span><span class="sxs-lookup"><span data-stu-id="a79dd-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="a79dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="a79dd-104">SYNTAX</span></span>

### <span data-ttu-id="a79dd-105">HostedGatewayParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a79dd-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79dd-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a79dd-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a79dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="a79dd-107">DESCRIPTION</span></span>
<span data-ttu-id="a79dd-108">**新的-AzVirtualRouter** Cmdlet 會建立 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a79dd-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="a79dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="a79dd-109">EXAMPLES</span></span>

### <span data-ttu-id="a79dd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a79dd-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="a79dd-111">範例2</span><span class="sxs-lookup"><span data-stu-id="a79dd-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="a79dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="a79dd-112">PARAMETERS</span></span>

### <span data-ttu-id="a79dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a79dd-113">-AsJob</span></span>
<span data-ttu-id="a79dd-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a79dd-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79dd-115">-DefaultProfile</span></span>
<span data-ttu-id="a79dd-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a79dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a79dd-117">-Force</span></span>
<span data-ttu-id="a79dd-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="a79dd-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="a79dd-119">-HostedGateway</span></span>
<span data-ttu-id="a79dd-120">需要託管虛擬路由器的閘道。</span><span class="sxs-lookup"><span data-stu-id="a79dd-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="a79dd-121">-HostedGatewayId</span></span>
<span data-ttu-id="a79dd-122">需要託管虛擬路由器之閘道的 id。</span><span class="sxs-lookup"><span data-stu-id="a79dd-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-123">-位置</span><span class="sxs-lookup"><span data-stu-id="a79dd-123">-Location</span></span>
<span data-ttu-id="a79dd-124">位置。</span><span class="sxs-lookup"><span data-stu-id="a79dd-124">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a79dd-125">-Name</span></span>
<span data-ttu-id="a79dd-126">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a79dd-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="a79dd-128">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a79dd-128">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="a79dd-129">-Tag</span></span>
<span data-ttu-id="a79dd-130">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="a79dd-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a79dd-131">-Confirm</span></span>
<span data-ttu-id="a79dd-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a79dd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79dd-133">-WhatIf</span></span>
<span data-ttu-id="a79dd-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a79dd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a79dd-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a79dd-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79dd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79dd-136">CommonParameters</span></span>
<span data-ttu-id="a79dd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a79dd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a79dd-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a79dd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79dd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a79dd-139">INPUTS</span></span>

### <span data-ttu-id="a79dd-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a79dd-140">System.String</span></span>

### <span data-ttu-id="a79dd-141">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a79dd-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a79dd-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a79dd-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a79dd-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a79dd-143">OUTPUTS</span></span>

### <span data-ttu-id="a79dd-144">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a79dd-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a79dd-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a79dd-145">NOTES</span></span>

## <span data-ttu-id="a79dd-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a79dd-146">RELATED LINKS</span></span>
