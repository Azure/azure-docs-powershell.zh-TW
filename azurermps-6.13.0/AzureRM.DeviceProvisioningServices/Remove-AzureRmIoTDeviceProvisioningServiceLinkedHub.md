---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626105"
---
# <span data-ttu-id="29bce-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="29bce-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="29bce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29bce-102">SYNOPSIS</span></span>
<span data-ttu-id="29bce-103">在 Azure IoT 中樞裝置提供服務中刪除連結的 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="29bce-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29bce-104">句法</span><span class="sxs-lookup"><span data-stu-id="29bce-104">SYNTAX</span></span>

### <span data-ttu-id="29bce-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="29bce-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29bce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29bce-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29bce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29bce-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29bce-108">說明</span><span class="sxs-lookup"><span data-stu-id="29bce-108">DESCRIPTION</span></span>
<span data-ttu-id="29bce-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="29bce-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="29bce-110">示例</span><span class="sxs-lookup"><span data-stu-id="29bce-110">EXAMPLES</span></span>

### <span data-ttu-id="29bce-111">範例1</span><span class="sxs-lookup"><span data-stu-id="29bce-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="29bce-112">在 Azure IoT Hub 裝置提供服務中刪除連結的 IoT hub "myiothub"。</span><span class="sxs-lookup"><span data-stu-id="29bce-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="29bce-113">範例2</span><span class="sxs-lookup"><span data-stu-id="29bce-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="29bce-114">使用管道在 Azure IoT 中樞裝置中刪除連結的 IoT hub "myiothub"。</span><span class="sxs-lookup"><span data-stu-id="29bce-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="29bce-115">參數</span><span class="sxs-lookup"><span data-stu-id="29bce-115">PARAMETERS</span></span>

### <span data-ttu-id="29bce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bce-116">-DefaultProfile</span></span>
<span data-ttu-id="29bce-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29bce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29bce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29bce-118">-InputObject</span></span>
<span data-ttu-id="29bce-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="29bce-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="29bce-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="29bce-120">-LinkedHubName</span></span>
<span data-ttu-id="29bce-121">連結 IoT 中樞的主機名稱</span><span class="sxs-lookup"><span data-stu-id="29bce-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="29bce-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="29bce-122">-Name</span></span>
<span data-ttu-id="29bce-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="29bce-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="29bce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29bce-124">-PassThru</span></span>
<span data-ttu-id="29bce-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="29bce-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29bce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bce-126">-ResourceGroupName</span></span>
<span data-ttu-id="29bce-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="29bce-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29bce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29bce-128">-ResourceId</span></span>
<span data-ttu-id="29bce-129">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="29bce-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="29bce-130">-確認</span><span class="sxs-lookup"><span data-stu-id="29bce-130">-Confirm</span></span>
<span data-ttu-id="29bce-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29bce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bce-132">-WhatIf</span></span>
<span data-ttu-id="29bce-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29bce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bce-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29bce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bce-135">CommonParameters</span></span>
<span data-ttu-id="29bce-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29bce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bce-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29bce-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bce-138">輸入</span><span class="sxs-lookup"><span data-stu-id="29bce-138">INPUTS</span></span>

### <span data-ttu-id="29bce-139">PSIotHubDefinitionDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="29bce-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="29bce-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="29bce-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="29bce-141">System.object</span><span class="sxs-lookup"><span data-stu-id="29bce-141">System.String</span></span>

## <span data-ttu-id="29bce-142">輸出</span><span class="sxs-lookup"><span data-stu-id="29bce-142">OUTPUTS</span></span>

### <span data-ttu-id="29bce-143">System.object</span><span class="sxs-lookup"><span data-stu-id="29bce-143">System.Boolean</span></span>

## <span data-ttu-id="29bce-144">筆記</span><span class="sxs-lookup"><span data-stu-id="29bce-144">NOTES</span></span>

## <span data-ttu-id="29bce-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="29bce-145">RELATED LINKS</span></span>
