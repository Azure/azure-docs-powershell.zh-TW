---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 2cac00b1510c658b01d815d281ef16cef02b1dc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915481"
---
# <span data-ttu-id="3b4b7-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3b4b7-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="3b4b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4b7-103">更新 IoT 中心中的路由</span><span class="sxs-lookup"><span data-stu-id="3b4b7-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="3b4b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b4b7-104">SYNTAX</span></span>

### <span data-ttu-id="3b4b7-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b4b7-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b4b7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3b4b7-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b4b7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3b4b7-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b4b7-108">描述</span><span class="sxs-lookup"><span data-stu-id="3b4b7-108">DESCRIPTION</span></span>
<span data-ttu-id="3b4b7-109">編輯路由。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-109">Edit a route.</span></span> <span data-ttu-id="3b4b7-110">您可以更新路由中所有欄位，包括資料來源、端點、路由查詢，也可以啟用或停用路由。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="3b4b7-111">例子</span><span class="sxs-lookup"><span data-stu-id="3b4b7-111">EXAMPLES</span></span>

### <span data-ttu-id="3b4b7-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="3b4b7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="3b4b7-113">更新路由資訊。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-113">Updating the route information.</span></span>

### <span data-ttu-id="3b4b7-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="3b4b7-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="3b4b7-115">更新路由資訊。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-115">Updating the route information.</span></span>

### <span data-ttu-id="3b4b7-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="3b4b7-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="3b4b7-117">更新路由資訊。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-117">Updating the route information.</span></span>

## <span data-ttu-id="3b4b7-118">參數</span><span class="sxs-lookup"><span data-stu-id="3b4b7-118">PARAMETERS</span></span>

### <span data-ttu-id="3b4b7-119">-條件</span><span class="sxs-lookup"><span data-stu-id="3b4b7-119">-Condition</span></span>
<span data-ttu-id="3b4b7-120">評估為適用路由規則的條件</span><span class="sxs-lookup"><span data-stu-id="3b4b7-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="3b4b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4b7-121">-DefaultProfile</span></span>
<span data-ttu-id="3b4b7-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b4b7-123">-已啟用</span><span class="sxs-lookup"><span data-stu-id="3b4b7-123">-Enabled</span></span>
<span data-ttu-id="3b4b7-124">啟用路由</span><span class="sxs-lookup"><span data-stu-id="3b4b7-124">Enable route</span></span>

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

### <span data-ttu-id="3b4b7-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3b4b7-125">-EndpointName</span></span>
<span data-ttu-id="3b4b7-126">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="3b4b7-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="3b4b7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b4b7-127">-InputObject</span></span>
<span data-ttu-id="3b4b7-128">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="3b4b7-128">IotHub Object</span></span>

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

### <span data-ttu-id="3b4b7-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b4b7-129">-Name</span></span>
<span data-ttu-id="3b4b7-130">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="3b4b7-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3b4b7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4b7-131">-ResourceGroupName</span></span>
<span data-ttu-id="3b4b7-132">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="3b4b7-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3b4b7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b4b7-133">-ResourceId</span></span>
<span data-ttu-id="3b4b7-134">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3b4b7-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3b4b7-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3b4b7-135">-RouteName</span></span>
<span data-ttu-id="3b4b7-136">路線名稱</span><span class="sxs-lookup"><span data-stu-id="3b4b7-136">Name of the Route</span></span>

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

### <span data-ttu-id="3b4b7-137">-來源</span><span class="sxs-lookup"><span data-stu-id="3b4b7-137">-Source</span></span>
<span data-ttu-id="3b4b7-138">路由的來源</span><span class="sxs-lookup"><span data-stu-id="3b4b7-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4b7-139">-確認</span><span class="sxs-lookup"><span data-stu-id="3b4b7-139">-Confirm</span></span>
<span data-ttu-id="3b4b7-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b4b7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b4b7-141">-WhatIf</span></span>
<span data-ttu-id="3b4b7-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b4b7-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b4b7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4b7-144">CommonParameters</span></span>
<span data-ttu-id="3b4b7-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4b7-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4b7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3b4b7-147">INPUTS</span></span>

### <span data-ttu-id="3b4b7-148">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3b4b7-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3b4b7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3b4b7-149">System.String</span></span>

## <span data-ttu-id="3b4b7-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3b4b7-150">OUTPUTS</span></span>

### <span data-ttu-id="3b4b7-151">Microsoft.Azure.Commands.management.IotHub.models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="3b4b7-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="3b4b7-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3b4b7-152">NOTES</span></span>

## <span data-ttu-id="3b4b7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b4b7-153">RELATED LINKS</span></span>
