---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7e1181ba837f0d2447a46f051765b0430399b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910214"
---
# <span data-ttu-id="07469-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="07469-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="07469-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07469-102">SYNOPSIS</span></span>
<span data-ttu-id="07469-103">更新 Azure IoT Hub 裝置設置服務。</span><span class="sxs-lookup"><span data-stu-id="07469-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="07469-104">語法</span><span class="sxs-lookup"><span data-stu-id="07469-104">SYNTAX</span></span>

### <span data-ttu-id="07469-105">ResourceUpdateSet (預設) </span><span class="sxs-lookup"><span data-stu-id="07469-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07469-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="07469-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07469-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="07469-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07469-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="07469-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07469-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="07469-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07469-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="07469-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07469-111">描述</span><span class="sxs-lookup"><span data-stu-id="07469-111">DESCRIPTION</span></span>
<span data-ttu-id="07469-112">有關 Azure IoT Hub 裝置設置服務的簡介，請參閱 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="07469-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="07469-113">例子</span><span class="sxs-lookup"><span data-stu-id="07469-113">EXAMPLES</span></span>

### <span data-ttu-id="07469-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="07469-114">Example 1</span></span>
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

<span data-ttu-id="07469-115">將配置策略更新為 Azure IoT Hub 裝置布布服務「myiotdps」的「GeoLatency」。</span><span class="sxs-lookup"><span data-stu-id="07469-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="07469-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="07469-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

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

<span data-ttu-id="07469-117">新增標記至 Azure IoT Hub 裝置布備服務「myiotdps」。</span><span class="sxs-lookup"><span data-stu-id="07469-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="07469-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="07469-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

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

<span data-ttu-id="07469-119">使用管線刪除標記，並新增標記至 Azure IoT Hub 裝置佈設服務「myiotdps」。</span><span class="sxs-lookup"><span data-stu-id="07469-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="07469-120">參數</span><span class="sxs-lookup"><span data-stu-id="07469-120">PARAMETERS</span></span>

### <span data-ttu-id="07469-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="07469-121">-AllocationPolicy</span></span>
<span data-ttu-id="07469-122">IoT 裝置提供服務配置政策</span><span class="sxs-lookup"><span data-stu-id="07469-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="07469-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07469-123">-DefaultProfile</span></span>
<span data-ttu-id="07469-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07469-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07469-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07469-125">-InputObject</span></span>
<span data-ttu-id="07469-126">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="07469-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="07469-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="07469-127">-Name</span></span>
<span data-ttu-id="07469-128">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="07469-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="07469-129">-重設</span><span class="sxs-lookup"><span data-stu-id="07469-129">-Reset</span></span>
<span data-ttu-id="07469-130">重設 IoT 裝置設置服務標記</span><span class="sxs-lookup"><span data-stu-id="07469-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="07469-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07469-131">-ResourceGroupName</span></span>
<span data-ttu-id="07469-132">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="07469-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="07469-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07469-133">-ResourceId</span></span>
<span data-ttu-id="07469-134">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="07469-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="07469-135">-標記</span><span class="sxs-lookup"><span data-stu-id="07469-135">-Tag</span></span>
<span data-ttu-id="07469-136">IoT 裝置提供服務標記集合</span><span class="sxs-lookup"><span data-stu-id="07469-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="07469-137">-確認</span><span class="sxs-lookup"><span data-stu-id="07469-137">-Confirm</span></span>
<span data-ttu-id="07469-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="07469-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07469-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07469-139">-WhatIf</span></span>
<span data-ttu-id="07469-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07469-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07469-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07469-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07469-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07469-142">CommonParameters</span></span>
<span data-ttu-id="07469-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07469-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07469-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="07469-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07469-145">輸入</span><span class="sxs-lookup"><span data-stu-id="07469-145">INPUTS</span></span>

### <span data-ttu-id="07469-146">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="07469-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="07469-147">System.String</span><span class="sxs-lookup"><span data-stu-id="07469-147">System.String</span></span>

## <span data-ttu-id="07469-148">輸出</span><span class="sxs-lookup"><span data-stu-id="07469-148">OUTPUTS</span></span>

### <span data-ttu-id="07469-149">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="07469-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="07469-150">筆記</span><span class="sxs-lookup"><span data-stu-id="07469-150">NOTES</span></span>

## <span data-ttu-id="07469-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="07469-151">RELATED LINKS</span></span>
