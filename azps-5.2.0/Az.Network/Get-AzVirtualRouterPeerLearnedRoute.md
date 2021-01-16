---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280639"
---
# <span data-ttu-id="19786-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="19786-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="19786-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19786-102">SYNOPSIS</span></span>
<span data-ttu-id="19786-103">由特定虛擬路由器對等的清單路由</span><span class="sxs-lookup"><span data-stu-id="19786-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="19786-104">句法</span><span class="sxs-lookup"><span data-stu-id="19786-104">SYNTAX</span></span>

### <span data-ttu-id="19786-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="19786-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19786-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19786-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19786-107">說明</span><span class="sxs-lookup"><span data-stu-id="19786-107">DESCRIPTION</span></span>
<span data-ttu-id="19786-108">列舉由虛擬路由器對等其他來源所學的路由。</span><span class="sxs-lookup"><span data-stu-id="19786-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="19786-109">示例</span><span class="sxs-lookup"><span data-stu-id="19786-109">EXAMPLES</span></span>

### <span data-ttu-id="19786-110">範例1</span><span class="sxs-lookup"><span data-stu-id="19786-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="19786-111">範例2</span><span class="sxs-lookup"><span data-stu-id="19786-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="19786-112">參數</span><span class="sxs-lookup"><span data-stu-id="19786-112">PARAMETERS</span></span>

### <span data-ttu-id="19786-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19786-113">-AsJob</span></span>
<span data-ttu-id="19786-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="19786-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19786-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19786-115">-DefaultProfile</span></span>
<span data-ttu-id="19786-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19786-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19786-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19786-117">-InputObject</span></span>
<span data-ttu-id="19786-118">虛擬路由器對等輸入物件。</span><span class="sxs-lookup"><span data-stu-id="19786-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="19786-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="19786-119">-PeerName</span></span>
<span data-ttu-id="19786-120">虛擬路由器對等名稱</span><span class="sxs-lookup"><span data-stu-id="19786-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="19786-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19786-121">-ResourceGroupName</span></span>
<span data-ttu-id="19786-122">虛擬路由器對等資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="19786-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="19786-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="19786-123">-VirtualRouterName</span></span>
<span data-ttu-id="19786-124">虛擬路由器名稱</span><span class="sxs-lookup"><span data-stu-id="19786-124">Virtual router name</span></span>

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

### <span data-ttu-id="19786-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19786-125">CommonParameters</span></span>
<span data-ttu-id="19786-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19786-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19786-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="19786-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19786-128">輸入</span><span class="sxs-lookup"><span data-stu-id="19786-128">INPUTS</span></span>

### <span data-ttu-id="19786-129">System.object</span><span class="sxs-lookup"><span data-stu-id="19786-129">System.String</span></span>

### <span data-ttu-id="19786-130">PSVirtualRouterPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="19786-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="19786-131">輸出</span><span class="sxs-lookup"><span data-stu-id="19786-131">OUTPUTS</span></span>

### <span data-ttu-id="19786-132">PSPeerRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="19786-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="19786-133">筆記</span><span class="sxs-lookup"><span data-stu-id="19786-133">NOTES</span></span>

## <span data-ttu-id="19786-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="19786-134">RELATED LINKS</span></span>
