---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: f6341a2d9583c9694d153ec7aca3a39726d72439
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787469"
---
# <span data-ttu-id="175de-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="175de-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="175de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="175de-102">SYNOPSIS</span></span>
<span data-ttu-id="175de-103">在 IoT 中心更新路線</span><span class="sxs-lookup"><span data-stu-id="175de-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="175de-104">句法</span><span class="sxs-lookup"><span data-stu-id="175de-104">SYNTAX</span></span>

### <span data-ttu-id="175de-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="175de-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175de-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="175de-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175de-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="175de-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="175de-108">說明</span><span class="sxs-lookup"><span data-stu-id="175de-108">DESCRIPTION</span></span>
<span data-ttu-id="175de-109">編輯路線。</span><span class="sxs-lookup"><span data-stu-id="175de-109">Edit a route.</span></span> <span data-ttu-id="175de-110">您可以更新工藝路線中的所有欄位，包括資料來源、端點、路由查詢，以及啟用或停用路線。</span><span class="sxs-lookup"><span data-stu-id="175de-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="175de-111">示例</span><span class="sxs-lookup"><span data-stu-id="175de-111">EXAMPLES</span></span>

### <span data-ttu-id="175de-112">範例1</span><span class="sxs-lookup"><span data-stu-id="175de-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="175de-113">更新路線資訊。</span><span class="sxs-lookup"><span data-stu-id="175de-113">Updating the route information.</span></span>

### <span data-ttu-id="175de-114">範例2</span><span class="sxs-lookup"><span data-stu-id="175de-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="175de-115">更新路線資訊。</span><span class="sxs-lookup"><span data-stu-id="175de-115">Updating the route information.</span></span>

### <span data-ttu-id="175de-116">範例3</span><span class="sxs-lookup"><span data-stu-id="175de-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="175de-117">更新路線資訊。</span><span class="sxs-lookup"><span data-stu-id="175de-117">Updating the route information.</span></span>

## <span data-ttu-id="175de-118">參數</span><span class="sxs-lookup"><span data-stu-id="175de-118">PARAMETERS</span></span>

### <span data-ttu-id="175de-119">-條件</span><span class="sxs-lookup"><span data-stu-id="175de-119">-Condition</span></span>
<span data-ttu-id="175de-120">評估以套用路由規則的條件</span><span class="sxs-lookup"><span data-stu-id="175de-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="175de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175de-121">-DefaultProfile</span></span>
<span data-ttu-id="175de-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="175de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="175de-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="175de-123">-Enabled</span></span>
<span data-ttu-id="175de-124">啟用路線</span><span class="sxs-lookup"><span data-stu-id="175de-124">Enable route</span></span>

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

### <span data-ttu-id="175de-125">-終結點</span><span class="sxs-lookup"><span data-stu-id="175de-125">-EndpointName</span></span>
<span data-ttu-id="175de-126">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="175de-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="175de-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="175de-127">-InputObject</span></span>
<span data-ttu-id="175de-128">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="175de-128">IotHub Object</span></span>

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

### <span data-ttu-id="175de-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="175de-129">-Name</span></span>
<span data-ttu-id="175de-130">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="175de-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="175de-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="175de-131">-ResourceGroupName</span></span>
<span data-ttu-id="175de-132">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="175de-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="175de-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="175de-133">-ResourceId</span></span>
<span data-ttu-id="175de-134">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="175de-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="175de-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="175de-135">-RouteName</span></span>
<span data-ttu-id="175de-136">路線的名稱</span><span class="sxs-lookup"><span data-stu-id="175de-136">Name of the Route</span></span>

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

### <span data-ttu-id="175de-137">-來源</span><span class="sxs-lookup"><span data-stu-id="175de-137">-Source</span></span>
<span data-ttu-id="175de-138">路線來源</span><span class="sxs-lookup"><span data-stu-id="175de-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175de-139">-確認</span><span class="sxs-lookup"><span data-stu-id="175de-139">-Confirm</span></span>
<span data-ttu-id="175de-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="175de-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="175de-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175de-141">-WhatIf</span></span>
<span data-ttu-id="175de-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="175de-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="175de-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="175de-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="175de-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175de-144">CommonParameters</span></span>
<span data-ttu-id="175de-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="175de-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175de-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="175de-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175de-147">輸入</span><span class="sxs-lookup"><span data-stu-id="175de-147">INPUTS</span></span>

### <span data-ttu-id="175de-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="175de-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="175de-149">System.object</span><span class="sxs-lookup"><span data-stu-id="175de-149">System.String</span></span>

## <span data-ttu-id="175de-150">輸出</span><span class="sxs-lookup"><span data-stu-id="175de-150">OUTPUTS</span></span>

### <span data-ttu-id="175de-151">PSRouteMetadata （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="175de-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="175de-152">筆記</span><span class="sxs-lookup"><span data-stu-id="175de-152">NOTES</span></span>

## <span data-ttu-id="175de-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="175de-153">RELATED LINKS</span></span>
