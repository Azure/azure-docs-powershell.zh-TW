---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957853"
---
# <span data-ttu-id="b49bc-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="b49bc-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="b49bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b49bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b49bc-103">刪除 Azure IoT 中樞裝置置備服務。</span><span class="sxs-lookup"><span data-stu-id="b49bc-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b49bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b49bc-104">SYNTAX</span></span>

### <span data-ttu-id="b49bc-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b49bc-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49bc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b49bc-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49bc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b49bc-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b49bc-108">說明</span><span class="sxs-lookup"><span data-stu-id="b49bc-108">DESCRIPTION</span></span>
<span data-ttu-id="b49bc-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="b49bc-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b49bc-110">示例</span><span class="sxs-lookup"><span data-stu-id="b49bc-110">EXAMPLES</span></span>

### <span data-ttu-id="b49bc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b49bc-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="b49bc-112">刪除 Azure IoT 中樞裝置預配服務 ' myiotdps」。</span><span class="sxs-lookup"><span data-stu-id="b49bc-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="b49bc-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b49bc-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="b49bc-114">使用管線刪除 Azure IoT 中樞裝置預配服務 ' myiotdps」。</span><span class="sxs-lookup"><span data-stu-id="b49bc-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="b49bc-115">參數</span><span class="sxs-lookup"><span data-stu-id="b49bc-115">PARAMETERS</span></span>

### <span data-ttu-id="b49bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49bc-116">-DefaultProfile</span></span>
<span data-ttu-id="b49bc-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b49bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b49bc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b49bc-118">-InputObject</span></span>
<span data-ttu-id="b49bc-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="b49bc-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b49bc-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b49bc-120">-Name</span></span>
<span data-ttu-id="b49bc-121">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="b49bc-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b49bc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b49bc-122">-PassThru</span></span>
<span data-ttu-id="b49bc-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="b49bc-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b49bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="b49bc-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b49bc-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b49bc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b49bc-126">-ResourceId</span></span>
<span data-ttu-id="b49bc-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b49bc-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b49bc-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b49bc-128">-Confirm</span></span>
<span data-ttu-id="b49bc-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b49bc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b49bc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49bc-130">-WhatIf</span></span>
<span data-ttu-id="b49bc-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b49bc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b49bc-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b49bc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b49bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49bc-133">CommonParameters</span></span>
<span data-ttu-id="b49bc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b49bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49bc-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b49bc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49bc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b49bc-136">INPUTS</span></span>

### <span data-ttu-id="b49bc-137">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="b49bc-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b49bc-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b49bc-138">System.String</span></span>

## <span data-ttu-id="b49bc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b49bc-139">OUTPUTS</span></span>

### <span data-ttu-id="b49bc-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b49bc-140">System.Boolean</span></span>

## <span data-ttu-id="b49bc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b49bc-141">NOTES</span></span>

## <span data-ttu-id="b49bc-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b49bc-142">RELATED LINKS</span></span>
