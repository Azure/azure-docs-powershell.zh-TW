---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969739"
---
# <span data-ttu-id="08a17-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="08a17-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="08a17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08a17-102">SYNOPSIS</span></span>
<span data-ttu-id="08a17-103">更新裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="08a17-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="08a17-104">句法</span><span class="sxs-lookup"><span data-stu-id="08a17-104">SYNTAX</span></span>

### <span data-ttu-id="08a17-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="08a17-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08a17-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="08a17-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08a17-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="08a17-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a17-108">說明</span><span class="sxs-lookup"><span data-stu-id="08a17-108">DESCRIPTION</span></span>
<span data-ttu-id="08a17-109">更新 Azure IoT 中樞裝置置備服務中的註冊群組。</span><span class="sxs-lookup"><span data-stu-id="08a17-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="08a17-110">示例</span><span class="sxs-lookup"><span data-stu-id="08a17-110">EXAMPLES</span></span>

### <span data-ttu-id="08a17-111">範例1</span><span class="sxs-lookup"><span data-stu-id="08a17-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="08a17-112">更新登記群組的分配原則與中樞。</span><span class="sxs-lookup"><span data-stu-id="08a17-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="08a17-113">參數</span><span class="sxs-lookup"><span data-stu-id="08a17-113">PARAMETERS</span></span>

### <span data-ttu-id="08a17-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="08a17-114">-AllocationPolicy</span></span>
<span data-ttu-id="08a17-115">指派給中樞之裝置的配置類型。</span><span class="sxs-lookup"><span data-stu-id="08a17-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="08a17-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="08a17-116">-ApiVersion</span></span>
<span data-ttu-id="08a17-117">自訂配置要求中的 [提供服務] API 版本。</span><span class="sxs-lookup"><span data-stu-id="08a17-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="08a17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a17-118">-DefaultProfile</span></span>
<span data-ttu-id="08a17-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08a17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08a17-120">-所需</span><span class="sxs-lookup"><span data-stu-id="08a17-120">-Desired</span></span>
<span data-ttu-id="08a17-121">初始的想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="08a17-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="08a17-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="08a17-122">-DpsName</span></span>
<span data-ttu-id="08a17-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="08a17-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="08a17-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="08a17-124">-DpsObject</span></span>
<span data-ttu-id="08a17-125">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="08a17-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="08a17-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="08a17-126">-EdgeEnabled</span></span>
<span data-ttu-id="08a17-127">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="08a17-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="08a17-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="08a17-128">-IotHub</span></span>
<span data-ttu-id="08a17-129">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="08a17-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="08a17-130">使用以空格分隔的清單來進行多個 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="08a17-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="08a17-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="08a17-131">-IotHubHostName</span></span>
<span data-ttu-id="08a17-132">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="08a17-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="08a17-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="08a17-133">-Name</span></span>
<span data-ttu-id="08a17-134">註冊群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08a17-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="08a17-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="08a17-135">-ProvisioningStatus</span></span>
<span data-ttu-id="08a17-136">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="08a17-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="08a17-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="08a17-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="08a17-138">重新調配至不同的 Iot 中樞時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="08a17-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="08a17-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08a17-139">-ResourceGroupName</span></span>
<span data-ttu-id="08a17-140">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="08a17-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="08a17-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08a17-141">-ResourceId</span></span>
<span data-ttu-id="08a17-142">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="08a17-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="08a17-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="08a17-143">-Tag</span></span>
<span data-ttu-id="08a17-144">初始的雙子標記。</span><span class="sxs-lookup"><span data-stu-id="08a17-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="08a17-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="08a17-145">-WebhookUrl</span></span>
<span data-ttu-id="08a17-146">用於自訂配置要求的 webhook URL。</span><span class="sxs-lookup"><span data-stu-id="08a17-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="08a17-147">-確認</span><span class="sxs-lookup"><span data-stu-id="08a17-147">-Confirm</span></span>
<span data-ttu-id="08a17-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08a17-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a17-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a17-149">-WhatIf</span></span>
<span data-ttu-id="08a17-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08a17-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08a17-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08a17-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a17-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a17-152">CommonParameters</span></span>
<span data-ttu-id="08a17-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08a17-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a17-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08a17-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a17-155">輸入</span><span class="sxs-lookup"><span data-stu-id="08a17-155">INPUTS</span></span>

### <span data-ttu-id="08a17-156">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="08a17-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="08a17-157">System.object</span><span class="sxs-lookup"><span data-stu-id="08a17-157">System.String</span></span>

## <span data-ttu-id="08a17-158">輸出</span><span class="sxs-lookup"><span data-stu-id="08a17-158">OUTPUTS</span></span>

### <span data-ttu-id="08a17-159">PSEnrollmentGroup （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="08a17-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="08a17-160">筆記</span><span class="sxs-lookup"><span data-stu-id="08a17-160">NOTES</span></span>

## <span data-ttu-id="08a17-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="08a17-161">RELATED LINKS</span></span>