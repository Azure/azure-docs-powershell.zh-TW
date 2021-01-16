---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280315"
---
# <span data-ttu-id="8e367-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8e367-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="8e367-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e367-102">SYNOPSIS</span></span>
<span data-ttu-id="8e367-103">更新 Azure VirtualRouter 中的對等</span><span class="sxs-lookup"><span data-stu-id="8e367-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="8e367-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e367-104">SYNTAX</span></span>

### <span data-ttu-id="8e367-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8e367-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e367-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e367-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e367-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e367-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e367-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e367-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e367-109">說明</span><span class="sxs-lookup"><span data-stu-id="8e367-109">DESCRIPTION</span></span>
<span data-ttu-id="8e367-110">**AzVirtualRouterPeer** Cmdlet 會將 VirtualRouter 對等更新到 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8e367-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="8e367-111">示例</span><span class="sxs-lookup"><span data-stu-id="8e367-111">EXAMPLES</span></span>

### <span data-ttu-id="8e367-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8e367-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8e367-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8e367-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8e367-114">範例3</span><span class="sxs-lookup"><span data-stu-id="8e367-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="8e367-115">參數</span><span class="sxs-lookup"><span data-stu-id="8e367-115">PARAMETERS</span></span>

### <span data-ttu-id="8e367-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e367-116">-AsJob</span></span>
<span data-ttu-id="8e367-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e367-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e367-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e367-118">-DefaultProfile</span></span>
<span data-ttu-id="8e367-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e367-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e367-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8e367-120">-Force</span></span>
<span data-ttu-id="8e367-121">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8e367-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8e367-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e367-122">-InputObject</span></span>
<span data-ttu-id="8e367-123">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8e367-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="8e367-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8e367-124">-PeerAsn</span></span>
<span data-ttu-id="8e367-125">對等 ASN。</span><span class="sxs-lookup"><span data-stu-id="8e367-125">Peer ASN.</span></span>

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

### <span data-ttu-id="8e367-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="8e367-126">-PeerIp</span></span>
<span data-ttu-id="8e367-127">對等 Ip。</span><span class="sxs-lookup"><span data-stu-id="8e367-127">Peer Ip.</span></span>

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

### <span data-ttu-id="8e367-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8e367-128">-PeerName</span></span>
<span data-ttu-id="8e367-129">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e367-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="8e367-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e367-130">-ResourceGroupName</span></span>
<span data-ttu-id="8e367-131">虛擬路由器/對等的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8e367-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="8e367-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e367-132">-ResourceId</span></span>
<span data-ttu-id="8e367-133">虛擬路由器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e367-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="8e367-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="8e367-134">-VirtualRouterName</span></span>
<span data-ttu-id="8e367-135">對等所在的虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="8e367-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="8e367-136">-確認</span><span class="sxs-lookup"><span data-stu-id="8e367-136">-Confirm</span></span>
<span data-ttu-id="8e367-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e367-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e367-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e367-138">-WhatIf</span></span>
<span data-ttu-id="8e367-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e367-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e367-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e367-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e367-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e367-141">CommonParameters</span></span>
<span data-ttu-id="8e367-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e367-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e367-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e367-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e367-144">輸入</span><span class="sxs-lookup"><span data-stu-id="8e367-144">INPUTS</span></span>

### <span data-ttu-id="8e367-145">System.object</span><span class="sxs-lookup"><span data-stu-id="8e367-145">System.String</span></span>

### <span data-ttu-id="8e367-146">UInt32</span><span class="sxs-lookup"><span data-stu-id="8e367-146">System.UInt32</span></span>

### <span data-ttu-id="8e367-147">PSVirtualRouterPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e367-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="8e367-148">輸出</span><span class="sxs-lookup"><span data-stu-id="8e367-148">OUTPUTS</span></span>

### <span data-ttu-id="8e367-149">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e367-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8e367-150">筆記</span><span class="sxs-lookup"><span data-stu-id="8e367-150">NOTES</span></span>

## <span data-ttu-id="8e367-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e367-151">RELATED LINKS</span></span>
