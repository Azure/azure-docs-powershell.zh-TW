---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 4065e44d9ec0ed2512438356231176a1de10e7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910210"
---
# <span data-ttu-id="4ca2f-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="4ca2f-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="4ca2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ca2f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca2f-103">更新 Azure IoT Hub 裝置設置服務中的連結 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4ca2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ca2f-104">SYNTAX</span></span>

### <span data-ttu-id="4ca2f-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4ca2f-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca2f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ca2f-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca2f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ca2f-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca2f-108">描述</span><span class="sxs-lookup"><span data-stu-id="4ca2f-108">DESCRIPTION</span></span>
<span data-ttu-id="4ca2f-109">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4ca2f-110">例子</span><span class="sxs-lookup"><span data-stu-id="4ca2f-110">EXAMPLES</span></span>

### <span data-ttu-id="4ca2f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4ca2f-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="4ca2f-112">在 Azure IoT 中心裝置布myiothub.azure-devices.net服務中更新連結的 IoT 中樞 「myiothub.azure-devices.net」。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4ca2f-113">參數</span><span class="sxs-lookup"><span data-stu-id="4ca2f-113">PARAMETERS</span></span>

### <span data-ttu-id="4ca2f-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="4ca2f-114">-AllocationWeight</span></span>
<span data-ttu-id="4ca2f-115">IoT 中樞的分配權重</span><span class="sxs-lookup"><span data-stu-id="4ca2f-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="4ca2f-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca2f-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="4ca2f-117">將配置原則適用于 IoT 中心</span><span class="sxs-lookup"><span data-stu-id="4ca2f-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="4ca2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca2f-118">-DefaultProfile</span></span>
<span data-ttu-id="4ca2f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca2f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ca2f-120">-InputObject</span></span>
<span data-ttu-id="4ca2f-121">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="4ca2f-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca2f-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="4ca2f-122">-LinkedHubName</span></span>
<span data-ttu-id="4ca2f-123">連結 IoT 中樞的主機名稱稱</span><span class="sxs-lookup"><span data-stu-id="4ca2f-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca2f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ca2f-124">-Name</span></span>
<span data-ttu-id="4ca2f-125">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="4ca2f-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4ca2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ca2f-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="4ca2f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ca2f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca2f-128">-ResourceId</span></span>
<span data-ttu-id="4ca2f-129">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4ca2f-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4ca2f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="4ca2f-130">-Confirm</span></span>
<span data-ttu-id="4ca2f-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca2f-132">-WhatIf</span></span>
<span data-ttu-id="4ca2f-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca2f-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca2f-135">CommonParameters</span></span>
<span data-ttu-id="4ca2f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca2f-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4ca2f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca2f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4ca2f-138">INPUTS</span></span>

### <span data-ttu-id="4ca2f-139">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="4ca2f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="4ca2f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4ca2f-140">System.String</span></span>

## <span data-ttu-id="4ca2f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4ca2f-141">OUTPUTS</span></span>

### <span data-ttu-id="4ca2f-142">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="4ca2f-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="4ca2f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4ca2f-143">NOTES</span></span>

## <span data-ttu-id="4ca2f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ca2f-144">RELATED LINKS</span></span>
