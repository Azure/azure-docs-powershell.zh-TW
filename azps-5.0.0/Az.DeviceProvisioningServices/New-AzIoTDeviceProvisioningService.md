---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136955"
---
# <span data-ttu-id="7155e-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="7155e-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="7155e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7155e-102">SYNOPSIS</span></span>
<span data-ttu-id="7155e-103">建立 Azure IoT 中樞裝置置備服務。</span><span class="sxs-lookup"><span data-stu-id="7155e-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7155e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7155e-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7155e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7155e-105">DESCRIPTION</span></span>
<span data-ttu-id="7155e-106">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="7155e-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7155e-107">示例</span><span class="sxs-lookup"><span data-stu-id="7155e-107">EXAMPLES</span></span>

### <span data-ttu-id="7155e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7155e-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="7155e-109">在資源群組的地區，使用標準定價層 S1 建立 Azure IoT 中樞裝置置備服務。</span><span class="sxs-lookup"><span data-stu-id="7155e-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="7155e-110">範例2</span><span class="sxs-lookup"><span data-stu-id="7155e-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="7155e-111">在 "eastus" 區域中，使用標準定價層 S1 建立 Azure IoT 中樞裝置置備服務。</span><span class="sxs-lookup"><span data-stu-id="7155e-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="7155e-112">參數</span><span class="sxs-lookup"><span data-stu-id="7155e-112">PARAMETERS</span></span>

### <span data-ttu-id="7155e-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7155e-113">-AllocationPolicy</span></span>
<span data-ttu-id="7155e-114">IoT 裝置置備服務分配原則</span><span class="sxs-lookup"><span data-stu-id="7155e-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7155e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7155e-115">-DefaultProfile</span></span>
<span data-ttu-id="7155e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7155e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7155e-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7155e-117">-Location</span></span>
<span data-ttu-id="7155e-118">位於</span><span class="sxs-lookup"><span data-stu-id="7155e-118">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7155e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7155e-119">-Name</span></span>
<span data-ttu-id="7155e-120">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="7155e-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7155e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7155e-121">-ResourceGroupName</span></span>
<span data-ttu-id="7155e-122">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7155e-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7155e-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7155e-123">-SkuName</span></span>
<span data-ttu-id="7155e-124">Sku</span><span class="sxs-lookup"><span data-stu-id="7155e-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7155e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="7155e-125">-Confirm</span></span>
<span data-ttu-id="7155e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7155e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7155e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7155e-127">-WhatIf</span></span>
<span data-ttu-id="7155e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7155e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7155e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7155e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7155e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7155e-130">CommonParameters</span></span>
<span data-ttu-id="7155e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7155e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7155e-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7155e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7155e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7155e-133">INPUTS</span></span>

### <span data-ttu-id="7155e-134">所有</span><span class="sxs-lookup"><span data-stu-id="7155e-134">None</span></span>

## <span data-ttu-id="7155e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7155e-135">OUTPUTS</span></span>

### <span data-ttu-id="7155e-136">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="7155e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="7155e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7155e-137">NOTES</span></span>

## <span data-ttu-id="7155e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7155e-138">RELATED LINKS</span></span>
