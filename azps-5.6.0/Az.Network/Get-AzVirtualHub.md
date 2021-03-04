---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 630e0a6759e278e4da2d6d56cf34bb5fa5812595
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902422"
---
# <span data-ttu-id="da38c-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="da38c-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="da38c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="da38c-102">SYNOPSIS</span></span>
<span data-ttu-id="da38c-103">按名稱和資源GroupName 來獲得 Azure VirtualHub，或按 ResourceGroupName/Subscription 列出所有虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="da38c-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="da38c-104">語法</span><span class="sxs-lookup"><span data-stu-id="da38c-104">SYNTAX</span></span>

### <span data-ttu-id="da38c-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="da38c-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da38c-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da38c-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da38c-107">描述</span><span class="sxs-lookup"><span data-stu-id="da38c-107">DESCRIPTION</span></span>
<span data-ttu-id="da38c-108">按名稱和資源GroupName 來獲得 Azure VirtualHub，或按 ResourceGroupName/Subscription 列出所有虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="da38c-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="da38c-109">例子</span><span class="sxs-lookup"><span data-stu-id="da38c-109">EXAMPLES</span></span>

### <span data-ttu-id="da38c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="da38c-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="da38c-111">上述步驟將在 Azure 資源群組中建立資源群組「testRG」、一個虛擬 WAN，以及美國西部的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="da38c-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="da38c-112">虛擬中樞的位址空間為「10.0.1.0/24」。</span><span class="sxs-lookup"><span data-stu-id="da38c-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="da38c-113">然後，它會使用 ResourceGroupName 和 ResourceName 來獲得虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="da38c-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="da38c-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="da38c-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="da38c-115">此 Cmdlet 會使用篩選功能獲得虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="da38c-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="da38c-116">參數</span><span class="sxs-lookup"><span data-stu-id="da38c-116">PARAMETERS</span></span>

### <span data-ttu-id="da38c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da38c-117">-DefaultProfile</span></span>
<span data-ttu-id="da38c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="da38c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da38c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="da38c-119">-Name</span></span>
<span data-ttu-id="da38c-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="da38c-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="da38c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da38c-121">-ResourceGroupName</span></span>
<span data-ttu-id="da38c-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="da38c-122">The resource group name.</span></span>

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

### <span data-ttu-id="da38c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da38c-123">CommonParameters</span></span>
<span data-ttu-id="da38c-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="da38c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da38c-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da38c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da38c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="da38c-126">INPUTS</span></span>

### <span data-ttu-id="da38c-127">沒有</span><span class="sxs-lookup"><span data-stu-id="da38c-127">None</span></span>

## <span data-ttu-id="da38c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="da38c-128">OUTPUTS</span></span>

### <span data-ttu-id="da38c-129">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="da38c-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="da38c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="da38c-130">NOTES</span></span>

## <span data-ttu-id="da38c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="da38c-131">RELATED LINKS</span></span>

[<span data-ttu-id="da38c-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="da38c-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="da38c-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="da38c-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="da38c-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="da38c-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
