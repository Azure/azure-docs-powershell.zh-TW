---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278676"
---
# <span data-ttu-id="16b61-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="16b61-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="16b61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16b61-102">SYNOPSIS</span></span>
<span data-ttu-id="16b61-103">在 Azure IoT 中樞裝置提供服務中刪除連結的 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="16b61-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="16b61-104">句法</span><span class="sxs-lookup"><span data-stu-id="16b61-104">SYNTAX</span></span>

### <span data-ttu-id="16b61-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="16b61-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16b61-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16b61-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b61-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16b61-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16b61-108">說明</span><span class="sxs-lookup"><span data-stu-id="16b61-108">DESCRIPTION</span></span>
<span data-ttu-id="16b61-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="16b61-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="16b61-110">示例</span><span class="sxs-lookup"><span data-stu-id="16b61-110">EXAMPLES</span></span>

### <span data-ttu-id="16b61-111">範例1</span><span class="sxs-lookup"><span data-stu-id="16b61-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="16b61-112">在 Azure IoT Hub 裝置提供服務中刪除連結的 IoT hub "myiothub"。</span><span class="sxs-lookup"><span data-stu-id="16b61-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="16b61-113">範例2</span><span class="sxs-lookup"><span data-stu-id="16b61-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="16b61-114">使用管道在 Azure IoT 中樞裝置中刪除連結的 IoT hub "myiothub"。</span><span class="sxs-lookup"><span data-stu-id="16b61-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="16b61-115">參數</span><span class="sxs-lookup"><span data-stu-id="16b61-115">PARAMETERS</span></span>

### <span data-ttu-id="16b61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b61-116">-DefaultProfile</span></span>
<span data-ttu-id="16b61-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16b61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b61-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16b61-118">-InputObject</span></span>
<span data-ttu-id="16b61-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="16b61-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="16b61-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="16b61-120">-LinkedHubName</span></span>
<span data-ttu-id="16b61-121">連結 IoT 中樞的主機名稱</span><span class="sxs-lookup"><span data-stu-id="16b61-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="16b61-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="16b61-122">-Name</span></span>
<span data-ttu-id="16b61-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="16b61-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="16b61-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16b61-124">-PassThru</span></span>
<span data-ttu-id="16b61-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="16b61-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="16b61-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b61-126">-ResourceGroupName</span></span>
<span data-ttu-id="16b61-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="16b61-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16b61-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16b61-128">-ResourceId</span></span>
<span data-ttu-id="16b61-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="16b61-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="16b61-130">-確認</span><span class="sxs-lookup"><span data-stu-id="16b61-130">-Confirm</span></span>
<span data-ttu-id="16b61-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16b61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b61-132">-WhatIf</span></span>
<span data-ttu-id="16b61-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16b61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b61-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16b61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b61-135">CommonParameters</span></span>
<span data-ttu-id="16b61-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16b61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b61-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16b61-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b61-138">輸入</span><span class="sxs-lookup"><span data-stu-id="16b61-138">INPUTS</span></span>

### <span data-ttu-id="16b61-139">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="16b61-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="16b61-140">System.object</span><span class="sxs-lookup"><span data-stu-id="16b61-140">System.String</span></span>

## <span data-ttu-id="16b61-141">輸出</span><span class="sxs-lookup"><span data-stu-id="16b61-141">OUTPUTS</span></span>

### <span data-ttu-id="16b61-142">System.object</span><span class="sxs-lookup"><span data-stu-id="16b61-142">System.Boolean</span></span>

## <span data-ttu-id="16b61-143">筆記</span><span class="sxs-lookup"><span data-stu-id="16b61-143">NOTES</span></span>

## <span data-ttu-id="16b61-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="16b61-144">RELATED LINKS</span></span>
