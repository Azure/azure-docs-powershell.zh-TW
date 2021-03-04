---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 7b17b124b7d4e0dc89ee7e61469b26401002db9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904609"
---
# <span data-ttu-id="3b6ed-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3b6ed-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="3b6ed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6ed-103">在 Azure VirtualRouter 中建立 VirtualRouter 對等程式</span><span class="sxs-lookup"><span data-stu-id="3b6ed-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="3b6ed-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b6ed-104">SYNTAX</span></span>

### <span data-ttu-id="3b6ed-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b6ed-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b6ed-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b6ed-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b6ed-107">描述</span><span class="sxs-lookup"><span data-stu-id="3b6ed-107">DESCRIPTION</span></span>
<span data-ttu-id="3b6ed-108">**Get-AzVirtualRouterPeer Cmdlet** 在 Azure VirtualRouter 中取得對等</span><span class="sxs-lookup"><span data-stu-id="3b6ed-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="3b6ed-109">例子</span><span class="sxs-lookup"><span data-stu-id="3b6ed-109">EXAMPLES</span></span>

### <span data-ttu-id="3b6ed-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3b6ed-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="3b6ed-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="3b6ed-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="3b6ed-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b6ed-112">PARAMETERS</span></span>

### <span data-ttu-id="3b6ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6ed-113">-DefaultProfile</span></span>
<span data-ttu-id="3b6ed-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b6ed-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3b6ed-115">-PeerName</span></span>
<span data-ttu-id="3b6ed-116">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="3b6ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b6ed-118">虛擬路由器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="3b6ed-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b6ed-119">-ResourceId</span></span>
<span data-ttu-id="3b6ed-120">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="3b6ed-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="3b6ed-121">-VirtualRouterName</span></span>
<span data-ttu-id="3b6ed-122">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="3b6ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6ed-123">CommonParameters</span></span>
<span data-ttu-id="3b6ed-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6ed-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b6ed-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6ed-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3b6ed-126">INPUTS</span></span>

### <span data-ttu-id="3b6ed-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3b6ed-127">System.String</span></span>

## <span data-ttu-id="3b6ed-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3b6ed-128">OUTPUTS</span></span>

### <span data-ttu-id="3b6ed-129">Microsoft.Azure.Commands.Network.models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3b6ed-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="3b6ed-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3b6ed-130">NOTES</span></span>

## <span data-ttu-id="3b6ed-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b6ed-131">RELATED LINKS</span></span>
