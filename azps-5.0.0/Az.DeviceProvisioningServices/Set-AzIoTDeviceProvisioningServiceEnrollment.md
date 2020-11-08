---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136938"
---
# <span data-ttu-id="6238f-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="6238f-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="6238f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6238f-102">SYNOPSIS</span></span>
<span data-ttu-id="6238f-103">更新裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="6238f-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="6238f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6238f-104">SYNTAX</span></span>

### <span data-ttu-id="6238f-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6238f-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6238f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6238f-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6238f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6238f-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6238f-108">說明</span><span class="sxs-lookup"><span data-stu-id="6238f-108">DESCRIPTION</span></span>
<span data-ttu-id="6238f-109">更新 Azure IoT 中樞裝置置備服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="6238f-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6238f-110">示例</span><span class="sxs-lookup"><span data-stu-id="6238f-110">EXAMPLES</span></span>

### <span data-ttu-id="6238f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6238f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="6238f-112">針對登記記錄更新分派原則與中樞。</span><span class="sxs-lookup"><span data-stu-id="6238f-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="6238f-113">參數</span><span class="sxs-lookup"><span data-stu-id="6238f-113">PARAMETERS</span></span>

### <span data-ttu-id="6238f-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="6238f-114">-AllocationPolicy</span></span>
<span data-ttu-id="6238f-115">指派給中樞之裝置的配置類型。</span><span class="sxs-lookup"><span data-stu-id="6238f-115">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6238f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6238f-116">-ApiVersion</span></span>
<span data-ttu-id="6238f-117">自訂配置要求中的 [提供服務] API 版本。</span><span class="sxs-lookup"><span data-stu-id="6238f-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="6238f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6238f-118">-DefaultProfile</span></span>
<span data-ttu-id="6238f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6238f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6238f-120">-所需</span><span class="sxs-lookup"><span data-stu-id="6238f-120">-Desired</span></span>
<span data-ttu-id="6238f-121">初始的想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="6238f-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="6238f-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6238f-122">-DeviceId</span></span>
<span data-ttu-id="6238f-123">IoT 中樞裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6238f-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="6238f-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6238f-124">-DpsName</span></span>
<span data-ttu-id="6238f-125">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="6238f-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6238f-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6238f-126">-DpsObject</span></span>
<span data-ttu-id="6238f-127">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="6238f-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6238f-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6238f-128">-EdgeEnabled</span></span>
<span data-ttu-id="6238f-129">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="6238f-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6238f-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="6238f-130">-IotHub</span></span>
<span data-ttu-id="6238f-131">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6238f-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="6238f-132">使用以空格分隔的清單來進行多個 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="6238f-132">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6238f-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="6238f-133">-IotHubHostName</span></span>
<span data-ttu-id="6238f-134">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6238f-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="6238f-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="6238f-135">-ProvisioningStatus</span></span>
<span data-ttu-id="6238f-136">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="6238f-136">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6238f-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="6238f-137">-RegistrationId</span></span>
<span data-ttu-id="6238f-138">個人登記登記 id。</span><span class="sxs-lookup"><span data-stu-id="6238f-138">Individual enrollment registration id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6238f-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="6238f-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="6238f-140">重新調配至不同的 Iot 中樞時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="6238f-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6238f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6238f-141">-ResourceGroupName</span></span>
<span data-ttu-id="6238f-142">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6238f-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6238f-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6238f-143">-ResourceId</span></span>
<span data-ttu-id="6238f-144">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6238f-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6238f-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="6238f-145">-Tag</span></span>
<span data-ttu-id="6238f-146">初始的雙子標記。</span><span class="sxs-lookup"><span data-stu-id="6238f-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="6238f-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="6238f-147">-WebhookUrl</span></span>
<span data-ttu-id="6238f-148">用於自訂配置要求的 webhook URL。</span><span class="sxs-lookup"><span data-stu-id="6238f-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="6238f-149">-確認</span><span class="sxs-lookup"><span data-stu-id="6238f-149">-Confirm</span></span>
<span data-ttu-id="6238f-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6238f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6238f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6238f-151">-WhatIf</span></span>
<span data-ttu-id="6238f-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6238f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6238f-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6238f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6238f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6238f-154">CommonParameters</span></span>
<span data-ttu-id="6238f-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6238f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6238f-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6238f-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6238f-157">輸入</span><span class="sxs-lookup"><span data-stu-id="6238f-157">INPUTS</span></span>

### <span data-ttu-id="6238f-158">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="6238f-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6238f-159">System.object</span><span class="sxs-lookup"><span data-stu-id="6238f-159">System.String</span></span>

## <span data-ttu-id="6238f-160">輸出</span><span class="sxs-lookup"><span data-stu-id="6238f-160">OUTPUTS</span></span>

### <span data-ttu-id="6238f-161">PSIndividualEnrollment （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="6238f-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="6238f-162">筆記</span><span class="sxs-lookup"><span data-stu-id="6238f-162">NOTES</span></span>

## <span data-ttu-id="6238f-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="6238f-163">RELATED LINKS</span></span>
