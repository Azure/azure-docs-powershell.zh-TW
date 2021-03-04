---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: fc1b8bbe14fb35e7613ac1ed09ecf87624920081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910234"
---
# <span data-ttu-id="f914a-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="f914a-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="f914a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f914a-102">SYNOPSIS</span></span>
<span data-ttu-id="f914a-103">刪除 Azure IoT 中心裝置設置服務中的連結 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="f914a-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="f914a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f914a-104">SYNTAX</span></span>

### <span data-ttu-id="f914a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f914a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f914a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f914a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f914a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f914a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f914a-108">描述</span><span class="sxs-lookup"><span data-stu-id="f914a-108">DESCRIPTION</span></span>
<span data-ttu-id="f914a-109">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="f914a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f914a-110">例子</span><span class="sxs-lookup"><span data-stu-id="f914a-110">EXAMPLES</span></span>

### <span data-ttu-id="f914a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f914a-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="f914a-112">在 Azure IoT 中心裝置布布服務中刪除連結的 IoT 中心"myiothub"。</span><span class="sxs-lookup"><span data-stu-id="f914a-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="f914a-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f914a-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="f914a-114">在 Azure IoT Hub 裝置佈設服務中，使用管線刪除連結的 IoT 中樞"myiothub"。</span><span class="sxs-lookup"><span data-stu-id="f914a-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="f914a-115">參數</span><span class="sxs-lookup"><span data-stu-id="f914a-115">PARAMETERS</span></span>

### <span data-ttu-id="f914a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f914a-116">-DefaultProfile</span></span>
<span data-ttu-id="f914a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f914a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f914a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f914a-118">-InputObject</span></span>
<span data-ttu-id="f914a-119">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="f914a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f914a-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="f914a-120">-LinkedHubName</span></span>
<span data-ttu-id="f914a-121">連結 IoT 中樞的主機名稱稱</span><span class="sxs-lookup"><span data-stu-id="f914a-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="f914a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f914a-122">-Name</span></span>
<span data-ttu-id="f914a-123">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="f914a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f914a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f914a-124">-PassThru</span></span>
<span data-ttu-id="f914a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f914a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f914a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f914a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f914a-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="f914a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f914a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f914a-128">-ResourceId</span></span>
<span data-ttu-id="f914a-129">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f914a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f914a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f914a-130">-Confirm</span></span>
<span data-ttu-id="f914a-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f914a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f914a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f914a-132">-WhatIf</span></span>
<span data-ttu-id="f914a-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f914a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f914a-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f914a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f914a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f914a-135">CommonParameters</span></span>
<span data-ttu-id="f914a-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f914a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f914a-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f914a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f914a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f914a-138">INPUTS</span></span>

### <span data-ttu-id="f914a-139">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="f914a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="f914a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f914a-140">System.String</span></span>

## <span data-ttu-id="f914a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f914a-141">OUTPUTS</span></span>

### <span data-ttu-id="f914a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f914a-142">System.Boolean</span></span>

## <span data-ttu-id="f914a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f914a-143">NOTES</span></span>

## <span data-ttu-id="f914a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f914a-144">RELATED LINKS</span></span>
