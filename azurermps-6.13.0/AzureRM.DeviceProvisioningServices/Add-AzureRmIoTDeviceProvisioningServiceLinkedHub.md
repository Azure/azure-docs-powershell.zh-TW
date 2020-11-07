---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ca32f2d0436ea16d8897f279239ce4de079d1550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624395"
---
# <span data-ttu-id="a4282-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="a4282-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="a4282-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4282-102">SYNOPSIS</span></span>
<span data-ttu-id="a4282-103">連結 IoT 中樞至 Azure IoT 中心裝置的提供服務。</span><span class="sxs-lookup"><span data-stu-id="a4282-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4282-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4282-104">SYNTAX</span></span>

### <span data-ttu-id="a4282-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4282-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4282-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4282-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4282-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4282-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4282-108">說明</span><span class="sxs-lookup"><span data-stu-id="a4282-108">DESCRIPTION</span></span>
<span data-ttu-id="a4282-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="a4282-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a4282-110">示例</span><span class="sxs-lookup"><span data-stu-id="a4282-110">EXAMPLES</span></span>

### <span data-ttu-id="a4282-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a4282-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="a4282-112">連結 IoT 中樞至 Azure IoT 中心裝置的提供服務。</span><span class="sxs-lookup"><span data-stu-id="a4282-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a4282-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a4282-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="a4282-114">連結 IoT 中樞至 Azure IoT 中樞裝置使用 AllocationWeight 和 ApplyAllocationPolicy 的提供服務。</span><span class="sxs-lookup"><span data-stu-id="a4282-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="a4282-115">參數</span><span class="sxs-lookup"><span data-stu-id="a4282-115">PARAMETERS</span></span>

### <span data-ttu-id="a4282-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="a4282-116">-AllocationWeight</span></span>
<span data-ttu-id="a4282-117">IoT 中心的配置權重</span><span class="sxs-lookup"><span data-stu-id="a4282-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4282-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a4282-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="a4282-119">布林值，指出是否要將配置原則套用到 IoT 中樞</span><span class="sxs-lookup"><span data-stu-id="a4282-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="a4282-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4282-120">-DefaultProfile</span></span>
<span data-ttu-id="a4282-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4282-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4282-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a4282-122">-DpsObject</span></span>
<span data-ttu-id="a4282-123">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="a4282-123">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4282-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="a4282-124">-IotHubConnectionString</span></span>
<span data-ttu-id="a4282-125">Iot 中心資源的連線字串。</span><span class="sxs-lookup"><span data-stu-id="a4282-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="a4282-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="a4282-126">-IotHubLocation</span></span>
<span data-ttu-id="a4282-127">Iot 中樞的位置</span><span class="sxs-lookup"><span data-stu-id="a4282-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4282-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4282-128">-Name</span></span>
<span data-ttu-id="a4282-129">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="a4282-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a4282-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4282-130">-ResourceGroupName</span></span>
<span data-ttu-id="a4282-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a4282-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a4282-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4282-132">-ResourceId</span></span>
<span data-ttu-id="a4282-133">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a4282-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a4282-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a4282-134">-Confirm</span></span>
<span data-ttu-id="a4282-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4282-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4282-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4282-136">-WhatIf</span></span>
<span data-ttu-id="a4282-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4282-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4282-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4282-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4282-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4282-139">CommonParameters</span></span>
<span data-ttu-id="a4282-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4282-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4282-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4282-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4282-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a4282-142">INPUTS</span></span>

### <span data-ttu-id="a4282-143">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a4282-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="a4282-144">參數： DpsObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a4282-144">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="a4282-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a4282-145">System.String</span></span>

## <span data-ttu-id="a4282-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a4282-146">OUTPUTS</span></span>

### <span data-ttu-id="a4282-147">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a4282-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="a4282-148">PSIotHubDefinitions （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a4282-148">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="a4282-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a4282-149">NOTES</span></span>

## <span data-ttu-id="a4282-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4282-150">RELATED LINKS</span></span>
