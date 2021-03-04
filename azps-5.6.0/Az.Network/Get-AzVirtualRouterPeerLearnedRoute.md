---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 99f76a12afdbc883d990fff5a05e06e2880aecf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910449"
---
# <span data-ttu-id="e9f51-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="e9f51-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="e9f51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9f51-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f51-103">列出特定虛擬路由器對等體所學習的路由</span><span class="sxs-lookup"><span data-stu-id="e9f51-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="e9f51-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9f51-104">SYNTAX</span></span>

### <span data-ttu-id="e9f51-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9f51-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9f51-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9f51-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9f51-107">描述</span><span class="sxs-lookup"><span data-stu-id="e9f51-107">DESCRIPTION</span></span>
<span data-ttu-id="e9f51-108">列舉由虛擬路由器對等體從其他來源得知的路由。</span><span class="sxs-lookup"><span data-stu-id="e9f51-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="e9f51-109">例子</span><span class="sxs-lookup"><span data-stu-id="e9f51-109">EXAMPLES</span></span>

### <span data-ttu-id="e9f51-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e9f51-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="e9f51-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="e9f51-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="e9f51-112">參數</span><span class="sxs-lookup"><span data-stu-id="e9f51-112">PARAMETERS</span></span>

### <span data-ttu-id="e9f51-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9f51-113">-AsJob</span></span>
<span data-ttu-id="e9f51-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9f51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9f51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f51-115">-DefaultProfile</span></span>
<span data-ttu-id="e9f51-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9f51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f51-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9f51-117">-InputObject</span></span>
<span data-ttu-id="e9f51-118">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e9f51-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="e9f51-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e9f51-119">-PeerName</span></span>
<span data-ttu-id="e9f51-120">虛擬路由器對等名稱</span><span class="sxs-lookup"><span data-stu-id="e9f51-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="e9f51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f51-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9f51-122">虛擬路由器對等資源組名</span><span class="sxs-lookup"><span data-stu-id="e9f51-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="e9f51-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="e9f51-123">-VirtualRouterName</span></span>
<span data-ttu-id="e9f51-124">虛擬路由器名稱</span><span class="sxs-lookup"><span data-stu-id="e9f51-124">Virtual router name</span></span>

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

### <span data-ttu-id="e9f51-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f51-125">CommonParameters</span></span>
<span data-ttu-id="e9f51-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9f51-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f51-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9f51-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f51-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e9f51-128">INPUTS</span></span>

### <span data-ttu-id="e9f51-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f51-129">System.String</span></span>

### <span data-ttu-id="e9f51-130">Microsoft.Azure.Commands.Network.models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e9f51-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="e9f51-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e9f51-131">OUTPUTS</span></span>

### <span data-ttu-id="e9f51-132">Microsoft.Azure.Commands.Network.models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="e9f51-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="e9f51-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e9f51-133">NOTES</span></span>

## <span data-ttu-id="e9f51-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9f51-134">RELATED LINKS</span></span>
