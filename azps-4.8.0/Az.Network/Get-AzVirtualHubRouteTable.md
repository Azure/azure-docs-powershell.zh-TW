---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126987"
---
# <span data-ttu-id="6d8a8-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d8a8-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="6d8a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8a8-103">取得虛擬中樞中的虛擬中樞路由資料表，或列出虛擬中樞中的所有路由資料表。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="6d8a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d8a8-104">SYNTAX</span></span>

### <span data-ttu-id="6d8a8-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="6d8a8-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d8a8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6d8a8-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d8a8-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6d8a8-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d8a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="6d8a8-108">DESCRIPTION</span></span>
<span data-ttu-id="6d8a8-109">取得虛擬中樞中的虛擬中樞路由資料表，或列出虛擬中樞中的所有路由資料表。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="6d8a8-110">示例</span><span class="sxs-lookup"><span data-stu-id="6d8a8-110">EXAMPLES</span></span>

### <span data-ttu-id="6d8a8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6d8a8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="6d8a8-112">這個 Cmdlet 使用資源群組名稱、中樞名稱和路由資料表名稱來檢索路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="6d8a8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6d8a8-113">Example 2</span></span>
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

<span data-ttu-id="6d8a8-114">這個 Cmdlet 會使用資源組名稱和中樞名稱列出在虛擬中樞中存在的所有路由資料表。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="6d8a8-115">參數</span><span class="sxs-lookup"><span data-stu-id="6d8a8-115">PARAMETERS</span></span>

### <span data-ttu-id="6d8a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8a8-116">-DefaultProfile</span></span>
<span data-ttu-id="6d8a8-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d8a8-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="6d8a8-118">-HubName</span></span>
<span data-ttu-id="6d8a8-119">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-119">The parent resource name.</span></span>

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

### <span data-ttu-id="6d8a8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d8a8-120">-Name</span></span>
<span data-ttu-id="6d8a8-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-121">The resource name.</span></span>

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

### <span data-ttu-id="6d8a8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6d8a8-122">-ParentResourceId</span></span>
<span data-ttu-id="6d8a8-123">[父資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-123">The parent resource id.</span></span>

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

### <span data-ttu-id="6d8a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d8a8-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-125">The resource group name.</span></span>

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

### <span data-ttu-id="6d8a8-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d8a8-126">-VirtualHub</span></span>
<span data-ttu-id="6d8a8-127">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-127">The parent resource.</span></span>

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

### <span data-ttu-id="6d8a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8a8-128">CommonParameters</span></span>
<span data-ttu-id="6d8a8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8a8-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6d8a8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8a8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6d8a8-131">INPUTS</span></span>

### <span data-ttu-id="6d8a8-132">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6d8a8-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6d8a8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="6d8a8-133">System.String</span></span>

## <span data-ttu-id="6d8a8-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6d8a8-134">OUTPUTS</span></span>

### <span data-ttu-id="6d8a8-135">PSVirtualHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6d8a8-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="6d8a8-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6d8a8-136">NOTES</span></span>

## <span data-ttu-id="6d8a8-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d8a8-137">RELATED LINKS</span></span>