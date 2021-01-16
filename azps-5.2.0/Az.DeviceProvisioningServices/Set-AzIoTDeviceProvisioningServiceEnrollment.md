---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277983"
---
# <span data-ttu-id="d87a5-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="d87a5-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="d87a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d87a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d87a5-103">更新裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="d87a5-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="d87a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d87a5-104">SYNTAX</span></span>

### <span data-ttu-id="d87a5-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d87a5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d87a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d87a5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d87a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d87a5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87a5-108">說明</span><span class="sxs-lookup"><span data-stu-id="d87a5-108">DESCRIPTION</span></span>
<span data-ttu-id="d87a5-109">更新 Azure IoT 中樞裝置置備服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="d87a5-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d87a5-110">示例</span><span class="sxs-lookup"><span data-stu-id="d87a5-110">EXAMPLES</span></span>

### <span data-ttu-id="d87a5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d87a5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="d87a5-112">針對登記記錄更新分派原則與中樞。</span><span class="sxs-lookup"><span data-stu-id="d87a5-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="d87a5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d87a5-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="d87a5-114">更新登記的初始最雙子狀態。</span><span class="sxs-lookup"><span data-stu-id="d87a5-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="d87a5-115">參數</span><span class="sxs-lookup"><span data-stu-id="d87a5-115">PARAMETERS</span></span>

### <span data-ttu-id="d87a5-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="d87a5-116">-AllocationPolicy</span></span>
<span data-ttu-id="d87a5-117">指派給中樞之裝置的配置類型。</span><span class="sxs-lookup"><span data-stu-id="d87a5-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="d87a5-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d87a5-118">-ApiVersion</span></span>
<span data-ttu-id="d87a5-119">自訂配置要求中的 [提供服務] API 版本。</span><span class="sxs-lookup"><span data-stu-id="d87a5-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="d87a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87a5-120">-DefaultProfile</span></span>
<span data-ttu-id="d87a5-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d87a5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d87a5-122">-所需</span><span class="sxs-lookup"><span data-stu-id="d87a5-122">-Desired</span></span>
<span data-ttu-id="d87a5-123">初始的想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="d87a5-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="d87a5-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d87a5-124">-DeviceId</span></span>
<span data-ttu-id="d87a5-125">IoT 中樞裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d87a5-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="d87a5-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d87a5-126">-DpsName</span></span>
<span data-ttu-id="d87a5-127">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="d87a5-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d87a5-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d87a5-128">-DpsObject</span></span>
<span data-ttu-id="d87a5-129">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="d87a5-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d87a5-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="d87a5-130">-EdgeEnabled</span></span>
<span data-ttu-id="d87a5-131">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="d87a5-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="d87a5-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="d87a5-132">-IotHub</span></span>
<span data-ttu-id="d87a5-133">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d87a5-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="d87a5-134">使用以空格分隔的清單來進行多個 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="d87a5-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="d87a5-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="d87a5-135">-IotHubHostName</span></span>
<span data-ttu-id="d87a5-136">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d87a5-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="d87a5-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="d87a5-137">-ProvisioningStatus</span></span>
<span data-ttu-id="d87a5-138">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="d87a5-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="d87a5-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="d87a5-139">-RegistrationId</span></span>
<span data-ttu-id="d87a5-140">個人登記登記 id。</span><span class="sxs-lookup"><span data-stu-id="d87a5-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="d87a5-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="d87a5-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="d87a5-142">重新調配至不同的 Iot 中樞時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="d87a5-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="d87a5-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87a5-143">-ResourceGroupName</span></span>
<span data-ttu-id="d87a5-144">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d87a5-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d87a5-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d87a5-145">-ResourceId</span></span>
<span data-ttu-id="d87a5-146">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d87a5-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d87a5-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="d87a5-147">-Tag</span></span>
<span data-ttu-id="d87a5-148">初始的雙子標記。</span><span class="sxs-lookup"><span data-stu-id="d87a5-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="d87a5-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="d87a5-149">-WebhookUrl</span></span>
<span data-ttu-id="d87a5-150">用於自訂配置要求的 webhook URL。</span><span class="sxs-lookup"><span data-stu-id="d87a5-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="d87a5-151">-確認</span><span class="sxs-lookup"><span data-stu-id="d87a5-151">-Confirm</span></span>
<span data-ttu-id="d87a5-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d87a5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d87a5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87a5-153">-WhatIf</span></span>
<span data-ttu-id="d87a5-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d87a5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d87a5-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d87a5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d87a5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87a5-156">CommonParameters</span></span>
<span data-ttu-id="d87a5-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d87a5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87a5-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d87a5-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87a5-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d87a5-159">INPUTS</span></span>

### <span data-ttu-id="d87a5-160">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="d87a5-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d87a5-161">System.object</span><span class="sxs-lookup"><span data-stu-id="d87a5-161">System.String</span></span>

## <span data-ttu-id="d87a5-162">輸出</span><span class="sxs-lookup"><span data-stu-id="d87a5-162">OUTPUTS</span></span>

### <span data-ttu-id="d87a5-163">PSIndividualEnrollment （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="d87a5-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="d87a5-164">筆記</span><span class="sxs-lookup"><span data-stu-id="d87a5-164">NOTES</span></span>

## <span data-ttu-id="d87a5-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="d87a5-165">RELATED LINKS</span></span>
