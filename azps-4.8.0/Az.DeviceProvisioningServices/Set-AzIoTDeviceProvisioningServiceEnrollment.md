---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129553"
---
# <span data-ttu-id="5816a-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="5816a-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="5816a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5816a-102">SYNOPSIS</span></span>
<span data-ttu-id="5816a-103">更新裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="5816a-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="5816a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5816a-104">SYNTAX</span></span>

### <span data-ttu-id="5816a-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5816a-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5816a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5816a-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5816a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5816a-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5816a-108">說明</span><span class="sxs-lookup"><span data-stu-id="5816a-108">DESCRIPTION</span></span>
<span data-ttu-id="5816a-109">更新 Azure IoT 中樞裝置置備服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="5816a-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5816a-110">示例</span><span class="sxs-lookup"><span data-stu-id="5816a-110">EXAMPLES</span></span>

### <span data-ttu-id="5816a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5816a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="5816a-112">針對登記記錄更新分派原則與中樞。</span><span class="sxs-lookup"><span data-stu-id="5816a-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="5816a-113">參數</span><span class="sxs-lookup"><span data-stu-id="5816a-113">PARAMETERS</span></span>

### <span data-ttu-id="5816a-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5816a-114">-AllocationPolicy</span></span>
<span data-ttu-id="5816a-115">指派給中樞之裝置的配置類型。</span><span class="sxs-lookup"><span data-stu-id="5816a-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="5816a-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5816a-116">-ApiVersion</span></span>
<span data-ttu-id="5816a-117">自訂配置要求中的 [提供服務] API 版本。</span><span class="sxs-lookup"><span data-stu-id="5816a-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="5816a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5816a-118">-DefaultProfile</span></span>
<span data-ttu-id="5816a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5816a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5816a-120">-所需</span><span class="sxs-lookup"><span data-stu-id="5816a-120">-Desired</span></span>
<span data-ttu-id="5816a-121">初始的想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="5816a-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="5816a-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5816a-122">-DeviceId</span></span>
<span data-ttu-id="5816a-123">IoT 中樞裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5816a-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="5816a-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="5816a-124">-DpsName</span></span>
<span data-ttu-id="5816a-125">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="5816a-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5816a-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5816a-126">-DpsObject</span></span>
<span data-ttu-id="5816a-127">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="5816a-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5816a-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5816a-128">-EdgeEnabled</span></span>
<span data-ttu-id="5816a-129">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="5816a-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="5816a-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="5816a-130">-IotHub</span></span>
<span data-ttu-id="5816a-131">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5816a-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="5816a-132">使用以空格分隔的清單來進行多個 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="5816a-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="5816a-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="5816a-133">-IotHubHostName</span></span>
<span data-ttu-id="5816a-134">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5816a-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="5816a-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="5816a-135">-ProvisioningStatus</span></span>
<span data-ttu-id="5816a-136">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="5816a-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="5816a-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="5816a-137">-RegistrationId</span></span>
<span data-ttu-id="5816a-138">個人登記登記 id。</span><span class="sxs-lookup"><span data-stu-id="5816a-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="5816a-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="5816a-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="5816a-140">重新調配至不同的 Iot 中樞時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="5816a-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="5816a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5816a-141">-ResourceGroupName</span></span>
<span data-ttu-id="5816a-142">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="5816a-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5816a-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5816a-143">-ResourceId</span></span>
<span data-ttu-id="5816a-144">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5816a-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5816a-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="5816a-145">-Tag</span></span>
<span data-ttu-id="5816a-146">初始的雙子標記。</span><span class="sxs-lookup"><span data-stu-id="5816a-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="5816a-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="5816a-147">-WebhookUrl</span></span>
<span data-ttu-id="5816a-148">用於自訂配置要求的 webhook URL。</span><span class="sxs-lookup"><span data-stu-id="5816a-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="5816a-149">-確認</span><span class="sxs-lookup"><span data-stu-id="5816a-149">-Confirm</span></span>
<span data-ttu-id="5816a-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5816a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5816a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5816a-151">-WhatIf</span></span>
<span data-ttu-id="5816a-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5816a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5816a-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5816a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5816a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5816a-154">CommonParameters</span></span>
<span data-ttu-id="5816a-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5816a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5816a-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5816a-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5816a-157">輸入</span><span class="sxs-lookup"><span data-stu-id="5816a-157">INPUTS</span></span>

### <span data-ttu-id="5816a-158">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="5816a-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5816a-159">System.object</span><span class="sxs-lookup"><span data-stu-id="5816a-159">System.String</span></span>

## <span data-ttu-id="5816a-160">輸出</span><span class="sxs-lookup"><span data-stu-id="5816a-160">OUTPUTS</span></span>

### <span data-ttu-id="5816a-161">PSIndividualEnrollment （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="5816a-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="5816a-162">筆記</span><span class="sxs-lookup"><span data-stu-id="5816a-162">NOTES</span></span>

## <span data-ttu-id="5816a-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="5816a-163">RELATED LINKS</span></span>
