---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 87647d504d47bf3f53b775d68b42ab617485f73d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908853"
---
# <span data-ttu-id="559ed-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="559ed-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="559ed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="559ed-102">SYNOPSIS</span></span>
<span data-ttu-id="559ed-103">新增對等至 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="559ed-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="559ed-104">語法</span><span class="sxs-lookup"><span data-stu-id="559ed-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="559ed-105">描述</span><span class="sxs-lookup"><span data-stu-id="559ed-105">DESCRIPTION</span></span>
<span data-ttu-id="559ed-106">**Add-AzVirtualRouterPeer Cmdlet** 會將 VirtualRouter 對等加入 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="559ed-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="559ed-107">例子</span><span class="sxs-lookup"><span data-stu-id="559ed-107">EXAMPLES</span></span>

### <span data-ttu-id="559ed-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="559ed-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="559ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="559ed-109">PARAMETERS</span></span>

### <span data-ttu-id="559ed-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="559ed-110">-AsJob</span></span>
<span data-ttu-id="559ed-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="559ed-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="559ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559ed-112">-DefaultProfile</span></span>
<span data-ttu-id="559ed-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="559ed-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="559ed-114">-強制</span><span class="sxs-lookup"><span data-stu-id="559ed-114">-Force</span></span>
<span data-ttu-id="559ed-115">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="559ed-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="559ed-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="559ed-116">-PeerAsn</span></span>
<span data-ttu-id="559ed-117">對等 ASN。</span><span class="sxs-lookup"><span data-stu-id="559ed-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="559ed-118">-對等互連</span><span class="sxs-lookup"><span data-stu-id="559ed-118">-PeerIp</span></span>
<span data-ttu-id="559ed-119">對等 Ip。</span><span class="sxs-lookup"><span data-stu-id="559ed-119">Peer Ip.</span></span>

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

### <span data-ttu-id="559ed-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="559ed-120">-PeerName</span></span>
<span data-ttu-id="559ed-121">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="559ed-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="559ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="559ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="559ed-123">虛擬路由器/對等的資源組名。</span><span class="sxs-lookup"><span data-stu-id="559ed-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="559ed-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="559ed-124">-VirtualRouterName</span></span>
<span data-ttu-id="559ed-125">對等存在之虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="559ed-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="559ed-126">-確認</span><span class="sxs-lookup"><span data-stu-id="559ed-126">-Confirm</span></span>
<span data-ttu-id="559ed-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="559ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="559ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559ed-128">-WhatIf</span></span>
<span data-ttu-id="559ed-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="559ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="559ed-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="559ed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="559ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559ed-131">CommonParameters</span></span>
<span data-ttu-id="559ed-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="559ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559ed-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="559ed-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559ed-134">輸入</span><span class="sxs-lookup"><span data-stu-id="559ed-134">INPUTS</span></span>

### <span data-ttu-id="559ed-135">System.String</span><span class="sxs-lookup"><span data-stu-id="559ed-135">System.String</span></span>

### <span data-ttu-id="559ed-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="559ed-136">System.UInt32</span></span>

## <span data-ttu-id="559ed-137">輸出</span><span class="sxs-lookup"><span data-stu-id="559ed-137">OUTPUTS</span></span>

### <span data-ttu-id="559ed-138">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="559ed-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="559ed-139">筆記</span><span class="sxs-lookup"><span data-stu-id="559ed-139">NOTES</span></span>

## <span data-ttu-id="559ed-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="559ed-140">RELATED LINKS</span></span>
