---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279219"
---
# <span data-ttu-id="0d9fc-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d9fc-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="0d9fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9fc-103">更新私人端點。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="0d9fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d9fc-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d9fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d9fc-105">DESCRIPTION</span></span>
<span data-ttu-id="0d9fc-106">**AzPrivateEndpoint** Cmdlet 會更新私人端點。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="0d9fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d9fc-107">EXAMPLES</span></span>

### <span data-ttu-id="0d9fc-108">1：建立私用端點並將其中一個子網取代成另一個。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="0d9fc-109">這個範例會建立一個含有一個子網的專用端點，然後從虛擬網路的記憶體內部標記法取代成另一個子網。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="0d9fc-110">然後使用 Set-PrivateEndpoint Cmdlet，在服務端寫入修改過的專用端點狀態。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="0d9fc-111">參數</span><span class="sxs-lookup"><span data-stu-id="0d9fc-111">PARAMETERS</span></span>

### <span data-ttu-id="0d9fc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d9fc-112">-AsJob</span></span>
<span data-ttu-id="0d9fc-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0d9fc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d9fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d9fc-114">-DefaultProfile</span></span>
<span data-ttu-id="0d9fc-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d9fc-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d9fc-116">-PrivateEndpoint</span></span>
<span data-ttu-id="0d9fc-117">指定私人端點物件，該物件代表應該設定專用端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="0d9fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9fc-118">CommonParameters</span></span>
<span data-ttu-id="0d9fc-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9fc-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d9fc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9fc-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0d9fc-121">INPUTS</span></span>

### <span data-ttu-id="0d9fc-122">PSPrivateEndpoint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0d9fc-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="0d9fc-123">輸出</span><span class="sxs-lookup"><span data-stu-id="0d9fc-123">OUTPUTS</span></span>

### <span data-ttu-id="0d9fc-124">PSPrivateEndpoint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0d9fc-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="0d9fc-125">筆記</span><span class="sxs-lookup"><span data-stu-id="0d9fc-125">NOTES</span></span>

## <span data-ttu-id="0d9fc-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d9fc-126">RELATED LINKS</span></span>

[<span data-ttu-id="0d9fc-127">AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d9fc-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="0d9fc-128">新-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d9fc-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="0d9fc-129">移除-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d9fc-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


