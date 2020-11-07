---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958284"
---
# <span data-ttu-id="2fc39-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="2fc39-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="2fc39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fc39-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc39-103">在 Azure IoT 中心裝置的 [提供服務] 中更新連結的 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="2fc39-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2fc39-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fc39-104">SYNTAX</span></span>

### <span data-ttu-id="2fc39-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2fc39-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc39-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2fc39-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc39-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2fc39-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc39-108">說明</span><span class="sxs-lookup"><span data-stu-id="2fc39-108">DESCRIPTION</span></span>
<span data-ttu-id="2fc39-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="2fc39-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2fc39-110">示例</span><span class="sxs-lookup"><span data-stu-id="2fc39-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc39-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2fc39-111">Example 1</span></span>
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

<span data-ttu-id="2fc39-112">在 Azure IoT 中樞裝置提供服務中更新連結的 IoT hub "myiothub.azure-devices.net"。</span><span class="sxs-lookup"><span data-stu-id="2fc39-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2fc39-113">參數</span><span class="sxs-lookup"><span data-stu-id="2fc39-113">PARAMETERS</span></span>

### <span data-ttu-id="2fc39-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="2fc39-114">-AllocationWeight</span></span>
<span data-ttu-id="2fc39-115">IoT 中心的配置權重</span><span class="sxs-lookup"><span data-stu-id="2fc39-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="2fc39-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="2fc39-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="2fc39-117">將分攤原則套用到 IoT 中樞</span><span class="sxs-lookup"><span data-stu-id="2fc39-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="2fc39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc39-118">-DefaultProfile</span></span>
<span data-ttu-id="2fc39-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fc39-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc39-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc39-120">-InputObject</span></span>
<span data-ttu-id="2fc39-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="2fc39-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2fc39-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="2fc39-122">-LinkedHubName</span></span>
<span data-ttu-id="2fc39-123">連結 IoT 中樞的主機名稱</span><span class="sxs-lookup"><span data-stu-id="2fc39-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="2fc39-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fc39-124">-Name</span></span>
<span data-ttu-id="2fc39-125">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="2fc39-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2fc39-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc39-126">-ResourceGroupName</span></span>
<span data-ttu-id="2fc39-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2fc39-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2fc39-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc39-128">-ResourceId</span></span>
<span data-ttu-id="2fc39-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2fc39-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2fc39-130">-確認</span><span class="sxs-lookup"><span data-stu-id="2fc39-130">-Confirm</span></span>
<span data-ttu-id="2fc39-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2fc39-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc39-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc39-132">-WhatIf</span></span>
<span data-ttu-id="2fc39-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fc39-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc39-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fc39-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc39-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc39-135">CommonParameters</span></span>
<span data-ttu-id="2fc39-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fc39-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc39-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2fc39-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc39-138">輸入</span><span class="sxs-lookup"><span data-stu-id="2fc39-138">INPUTS</span></span>

### <span data-ttu-id="2fc39-139">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="2fc39-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="2fc39-140">System.object</span><span class="sxs-lookup"><span data-stu-id="2fc39-140">System.String</span></span>

## <span data-ttu-id="2fc39-141">輸出</span><span class="sxs-lookup"><span data-stu-id="2fc39-141">OUTPUTS</span></span>

### <span data-ttu-id="2fc39-142">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="2fc39-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="2fc39-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2fc39-143">NOTES</span></span>

## <span data-ttu-id="2fc39-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fc39-144">RELATED LINKS</span></span>
