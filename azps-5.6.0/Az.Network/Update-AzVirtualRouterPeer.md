---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 9e82946d13ac830d50affc621c965cfe8b81c503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901793"
---
# <span data-ttu-id="a58bf-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a58bf-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="a58bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a58bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a58bf-103">在 Azure VirtualRouter 中更新對等程式</span><span class="sxs-lookup"><span data-stu-id="a58bf-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="a58bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="a58bf-104">SYNTAX</span></span>

### <span data-ttu-id="a58bf-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a58bf-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58bf-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58bf-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a58bf-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58bf-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58bf-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58bf-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a58bf-109">描述</span><span class="sxs-lookup"><span data-stu-id="a58bf-109">DESCRIPTION</span></span>
<span data-ttu-id="a58bf-110">**Update-AzVirtualRouterPeer** Cmdlet 將 VirtualRouter 對等更新為 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a58bf-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="a58bf-111">例子</span><span class="sxs-lookup"><span data-stu-id="a58bf-111">EXAMPLES</span></span>

### <span data-ttu-id="a58bf-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a58bf-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="a58bf-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a58bf-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="a58bf-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="a58bf-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="a58bf-115">參數</span><span class="sxs-lookup"><span data-stu-id="a58bf-115">PARAMETERS</span></span>

### <span data-ttu-id="a58bf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a58bf-116">-AsJob</span></span>
<span data-ttu-id="a58bf-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a58bf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a58bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58bf-118">-DefaultProfile</span></span>
<span data-ttu-id="a58bf-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a58bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58bf-120">-強制</span><span class="sxs-lookup"><span data-stu-id="a58bf-120">-Force</span></span>
<span data-ttu-id="a58bf-121">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="a58bf-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a58bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a58bf-122">-InputObject</span></span>
<span data-ttu-id="a58bf-123">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a58bf-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="a58bf-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a58bf-124">-PeerAsn</span></span>
<span data-ttu-id="a58bf-125">對等 ASN。</span><span class="sxs-lookup"><span data-stu-id="a58bf-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58bf-126">-對等互連</span><span class="sxs-lookup"><span data-stu-id="a58bf-126">-PeerIp</span></span>
<span data-ttu-id="a58bf-127">對等 Ip。</span><span class="sxs-lookup"><span data-stu-id="a58bf-127">Peer Ip.</span></span>

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

### <span data-ttu-id="a58bf-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a58bf-128">-PeerName</span></span>
<span data-ttu-id="a58bf-129">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="a58bf-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="a58bf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58bf-130">-ResourceGroupName</span></span>
<span data-ttu-id="a58bf-131">虛擬路由器/對等的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a58bf-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="a58bf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a58bf-132">-ResourceId</span></span>
<span data-ttu-id="a58bf-133">虛擬路由器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a58bf-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="a58bf-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="a58bf-134">-VirtualRouterName</span></span>
<span data-ttu-id="a58bf-135">對等存在之虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="a58bf-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="a58bf-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a58bf-136">-Confirm</span></span>
<span data-ttu-id="a58bf-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a58bf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a58bf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58bf-138">-WhatIf</span></span>
<span data-ttu-id="a58bf-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a58bf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58bf-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a58bf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a58bf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58bf-141">CommonParameters</span></span>
<span data-ttu-id="a58bf-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a58bf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58bf-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a58bf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58bf-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a58bf-144">INPUTS</span></span>

### <span data-ttu-id="a58bf-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a58bf-145">System.String</span></span>

### <span data-ttu-id="a58bf-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="a58bf-146">System.UInt32</span></span>

### <span data-ttu-id="a58bf-147">Microsoft.Azure.Commands.Network.models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a58bf-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="a58bf-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a58bf-148">OUTPUTS</span></span>

### <span data-ttu-id="a58bf-149">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a58bf-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a58bf-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a58bf-150">NOTES</span></span>

## <span data-ttu-id="a58bf-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="a58bf-151">RELATED LINKS</span></span>
