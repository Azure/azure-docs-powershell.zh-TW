---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274864"
---
# <span data-ttu-id="0e41b-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="0e41b-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="0e41b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e41b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e41b-103">建立裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="0e41b-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="0e41b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e41b-104">SYNTAX</span></span>

### <span data-ttu-id="0e41b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0e41b-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="0e41b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e41b-106">InputObjectSet</span></span>
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

### <span data-ttu-id="0e41b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e41b-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="0e41b-108">說明</span><span class="sxs-lookup"><span data-stu-id="0e41b-108">DESCRIPTION</span></span>
<span data-ttu-id="0e41b-109">在 Azure IoT 中樞裝置預配服務中建立裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="0e41b-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="0e41b-110">示例</span><span class="sxs-lookup"><span data-stu-id="0e41b-110">EXAMPLES</span></span>

### <span data-ttu-id="0e41b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0e41b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="0e41b-112">使用證明類型 SymmetricKey 建立登記</span><span class="sxs-lookup"><span data-stu-id="0e41b-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="0e41b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0e41b-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="0e41b-114">使用 TPM 證明建立註冊。</span><span class="sxs-lookup"><span data-stu-id="0e41b-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="0e41b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="0e41b-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="0e41b-116">使用證明類型 X509 建立登記</span><span class="sxs-lookup"><span data-stu-id="0e41b-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="0e41b-117">範例4</span><span class="sxs-lookup"><span data-stu-id="0e41b-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="0e41b-118">使用證明類型 SymmetricKey 和初始內部類型的狀態建立註冊。</span><span class="sxs-lookup"><span data-stu-id="0e41b-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="0e41b-119">參數</span><span class="sxs-lookup"><span data-stu-id="0e41b-119">PARAMETERS</span></span>

### <span data-ttu-id="0e41b-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0e41b-120">-AllocationPolicy</span></span>
<span data-ttu-id="0e41b-121">指派給中樞之裝置的配置類型。</span><span class="sxs-lookup"><span data-stu-id="0e41b-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="0e41b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e41b-122">-ApiVersion</span></span>
<span data-ttu-id="0e41b-123">自訂配置要求中的 [提供服務] API 版本。</span><span class="sxs-lookup"><span data-stu-id="0e41b-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="0e41b-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="0e41b-124">-AttestationType</span></span>
<span data-ttu-id="0e41b-125">認證機制。</span><span class="sxs-lookup"><span data-stu-id="0e41b-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="0e41b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e41b-126">-DefaultProfile</span></span>
<span data-ttu-id="0e41b-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e41b-128">-所需</span><span class="sxs-lookup"><span data-stu-id="0e41b-128">-Desired</span></span>
<span data-ttu-id="0e41b-129">初始的想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e41b-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="0e41b-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0e41b-130">-DeviceId</span></span>
<span data-ttu-id="0e41b-131">IoT 中樞裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e41b-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="0e41b-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="0e41b-132">-DpsName</span></span>
<span data-ttu-id="0e41b-133">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="0e41b-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0e41b-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0e41b-134">-DpsObject</span></span>
<span data-ttu-id="0e41b-135">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="0e41b-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0e41b-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="0e41b-136">-EdgeEnabled</span></span>
<span data-ttu-id="0e41b-137">指示 edge 啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="0e41b-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="0e41b-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="0e41b-138">-EndorsementKey</span></span>
<span data-ttu-id="0e41b-139">Tpm 裝置的 TPM 簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="0e41b-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="0e41b-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="0e41b-140">-IotHub</span></span>
<span data-ttu-id="0e41b-141">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="0e41b-142">使用以空格分隔的清單來進行多個 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="0e41b-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="0e41b-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="0e41b-143">-IotHubHostName</span></span>
<span data-ttu-id="0e41b-144">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="0e41b-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="0e41b-145">-PrimaryCAName</span></span>
<span data-ttu-id="0e41b-146">主要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="0e41b-147">如果您想要具備根 CA 憑證的證明，必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="0e41b-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="0e41b-148">-PrimaryCertificate</span></span>
<span data-ttu-id="0e41b-149">包含主要憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0e41b-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="0e41b-150">X509 certificate .cer 檔案或 pem 檔案路徑的 Base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="0e41b-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="0e41b-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0e41b-151">-PrimaryKey</span></span>
<span data-ttu-id="0e41b-152">以 base64 格式儲存的主要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0e41b-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="0e41b-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="0e41b-153">-ProvisioningStatus</span></span>
<span data-ttu-id="0e41b-154">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="0e41b-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="0e41b-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="0e41b-155">-RegistrationId</span></span>
<span data-ttu-id="0e41b-156">個人登記登記 id。</span><span class="sxs-lookup"><span data-stu-id="0e41b-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="0e41b-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e41b-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="0e41b-158">重新調配至不同的 Iot 中樞時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="0e41b-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="0e41b-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e41b-159">-ResourceGroupName</span></span>
<span data-ttu-id="0e41b-160">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="0e41b-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0e41b-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e41b-161">-ResourceId</span></span>
<span data-ttu-id="0e41b-162">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0e41b-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0e41b-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="0e41b-163">-RootCertificate</span></span>
<span data-ttu-id="0e41b-164">可讓您使用根憑證建立 X509attestation。</span><span class="sxs-lookup"><span data-stu-id="0e41b-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="0e41b-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="0e41b-165">-SecondaryCAName</span></span>
<span data-ttu-id="0e41b-166">副根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="0e41b-167">如果您想要具備根 CA 憑證的證明，必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="0e41b-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="0e41b-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="0e41b-168">-SecondaryCertificate</span></span>
<span data-ttu-id="0e41b-169">包含副憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0e41b-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="0e41b-170">X509 certificate .cer 檔案或 pem 檔案路徑的 Base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="0e41b-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="0e41b-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0e41b-171">-SecondaryKey</span></span>
<span data-ttu-id="0e41b-172">以 base64 格式儲存的副對稱式共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0e41b-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="0e41b-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="0e41b-173">-StorageRootKey</span></span>
<span data-ttu-id="0e41b-174">Tpm 裝置的 TPM 儲存空間根機碼。</span><span class="sxs-lookup"><span data-stu-id="0e41b-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="0e41b-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e41b-175">-Tag</span></span>
<span data-ttu-id="0e41b-176">初始的雙子標記。</span><span class="sxs-lookup"><span data-stu-id="0e41b-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="0e41b-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="0e41b-177">-WebhookUrl</span></span>
<span data-ttu-id="0e41b-178">用於自訂配置要求的 webhook URL。</span><span class="sxs-lookup"><span data-stu-id="0e41b-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="0e41b-179">-確認</span><span class="sxs-lookup"><span data-stu-id="0e41b-179">-Confirm</span></span>
<span data-ttu-id="0e41b-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e41b-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e41b-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e41b-181">-WhatIf</span></span>
<span data-ttu-id="0e41b-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e41b-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e41b-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e41b-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e41b-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e41b-184">CommonParameters</span></span>
<span data-ttu-id="0e41b-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e41b-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e41b-186">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e41b-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e41b-187">輸入</span><span class="sxs-lookup"><span data-stu-id="0e41b-187">INPUTS</span></span>

### <span data-ttu-id="0e41b-188">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="0e41b-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0e41b-189">System.object</span><span class="sxs-lookup"><span data-stu-id="0e41b-189">System.String</span></span>

## <span data-ttu-id="0e41b-190">輸出</span><span class="sxs-lookup"><span data-stu-id="0e41b-190">OUTPUTS</span></span>

### <span data-ttu-id="0e41b-191">PSIndividualEnrollment （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="0e41b-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="0e41b-192">筆記</span><span class="sxs-lookup"><span data-stu-id="0e41b-192">NOTES</span></span>

## <span data-ttu-id="0e41b-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e41b-193">RELATED LINKS</span></span>
