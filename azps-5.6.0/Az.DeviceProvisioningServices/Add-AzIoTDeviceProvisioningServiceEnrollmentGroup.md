---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 89a1bede6ff90b58b83a7c401860c66430958fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913534"
---
# <span data-ttu-id="34c22-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="34c22-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="34c22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="34c22-102">SYNOPSIS</span></span>
<span data-ttu-id="34c22-103">建立裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="34c22-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="34c22-104">語法</span><span class="sxs-lookup"><span data-stu-id="34c22-104">SYNTAX</span></span>

### <span data-ttu-id="34c22-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="34c22-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c22-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="34c22-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c22-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="34c22-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c22-108">描述</span><span class="sxs-lookup"><span data-stu-id="34c22-108">DESCRIPTION</span></span>
<span data-ttu-id="34c22-109">在 Azure IoT 中心裝置設置服務中建立註冊群組。</span><span class="sxs-lookup"><span data-stu-id="34c22-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="34c22-110">例子</span><span class="sxs-lookup"><span data-stu-id="34c22-110">EXAMPLES</span></span>

### <span data-ttu-id="34c22-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="34c22-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="34c22-112">使用證明類型 SymmetricKey 建立註冊</span><span class="sxs-lookup"><span data-stu-id="34c22-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="34c22-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="34c22-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="34c22-114">使用證明類型 X509 建立註冊</span><span class="sxs-lookup"><span data-stu-id="34c22-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="34c22-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="34c22-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="34c22-116">使用證明類型 SymmetricKey 和初始啟動狀態建立註冊。</span><span class="sxs-lookup"><span data-stu-id="34c22-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="34c22-117">參數</span><span class="sxs-lookup"><span data-stu-id="34c22-117">PARAMETERS</span></span>

### <span data-ttu-id="34c22-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="34c22-118">-AllocationPolicy</span></span>
<span data-ttu-id="34c22-119">指派給中樞的裝置配置類型。</span><span class="sxs-lookup"><span data-stu-id="34c22-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="34c22-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34c22-120">-ApiVersion</span></span>
<span data-ttu-id="34c22-121">自訂配置要求中的資源佈建服務的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="34c22-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="34c22-122">-表示類型</span><span class="sxs-lookup"><span data-stu-id="34c22-122">-AttestationType</span></span>
<span data-ttu-id="34c22-123">證明機制。</span><span class="sxs-lookup"><span data-stu-id="34c22-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c22-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c22-124">-DefaultProfile</span></span>
<span data-ttu-id="34c22-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="34c22-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c22-126">-需要</span><span class="sxs-lookup"><span data-stu-id="34c22-126">-Desired</span></span>
<span data-ttu-id="34c22-127">初始預期屬性。</span><span class="sxs-lookup"><span data-stu-id="34c22-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="34c22-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="34c22-128">-DpsName</span></span>
<span data-ttu-id="34c22-129">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="34c22-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="34c22-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="34c22-130">-DpsObject</span></span>
<span data-ttu-id="34c22-131">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="34c22-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="34c22-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="34c22-132">-EdgeEnabled</span></span>
<span data-ttu-id="34c22-133">指出邊緣啟用的標號。</span><span class="sxs-lookup"><span data-stu-id="34c22-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="34c22-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="34c22-134">-IotHub</span></span>
<span data-ttu-id="34c22-135">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="34c22-136">針對多個 IoT 中樞使用空格分隔清單。</span><span class="sxs-lookup"><span data-stu-id="34c22-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="34c22-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="34c22-137">-IotHubHostName</span></span>
<span data-ttu-id="34c22-138">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="34c22-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="34c22-139">-Name</span></span>
<span data-ttu-id="34c22-140">註冊組的名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="34c22-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="34c22-141">-PrimaryCAName</span></span>
<span data-ttu-id="34c22-142">主要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="34c22-143">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="34c22-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="34c22-144">-PrimaryCertificate</span></span>
<span data-ttu-id="34c22-145">包含主憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="34c22-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="34c22-146">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="34c22-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="34c22-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="34c22-147">-PrimaryKey</span></span>
<span data-ttu-id="34c22-148">以 base64 格式儲存的主要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="34c22-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="34c22-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="34c22-149">-ProvisioningStatus</span></span>
<span data-ttu-id="34c22-150">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="34c22-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="34c22-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="34c22-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="34c22-152">重新提供至不同 Iot Hub 時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="34c22-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="34c22-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c22-153">-ResourceGroupName</span></span>
<span data-ttu-id="34c22-154">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="34c22-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="34c22-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34c22-155">-ResourceId</span></span>
<span data-ttu-id="34c22-156">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="34c22-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="34c22-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="34c22-157">-RootCertificate</span></span>
<span data-ttu-id="34c22-158">允許使用根憑證建立 X509attation。</span><span class="sxs-lookup"><span data-stu-id="34c22-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="34c22-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="34c22-159">-SecondaryCAName</span></span>
<span data-ttu-id="34c22-160">次要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="34c22-161">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="34c22-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="34c22-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="34c22-162">-SecondaryCertificate</span></span>
<span data-ttu-id="34c22-163">包含次要憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="34c22-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="34c22-164">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="34c22-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="34c22-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="34c22-165">-SecondaryKey</span></span>
<span data-ttu-id="34c22-166">以 base64 格式儲存的次要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="34c22-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="34c22-167">-標記</span><span class="sxs-lookup"><span data-stu-id="34c22-167">-Tag</span></span>
<span data-ttu-id="34c22-168">初始標記。</span><span class="sxs-lookup"><span data-stu-id="34c22-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="34c22-169">-Web上Url</span><span class="sxs-lookup"><span data-stu-id="34c22-169">-WebhookUrl</span></span>
<span data-ttu-id="34c22-170">用於自訂配置要求的網頁連結 URL。</span><span class="sxs-lookup"><span data-stu-id="34c22-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="34c22-171">-確認</span><span class="sxs-lookup"><span data-stu-id="34c22-171">-Confirm</span></span>
<span data-ttu-id="34c22-172">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="34c22-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c22-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c22-173">-WhatIf</span></span>
<span data-ttu-id="34c22-174">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34c22-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34c22-175">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34c22-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34c22-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c22-176">CommonParameters</span></span>
<span data-ttu-id="34c22-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="34c22-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c22-178">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="34c22-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c22-179">輸入</span><span class="sxs-lookup"><span data-stu-id="34c22-179">INPUTS</span></span>

### <span data-ttu-id="34c22-180">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="34c22-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="34c22-181">System.String</span><span class="sxs-lookup"><span data-stu-id="34c22-181">System.String</span></span>

## <span data-ttu-id="34c22-182">輸出</span><span class="sxs-lookup"><span data-stu-id="34c22-182">OUTPUTS</span></span>

### <span data-ttu-id="34c22-183">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="34c22-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="34c22-184">筆記</span><span class="sxs-lookup"><span data-stu-id="34c22-184">NOTES</span></span>

## <span data-ttu-id="34c22-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="34c22-185">RELATED LINKS</span></span>
