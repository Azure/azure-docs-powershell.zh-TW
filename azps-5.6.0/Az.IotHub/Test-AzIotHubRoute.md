---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 56ac931259de9705e0d6703e1387853aba77b028
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915474"
---
# <span data-ttu-id="354b7-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="354b7-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="354b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="354b7-102">SYNOPSIS</span></span>
<span data-ttu-id="354b7-103">在 IoT 中心測試路由</span><span class="sxs-lookup"><span data-stu-id="354b7-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="354b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="354b7-104">SYNTAX</span></span>

### <span data-ttu-id="354b7-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="354b7-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354b7-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="354b7-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354b7-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="354b7-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="354b7-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="354b7-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354b7-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="354b7-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="354b7-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="354b7-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354b7-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="354b7-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="354b7-112">描述</span><span class="sxs-lookup"><span data-stu-id="354b7-112">DESCRIPTION</span></span>
<span data-ttu-id="354b7-113">測試特定路由。</span><span class="sxs-lookup"><span data-stu-id="354b7-113">Test a specific route.</span></span>

## <span data-ttu-id="354b7-114">例子</span><span class="sxs-lookup"><span data-stu-id="354b7-114">EXAMPLES</span></span>

### <span data-ttu-id="354b7-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="354b7-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="354b7-116">使用來源「DeviceMessages」測試所有路由。</span><span class="sxs-lookup"><span data-stu-id="354b7-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="354b7-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="354b7-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="354b7-118">測試特定路由。</span><span class="sxs-lookup"><span data-stu-id="354b7-118">Test a specific route.</span></span>

### <span data-ttu-id="354b7-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="354b7-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="354b7-120">測試特定路由，並顯示失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="354b7-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="354b7-121">範例 4</span><span class="sxs-lookup"><span data-stu-id="354b7-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="354b7-122">使用 AppProperty 和 SystemProperty 測試特定路由。</span><span class="sxs-lookup"><span data-stu-id="354b7-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="354b7-123">參數</span><span class="sxs-lookup"><span data-stu-id="354b7-123">PARAMETERS</span></span>

### <span data-ttu-id="354b7-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="354b7-124">-AppProperty</span></span>
<span data-ttu-id="354b7-125">路由訊息的應用程式屬性</span><span class="sxs-lookup"><span data-stu-id="354b7-125">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-126">-Body</span><span class="sxs-lookup"><span data-stu-id="354b7-126">-Body</span></span>
<span data-ttu-id="354b7-127">路由訊息的內文</span><span class="sxs-lookup"><span data-stu-id="354b7-127">Body of the route message</span></span>

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

### <span data-ttu-id="354b7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354b7-128">-DefaultProfile</span></span>
<span data-ttu-id="354b7-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="354b7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354b7-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="354b7-130">-InputObject</span></span>
<span data-ttu-id="354b7-131">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="354b7-131">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="354b7-132">-Name</span></span>
<span data-ttu-id="354b7-133">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="354b7-133">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354b7-134">-ResourceGroupName</span></span>
<span data-ttu-id="354b7-135">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="354b7-135">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="354b7-136">-ResourceId</span></span>
<span data-ttu-id="354b7-137">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="354b7-137">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="354b7-138">-RouteName</span></span>
<span data-ttu-id="354b7-139">路線名稱</span><span class="sxs-lookup"><span data-stu-id="354b7-139">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="354b7-140">-ShowError</span></span>
<span data-ttu-id="354b7-141">顯示詳細的錯誤 （如果有）</span><span class="sxs-lookup"><span data-stu-id="354b7-141">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-142">-來源</span><span class="sxs-lookup"><span data-stu-id="354b7-142">-Source</span></span>
<span data-ttu-id="354b7-143">路由的來源</span><span class="sxs-lookup"><span data-stu-id="354b7-143">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="354b7-144">-SystemProperty</span></span>
<span data-ttu-id="354b7-145">路由訊息的系統屬性</span><span class="sxs-lookup"><span data-stu-id="354b7-145">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354b7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354b7-146">CommonParameters</span></span>
<span data-ttu-id="354b7-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="354b7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354b7-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="354b7-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354b7-149">輸入</span><span class="sxs-lookup"><span data-stu-id="354b7-149">INPUTS</span></span>

### <span data-ttu-id="354b7-150">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="354b7-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="354b7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="354b7-151">System.String</span></span>

## <span data-ttu-id="354b7-152">輸出</span><span class="sxs-lookup"><span data-stu-id="354b7-152">OUTPUTS</span></span>

### <span data-ttu-id="354b7-153">Microsoft.Azure.Commands.management.IotHub.models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="354b7-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="354b7-154">Microsoft.Azure.Commands.management.IotHub.models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="354b7-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="354b7-155">Microsoft.Azure.Commands.management.IotHub.models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="354b7-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="354b7-156">筆記</span><span class="sxs-lookup"><span data-stu-id="354b7-156">NOTES</span></span>

## <span data-ttu-id="354b7-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="354b7-157">RELATED LINKS</span></span>
