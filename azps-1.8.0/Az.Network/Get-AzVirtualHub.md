---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621936"
---
# <span data-ttu-id="3ac52-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ac52-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="3ac52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ac52-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac52-103">透過 ResourceGroupName/訂閱取得名稱和 ResourceGroupName 或列出所有虛擬中樞的 Azure VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="3ac52-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="3ac52-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ac52-104">SYNTAX</span></span>

### <span data-ttu-id="3ac52-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="3ac52-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ac52-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac52-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ac52-107">說明</span><span class="sxs-lookup"><span data-stu-id="3ac52-107">DESCRIPTION</span></span>
<span data-ttu-id="3ac52-108">透過 ResourceGroupName/訂閱取得名稱和 ResourceGroupName 或列出所有虛擬中樞的 Azure VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="3ac52-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="3ac52-109">示例</span><span class="sxs-lookup"><span data-stu-id="3ac52-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac52-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3ac52-110">Example 1</span></span>

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

<span data-ttu-id="3ac52-111">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="3ac52-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="3ac52-112">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="3ac52-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="3ac52-113">接著，它會使用虛擬中心的 ResourceGroupName 和使用方式來取得它。</span><span class="sxs-lookup"><span data-stu-id="3ac52-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="3ac52-114">範例2</span><span class="sxs-lookup"><span data-stu-id="3ac52-114">Example 2</span></span>

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

<span data-ttu-id="3ac52-115">這個 Cmdlet 會使用篩選來取得虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="3ac52-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="3ac52-116">參數</span><span class="sxs-lookup"><span data-stu-id="3ac52-116">PARAMETERS</span></span>

### <span data-ttu-id="3ac52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac52-117">-DefaultProfile</span></span>
<span data-ttu-id="3ac52-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ac52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac52-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ac52-119">-Name</span></span>
<span data-ttu-id="3ac52-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac52-120">The resource name.</span></span>

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

### <span data-ttu-id="3ac52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac52-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ac52-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac52-122">The resource group name.</span></span>

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

### <span data-ttu-id="3ac52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac52-123">CommonParameters</span></span>
<span data-ttu-id="3ac52-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ac52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac52-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ac52-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac52-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3ac52-126">INPUTS</span></span>

### <span data-ttu-id="3ac52-127">所有</span><span class="sxs-lookup"><span data-stu-id="3ac52-127">None</span></span>

## <span data-ttu-id="3ac52-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3ac52-128">OUTPUTS</span></span>

### <span data-ttu-id="3ac52-129">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3ac52-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="3ac52-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3ac52-130">NOTES</span></span>

## <span data-ttu-id="3ac52-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ac52-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ac52-132">新-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ac52-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="3ac52-133">移除-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ac52-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="3ac52-134">更新-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ac52-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
