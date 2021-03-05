---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917965"
---
# <span data-ttu-id="ef4f7-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ef4f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4f7-103">更新私人端點。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="ef4f7-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef4f7-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef4f7-105">描述</span><span class="sxs-lookup"><span data-stu-id="ef4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4f7-106">**Set-AzPrivateEndpoint** Cmdlet 會更新私人端點。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="ef4f7-107">例子</span><span class="sxs-lookup"><span data-stu-id="ef4f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4f7-108">1：建立私人端點，並將其其中一個子網取代為另一個子網</span><span class="sxs-lookup"><span data-stu-id="ef4f7-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="ef4f7-109">此範例會建立一個子網的私人端點，然後從虛擬網路的記憶體中表示方式取代為另一個子網。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="ef4f7-110">然後Set-PrivateEndpoint Cmdlet，在服務端寫入經過修改的私人端點狀態。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="ef4f7-111">參數</span><span class="sxs-lookup"><span data-stu-id="ef4f7-111">PARAMETERS</span></span>

### <span data-ttu-id="ef4f7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef4f7-112">-AsJob</span></span>
<span data-ttu-id="ef4f7-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef4f7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef4f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4f7-114">-DefaultProfile</span></span>
<span data-ttu-id="ef4f7-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef4f7-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-116">-PrivateEndpoint</span></span>
<span data-ttu-id="ef4f7-117">指定代表應該設定私人端點之狀態的私人端點物件。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4f7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4f7-118">CommonParameters</span></span>
<span data-ttu-id="ef4f7-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef4f7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4f7-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef4f7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4f7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ef4f7-121">INPUTS</span></span>

### <span data-ttu-id="ef4f7-122">Microsoft.Azure.Commands.Network.models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="ef4f7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ef4f7-123">OUTPUTS</span></span>

### <span data-ttu-id="ef4f7-124">Microsoft.Azure.Commands.Network.models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="ef4f7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ef4f7-125">NOTES</span></span>

## <span data-ttu-id="ef4f7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef4f7-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef4f7-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="ef4f7-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="ef4f7-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4f7-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


