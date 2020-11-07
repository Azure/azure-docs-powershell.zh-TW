---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625837"
---
# <span data-ttu-id="bf2bd-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf2bd-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="bf2bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="bf2bd-103">在您的 IoT 中心中取得所有端點的相關資訊</span><span class="sxs-lookup"><span data-stu-id="bf2bd-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf2bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf2bd-104">SYNTAX</span></span>

### <span data-ttu-id="bf2bd-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bf2bd-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf2bd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bf2bd-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf2bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bf2bd-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf2bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="bf2bd-108">DESCRIPTION</span></span>
<span data-ttu-id="bf2bd-109">取得端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="bf2bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="bf2bd-110">EXAMPLES</span></span>

### <span data-ttu-id="bf2bd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bf2bd-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="bf2bd-112">從「myiothub」 IoT 中樞取得所有端點。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="bf2bd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="bf2bd-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="bf2bd-114">從「myiothub」 IoT 中樞取得類型為 EventHub 的所有端點。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="bf2bd-115">範例3</span><span class="sxs-lookup"><span data-stu-id="bf2bd-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="bf2bd-116">從「myiothub」 IoT 中樞取得類型為 EventHub 的所有端點。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="bf2bd-117">範例4</span><span class="sxs-lookup"><span data-stu-id="bf2bd-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="bf2bd-118">從「myiothub」 IoT 中樞取得端點資訊。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="bf2bd-119">參數</span><span class="sxs-lookup"><span data-stu-id="bf2bd-119">PARAMETERS</span></span>

### <span data-ttu-id="bf2bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf2bd-120">-DefaultProfile</span></span>
<span data-ttu-id="bf2bd-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf2bd-122">-終結點</span><span class="sxs-lookup"><span data-stu-id="bf2bd-122">-EndpointName</span></span>
<span data-ttu-id="bf2bd-123">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="bf2bd-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="bf2bd-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="bf2bd-124">-EndpointType</span></span>
<span data-ttu-id="bf2bd-125">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="bf2bd-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="bf2bd-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf2bd-126">-InputObject</span></span>
<span data-ttu-id="bf2bd-127">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="bf2bd-127">IotHub Object</span></span>

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

### <span data-ttu-id="bf2bd-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf2bd-128">-Name</span></span>
<span data-ttu-id="bf2bd-129">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="bf2bd-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bf2bd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf2bd-130">-ResourceGroupName</span></span>
<span data-ttu-id="bf2bd-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="bf2bd-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bf2bd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf2bd-132">-ResourceId</span></span>
<span data-ttu-id="bf2bd-133">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bf2bd-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bf2bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf2bd-134">CommonParameters</span></span>
<span data-ttu-id="bf2bd-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf2bd-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf2bd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bf2bd-137">INPUTS</span></span>

### <span data-ttu-id="bf2bd-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="bf2bd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bf2bd-139">System.String</span></span>

## <span data-ttu-id="bf2bd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bf2bd-140">OUTPUTS</span></span>

### <span data-ttu-id="bf2bd-141">PSRoutingEventHubEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bf2bd-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="bf2bd-142">[System.object]. 清單 `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [IotHub. PSRoutingServiceBusQueueEndpointProperties，IotHub，版本 = 3.1.3.0，Culture = 中性，PublicKeyToken = null]].. List 1 [[]。清單 1 []。 |. 清單 1 []。 | " `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` microsoft Azure. IotHub （PSRoutingStorageContainerProperties） IotHub，版本 = 3.1.3.0，Culture = 中立，PublicKeyToken = null]] System. 集合. 清單 ' 1 []。 IotHub，版本 = PSRoutingCustomEndpoint，Culture = 中性，PublicKeyToken = IotHub，Culture = 中立，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bf2bd-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bf2bd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bf2bd-143">NOTES</span></span>

## <span data-ttu-id="bf2bd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf2bd-144">RELATED LINKS</span></span>
