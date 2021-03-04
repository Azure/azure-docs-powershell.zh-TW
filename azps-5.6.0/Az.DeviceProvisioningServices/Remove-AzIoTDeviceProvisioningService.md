---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 99df3feae227aff03d49bfd029f34be4bc32d250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906701"
---
# <span data-ttu-id="3dc4c-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3dc4c-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3dc4c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3dc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc4c-103">刪除 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3dc4c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3dc4c-104">SYNTAX</span></span>

### <span data-ttu-id="3dc4c-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3dc4c-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc4c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3dc4c-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc4c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3dc4c-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc4c-108">描述</span><span class="sxs-lookup"><span data-stu-id="3dc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="3dc4c-109">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3dc4c-110">例子</span><span class="sxs-lookup"><span data-stu-id="3dc4c-110">EXAMPLES</span></span>

### <span data-ttu-id="3dc4c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3dc4c-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="3dc4c-112">刪除 Azure IoT Hub 裝置設置服務 "myiotdps"。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="3dc4c-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="3dc4c-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="3dc4c-114">使用管線刪除 Azure IoT Hub 裝置設置服務"myiotdps"。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="3dc4c-115">參數</span><span class="sxs-lookup"><span data-stu-id="3dc4c-115">PARAMETERS</span></span>

### <span data-ttu-id="3dc4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc4c-116">-DefaultProfile</span></span>
<span data-ttu-id="3dc4c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc4c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dc4c-118">-InputObject</span></span>
<span data-ttu-id="3dc4c-119">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="3dc4c-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3dc4c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3dc4c-120">-Name</span></span>
<span data-ttu-id="3dc4c-121">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="3dc4c-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3dc4c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dc4c-122">-PassThru</span></span>
<span data-ttu-id="3dc4c-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3dc4c-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3dc4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="3dc4c-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="3dc4c-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3dc4c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc4c-126">-ResourceId</span></span>
<span data-ttu-id="3dc4c-127">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3dc4c-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3dc4c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="3dc4c-128">-Confirm</span></span>
<span data-ttu-id="3dc4c-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc4c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc4c-130">-WhatIf</span></span>
<span data-ttu-id="3dc4c-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc4c-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc4c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc4c-133">CommonParameters</span></span>
<span data-ttu-id="3dc4c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc4c-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3dc4c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc4c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3dc4c-136">INPUTS</span></span>

### <span data-ttu-id="3dc4c-137">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3dc4c-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3dc4c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3dc4c-138">System.String</span></span>

## <span data-ttu-id="3dc4c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3dc4c-139">OUTPUTS</span></span>

### <span data-ttu-id="3dc4c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3dc4c-140">System.Boolean</span></span>

## <span data-ttu-id="3dc4c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3dc4c-141">NOTES</span></span>

## <span data-ttu-id="3dc4c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dc4c-142">RELATED LINKS</span></span>
