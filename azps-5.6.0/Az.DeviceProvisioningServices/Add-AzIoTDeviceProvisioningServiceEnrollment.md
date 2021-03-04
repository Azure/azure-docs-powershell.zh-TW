---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 5aca36433089a2e84965ee6d1d8b2c17d3c53205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907134"
---
# <span data-ttu-id="50754-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="50754-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="50754-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50754-102">SYNOPSIS</span></span>
<span data-ttu-id="50754-103">建立裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="50754-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="50754-104">語法</span><span class="sxs-lookup"><span data-stu-id="50754-104">SYNTAX</span></span>

### <span data-ttu-id="50754-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="50754-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50754-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50754-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50754-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50754-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50754-108">描述</span><span class="sxs-lookup"><span data-stu-id="50754-108">DESCRIPTION</span></span>
<span data-ttu-id="50754-109">在 Azure IoT 中心裝置設置服務中建立裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="50754-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="50754-110">例子</span><span class="sxs-lookup"><span data-stu-id="50754-110">EXAMPLES</span></span>

### <span data-ttu-id="50754-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="50754-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="50754-112">使用證明類型 SymmetricKey 建立註冊</span><span class="sxs-lookup"><span data-stu-id="50754-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="50754-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="50754-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="50754-114">使用 TPM 證明建立註冊。</span><span class="sxs-lookup"><span data-stu-id="50754-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="50754-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="50754-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="50754-116">使用證明類型 X509 建立註冊</span><span class="sxs-lookup"><span data-stu-id="50754-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="50754-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="50754-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="50754-118">使用證明類型 SymmetricKey 和初始啟動狀態建立註冊。</span><span class="sxs-lookup"><span data-stu-id="50754-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="50754-119">參數</span><span class="sxs-lookup"><span data-stu-id="50754-119">PARAMETERS</span></span>

### <span data-ttu-id="50754-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="50754-120">-AllocationPolicy</span></span>
<span data-ttu-id="50754-121">指派給中樞的裝置配置類型。</span><span class="sxs-lookup"><span data-stu-id="50754-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="50754-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50754-122">-ApiVersion</span></span>
<span data-ttu-id="50754-123">自訂配置要求中的資源佈建服務的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="50754-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="50754-124">-表示類型</span><span class="sxs-lookup"><span data-stu-id="50754-124">-AttestationType</span></span>
<span data-ttu-id="50754-125">證明機制。</span><span class="sxs-lookup"><span data-stu-id="50754-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="50754-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50754-126">-DefaultProfile</span></span>
<span data-ttu-id="50754-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50754-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50754-128">-需要</span><span class="sxs-lookup"><span data-stu-id="50754-128">-Desired</span></span>
<span data-ttu-id="50754-129">初始預期屬性。</span><span class="sxs-lookup"><span data-stu-id="50754-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="50754-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="50754-130">-DeviceId</span></span>
<span data-ttu-id="50754-131">IoT Hub 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="50754-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="50754-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="50754-132">-DpsName</span></span>
<span data-ttu-id="50754-133">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="50754-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="50754-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="50754-134">-DpsObject</span></span>
<span data-ttu-id="50754-135">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="50754-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="50754-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="50754-136">-EdgeEnabled</span></span>
<span data-ttu-id="50754-137">指出邊緣啟用的標號。</span><span class="sxs-lookup"><span data-stu-id="50754-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="50754-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="50754-138">-EndorsementKey</span></span>
<span data-ttu-id="50754-139">TPM 裝置 TPM 背書金鑰。</span><span class="sxs-lookup"><span data-stu-id="50754-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="50754-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="50754-140">-IotHub</span></span>
<span data-ttu-id="50754-141">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="50754-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="50754-142">針對多個 IoT 中樞使用空格分隔清單。</span><span class="sxs-lookup"><span data-stu-id="50754-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="50754-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="50754-143">-IotHubHostName</span></span>
<span data-ttu-id="50754-144">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="50754-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="50754-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="50754-145">-PrimaryCAName</span></span>
<span data-ttu-id="50754-146">主要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="50754-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="50754-147">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="50754-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="50754-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="50754-148">-PrimaryCertificate</span></span>
<span data-ttu-id="50754-149">包含主憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="50754-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="50754-150">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="50754-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="50754-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="50754-151">-PrimaryKey</span></span>
<span data-ttu-id="50754-152">以 base64 格式儲存的主要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="50754-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="50754-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="50754-153">-ProvisioningStatus</span></span>
<span data-ttu-id="50754-154">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="50754-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="50754-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="50754-155">-RegistrationId</span></span>
<span data-ttu-id="50754-156">個別註冊註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="50754-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="50754-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="50754-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="50754-158">重新提供至不同 Iot Hub 時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="50754-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="50754-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50754-159">-ResourceGroupName</span></span>
<span data-ttu-id="50754-160">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="50754-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="50754-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50754-161">-ResourceId</span></span>
<span data-ttu-id="50754-162">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="50754-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="50754-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="50754-163">-RootCertificate</span></span>
<span data-ttu-id="50754-164">允許使用根憑證建立 X509attation。</span><span class="sxs-lookup"><span data-stu-id="50754-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="50754-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="50754-165">-SecondaryCAName</span></span>
<span data-ttu-id="50754-166">次要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="50754-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="50754-167">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="50754-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="50754-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="50754-168">-SecondaryCertificate</span></span>
<span data-ttu-id="50754-169">包含次要憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="50754-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="50754-170">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="50754-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="50754-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="50754-171">-SecondaryKey</span></span>
<span data-ttu-id="50754-172">以 base64 格式儲存的次要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="50754-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="50754-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="50754-173">-StorageRootKey</span></span>
<span data-ttu-id="50754-174">TPM 裝置 TPM 儲存根鍵。</span><span class="sxs-lookup"><span data-stu-id="50754-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="50754-175">-標記</span><span class="sxs-lookup"><span data-stu-id="50754-175">-Tag</span></span>
<span data-ttu-id="50754-176">初始標記。</span><span class="sxs-lookup"><span data-stu-id="50754-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="50754-177">-Web上Url</span><span class="sxs-lookup"><span data-stu-id="50754-177">-WebhookUrl</span></span>
<span data-ttu-id="50754-178">用於自訂配置要求的網頁連結 URL。</span><span class="sxs-lookup"><span data-stu-id="50754-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="50754-179">-確認</span><span class="sxs-lookup"><span data-stu-id="50754-179">-Confirm</span></span>
<span data-ttu-id="50754-180">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50754-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50754-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50754-181">-WhatIf</span></span>
<span data-ttu-id="50754-182">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50754-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50754-183">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50754-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50754-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50754-184">CommonParameters</span></span>
<span data-ttu-id="50754-185">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50754-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50754-186">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="50754-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50754-187">輸入</span><span class="sxs-lookup"><span data-stu-id="50754-187">INPUTS</span></span>

### <span data-ttu-id="50754-188">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="50754-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="50754-189">System.String</span><span class="sxs-lookup"><span data-stu-id="50754-189">System.String</span></span>

## <span data-ttu-id="50754-190">輸出</span><span class="sxs-lookup"><span data-stu-id="50754-190">OUTPUTS</span></span>

### <span data-ttu-id="50754-191">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="50754-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="50754-192">筆記</span><span class="sxs-lookup"><span data-stu-id="50754-192">NOTES</span></span>

## <span data-ttu-id="50754-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="50754-193">RELATED LINKS</span></span>
