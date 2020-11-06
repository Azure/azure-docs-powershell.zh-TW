---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448427"
---
# <span data-ttu-id="7febd-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="7febd-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="7febd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7febd-102">SYNOPSIS</span></span>
<span data-ttu-id="7febd-103">刪除 Azure IoT 中樞裝置置備服務。</span><span class="sxs-lookup"><span data-stu-id="7febd-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7febd-104">句法</span><span class="sxs-lookup"><span data-stu-id="7febd-104">SYNTAX</span></span>

### <span data-ttu-id="7febd-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7febd-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7febd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7febd-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7febd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7febd-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7febd-108">說明</span><span class="sxs-lookup"><span data-stu-id="7febd-108">DESCRIPTION</span></span>
<span data-ttu-id="7febd-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="7febd-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7febd-110">示例</span><span class="sxs-lookup"><span data-stu-id="7febd-110">EXAMPLES</span></span>

### <span data-ttu-id="7febd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7febd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="7febd-112">刪除 Azure IoT 中樞裝置預配服務 ' myiotdps」。</span><span class="sxs-lookup"><span data-stu-id="7febd-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="7febd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7febd-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="7febd-114">使用管線刪除 Azure IoT 中樞裝置預配服務 ' myiotdps」。</span><span class="sxs-lookup"><span data-stu-id="7febd-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="7febd-115">參數</span><span class="sxs-lookup"><span data-stu-id="7febd-115">PARAMETERS</span></span>

### <span data-ttu-id="7febd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7febd-116">-DefaultProfile</span></span>
<span data-ttu-id="7febd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7febd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7febd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7febd-118">-InputObject</span></span>
<span data-ttu-id="7febd-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="7febd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7febd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7febd-120">-Name</span></span>
<span data-ttu-id="7febd-121">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="7febd-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7febd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7febd-122">-PassThru</span></span>
<span data-ttu-id="7febd-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="7febd-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7febd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7febd-124">-ResourceGroupName</span></span>
<span data-ttu-id="7febd-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7febd-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7febd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7febd-126">-ResourceId</span></span>
<span data-ttu-id="7febd-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7febd-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7febd-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7febd-128">-Confirm</span></span>
<span data-ttu-id="7febd-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7febd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7febd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7febd-130">-WhatIf</span></span>
<span data-ttu-id="7febd-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7febd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7febd-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7febd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7febd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7febd-133">CommonParameters</span></span>
<span data-ttu-id="7febd-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7febd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7febd-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7febd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7febd-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7febd-136">INPUTS</span></span>

### <span data-ttu-id="7febd-137">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="7febd-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="7febd-138">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="7febd-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7febd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7febd-139">System.String</span></span>

## <span data-ttu-id="7febd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="7febd-140">OUTPUTS</span></span>

### <span data-ttu-id="7febd-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7febd-141">System.Boolean</span></span>

## <span data-ttu-id="7febd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="7febd-142">NOTES</span></span>

## <span data-ttu-id="7febd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="7febd-143">RELATED LINKS</span></span>
