---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131314"
---
# <span data-ttu-id="85ca1-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="85ca1-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="85ca1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="85ca1-103">取得 Azure VirtualRouter 中的 VirtualRouter 對等</span><span class="sxs-lookup"><span data-stu-id="85ca1-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="85ca1-104">句法</span><span class="sxs-lookup"><span data-stu-id="85ca1-104">SYNTAX</span></span>

### <span data-ttu-id="85ca1-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="85ca1-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85ca1-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85ca1-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85ca1-107">說明</span><span class="sxs-lookup"><span data-stu-id="85ca1-107">DESCRIPTION</span></span>
<span data-ttu-id="85ca1-108">**AzVirtualRouterPeer** Cmdlet 會取得 Azure VirtualRouter 中的對等</span><span class="sxs-lookup"><span data-stu-id="85ca1-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="85ca1-109">示例</span><span class="sxs-lookup"><span data-stu-id="85ca1-109">EXAMPLES</span></span>

### <span data-ttu-id="85ca1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="85ca1-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="85ca1-111">範例2</span><span class="sxs-lookup"><span data-stu-id="85ca1-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="85ca1-112">參數</span><span class="sxs-lookup"><span data-stu-id="85ca1-112">PARAMETERS</span></span>

### <span data-ttu-id="85ca1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ca1-113">-DefaultProfile</span></span>
<span data-ttu-id="85ca1-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85ca1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ca1-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="85ca1-115">-PeerName</span></span>
<span data-ttu-id="85ca1-116">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ca1-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="85ca1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ca1-117">-ResourceGroupName</span></span>
<span data-ttu-id="85ca1-118">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="85ca1-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="85ca1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85ca1-119">-ResourceId</span></span>
<span data-ttu-id="85ca1-120">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="85ca1-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="85ca1-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="85ca1-121">-VirtualRouterName</span></span>
<span data-ttu-id="85ca1-122">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ca1-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="85ca1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ca1-123">CommonParameters</span></span>
<span data-ttu-id="85ca1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85ca1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ca1-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="85ca1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ca1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="85ca1-126">INPUTS</span></span>

### <span data-ttu-id="85ca1-127">System.object</span><span class="sxs-lookup"><span data-stu-id="85ca1-127">System.String</span></span>

## <span data-ttu-id="85ca1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="85ca1-128">OUTPUTS</span></span>

### <span data-ttu-id="85ca1-129">PSVirtualRouterPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85ca1-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="85ca1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="85ca1-130">NOTES</span></span>

## <span data-ttu-id="85ca1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="85ca1-131">RELATED LINKS</span></span>
