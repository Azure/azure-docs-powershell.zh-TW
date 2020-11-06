---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: d5314453be4d2f9042fd5034cc864d94caf1dbd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622024"
---
# <span data-ttu-id="6ecb3-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="6ecb3-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="6ecb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ecb3-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecb3-103">使用 ResourceGroupName 和 GatewayName 取得 ExpressRouteGateway 資源，或以 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="6ecb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ecb3-104">SYNTAX</span></span>

### <span data-ttu-id="6ecb3-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="6ecb3-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ecb3-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecb3-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ecb3-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6ecb3-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ecb3-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ecb3-108">DESCRIPTION</span></span>
<span data-ttu-id="6ecb3-109">使用 ResourceGroupName 和 GatewayName 取得 ExpressRouteGateway 資源，或以 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="6ecb3-110">示例</span><span class="sxs-lookup"><span data-stu-id="6ecb3-110">EXAMPLES</span></span>

### <span data-ttu-id="6ecb3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6ecb3-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="6ecb3-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬廣域網路、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6ecb3-113">在具有2個比例單位的虛擬中樞中，將會建立 ExpressRoute 閘道。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6ecb3-114">然後它會使用其 resourceGroupName 和閘道名稱取得 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="6ecb3-115">範例2</span><span class="sxs-lookup"><span data-stu-id="6ecb3-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="6ecb3-116">這個命令會取得所有以「test」開頭的 ExpressRouteGateways。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="6ecb3-117">參數</span><span class="sxs-lookup"><span data-stu-id="6ecb3-117">PARAMETERS</span></span>

### <span data-ttu-id="6ecb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecb3-118">-DefaultProfile</span></span>
<span data-ttu-id="6ecb3-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ecb3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ecb3-120">-Name</span></span>
<span data-ttu-id="6ecb3-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6ecb3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecb3-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ecb3-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6ecb3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ecb3-124">-ResourceId</span></span>
<span data-ttu-id="6ecb3-125">要刪除之 expressRouteGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ecb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecb3-126">CommonParameters</span></span>
<span data-ttu-id="6ecb3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecb3-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecb3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6ecb3-129">INPUTS</span></span>

### <span data-ttu-id="6ecb3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="6ecb3-130">System.String</span></span>

## <span data-ttu-id="6ecb3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6ecb3-131">OUTPUTS</span></span>

### <span data-ttu-id="6ecb3-132">PSExpressRouteGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ecb3-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="6ecb3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6ecb3-133">NOTES</span></span>

## <span data-ttu-id="6ecb3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ecb3-134">RELATED LINKS</span></span>