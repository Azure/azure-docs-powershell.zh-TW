---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 2c88ac8c0f3f089a4a26bf0e29ec855281e7f8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915937"
---
# <span data-ttu-id="f74a3-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="f74a3-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="f74a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f74a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f74a3-103">從 Azure VirtualRouter 移除對等程式</span><span class="sxs-lookup"><span data-stu-id="f74a3-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="f74a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="f74a3-104">SYNTAX</span></span>

### <span data-ttu-id="f74a3-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f74a3-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74a3-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f74a3-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74a3-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f74a3-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74a3-108">描述</span><span class="sxs-lookup"><span data-stu-id="f74a3-108">DESCRIPTION</span></span>
<span data-ttu-id="f74a3-109">**Remove-AzVirtualRouterPeer Cmdlet** 會從 Azure VirtualRouter 移除 VirtualRouter 對等程式</span><span class="sxs-lookup"><span data-stu-id="f74a3-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="f74a3-110">例子</span><span class="sxs-lookup"><span data-stu-id="f74a3-110">EXAMPLES</span></span>

### <span data-ttu-id="f74a3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f74a3-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="f74a3-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="f74a3-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="f74a3-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="f74a3-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="f74a3-114">參數</span><span class="sxs-lookup"><span data-stu-id="f74a3-114">PARAMETERS</span></span>

### <span data-ttu-id="f74a3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f74a3-115">-AsJob</span></span>
<span data-ttu-id="f74a3-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f74a3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f74a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74a3-117">-DefaultProfile</span></span>
<span data-ttu-id="f74a3-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f74a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f74a3-119">-強制</span><span class="sxs-lookup"><span data-stu-id="f74a3-119">-Force</span></span>
<span data-ttu-id="f74a3-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="f74a3-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f74a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f74a3-121">-InputObject</span></span>
<span data-ttu-id="f74a3-122">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="f74a3-122">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f74a3-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="f74a3-123">-PeerName</span></span>
<span data-ttu-id="f74a3-124">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="f74a3-124">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="f74a3-126">虛擬路由器/對等的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f74a3-126">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74a3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f74a3-127">-ResourceId</span></span>
<span data-ttu-id="f74a3-128">虛擬路由器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f74a3-128">The virtual router peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74a3-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="f74a3-129">-VirtualRouterName</span></span>
<span data-ttu-id="f74a3-130">對等存在之虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="f74a3-130">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74a3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f74a3-131">-Confirm</span></span>
<span data-ttu-id="f74a3-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f74a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74a3-133">-WhatIf</span></span>
<span data-ttu-id="f74a3-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f74a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74a3-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f74a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74a3-136">CommonParameters</span></span>
<span data-ttu-id="f74a3-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f74a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74a3-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f74a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74a3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f74a3-139">INPUTS</span></span>

### <span data-ttu-id="f74a3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f74a3-140">System.String</span></span>

### <span data-ttu-id="f74a3-141">Microsoft.Azure.Commands.Network.models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="f74a3-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="f74a3-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f74a3-142">OUTPUTS</span></span>

### <span data-ttu-id="f74a3-143">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f74a3-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="f74a3-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f74a3-144">NOTES</span></span>

## <span data-ttu-id="f74a3-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f74a3-145">RELATED LINKS</span></span>
