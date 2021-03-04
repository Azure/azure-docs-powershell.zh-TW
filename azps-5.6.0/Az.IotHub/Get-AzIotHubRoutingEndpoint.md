---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 903c2d3e425ad64cd83072112f8da37f83e980c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905078"
---
# <span data-ttu-id="f09b6-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="f09b6-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="f09b6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f09b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f09b6-103">取得 IoT 中心所有端點的資訊</span><span class="sxs-lookup"><span data-stu-id="f09b6-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="f09b6-104">語法</span><span class="sxs-lookup"><span data-stu-id="f09b6-104">SYNTAX</span></span>

### <span data-ttu-id="f09b6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f09b6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f09b6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f09b6-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f09b6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f09b6-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f09b6-108">描述</span><span class="sxs-lookup"><span data-stu-id="f09b6-108">DESCRIPTION</span></span>
<span data-ttu-id="f09b6-109">取得端點上的資訊。</span><span class="sxs-lookup"><span data-stu-id="f09b6-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="f09b6-110">例子</span><span class="sxs-lookup"><span data-stu-id="f09b6-110">EXAMPLES</span></span>

### <span data-ttu-id="f09b6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f09b6-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="f09b6-112">從「myiothub」IoT 中心取得所有端點。</span><span class="sxs-lookup"><span data-stu-id="f09b6-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f09b6-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f09b6-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="f09b6-114">從「myiothub」IoT 中心取得類型為 EventHub 的所有端點。</span><span class="sxs-lookup"><span data-stu-id="f09b6-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="f09b6-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="f09b6-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="f09b6-116">從「myiothub」IoT 中心取得類型為 EventHub 的所有端點。</span><span class="sxs-lookup"><span data-stu-id="f09b6-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f09b6-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="f09b6-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="f09b6-118">從「myiothub」IoT 中心取得端點資訊。</span><span class="sxs-lookup"><span data-stu-id="f09b6-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="f09b6-119">參數</span><span class="sxs-lookup"><span data-stu-id="f09b6-119">PARAMETERS</span></span>

### <span data-ttu-id="f09b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09b6-120">-DefaultProfile</span></span>
<span data-ttu-id="f09b6-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f09b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f09b6-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f09b6-122">-EndpointName</span></span>
<span data-ttu-id="f09b6-123">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="f09b6-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="f09b6-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f09b6-124">-EndpointType</span></span>
<span data-ttu-id="f09b6-125">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="f09b6-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09b6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f09b6-126">-InputObject</span></span>
<span data-ttu-id="f09b6-127">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="f09b6-127">IotHub Object</span></span>

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

### <span data-ttu-id="f09b6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f09b6-128">-Name</span></span>
<span data-ttu-id="f09b6-129">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="f09b6-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f09b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f09b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="f09b6-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="f09b6-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f09b6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f09b6-132">-ResourceId</span></span>
<span data-ttu-id="f09b6-133">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f09b6-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f09b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09b6-134">CommonParameters</span></span>
<span data-ttu-id="f09b6-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f09b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09b6-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f09b6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09b6-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f09b6-137">INPUTS</span></span>

### <span data-ttu-id="f09b6-138">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f09b6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f09b6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f09b6-139">System.String</span></span>

## <span data-ttu-id="f09b6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f09b6-140">OUTPUTS</span></span>

### <span data-ttu-id="f09b6-141">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="f09b6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="f09b6-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f09b6-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f09b6-143">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="f09b6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="f09b6-144">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="f09b6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="f09b6-145">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="f09b6-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="f09b6-146">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="f09b6-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="f09b6-147">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f09b6-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="f09b6-148">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="f09b6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="f09b6-149">Microsoft.Azure.Commands.management.IotHub.models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="f09b6-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="f09b6-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f09b6-150">NOTES</span></span>

## <span data-ttu-id="f09b6-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f09b6-151">RELATED LINKS</span></span>
