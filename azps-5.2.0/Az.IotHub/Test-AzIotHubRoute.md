---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282022"
---
# <span data-ttu-id="f7899-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="f7899-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="f7899-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7899-102">SYNOPSIS</span></span>
<span data-ttu-id="f7899-103">IoT 中樞中的測試路由</span><span class="sxs-lookup"><span data-stu-id="f7899-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="f7899-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7899-104">SYNTAX</span></span>

### <span data-ttu-id="f7899-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f7899-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7899-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="f7899-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7899-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="f7899-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7899-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="f7899-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7899-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="f7899-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7899-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="f7899-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7899-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="f7899-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7899-112">說明</span><span class="sxs-lookup"><span data-stu-id="f7899-112">DESCRIPTION</span></span>
<span data-ttu-id="f7899-113">測試特定的路線。</span><span class="sxs-lookup"><span data-stu-id="f7899-113">Test a specific route.</span></span>

## <span data-ttu-id="f7899-114">示例</span><span class="sxs-lookup"><span data-stu-id="f7899-114">EXAMPLES</span></span>

### <span data-ttu-id="f7899-115">範例1</span><span class="sxs-lookup"><span data-stu-id="f7899-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="f7899-116">測試來源為 "DeviceMessages" 的所有路由。</span><span class="sxs-lookup"><span data-stu-id="f7899-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="f7899-117">範例2</span><span class="sxs-lookup"><span data-stu-id="f7899-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="f7899-118">測試特定的路線。</span><span class="sxs-lookup"><span data-stu-id="f7899-118">Test a specific route.</span></span>

### <span data-ttu-id="f7899-119">範例3</span><span class="sxs-lookup"><span data-stu-id="f7899-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="f7899-120">測試特定路線，並顯示失敗原因。</span><span class="sxs-lookup"><span data-stu-id="f7899-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="f7899-121">範例4</span><span class="sxs-lookup"><span data-stu-id="f7899-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="f7899-122">使用 AppProperty 和 SystemProperty 測試特定路線。</span><span class="sxs-lookup"><span data-stu-id="f7899-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="f7899-123">參數</span><span class="sxs-lookup"><span data-stu-id="f7899-123">PARAMETERS</span></span>

### <span data-ttu-id="f7899-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="f7899-124">-AppProperty</span></span>
<span data-ttu-id="f7899-125">路由訊息的 App 屬性</span><span class="sxs-lookup"><span data-stu-id="f7899-125">App properties of the route message</span></span>

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

### <span data-ttu-id="f7899-126">-Body</span><span class="sxs-lookup"><span data-stu-id="f7899-126">-Body</span></span>
<span data-ttu-id="f7899-127">路線訊息的主體</span><span class="sxs-lookup"><span data-stu-id="f7899-127">Body of the route message</span></span>

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

### <span data-ttu-id="f7899-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7899-128">-DefaultProfile</span></span>
<span data-ttu-id="f7899-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7899-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7899-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7899-130">-InputObject</span></span>
<span data-ttu-id="f7899-131">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="f7899-131">IotHub Object</span></span>

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

### <span data-ttu-id="f7899-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7899-132">-Name</span></span>
<span data-ttu-id="f7899-133">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="f7899-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f7899-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7899-134">-ResourceGroupName</span></span>
<span data-ttu-id="f7899-135">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f7899-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f7899-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7899-136">-ResourceId</span></span>
<span data-ttu-id="f7899-137">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f7899-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f7899-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="f7899-138">-RouteName</span></span>
<span data-ttu-id="f7899-139">路線的名稱</span><span class="sxs-lookup"><span data-stu-id="f7899-139">Name of the Route</span></span>

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

### <span data-ttu-id="f7899-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="f7899-140">-ShowError</span></span>
<span data-ttu-id="f7899-141">顯示詳細的錯誤（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="f7899-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="f7899-142">-來源</span><span class="sxs-lookup"><span data-stu-id="f7899-142">-Source</span></span>
<span data-ttu-id="f7899-143">路線來源</span><span class="sxs-lookup"><span data-stu-id="f7899-143">Source of the route</span></span>

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

### <span data-ttu-id="f7899-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="f7899-144">-SystemProperty</span></span>
<span data-ttu-id="f7899-145">路由訊息的系統屬性</span><span class="sxs-lookup"><span data-stu-id="f7899-145">System properties of the route message</span></span>

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

### <span data-ttu-id="f7899-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7899-146">CommonParameters</span></span>
<span data-ttu-id="f7899-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7899-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7899-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7899-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7899-149">輸入</span><span class="sxs-lookup"><span data-stu-id="f7899-149">INPUTS</span></span>

### <span data-ttu-id="f7899-150">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="f7899-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f7899-151">System.object</span><span class="sxs-lookup"><span data-stu-id="f7899-151">System.String</span></span>

## <span data-ttu-id="f7899-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f7899-152">OUTPUTS</span></span>

### <span data-ttu-id="f7899-153">PSTestRouteResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="f7899-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="f7899-154">PSRouteCompilationError （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="f7899-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="f7899-155">PSRouteProperties []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="f7899-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="f7899-156">筆記</span><span class="sxs-lookup"><span data-stu-id="f7899-156">NOTES</span></span>

## <span data-ttu-id="f7899-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7899-157">RELATED LINKS</span></span>
