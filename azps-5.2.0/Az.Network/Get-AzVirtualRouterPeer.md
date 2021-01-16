---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280642"
---
# <span data-ttu-id="b8278-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="b8278-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="b8278-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8278-102">SYNOPSIS</span></span>
<span data-ttu-id="b8278-103">取得 Azure VirtualRouter 中的 VirtualRouter 對等</span><span class="sxs-lookup"><span data-stu-id="b8278-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="b8278-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8278-104">SYNTAX</span></span>

### <span data-ttu-id="b8278-105">VirtualRouterPeerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b8278-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8278-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8278-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8278-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8278-107">DESCRIPTION</span></span>
<span data-ttu-id="b8278-108">**AzVirtualRouterPeer** Cmdlet 會取得 Azure VirtualRouter 中的對等</span><span class="sxs-lookup"><span data-stu-id="b8278-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="b8278-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8278-109">EXAMPLES</span></span>

### <span data-ttu-id="b8278-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b8278-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="b8278-111">範例2</span><span class="sxs-lookup"><span data-stu-id="b8278-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="b8278-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8278-112">PARAMETERS</span></span>

### <span data-ttu-id="b8278-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8278-113">-DefaultProfile</span></span>
<span data-ttu-id="b8278-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8278-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8278-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="b8278-115">-PeerName</span></span>
<span data-ttu-id="b8278-116">虛擬路由器對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8278-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="b8278-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8278-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8278-118">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b8278-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="b8278-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8278-119">-ResourceId</span></span>
<span data-ttu-id="b8278-120">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b8278-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="b8278-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="b8278-121">-VirtualRouterName</span></span>
<span data-ttu-id="b8278-122">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8278-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="b8278-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8278-123">CommonParameters</span></span>
<span data-ttu-id="b8278-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8278-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8278-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8278-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8278-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b8278-126">INPUTS</span></span>

### <span data-ttu-id="b8278-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b8278-127">System.String</span></span>

## <span data-ttu-id="b8278-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b8278-128">OUTPUTS</span></span>

### <span data-ttu-id="b8278-129">PSVirtualRouterPeer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8278-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="b8278-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b8278-130">NOTES</span></span>

## <span data-ttu-id="b8278-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8278-131">RELATED LINKS</span></span>
