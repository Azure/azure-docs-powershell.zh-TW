---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: 56f0eb8362cef287cea326ea30a559d7efc70573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902410"
---
# <span data-ttu-id="153ae-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="153ae-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="153ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="153ae-102">SYNOPSIS</span></span>
<span data-ttu-id="153ae-103">在虛擬中樞中獲取虛擬中樞路由資料表，或在虛擬中樞中列出所有路由資料表。</span><span class="sxs-lookup"><span data-stu-id="153ae-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="153ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="153ae-104">SYNTAX</span></span>

### <span data-ttu-id="153ae-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="153ae-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="153ae-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="153ae-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="153ae-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="153ae-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="153ae-108">描述</span><span class="sxs-lookup"><span data-stu-id="153ae-108">DESCRIPTION</span></span>
<span data-ttu-id="153ae-109">在虛擬中樞中獲取虛擬中樞路由資料表，或在虛擬中樞中列出所有路由資料表。</span><span class="sxs-lookup"><span data-stu-id="153ae-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="153ae-110">例子</span><span class="sxs-lookup"><span data-stu-id="153ae-110">EXAMPLES</span></span>

### <span data-ttu-id="153ae-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="153ae-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="153ae-112">此 Cmdlet 會使用資源組名、中樞名稱和路由資料表名稱，來取回路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="153ae-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="153ae-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="153ae-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="153ae-114">此 Cmdlet 會使用資源組名和中樞名稱，列出虛擬中樞中所有呈現的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="153ae-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="153ae-115">參數</span><span class="sxs-lookup"><span data-stu-id="153ae-115">PARAMETERS</span></span>

### <span data-ttu-id="153ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153ae-116">-DefaultProfile</span></span>
<span data-ttu-id="153ae-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="153ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ae-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="153ae-118">-HubName</span></span>
<span data-ttu-id="153ae-119">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="153ae-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ae-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="153ae-120">-Name</span></span>
<span data-ttu-id="153ae-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="153ae-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ae-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="153ae-122">-ParentResourceId</span></span>
<span data-ttu-id="153ae-123">父資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="153ae-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="153ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="153ae-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="153ae-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ae-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="153ae-126">-VirtualHub</span></span>
<span data-ttu-id="153ae-127">父資源。</span><span class="sxs-lookup"><span data-stu-id="153ae-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="153ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153ae-128">CommonParameters</span></span>
<span data-ttu-id="153ae-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="153ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153ae-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="153ae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153ae-131">輸入</span><span class="sxs-lookup"><span data-stu-id="153ae-131">INPUTS</span></span>

### <span data-ttu-id="153ae-132">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="153ae-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="153ae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="153ae-133">System.String</span></span>

## <span data-ttu-id="153ae-134">輸出</span><span class="sxs-lookup"><span data-stu-id="153ae-134">OUTPUTS</span></span>

### <span data-ttu-id="153ae-135">Microsoft.Azure.Commands.Network.models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="153ae-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="153ae-136">筆記</span><span class="sxs-lookup"><span data-stu-id="153ae-136">NOTES</span></span>

## <span data-ttu-id="153ae-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="153ae-137">RELATED LINKS</span></span>
