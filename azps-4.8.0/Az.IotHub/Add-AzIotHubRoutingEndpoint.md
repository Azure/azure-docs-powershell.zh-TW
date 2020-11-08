---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128681"
---
# <span data-ttu-id="65345-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="65345-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="65345-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65345-102">SYNOPSIS</span></span>
<span data-ttu-id="65345-103">將端點新增到您的 IoT 中樞</span><span class="sxs-lookup"><span data-stu-id="65345-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="65345-104">句法</span><span class="sxs-lookup"><span data-stu-id="65345-104">SYNTAX</span></span>

### <span data-ttu-id="65345-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="65345-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65345-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65345-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65345-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="65345-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65345-108">說明</span><span class="sxs-lookup"><span data-stu-id="65345-108">DESCRIPTION</span></span>
<span data-ttu-id="65345-109">在您的 IoT 中樞中新增端點。</span><span class="sxs-lookup"><span data-stu-id="65345-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="65345-110">若要瞭解受支援的端點，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="65345-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="65345-111">示例</span><span class="sxs-lookup"><span data-stu-id="65345-111">EXAMPLES</span></span>

### <span data-ttu-id="65345-112">範例1</span><span class="sxs-lookup"><span data-stu-id="65345-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="65345-113">在 "myiothub" IoT 中樞中，新增類型為 EventHub 的新端點 "E2"。</span><span class="sxs-lookup"><span data-stu-id="65345-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="65345-114">範例2</span><span class="sxs-lookup"><span data-stu-id="65345-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="65345-115">將類型 AzureStorageContainer 的新端點 "S1" 新增到 "myiothub" IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="65345-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="65345-116">參數</span><span class="sxs-lookup"><span data-stu-id="65345-116">PARAMETERS</span></span>

### <span data-ttu-id="65345-117">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="65345-117">-ConnectionString</span></span>
<span data-ttu-id="65345-118">路由端點的連接字串</span><span class="sxs-lookup"><span data-stu-id="65345-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="65345-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65345-119">-DefaultProfile</span></span>
<span data-ttu-id="65345-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65345-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65345-121">-終結點</span><span class="sxs-lookup"><span data-stu-id="65345-121">-EndpointName</span></span>
<span data-ttu-id="65345-122">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="65345-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="65345-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="65345-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="65345-124">端點資源的資源群組</span><span class="sxs-lookup"><span data-stu-id="65345-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="65345-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65345-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="65345-126">端點資源的 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65345-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="65345-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="65345-127">-EndpointType</span></span>
<span data-ttu-id="65345-128">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="65345-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65345-129">-容器</span><span class="sxs-lookup"><span data-stu-id="65345-129">-ContainerName</span></span>
<span data-ttu-id="65345-130">儲存空間容器的名稱</span><span class="sxs-lookup"><span data-stu-id="65345-130">Name of the storage container</span></span>

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

### <span data-ttu-id="65345-131">編碼</span><span class="sxs-lookup"><span data-stu-id="65345-131">-Encoding</span></span>
<span data-ttu-id="65345-132">選取您要用來傳送資料的格式。</span><span class="sxs-lookup"><span data-stu-id="65345-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="65345-133">您可以選取 [JSON] 或 [AVRO]。</span><span class="sxs-lookup"><span data-stu-id="65345-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="65345-134">預設值會設定為 AVRO。</span><span class="sxs-lookup"><span data-stu-id="65345-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65345-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65345-135">-InputObject</span></span>
<span data-ttu-id="65345-136">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="65345-136">IotHub Object</span></span>

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

### <span data-ttu-id="65345-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="65345-137">-Name</span></span>
<span data-ttu-id="65345-138">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="65345-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="65345-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65345-139">-ResourceGroupName</span></span>
<span data-ttu-id="65345-140">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="65345-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="65345-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65345-141">-ResourceId</span></span>
<span data-ttu-id="65345-142">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="65345-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="65345-143">-確認</span><span class="sxs-lookup"><span data-stu-id="65345-143">-Confirm</span></span>
<span data-ttu-id="65345-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65345-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65345-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65345-145">-WhatIf</span></span>
<span data-ttu-id="65345-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65345-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65345-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65345-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65345-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65345-148">CommonParameters</span></span>
<span data-ttu-id="65345-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65345-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65345-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65345-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65345-151">輸入</span><span class="sxs-lookup"><span data-stu-id="65345-151">INPUTS</span></span>

### <span data-ttu-id="65345-152">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="65345-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="65345-153">System.object</span><span class="sxs-lookup"><span data-stu-id="65345-153">System.String</span></span>

## <span data-ttu-id="65345-154">輸出</span><span class="sxs-lookup"><span data-stu-id="65345-154">OUTPUTS</span></span>

### <span data-ttu-id="65345-155">PSRoutingEventHubEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="65345-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="65345-156">PSRoutingServiceBusQueueEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="65345-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="65345-157">PSRoutingServiceBusTopicEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="65345-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="65345-158">PSRoutingStorageContainerEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="65345-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="65345-159">筆記</span><span class="sxs-lookup"><span data-stu-id="65345-159">NOTES</span></span>

## <span data-ttu-id="65345-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="65345-160">RELATED LINKS</span></span>
