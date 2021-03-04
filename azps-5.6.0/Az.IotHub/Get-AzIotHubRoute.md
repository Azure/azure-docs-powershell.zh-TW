---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: d627460da42d5d5710aa9931d2e831320378b082
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911018"
---
# <span data-ttu-id="226ce-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="226ce-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="226ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="226ce-102">SYNOPSIS</span></span>
<span data-ttu-id="226ce-103">取得 IoT 中心中路由的資訊</span><span class="sxs-lookup"><span data-stu-id="226ce-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="226ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="226ce-104">SYNTAX</span></span>

### <span data-ttu-id="226ce-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="226ce-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="226ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="226ce-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="226ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="226ce-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="226ce-108">描述</span><span class="sxs-lookup"><span data-stu-id="226ce-108">DESCRIPTION</span></span>
<span data-ttu-id="226ce-109">取得路線資訊。您可以取得來自 IoT 中心的所有路由、取得端點類型的路由，或取得特定端點的路由。</span><span class="sxs-lookup"><span data-stu-id="226ce-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="226ce-110">例子</span><span class="sxs-lookup"><span data-stu-id="226ce-110">EXAMPLES</span></span>

### <span data-ttu-id="226ce-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="226ce-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="226ce-112">從 "myiothub" IoT Hub 取得所有路由。</span><span class="sxs-lookup"><span data-stu-id="226ce-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="226ce-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="226ce-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="226ce-114">從 "myiothub" IoT Hub 取得路由資訊。</span><span class="sxs-lookup"><span data-stu-id="226ce-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="226ce-115">參數</span><span class="sxs-lookup"><span data-stu-id="226ce-115">PARAMETERS</span></span>

### <span data-ttu-id="226ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226ce-116">-DefaultProfile</span></span>
<span data-ttu-id="226ce-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="226ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="226ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="226ce-118">-InputObject</span></span>
<span data-ttu-id="226ce-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="226ce-119">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="226ce-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="226ce-120">-Name</span></span>
<span data-ttu-id="226ce-121">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="226ce-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="226ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="226ce-123">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="226ce-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="226ce-124">-ResourceId</span></span>
<span data-ttu-id="226ce-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="226ce-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226ce-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="226ce-126">-RouteName</span></span>
<span data-ttu-id="226ce-127">路線名稱</span><span class="sxs-lookup"><span data-stu-id="226ce-127">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226ce-128">CommonParameters</span></span>
<span data-ttu-id="226ce-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="226ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226ce-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="226ce-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226ce-131">輸入</span><span class="sxs-lookup"><span data-stu-id="226ce-131">INPUTS</span></span>

### <span data-ttu-id="226ce-132">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="226ce-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="226ce-133">System.String</span><span class="sxs-lookup"><span data-stu-id="226ce-133">System.String</span></span>

## <span data-ttu-id="226ce-134">輸出</span><span class="sxs-lookup"><span data-stu-id="226ce-134">OUTPUTS</span></span>

### <span data-ttu-id="226ce-135">Microsoft.Azure.Commands.management.IotHub.models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="226ce-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="226ce-136">Microsoft.Azure.Commands.management.IotHub.models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="226ce-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="226ce-137">筆記</span><span class="sxs-lookup"><span data-stu-id="226ce-137">NOTES</span></span>

## <span data-ttu-id="226ce-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="226ce-138">RELATED LINKS</span></span>
