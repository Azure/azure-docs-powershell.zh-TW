---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136975"
---
# <span data-ttu-id="444ec-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="444ec-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="444ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="444ec-102">SYNOPSIS</span></span>
<span data-ttu-id="444ec-103">建立裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="444ec-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="444ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="444ec-104">SYNTAX</span></span>

### <span data-ttu-id="444ec-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="444ec-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444ec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="444ec-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="444ec-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="444ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="444ec-108">DESCRIPTION</span></span>
<span data-ttu-id="444ec-109">在 Azure IoT 中樞裝置提供服務中建立註冊群組。</span><span class="sxs-lookup"><span data-stu-id="444ec-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="444ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="444ec-110">EXAMPLES</span></span>

### <span data-ttu-id="444ec-111">範例1</span><span class="sxs-lookup"><span data-stu-id="444ec-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="444ec-112">使用證明類型 SymmetricKey 建立登記</span><span class="sxs-lookup"><span data-stu-id="444ec-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="444ec-113">範例2</span><span class="sxs-lookup"><span data-stu-id="444ec-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="444ec-114">使用證明類型 X509 建立登記</span><span class="sxs-lookup"><span data-stu-id="444ec-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="444ec-115">範例3</span><span class="sxs-lookup"><span data-stu-id="444ec-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="444ec-116">使用證明類型 SymmetricKey 和初始內部類型的狀態建立註冊。</span><span class="sxs-lookup"><span data-stu-id="444ec-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="444ec-117">參數</span><span class="sxs-lookup"><span data-stu-id="444ec-117">PARAMETERS</span></span>

### <span data-ttu-id="444ec-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="444ec-118">-AllocationPolicy</span></span>
<span data-ttu-id="444ec-119">指派給中樞之裝置的配置類型。</span><span class="sxs-lookup"><span data-stu-id="444ec-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="444ec-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="444ec-120">-ApiVersion</span></span>
<span data-ttu-id="444ec-121">自訂配置要求中的 [提供服務] API 版本。</span><span class="sxs-lookup"><span data-stu-id="444ec-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="444ec-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="444ec-122">-AttestationType</span></span>
<span data-ttu-id="444ec-123">認證機制。</span><span class="sxs-lookup"><span data-stu-id="444ec-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="444ec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444ec-124">-DefaultProfile</span></span>
<span data-ttu-id="444ec-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="444ec-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444ec-126">-所需</span><span class="sxs-lookup"><span data-stu-id="444ec-126">-Desired</span></span>
<span data-ttu-id="444ec-127">初始的想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="444ec-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="444ec-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="444ec-128">-DpsName</span></span>
<span data-ttu-id="444ec-129">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="444ec-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="444ec-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="444ec-130">-DpsObject</span></span>
<span data-ttu-id="444ec-131">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="444ec-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="444ec-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="444ec-132">-EdgeEnabled</span></span>
<span data-ttu-id="444ec-133">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="444ec-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="444ec-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="444ec-134">-IotHub</span></span>
<span data-ttu-id="444ec-135">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="444ec-136">使用以空格分隔的清單來進行多個 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="444ec-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="444ec-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="444ec-137">-IotHubHostName</span></span>
<span data-ttu-id="444ec-138">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="444ec-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="444ec-139">-Name</span></span>
<span data-ttu-id="444ec-140">註冊群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="444ec-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="444ec-141">-PrimaryCAName</span></span>
<span data-ttu-id="444ec-142">主要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="444ec-143">如果您想要具備根 CA 憑證的證明，必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="444ec-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="444ec-144">-PrimaryCertificate</span></span>
<span data-ttu-id="444ec-145">包含主要憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="444ec-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="444ec-146">X509 certificate .cer 檔案或 pem 檔案路徑的 Base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="444ec-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="444ec-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="444ec-147">-PrimaryKey</span></span>
<span data-ttu-id="444ec-148">以 base64 格式儲存的主要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="444ec-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="444ec-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="444ec-149">-ProvisioningStatus</span></span>
<span data-ttu-id="444ec-150">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="444ec-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="444ec-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="444ec-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="444ec-152">重新調配至不同的 Iot 中樞時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="444ec-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="444ec-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444ec-153">-ResourceGroupName</span></span>
<span data-ttu-id="444ec-154">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="444ec-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="444ec-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="444ec-155">-ResourceId</span></span>
<span data-ttu-id="444ec-156">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="444ec-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="444ec-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="444ec-157">-RootCertificate</span></span>
<span data-ttu-id="444ec-158">可讓您使用根憑證建立 X509attestation。</span><span class="sxs-lookup"><span data-stu-id="444ec-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="444ec-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="444ec-159">-SecondaryCAName</span></span>
<span data-ttu-id="444ec-160">副根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="444ec-161">如果您想要具備根 CA 憑證的證明，必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="444ec-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="444ec-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="444ec-162">-SecondaryCertificate</span></span>
<span data-ttu-id="444ec-163">包含副憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="444ec-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="444ec-164">X509 certificate .cer 檔案或 pem 檔案路徑的 Base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="444ec-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="444ec-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="444ec-165">-SecondaryKey</span></span>
<span data-ttu-id="444ec-166">以 base64 格式儲存的副對稱式共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="444ec-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="444ec-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="444ec-167">-Tag</span></span>
<span data-ttu-id="444ec-168">初始的雙子標記。</span><span class="sxs-lookup"><span data-stu-id="444ec-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="444ec-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="444ec-169">-WebhookUrl</span></span>
<span data-ttu-id="444ec-170">用於自訂配置要求的 webhook URL。</span><span class="sxs-lookup"><span data-stu-id="444ec-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="444ec-171">-確認</span><span class="sxs-lookup"><span data-stu-id="444ec-171">-Confirm</span></span>
<span data-ttu-id="444ec-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="444ec-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="444ec-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="444ec-173">-WhatIf</span></span>
<span data-ttu-id="444ec-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="444ec-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="444ec-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="444ec-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="444ec-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444ec-176">CommonParameters</span></span>
<span data-ttu-id="444ec-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="444ec-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444ec-178">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="444ec-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444ec-179">輸入</span><span class="sxs-lookup"><span data-stu-id="444ec-179">INPUTS</span></span>

### <span data-ttu-id="444ec-180">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="444ec-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="444ec-181">System.object</span><span class="sxs-lookup"><span data-stu-id="444ec-181">System.String</span></span>

## <span data-ttu-id="444ec-182">輸出</span><span class="sxs-lookup"><span data-stu-id="444ec-182">OUTPUTS</span></span>

### <span data-ttu-id="444ec-183">PSEnrollmentGroup （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="444ec-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="444ec-184">筆記</span><span class="sxs-lookup"><span data-stu-id="444ec-184">NOTES</span></span>

## <span data-ttu-id="444ec-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="444ec-185">RELATED LINKS</span></span>
