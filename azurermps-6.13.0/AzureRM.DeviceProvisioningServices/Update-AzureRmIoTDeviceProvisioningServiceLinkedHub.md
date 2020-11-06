---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b3cd05b286ddfef69228b8aae12e222e5fffd4d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449186"
---
# <span data-ttu-id="d0988-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="d0988-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="d0988-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0988-102">SYNOPSIS</span></span>
<span data-ttu-id="d0988-103">在 Azure IoT 中心裝置的 [提供服務] 中更新連結的 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="d0988-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0988-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0988-104">SYNTAX</span></span>

### <span data-ttu-id="d0988-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d0988-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0988-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0988-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0988-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0988-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0988-108">說明</span><span class="sxs-lookup"><span data-stu-id="d0988-108">DESCRIPTION</span></span>
<span data-ttu-id="d0988-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="d0988-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d0988-110">示例</span><span class="sxs-lookup"><span data-stu-id="d0988-110">EXAMPLES</span></span>

### <span data-ttu-id="d0988-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d0988-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="d0988-112">在 Azure IoT 中樞裝置提供服務中更新連結的 IoT hub "myiothub.azure-devices.net"。</span><span class="sxs-lookup"><span data-stu-id="d0988-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d0988-113">參數</span><span class="sxs-lookup"><span data-stu-id="d0988-113">PARAMETERS</span></span>

### <span data-ttu-id="d0988-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="d0988-114">-AllocationWeight</span></span>
<span data-ttu-id="d0988-115">IoT 中心的配置權重</span><span class="sxs-lookup"><span data-stu-id="d0988-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="d0988-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="d0988-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="d0988-117">將分攤原則套用到 IoT 中樞</span><span class="sxs-lookup"><span data-stu-id="d0988-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="d0988-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0988-118">-DefaultProfile</span></span>
<span data-ttu-id="d0988-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0988-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0988-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0988-120">-InputObject</span></span>
<span data-ttu-id="d0988-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="d0988-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d0988-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="d0988-122">-LinkedHubName</span></span>
<span data-ttu-id="d0988-123">連結 IoT 中樞的主機名稱</span><span class="sxs-lookup"><span data-stu-id="d0988-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="d0988-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0988-124">-Name</span></span>
<span data-ttu-id="d0988-125">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="d0988-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d0988-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0988-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0988-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d0988-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0988-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0988-128">-ResourceId</span></span>
<span data-ttu-id="d0988-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d0988-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d0988-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d0988-130">-Confirm</span></span>
<span data-ttu-id="d0988-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0988-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0988-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0988-132">-WhatIf</span></span>
<span data-ttu-id="d0988-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0988-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0988-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0988-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0988-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0988-135">CommonParameters</span></span>
<span data-ttu-id="d0988-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0988-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0988-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0988-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0988-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d0988-138">INPUTS</span></span>

### <span data-ttu-id="d0988-139">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="d0988-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="d0988-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d0988-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d0988-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d0988-141">System.String</span></span>

## <span data-ttu-id="d0988-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d0988-142">OUTPUTS</span></span>

### <span data-ttu-id="d0988-143">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="d0988-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="d0988-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d0988-144">NOTES</span></span>

## <span data-ttu-id="d0988-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0988-145">RELATED LINKS</span></span>
