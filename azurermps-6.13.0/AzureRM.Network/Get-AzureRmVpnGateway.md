---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448360"
---
# <span data-ttu-id="30b33-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="30b33-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="30b33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30b33-102">SYNOPSIS</span></span>
<span data-ttu-id="30b33-103">使用 ResourceGroupName 和 GatewayName 取得 VpnGateway 資源，或以 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="30b33-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30b33-104">句法</span><span class="sxs-lookup"><span data-stu-id="30b33-104">SYNTAX</span></span>

### <span data-ttu-id="30b33-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="30b33-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30b33-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b33-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30b33-107">說明</span><span class="sxs-lookup"><span data-stu-id="30b33-107">DESCRIPTION</span></span>
<span data-ttu-id="30b33-108">使用 ResourceGroupName 和 GatewayName 取得 VpnGateway 資源，或以 ResourceGroupName 或 SubscriptionId 列出所有閘道。</span><span class="sxs-lookup"><span data-stu-id="30b33-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="30b33-109">示例</span><span class="sxs-lookup"><span data-stu-id="30b33-109">EXAMPLES</span></span>

### <span data-ttu-id="30b33-110">範例1</span><span class="sxs-lookup"><span data-stu-id="30b33-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="30b33-111">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="30b33-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="30b33-112">此後，就會在具有2個比例單位的虛擬中樞中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="30b33-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="30b33-113">然後它會使用其 resourceGroupName 和閘道名稱取得 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="30b33-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="30b33-114">參數</span><span class="sxs-lookup"><span data-stu-id="30b33-114">PARAMETERS</span></span>

### <span data-ttu-id="30b33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b33-115">-DefaultProfile</span></span>
<span data-ttu-id="30b33-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30b33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b33-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="30b33-117">-Name</span></span>
<span data-ttu-id="30b33-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="30b33-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30b33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b33-119">-ResourceGroupName</span></span>
<span data-ttu-id="30b33-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30b33-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b33-121">CommonParameters</span></span>
<span data-ttu-id="30b33-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30b33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b33-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30b33-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b33-124">輸入</span><span class="sxs-lookup"><span data-stu-id="30b33-124">INPUTS</span></span>

### <span data-ttu-id="30b33-125">System.object</span><span class="sxs-lookup"><span data-stu-id="30b33-125">System.String</span></span>

## <span data-ttu-id="30b33-126">輸出</span><span class="sxs-lookup"><span data-stu-id="30b33-126">OUTPUTS</span></span>

### <span data-ttu-id="30b33-127">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="30b33-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="30b33-128">筆記</span><span class="sxs-lookup"><span data-stu-id="30b33-128">NOTES</span></span>

## <span data-ttu-id="30b33-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="30b33-129">RELATED LINKS</span></span>
