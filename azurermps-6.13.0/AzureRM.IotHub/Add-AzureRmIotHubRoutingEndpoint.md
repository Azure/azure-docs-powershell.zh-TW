---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448407"
---
# <span data-ttu-id="c6639-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="c6639-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="c6639-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6639-102">SYNOPSIS</span></span>
<span data-ttu-id="c6639-103">將端點新增到您的 IoT 中樞</span><span class="sxs-lookup"><span data-stu-id="c6639-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6639-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6639-104">SYNTAX</span></span>

### <span data-ttu-id="c6639-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6639-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6639-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6639-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6639-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c6639-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6639-108">說明</span><span class="sxs-lookup"><span data-stu-id="c6639-108">DESCRIPTION</span></span>
<span data-ttu-id="c6639-109">在您的 IoT 中樞中新增端點。</span><span class="sxs-lookup"><span data-stu-id="c6639-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="c6639-110">若要瞭解受支援的端點，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="c6639-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="c6639-111">示例</span><span class="sxs-lookup"><span data-stu-id="c6639-111">EXAMPLES</span></span>

### <span data-ttu-id="c6639-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c6639-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="c6639-113">在 "myiothub" IoT 中樞中，新增類型為 EventHub 的新端點 "E2"。</span><span class="sxs-lookup"><span data-stu-id="c6639-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="c6639-114">範例2</span><span class="sxs-lookup"><span data-stu-id="c6639-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="c6639-115">將類型 AzureStorageContainer 的新端點 "S1" 新增到 "myiothub" IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="c6639-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="c6639-116">參數</span><span class="sxs-lookup"><span data-stu-id="c6639-116">PARAMETERS</span></span>

### <span data-ttu-id="c6639-117">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c6639-117">-ConnectionString</span></span>
<span data-ttu-id="c6639-118">路由端點的連接字串</span><span class="sxs-lookup"><span data-stu-id="c6639-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6639-119">-DefaultProfile</span></span>
<span data-ttu-id="c6639-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6639-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6639-121">-終結點</span><span class="sxs-lookup"><span data-stu-id="c6639-121">-EndpointName</span></span>
<span data-ttu-id="c6639-122">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="c6639-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="c6639-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6639-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="c6639-124">端點 resoure 的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="c6639-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6639-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="c6639-126">端點資源的 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6639-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c6639-127">-EndpointType</span></span>
<span data-ttu-id="c6639-128">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="c6639-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6639-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6639-129">-InputObject</span></span>
<span data-ttu-id="c6639-130">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c6639-130">IotHub Object</span></span>

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

### <span data-ttu-id="c6639-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6639-131">-Name</span></span>
<span data-ttu-id="c6639-132">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="c6639-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c6639-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6639-133">-ResourceGroupName</span></span>
<span data-ttu-id="c6639-134">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c6639-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c6639-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6639-135">-ResourceId</span></span>
<span data-ttu-id="c6639-136">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c6639-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c6639-137">-確認</span><span class="sxs-lookup"><span data-stu-id="c6639-137">-Confirm</span></span>
<span data-ttu-id="c6639-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6639-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6639-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6639-139">-WhatIf</span></span>
<span data-ttu-id="c6639-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6639-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6639-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6639-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6639-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6639-142">CommonParameters</span></span>
<span data-ttu-id="c6639-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6639-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6639-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6639-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6639-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c6639-145">INPUTS</span></span>

### <span data-ttu-id="c6639-146">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c6639-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="c6639-147">System.object</span><span class="sxs-lookup"><span data-stu-id="c6639-147">System.String</span></span>

## <span data-ttu-id="c6639-148">輸出</span><span class="sxs-lookup"><span data-stu-id="c6639-148">OUTPUTS</span></span>

### <span data-ttu-id="c6639-149">PSRoutingEventHubEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c6639-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="c6639-150">PSRoutingServiceBusQueueEndpoint IotHub. IotHub.... IotHub. PSRoutingStorageContainerEndpoint... （）.。</span><span class="sxs-lookup"><span data-stu-id="c6639-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="c6639-151">筆記</span><span class="sxs-lookup"><span data-stu-id="c6639-151">NOTES</span></span>

## <span data-ttu-id="c6639-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6639-152">RELATED LINKS</span></span>
