---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625833"
---
# <span data-ttu-id="d863e-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d863e-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="d863e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d863e-102">SYNOPSIS</span></span>
<span data-ttu-id="d863e-103">取得 IoT 中心路由的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d863e-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d863e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d863e-104">SYNTAX</span></span>

### <span data-ttu-id="d863e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d863e-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d863e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d863e-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d863e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d863e-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d863e-108">說明</span><span class="sxs-lookup"><span data-stu-id="d863e-108">DESCRIPTION</span></span>
<span data-ttu-id="d863e-109">取得路線的相關資訊。您可以從 IoT 中樞取得所有路由、取得端點類型的路線，或取得特定端點的路線。</span><span class="sxs-lookup"><span data-stu-id="d863e-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="d863e-110">示例</span><span class="sxs-lookup"><span data-stu-id="d863e-110">EXAMPLES</span></span>

### <span data-ttu-id="d863e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d863e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="d863e-112">從「myiothub」 IoT 中樞取得所有路由。</span><span class="sxs-lookup"><span data-stu-id="d863e-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d863e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d863e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="d863e-114">從「myiothub」 IoT 中樞取得路由資訊。</span><span class="sxs-lookup"><span data-stu-id="d863e-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d863e-115">參數</span><span class="sxs-lookup"><span data-stu-id="d863e-115">PARAMETERS</span></span>

### <span data-ttu-id="d863e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d863e-116">-DefaultProfile</span></span>
<span data-ttu-id="d863e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d863e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d863e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d863e-118">-InputObject</span></span>
<span data-ttu-id="d863e-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="d863e-119">IotHub Object</span></span>

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

### <span data-ttu-id="d863e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d863e-120">-Name</span></span>
<span data-ttu-id="d863e-121">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="d863e-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d863e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d863e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d863e-123">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d863e-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d863e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d863e-124">-ResourceId</span></span>
<span data-ttu-id="d863e-125">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d863e-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d863e-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="d863e-126">-RouteName</span></span>
<span data-ttu-id="d863e-127">路線的名稱</span><span class="sxs-lookup"><span data-stu-id="d863e-127">Name of the Route</span></span>

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

### <span data-ttu-id="d863e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d863e-128">CommonParameters</span></span>
<span data-ttu-id="d863e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d863e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d863e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d863e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d863e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d863e-131">INPUTS</span></span>

### <span data-ttu-id="d863e-132">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="d863e-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="d863e-133">System.object</span><span class="sxs-lookup"><span data-stu-id="d863e-133">System.String</span></span>

## <span data-ttu-id="d863e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d863e-134">OUTPUTS</span></span>

### <span data-ttu-id="d863e-135">PSRouteMetadata （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="d863e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="d863e-136">[System.object]。清單 ' 1 [IotHub. PSRouteProperties，IotHub，版本 = 3.1.3.0，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="d863e-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d863e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d863e-137">NOTES</span></span>

## <span data-ttu-id="d863e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d863e-138">RELATED LINKS</span></span>
