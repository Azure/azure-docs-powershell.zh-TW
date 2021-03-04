---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: bb6094644b9f2cbd831aa8d64a142d5888a5bcc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917334"
---
# <span data-ttu-id="11394-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="11394-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="11394-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11394-102">SYNOPSIS</span></span>
<span data-ttu-id="11394-103">建立 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="11394-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="11394-104">語法</span><span class="sxs-lookup"><span data-stu-id="11394-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11394-105">描述</span><span class="sxs-lookup"><span data-stu-id="11394-105">DESCRIPTION</span></span>
<span data-ttu-id="11394-106">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="11394-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="11394-107">例子</span><span class="sxs-lookup"><span data-stu-id="11394-107">EXAMPLES</span></span>

### <span data-ttu-id="11394-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="11394-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="11394-109">在資源群組地區建立 Azure IoT Hub 裝置提供服務，並包含標準定價層級 S1 和標記。</span><span class="sxs-lookup"><span data-stu-id="11394-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="11394-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="11394-110">Example 2</span></span>
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

<span data-ttu-id="11394-111">在'eastus'地區，使用標準定價層級 S1 建立 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="11394-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="11394-112">參數</span><span class="sxs-lookup"><span data-stu-id="11394-112">PARAMETERS</span></span>

### <span data-ttu-id="11394-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="11394-113">-AllocationPolicy</span></span>
<span data-ttu-id="11394-114">IoT 裝置提供服務配置政策</span><span class="sxs-lookup"><span data-stu-id="11394-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="11394-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11394-115">-DefaultProfile</span></span>
<span data-ttu-id="11394-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11394-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11394-117">-位置</span><span class="sxs-lookup"><span data-stu-id="11394-117">-Location</span></span>
<span data-ttu-id="11394-118">位置</span><span class="sxs-lookup"><span data-stu-id="11394-118">Location</span></span>

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

### <span data-ttu-id="11394-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="11394-119">-Name</span></span>
<span data-ttu-id="11394-120">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="11394-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="11394-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11394-121">-ResourceGroupName</span></span>
<span data-ttu-id="11394-122">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="11394-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11394-123">-SKUName</span><span class="sxs-lookup"><span data-stu-id="11394-123">-SkuName</span></span>
<span data-ttu-id="11394-124">Sku</span><span class="sxs-lookup"><span data-stu-id="11394-124">Sku</span></span>

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

### <span data-ttu-id="11394-125">-標記</span><span class="sxs-lookup"><span data-stu-id="11394-125">-Tag</span></span>
<span data-ttu-id="11394-126">IoT 裝置提供服務實例標記。</span><span class="sxs-lookup"><span data-stu-id="11394-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="11394-127">以雜湊表形式，以索引鍵值組表示的屬性包。</span><span class="sxs-lookup"><span data-stu-id="11394-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11394-128">-確認</span><span class="sxs-lookup"><span data-stu-id="11394-128">-Confirm</span></span>
<span data-ttu-id="11394-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11394-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11394-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11394-130">-WhatIf</span></span>
<span data-ttu-id="11394-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11394-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11394-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11394-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11394-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11394-133">CommonParameters</span></span>
<span data-ttu-id="11394-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11394-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11394-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11394-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11394-136">輸入</span><span class="sxs-lookup"><span data-stu-id="11394-136">INPUTS</span></span>

### <span data-ttu-id="11394-137">沒有</span><span class="sxs-lookup"><span data-stu-id="11394-137">None</span></span>

## <span data-ttu-id="11394-138">輸出</span><span class="sxs-lookup"><span data-stu-id="11394-138">OUTPUTS</span></span>

### <span data-ttu-id="11394-139">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="11394-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="11394-140">筆記</span><span class="sxs-lookup"><span data-stu-id="11394-140">NOTES</span></span>

## <span data-ttu-id="11394-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="11394-141">RELATED LINKS</span></span>
