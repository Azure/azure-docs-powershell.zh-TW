---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910217"
---
# <span data-ttu-id="a4778-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a4778-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="a4778-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a4778-102">SYNOPSIS</span></span>
<span data-ttu-id="a4778-103">更新裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="a4778-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="a4778-104">語法</span><span class="sxs-lookup"><span data-stu-id="a4778-104">SYNTAX</span></span>

### <span data-ttu-id="a4778-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4778-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4778-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4778-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4778-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4778-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4778-108">描述</span><span class="sxs-lookup"><span data-stu-id="a4778-108">DESCRIPTION</span></span>
<span data-ttu-id="a4778-109">更新 Azure IoT Hub 裝置設置服務中的註冊群組。</span><span class="sxs-lookup"><span data-stu-id="a4778-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a4778-110">例子</span><span class="sxs-lookup"><span data-stu-id="a4778-110">EXAMPLES</span></span>

### <span data-ttu-id="a4778-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a4778-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="a4778-112">更新註冊群組的配置策略和中樞。</span><span class="sxs-lookup"><span data-stu-id="a4778-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="a4778-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a4778-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="a4778-114">更新註冊群組的初始啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="a4778-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="a4778-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="a4778-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="a4778-116">更新對稱金鑰註冊群組的主鍵和次要鍵</span><span class="sxs-lookup"><span data-stu-id="a4778-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="a4778-117">參數</span><span class="sxs-lookup"><span data-stu-id="a4778-117">PARAMETERS</span></span>

### <span data-ttu-id="a4778-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a4778-118">-AllocationPolicy</span></span>
<span data-ttu-id="a4778-119">指派給中樞的裝置配置類型。</span><span class="sxs-lookup"><span data-stu-id="a4778-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="a4778-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4778-120">-ApiVersion</span></span>
<span data-ttu-id="a4778-121">自訂配置要求中的資源佈建服務的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a4778-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="a4778-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4778-122">-DefaultProfile</span></span>
<span data-ttu-id="a4778-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4778-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4778-124">-需要</span><span class="sxs-lookup"><span data-stu-id="a4778-124">-Desired</span></span>
<span data-ttu-id="a4778-125">初始預期屬性。</span><span class="sxs-lookup"><span data-stu-id="a4778-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="a4778-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="a4778-126">-DpsName</span></span>
<span data-ttu-id="a4778-127">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="a4778-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a4778-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a4778-128">-DpsObject</span></span>
<span data-ttu-id="a4778-129">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="a4778-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a4778-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="a4778-130">-EdgeEnabled</span></span>
<span data-ttu-id="a4778-131">指出邊緣啟用的標號。</span><span class="sxs-lookup"><span data-stu-id="a4778-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="a4778-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="a4778-132">-IotHub</span></span>
<span data-ttu-id="a4778-133">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="a4778-134">針對多個 IoT 中樞使用空格分隔清單。</span><span class="sxs-lookup"><span data-stu-id="a4778-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="a4778-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="a4778-135">-IotHubHostName</span></span>
<span data-ttu-id="a4778-136">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="a4778-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4778-137">-Name</span></span>
<span data-ttu-id="a4778-138">註冊組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="a4778-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="a4778-139">-PrimaryCAName</span></span>
<span data-ttu-id="a4778-140">主要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="a4778-141">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="a4778-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="a4778-142">-PrimaryCertificate</span></span>
<span data-ttu-id="a4778-143">包含主憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a4778-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="a4778-144">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="a4778-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a4778-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a4778-145">-PrimaryKey</span></span>
<span data-ttu-id="a4778-146">以 base64 格式儲存的主要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a4778-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="a4778-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="a4778-147">-ProvisioningStatus</span></span>
<span data-ttu-id="a4778-148">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="a4778-148">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="a4778-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="a4778-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="a4778-150">重新提供至不同 Iot Hub 時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="a4778-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="a4778-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4778-151">-ResourceGroupName</span></span>
<span data-ttu-id="a4778-152">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="a4778-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a4778-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4778-153">-ResourceId</span></span>
<span data-ttu-id="a4778-154">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a4778-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a4778-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4778-155">-RootCertificate</span></span>
<span data-ttu-id="a4778-156">允許使用根憑證建立 X509attation。</span><span class="sxs-lookup"><span data-stu-id="a4778-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="a4778-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="a4778-157">-SecondaryCAName</span></span>
<span data-ttu-id="a4778-158">次要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="a4778-159">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4778-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="a4778-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="a4778-160">-SecondaryCertificate</span></span>
<span data-ttu-id="a4778-161">包含次要憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a4778-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="a4778-162">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="a4778-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a4778-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a4778-163">-SecondaryKey</span></span>
<span data-ttu-id="a4778-164">以 base64 格式儲存的次要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a4778-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="a4778-165">-標記</span><span class="sxs-lookup"><span data-stu-id="a4778-165">-Tag</span></span>
<span data-ttu-id="a4778-166">初始標記。</span><span class="sxs-lookup"><span data-stu-id="a4778-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="a4778-167">-Web上Url</span><span class="sxs-lookup"><span data-stu-id="a4778-167">-WebhookUrl</span></span>
<span data-ttu-id="a4778-168">用於自訂配置要求的網頁連結 URL。</span><span class="sxs-lookup"><span data-stu-id="a4778-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="a4778-169">-確認</span><span class="sxs-lookup"><span data-stu-id="a4778-169">-Confirm</span></span>
<span data-ttu-id="a4778-170">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a4778-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4778-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4778-171">-WhatIf</span></span>
<span data-ttu-id="a4778-172">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4778-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4778-173">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4778-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4778-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4778-174">CommonParameters</span></span>
<span data-ttu-id="a4778-175">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a4778-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4778-176">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a4778-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4778-177">輸入</span><span class="sxs-lookup"><span data-stu-id="a4778-177">INPUTS</span></span>

### <span data-ttu-id="a4778-178">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a4778-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a4778-179">System.String</span><span class="sxs-lookup"><span data-stu-id="a4778-179">System.String</span></span>

## <span data-ttu-id="a4778-180">輸出</span><span class="sxs-lookup"><span data-stu-id="a4778-180">OUTPUTS</span></span>

### <span data-ttu-id="a4778-181">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a4778-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="a4778-182">筆記</span><span class="sxs-lookup"><span data-stu-id="a4778-182">NOTES</span></span>

## <span data-ttu-id="a4778-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4778-183">RELATED LINKS</span></span>
