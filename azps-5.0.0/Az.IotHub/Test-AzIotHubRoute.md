---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284715"
---
# <span data-ttu-id="272db-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="272db-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="272db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="272db-102">SYNOPSIS</span></span>
<span data-ttu-id="272db-103">IoT 中樞中的測試路由</span><span class="sxs-lookup"><span data-stu-id="272db-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="272db-104">句法</span><span class="sxs-lookup"><span data-stu-id="272db-104">SYNTAX</span></span>

### <span data-ttu-id="272db-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="272db-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="272db-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="272db-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="272db-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="272db-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="272db-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="272db-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="272db-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="272db-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="272db-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="272db-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="272db-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="272db-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="272db-112">說明</span><span class="sxs-lookup"><span data-stu-id="272db-112">DESCRIPTION</span></span>
<span data-ttu-id="272db-113">測試特定的路線。</span><span class="sxs-lookup"><span data-stu-id="272db-113">Test a specific route.</span></span>

## <span data-ttu-id="272db-114">示例</span><span class="sxs-lookup"><span data-stu-id="272db-114">EXAMPLES</span></span>

### <span data-ttu-id="272db-115">範例1</span><span class="sxs-lookup"><span data-stu-id="272db-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="272db-116">測試來源為 "DeviceMessages" 的所有路由。</span><span class="sxs-lookup"><span data-stu-id="272db-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="272db-117">範例2</span><span class="sxs-lookup"><span data-stu-id="272db-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="272db-118">測試特定的路線。</span><span class="sxs-lookup"><span data-stu-id="272db-118">Test a specific route.</span></span>

### <span data-ttu-id="272db-119">範例3</span><span class="sxs-lookup"><span data-stu-id="272db-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="272db-120">測試特定路線，並顯示失敗原因。</span><span class="sxs-lookup"><span data-stu-id="272db-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="272db-121">參數</span><span class="sxs-lookup"><span data-stu-id="272db-121">PARAMETERS</span></span>

### <span data-ttu-id="272db-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="272db-122">-AppProperty</span></span>
<span data-ttu-id="272db-123">路由訊息的 App 屬性</span><span class="sxs-lookup"><span data-stu-id="272db-123">App properties of the route message</span></span>

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

### <span data-ttu-id="272db-124">-Body</span><span class="sxs-lookup"><span data-stu-id="272db-124">-Body</span></span>
<span data-ttu-id="272db-125">路線訊息的主體</span><span class="sxs-lookup"><span data-stu-id="272db-125">Body of the route message</span></span>

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

### <span data-ttu-id="272db-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272db-126">-DefaultProfile</span></span>
<span data-ttu-id="272db-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="272db-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="272db-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="272db-128">-InputObject</span></span>
<span data-ttu-id="272db-129">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="272db-129">IotHub Object</span></span>

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

### <span data-ttu-id="272db-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="272db-130">-Name</span></span>
<span data-ttu-id="272db-131">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="272db-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="272db-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272db-132">-ResourceGroupName</span></span>
<span data-ttu-id="272db-133">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="272db-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="272db-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="272db-134">-ResourceId</span></span>
<span data-ttu-id="272db-135">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="272db-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="272db-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="272db-136">-RouteName</span></span>
<span data-ttu-id="272db-137">路線的名稱</span><span class="sxs-lookup"><span data-stu-id="272db-137">Name of the Route</span></span>

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

### <span data-ttu-id="272db-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="272db-138">-ShowError</span></span>
<span data-ttu-id="272db-139">顯示詳細的錯誤（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="272db-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="272db-140">-來源</span><span class="sxs-lookup"><span data-stu-id="272db-140">-Source</span></span>
<span data-ttu-id="272db-141">路線來源</span><span class="sxs-lookup"><span data-stu-id="272db-141">Source of the route</span></span>

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

### <span data-ttu-id="272db-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="272db-142">-SystemProperty</span></span>
<span data-ttu-id="272db-143">路由訊息的系統屬性</span><span class="sxs-lookup"><span data-stu-id="272db-143">System properties of the route message</span></span>

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

### <span data-ttu-id="272db-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272db-144">CommonParameters</span></span>
<span data-ttu-id="272db-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="272db-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272db-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="272db-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272db-147">輸入</span><span class="sxs-lookup"><span data-stu-id="272db-147">INPUTS</span></span>

### <span data-ttu-id="272db-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="272db-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="272db-149">System.object</span><span class="sxs-lookup"><span data-stu-id="272db-149">System.String</span></span>

## <span data-ttu-id="272db-150">輸出</span><span class="sxs-lookup"><span data-stu-id="272db-150">OUTPUTS</span></span>

### <span data-ttu-id="272db-151">PSTestRouteResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="272db-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="272db-152">PSRouteCompilationError （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="272db-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="272db-153">PSRouteProperties []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="272db-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="272db-154">筆記</span><span class="sxs-lookup"><span data-stu-id="272db-154">NOTES</span></span>

## <span data-ttu-id="272db-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="272db-155">RELATED LINKS</span></span>
