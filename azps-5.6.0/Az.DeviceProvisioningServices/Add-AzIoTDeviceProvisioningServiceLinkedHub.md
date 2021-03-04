---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 8b5a42110c99a4572b411d082879f4f2853bac0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909810"
---
# <span data-ttu-id="007f6-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="007f6-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="007f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="007f6-102">SYNOPSIS</span></span>
<span data-ttu-id="007f6-103">連結 IoT 中樞至 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="007f6-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="007f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="007f6-104">SYNTAX</span></span>

### <span data-ttu-id="007f6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="007f6-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007f6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="007f6-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="007f6-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007f6-108">描述</span><span class="sxs-lookup"><span data-stu-id="007f6-108">DESCRIPTION</span></span>
<span data-ttu-id="007f6-109">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="007f6-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="007f6-110">例子</span><span class="sxs-lookup"><span data-stu-id="007f6-110">EXAMPLES</span></span>

### <span data-ttu-id="007f6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="007f6-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="007f6-112">連結 IoT 中樞至 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="007f6-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="007f6-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="007f6-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="007f6-114">使用 AllocationWeight 和 ApplyAllocationPolicy 將 IoT 中心連結至 Azure IoT 中樞裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="007f6-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="007f6-115">參數</span><span class="sxs-lookup"><span data-stu-id="007f6-115">PARAMETERS</span></span>

### <span data-ttu-id="007f6-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="007f6-116">-AllocationWeight</span></span>
<span data-ttu-id="007f6-117">IoT 中樞的分配權重</span><span class="sxs-lookup"><span data-stu-id="007f6-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="007f6-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="007f6-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="007f6-119">指出是否要將配置原則適用于 IoT 中樞的布林值</span><span class="sxs-lookup"><span data-stu-id="007f6-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="007f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007f6-120">-DefaultProfile</span></span>
<span data-ttu-id="007f6-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="007f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="007f6-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="007f6-122">-DpsObject</span></span>
<span data-ttu-id="007f6-123">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="007f6-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="007f6-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="007f6-124">-IotHubConnectionString</span></span>
<span data-ttu-id="007f6-125">Iot Hub 資源的連接字串。</span><span class="sxs-lookup"><span data-stu-id="007f6-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="007f6-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="007f6-126">-IotHubLocation</span></span>
<span data-ttu-id="007f6-127">Iot Hub 的位置</span><span class="sxs-lookup"><span data-stu-id="007f6-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="007f6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="007f6-128">-Name</span></span>
<span data-ttu-id="007f6-129">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="007f6-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="007f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="007f6-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="007f6-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="007f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="007f6-132">-ResourceId</span></span>
<span data-ttu-id="007f6-133">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="007f6-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="007f6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="007f6-134">-Confirm</span></span>
<span data-ttu-id="007f6-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="007f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="007f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007f6-136">-WhatIf</span></span>
<span data-ttu-id="007f6-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="007f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007f6-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="007f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="007f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007f6-139">CommonParameters</span></span>
<span data-ttu-id="007f6-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="007f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007f6-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="007f6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007f6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="007f6-142">INPUTS</span></span>

### <span data-ttu-id="007f6-143">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="007f6-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="007f6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="007f6-144">System.String</span></span>

## <span data-ttu-id="007f6-145">輸出</span><span class="sxs-lookup"><span data-stu-id="007f6-145">OUTPUTS</span></span>

### <span data-ttu-id="007f6-146">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="007f6-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="007f6-147">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="007f6-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="007f6-148">筆記</span><span class="sxs-lookup"><span data-stu-id="007f6-148">NOTES</span></span>

## <span data-ttu-id="007f6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="007f6-149">RELATED LINKS</span></span>
