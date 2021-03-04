---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 8dbc1ad62d11ac6b14897c27b11ebdb7f6fb8cc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904037"
---
# <span data-ttu-id="26270-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="26270-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="26270-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26270-102">SYNOPSIS</span></span>
<span data-ttu-id="26270-103">列出 Azure 虛擬網路閘道所學習的路由</span><span class="sxs-lookup"><span data-stu-id="26270-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="26270-104">語法</span><span class="sxs-lookup"><span data-stu-id="26270-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26270-105">描述</span><span class="sxs-lookup"><span data-stu-id="26270-105">DESCRIPTION</span></span>
<span data-ttu-id="26270-106">列舉 Azure 虛擬網路閘道從各種來源得知的路由。</span><span class="sxs-lookup"><span data-stu-id="26270-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="26270-107">這包括從 BGP 學習的路由，以及靜態路由。</span><span class="sxs-lookup"><span data-stu-id="26270-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="26270-108">例子</span><span class="sxs-lookup"><span data-stu-id="26270-108">EXAMPLES</span></span>

### <span data-ttu-id="26270-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="26270-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="26270-110">針對資源群組資源群組中名為閘道名稱的 Azure 虛擬網路閘道，會取回 Azure 閘道知道路由。</span><span class="sxs-lookup"><span data-stu-id="26270-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="26270-111">在此案例中，Azure 虛擬網路閘道有兩個靜態路由 (10.1.0.0/16 和 10.0.0.254/32) ，以及一個從 BGP (10.0.0.0/16) 學習的路由。</span><span class="sxs-lookup"><span data-stu-id="26270-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="26270-112">參數</span><span class="sxs-lookup"><span data-stu-id="26270-112">PARAMETERS</span></span>

### <span data-ttu-id="26270-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26270-113">-AsJob</span></span>
<span data-ttu-id="26270-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26270-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26270-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26270-115">-DefaultProfile</span></span>
<span data-ttu-id="26270-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="26270-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26270-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26270-117">-ResourceGroupName</span></span>
<span data-ttu-id="26270-118">虛擬網路閘道資源組名</span><span class="sxs-lookup"><span data-stu-id="26270-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="26270-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="26270-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="26270-120">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="26270-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="26270-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26270-121">CommonParameters</span></span>
<span data-ttu-id="26270-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26270-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26270-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26270-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26270-124">輸入</span><span class="sxs-lookup"><span data-stu-id="26270-124">INPUTS</span></span>

### <span data-ttu-id="26270-125">System.String</span><span class="sxs-lookup"><span data-stu-id="26270-125">System.String</span></span>

## <span data-ttu-id="26270-126">輸出</span><span class="sxs-lookup"><span data-stu-id="26270-126">OUTPUTS</span></span>

### <span data-ttu-id="26270-127">Microsoft.Azure.Commands.Network.models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="26270-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="26270-128">筆記</span><span class="sxs-lookup"><span data-stu-id="26270-128">NOTES</span></span>

## <span data-ttu-id="26270-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="26270-129">RELATED LINKS</span></span>
