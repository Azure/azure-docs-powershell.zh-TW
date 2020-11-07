---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 411d4594c94fe1eb031f60d6abbff35f5060d4e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957844"
---
# <span data-ttu-id="bf288-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="bf288-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="bf288-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf288-102">SYNOPSIS</span></span>
<span data-ttu-id="bf288-103">更新 Azure IoT 中樞裝置置備服務。</span><span class="sxs-lookup"><span data-stu-id="bf288-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="bf288-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf288-104">SYNTAX</span></span>

### <span data-ttu-id="bf288-105">ResourceUpdateSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bf288-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf288-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="bf288-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf288-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="bf288-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf288-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="bf288-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf288-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="bf288-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf288-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="bf288-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf288-111">說明</span><span class="sxs-lookup"><span data-stu-id="bf288-111">DESCRIPTION</span></span>
<span data-ttu-id="bf288-112">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="bf288-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="bf288-113">示例</span><span class="sxs-lookup"><span data-stu-id="bf288-113">EXAMPLES</span></span>

### <span data-ttu-id="bf288-114">範例1</span><span class="sxs-lookup"><span data-stu-id="bf288-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="bf288-115">將 [配置] 原則更新為 [Azure IoT 中心裝置] 的 [GeoLatency] 的 [myiotdps]。</span><span class="sxs-lookup"><span data-stu-id="bf288-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="bf288-116">範例2</span><span class="sxs-lookup"><span data-stu-id="bf288-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="bf288-117">將 " @tags " 新增至 Azure IoT 中樞裝置的標記 [myiotdps]。</span><span class="sxs-lookup"><span data-stu-id="bf288-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="bf288-118">範例3</span><span class="sxs-lookup"><span data-stu-id="bf288-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="bf288-119">刪除標記，並將新 @tags 的 "" 新增至 Azure IoT 中樞裝置的標記，並使用管道進行 [myiotdps]。</span><span class="sxs-lookup"><span data-stu-id="bf288-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="bf288-120">參數</span><span class="sxs-lookup"><span data-stu-id="bf288-120">PARAMETERS</span></span>

### <span data-ttu-id="bf288-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bf288-121">-AllocationPolicy</span></span>
<span data-ttu-id="bf288-122">IoT 裝置置備服務分配原則</span><span class="sxs-lookup"><span data-stu-id="bf288-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf288-123">-DefaultProfile</span></span>
<span data-ttu-id="bf288-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf288-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf288-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf288-125">-InputObject</span></span>
<span data-ttu-id="bf288-126">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="bf288-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf288-127">-Name</span></span>
<span data-ttu-id="bf288-128">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="bf288-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-129">-重設</span><span class="sxs-lookup"><span data-stu-id="bf288-129">-Reset</span></span>
<span data-ttu-id="bf288-130">重設 IoT 裝置預配服務標記</span><span class="sxs-lookup"><span data-stu-id="bf288-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf288-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf288-132">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="bf288-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf288-133">-ResourceId</span></span>
<span data-ttu-id="bf288-134">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bf288-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf288-135">-Tag</span></span>
<span data-ttu-id="bf288-136">IoT 裝置預配服務標記集合</span><span class="sxs-lookup"><span data-stu-id="bf288-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf288-137">-確認</span><span class="sxs-lookup"><span data-stu-id="bf288-137">-Confirm</span></span>
<span data-ttu-id="bf288-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf288-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf288-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf288-139">-WhatIf</span></span>
<span data-ttu-id="bf288-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf288-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf288-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf288-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf288-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf288-142">CommonParameters</span></span>
<span data-ttu-id="bf288-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf288-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf288-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf288-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf288-145">輸入</span><span class="sxs-lookup"><span data-stu-id="bf288-145">INPUTS</span></span>

### <span data-ttu-id="bf288-146">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="bf288-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="bf288-147">System.object</span><span class="sxs-lookup"><span data-stu-id="bf288-147">System.String</span></span>

## <span data-ttu-id="bf288-148">輸出</span><span class="sxs-lookup"><span data-stu-id="bf288-148">OUTPUTS</span></span>

### <span data-ttu-id="bf288-149">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="bf288-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="bf288-150">筆記</span><span class="sxs-lookup"><span data-stu-id="bf288-150">NOTES</span></span>

## <span data-ttu-id="bf288-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf288-151">RELATED LINKS</span></span>
