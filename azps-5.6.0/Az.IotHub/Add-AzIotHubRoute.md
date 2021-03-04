---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: fbb0801dd586731a938c773711d72847e7a96e50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913854"
---
# <span data-ttu-id="9dd79-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="9dd79-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="9dd79-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9dd79-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd79-103">在 IoT 中心建立路由</span><span class="sxs-lookup"><span data-stu-id="9dd79-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="9dd79-104">語法</span><span class="sxs-lookup"><span data-stu-id="9dd79-104">SYNTAX</span></span>

### <span data-ttu-id="9dd79-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9dd79-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dd79-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9dd79-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dd79-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9dd79-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd79-108">描述</span><span class="sxs-lookup"><span data-stu-id="9dd79-108">DESCRIPTION</span></span>
<span data-ttu-id="9dd79-109">建立傳送特定資料來源和條件至所需端點的路由。</span><span class="sxs-lookup"><span data-stu-id="9dd79-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="9dd79-110">例子</span><span class="sxs-lookup"><span data-stu-id="9dd79-110">EXAMPLES</span></span>

### <span data-ttu-id="9dd79-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9dd79-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="9dd79-112">建立新路由 "R1"。</span><span class="sxs-lookup"><span data-stu-id="9dd79-112">Create a new route "R1".</span></span>

## <span data-ttu-id="9dd79-113">參數</span><span class="sxs-lookup"><span data-stu-id="9dd79-113">PARAMETERS</span></span>

### <span data-ttu-id="9dd79-114">-條件</span><span class="sxs-lookup"><span data-stu-id="9dd79-114">-Condition</span></span>
<span data-ttu-id="9dd79-115">評估為適用路由規則的條件</span><span class="sxs-lookup"><span data-stu-id="9dd79-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="9dd79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd79-116">-DefaultProfile</span></span>
<span data-ttu-id="9dd79-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dd79-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd79-118">-已啟用</span><span class="sxs-lookup"><span data-stu-id="9dd79-118">-Enabled</span></span>
<span data-ttu-id="9dd79-119">啟用路由</span><span class="sxs-lookup"><span data-stu-id="9dd79-119">Enable route</span></span>

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

### <span data-ttu-id="9dd79-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9dd79-120">-EndpointName</span></span>
<span data-ttu-id="9dd79-121">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="9dd79-121">Name of the routing endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd79-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dd79-122">-InputObject</span></span>
<span data-ttu-id="9dd79-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="9dd79-123">IotHub Object</span></span>

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

### <span data-ttu-id="9dd79-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9dd79-124">-Name</span></span>
<span data-ttu-id="9dd79-125">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="9dd79-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9dd79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd79-126">-ResourceGroupName</span></span>
<span data-ttu-id="9dd79-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="9dd79-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9dd79-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd79-128">-ResourceId</span></span>
<span data-ttu-id="9dd79-129">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9dd79-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9dd79-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="9dd79-130">-RouteName</span></span>
<span data-ttu-id="9dd79-131">路線名稱</span><span class="sxs-lookup"><span data-stu-id="9dd79-131">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd79-132">-來源</span><span class="sxs-lookup"><span data-stu-id="9dd79-132">-Source</span></span>
<span data-ttu-id="9dd79-133">路由的來源</span><span class="sxs-lookup"><span data-stu-id="9dd79-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd79-134">-確認</span><span class="sxs-lookup"><span data-stu-id="9dd79-134">-Confirm</span></span>
<span data-ttu-id="9dd79-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9dd79-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd79-136">-WhatIf</span></span>
<span data-ttu-id="9dd79-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9dd79-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd79-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dd79-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd79-139">CommonParameters</span></span>
<span data-ttu-id="9dd79-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9dd79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd79-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9dd79-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd79-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9dd79-142">INPUTS</span></span>

### <span data-ttu-id="9dd79-143">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9dd79-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9dd79-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9dd79-144">System.String</span></span>

## <span data-ttu-id="9dd79-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9dd79-145">OUTPUTS</span></span>

### <span data-ttu-id="9dd79-146">Microsoft.Azure.Commands.management.IotHub.models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="9dd79-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="9dd79-147">筆記</span><span class="sxs-lookup"><span data-stu-id="9dd79-147">NOTES</span></span>

## <span data-ttu-id="9dd79-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dd79-148">RELATED LINKS</span></span>
