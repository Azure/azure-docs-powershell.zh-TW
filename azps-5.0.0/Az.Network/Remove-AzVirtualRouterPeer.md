---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137519"
---
# <span data-ttu-id="ae69b-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ae69b-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="ae69b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae69b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae69b-103">從 Azure VirtualRouter 中移除對等</span><span class="sxs-lookup"><span data-stu-id="ae69b-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="ae69b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae69b-104">SYNTAX</span></span>

### <span data-ttu-id="ae69b-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae69b-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae69b-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae69b-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae69b-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae69b-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae69b-108">說明</span><span class="sxs-lookup"><span data-stu-id="ae69b-108">DESCRIPTION</span></span>
<span data-ttu-id="ae69b-109">**AzVirtualRouterPeer** Cmdlet 會從 Azure VirtualRouter 中移除 VirtualRouter 對等</span><span class="sxs-lookup"><span data-stu-id="ae69b-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="ae69b-110">示例</span><span class="sxs-lookup"><span data-stu-id="ae69b-110">EXAMPLES</span></span>

### <span data-ttu-id="ae69b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ae69b-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="ae69b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ae69b-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="ae69b-113">範例3</span><span class="sxs-lookup"><span data-stu-id="ae69b-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="ae69b-114">參數</span><span class="sxs-lookup"><span data-stu-id="ae69b-114">PARAMETERS</span></span>

### <span data-ttu-id="ae69b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae69b-115">-AsJob</span></span>
<span data-ttu-id="ae69b-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ae69b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae69b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae69b-117">-DefaultProfile</span></span>
<span data-ttu-id="ae69b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae69b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae69b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ae69b-119">-Force</span></span>
<span data-ttu-id="ae69b-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="ae69b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ae69b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae69b-121">-InputObject</span></span>
<span data-ttu-id="ae69b-122">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="ae69b-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="ae69b-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ae69b-123">-PeerName</span></span>
<span data-ttu-id="ae69b-124">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae69b-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="ae69b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae69b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae69b-126">虛擬路由器/對等的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ae69b-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="ae69b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae69b-127">-ResourceId</span></span>
<span data-ttu-id="ae69b-128">虛擬路由器對等資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae69b-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="ae69b-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="ae69b-129">-VirtualRouterName</span></span>
<span data-ttu-id="ae69b-130">對等所在的虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="ae69b-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="ae69b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ae69b-131">-Confirm</span></span>
<span data-ttu-id="ae69b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae69b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae69b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae69b-133">-WhatIf</span></span>
<span data-ttu-id="ae69b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae69b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae69b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae69b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae69b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae69b-136">CommonParameters</span></span>
<span data-ttu-id="ae69b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae69b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae69b-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae69b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae69b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ae69b-139">INPUTS</span></span>

### <span data-ttu-id="ae69b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ae69b-140">System.String</span></span>

### <span data-ttu-id="ae69b-141">PSVirtualRouterPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae69b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="ae69b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ae69b-142">OUTPUTS</span></span>

### <span data-ttu-id="ae69b-143">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ae69b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ae69b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ae69b-144">NOTES</span></span>

## <span data-ttu-id="ae69b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae69b-145">RELATED LINKS</span></span>
