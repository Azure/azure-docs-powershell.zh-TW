---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
ms.openlocfilehash: 39bf91e5d346b475fe0c4b79b9128648555c6379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800853"
---
# <span data-ttu-id="b9c1f-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="b9c1f-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="b9c1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c1f-103">列出由 Azure 虛擬網路閘道所學的路線</span><span class="sxs-lookup"><span data-stu-id="b9c1f-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9c1f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c1f-106">列舉由來自各種來源的 Azure 虛擬網路閘道所瞭解的路由。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="b9c1f-107">這包括通過 BGP 以及靜態路由來獲知的路由。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="b9c1f-108">示例</span><span class="sxs-lookup"><span data-stu-id="b9c1f-108">EXAMPLES</span></span>

### <span data-ttu-id="b9c1f-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b9c1f-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="b9c1f-110">針對資源群組 resourceGroup 中名為 gatewayname 的 Azure 虛擬網路閘道，會檢索 Azure 閘道已知的路由。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="b9c1f-111">在這種情況下，Azure 虛擬網路閘道會有兩個靜態路由 (10.1.0.0/16 和 10.0.0.254/32) ，以及通過 BGP (10.0.0.0/16) 瞭解的一個路由。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="b9c1f-112">參數</span><span class="sxs-lookup"><span data-stu-id="b9c1f-112">PARAMETERS</span></span>

### <span data-ttu-id="b9c1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9c1f-113">-AsJob</span></span>
<span data-ttu-id="b9c1f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b9c1f-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c1f-115">-DefaultProfile</span></span>
<span data-ttu-id="b9c1f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9c1f-118">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b9c1f-118">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b9c1f-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b9c1f-120">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="b9c1f-120">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c1f-121">CommonParameters</span></span>
<span data-ttu-id="b9c1f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c1f-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9c1f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c1f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b9c1f-124">INPUTS</span></span>

### <span data-ttu-id="b9c1f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="b9c1f-125">System.String</span></span>

## <span data-ttu-id="b9c1f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b9c1f-126">OUTPUTS</span></span>

### <span data-ttu-id="b9c1f-127">PSGatewayRoute [] （[]）</span><span class="sxs-lookup"><span data-stu-id="b9c1f-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="b9c1f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b9c1f-128">NOTES</span></span>

## <span data-ttu-id="b9c1f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9c1f-129">RELATED LINKS</span></span>
