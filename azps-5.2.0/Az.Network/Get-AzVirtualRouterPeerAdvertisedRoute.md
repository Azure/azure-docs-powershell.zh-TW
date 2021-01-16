---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280641"
---
# <span data-ttu-id="883ed-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="883ed-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="883ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="883ed-102">SYNOPSIS</span></span>
<span data-ttu-id="883ed-103">依特定虛擬路由器對等的清單傳送路由</span><span class="sxs-lookup"><span data-stu-id="883ed-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="883ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="883ed-104">SYNTAX</span></span>

### <span data-ttu-id="883ed-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="883ed-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="883ed-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="883ed-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="883ed-107">說明</span><span class="sxs-lookup"><span data-stu-id="883ed-107">DESCRIPTION</span></span>
<span data-ttu-id="883ed-108">根據名稱或物件，給予虛擬路由器對等，列舉由特定虛擬路由器宣告到該對等的路由。</span><span class="sxs-lookup"><span data-stu-id="883ed-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="883ed-109">示例</span><span class="sxs-lookup"><span data-stu-id="883ed-109">EXAMPLES</span></span>

### <span data-ttu-id="883ed-110">範例1</span><span class="sxs-lookup"><span data-stu-id="883ed-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="883ed-111">範例2</span><span class="sxs-lookup"><span data-stu-id="883ed-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="883ed-112">參數</span><span class="sxs-lookup"><span data-stu-id="883ed-112">PARAMETERS</span></span>

### <span data-ttu-id="883ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="883ed-113">-AsJob</span></span>
<span data-ttu-id="883ed-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="883ed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="883ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883ed-115">-DefaultProfile</span></span>
<span data-ttu-id="883ed-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="883ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883ed-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="883ed-117">-InputObject</span></span>
<span data-ttu-id="883ed-118">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="883ed-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="883ed-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="883ed-119">-PeerName</span></span>
<span data-ttu-id="883ed-120">虛擬路由器對等名稱</span><span class="sxs-lookup"><span data-stu-id="883ed-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="883ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="883ed-122">虛擬路由器對等資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="883ed-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="883ed-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="883ed-123">-VirtualRouterName</span></span>
<span data-ttu-id="883ed-124">虛擬路由器名稱</span><span class="sxs-lookup"><span data-stu-id="883ed-124">Virtual router name</span></span>

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

### <span data-ttu-id="883ed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883ed-125">CommonParameters</span></span>
<span data-ttu-id="883ed-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="883ed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883ed-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="883ed-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883ed-128">輸入</span><span class="sxs-lookup"><span data-stu-id="883ed-128">INPUTS</span></span>

### <span data-ttu-id="883ed-129">System.object</span><span class="sxs-lookup"><span data-stu-id="883ed-129">System.String</span></span>

### <span data-ttu-id="883ed-130">PSVirtualRouterPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="883ed-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="883ed-131">輸出</span><span class="sxs-lookup"><span data-stu-id="883ed-131">OUTPUTS</span></span>

### <span data-ttu-id="883ed-132">PSPeerRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="883ed-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="883ed-133">筆記</span><span class="sxs-lookup"><span data-stu-id="883ed-133">NOTES</span></span>

## <span data-ttu-id="883ed-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="883ed-134">RELATED LINKS</span></span>
