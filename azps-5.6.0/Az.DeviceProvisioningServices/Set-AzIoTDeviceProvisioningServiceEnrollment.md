---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910218"
---
# <span data-ttu-id="4d1f0-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="4d1f0-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="4d1f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4d1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1f0-103">更新裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="4d1f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="4d1f0-104">SYNTAX</span></span>

### <span data-ttu-id="4d1f0-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4d1f0-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d1f0-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d1f0-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d1f0-108">描述</span><span class="sxs-lookup"><span data-stu-id="4d1f0-108">DESCRIPTION</span></span>
<span data-ttu-id="4d1f0-109">更新 Azure IoT Hub 裝置設置服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4d1f0-110">例子</span><span class="sxs-lookup"><span data-stu-id="4d1f0-110">EXAMPLES</span></span>

### <span data-ttu-id="4d1f0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4d1f0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="4d1f0-112">更新註冊記錄的配置策略和中樞。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="4d1f0-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="4d1f0-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="4d1f0-114">更新註冊的初始啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="4d1f0-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="4d1f0-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="4d1f0-116">更新對稱金鑰註冊的主要和次要憑證</span><span class="sxs-lookup"><span data-stu-id="4d1f0-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="4d1f0-117">參數</span><span class="sxs-lookup"><span data-stu-id="4d1f0-117">PARAMETERS</span></span>

### <span data-ttu-id="4d1f0-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="4d1f0-118">-AllocationPolicy</span></span>
<span data-ttu-id="4d1f0-119">指派給中樞的裝置配置類型。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="4d1f0-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4d1f0-120">-ApiVersion</span></span>
<span data-ttu-id="4d1f0-121">自訂配置要求中的資源佈建服務的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="4d1f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1f0-122">-DefaultProfile</span></span>
<span data-ttu-id="4d1f0-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d1f0-124">-需要</span><span class="sxs-lookup"><span data-stu-id="4d1f0-124">-Desired</span></span>
<span data-ttu-id="4d1f0-125">初始預期屬性。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="4d1f0-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4d1f0-126">-DeviceId</span></span>
<span data-ttu-id="4d1f0-127">IoT Hub 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="4d1f0-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4d1f0-128">-DpsName</span></span>
<span data-ttu-id="4d1f0-129">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="4d1f0-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4d1f0-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4d1f0-130">-DpsObject</span></span>
<span data-ttu-id="4d1f0-131">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="4d1f0-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4d1f0-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="4d1f0-132">-EdgeEnabled</span></span>
<span data-ttu-id="4d1f0-133">指出邊緣啟用的標號。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="4d1f0-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="4d1f0-134">-EndorsementKey</span></span>
<span data-ttu-id="4d1f0-135">TPM 裝置 TPM 背書金鑰。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="4d1f0-136">-IotHub</span><span class="sxs-lookup"><span data-stu-id="4d1f0-136">-IotHub</span></span>
<span data-ttu-id="4d1f0-137">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="4d1f0-138">針對多個 IoT 中樞使用空格分隔清單。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="4d1f0-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="4d1f0-139">-IotHubHostName</span></span>
<span data-ttu-id="4d1f0-140">目標 IoT 中樞的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="4d1f0-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="4d1f0-141">-PrimaryCAName</span></span>
<span data-ttu-id="4d1f0-142">主要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="4d1f0-143">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="4d1f0-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="4d1f0-144">-PrimaryCertificate</span></span>
<span data-ttu-id="4d1f0-145">包含主憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="4d1f0-146">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="4d1f0-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4d1f0-147">-PrimaryKey</span></span>
<span data-ttu-id="4d1f0-148">以 base64 格式儲存的主要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="4d1f0-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="4d1f0-149">-ProvisioningStatus</span></span>
<span data-ttu-id="4d1f0-150">啟用或停用註冊專案。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="4d1f0-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="4d1f0-151">-RegistrationId</span></span>
<span data-ttu-id="4d1f0-152">個別註冊註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="4d1f0-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="4d1f0-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="4d1f0-154">重新提供至不同 Iot Hub 時要處理的裝置資料。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="4d1f0-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1f0-155">-ResourceGroupName</span></span>
<span data-ttu-id="4d1f0-156">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="4d1f0-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4d1f0-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1f0-157">-ResourceId</span></span>
<span data-ttu-id="4d1f0-158">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4d1f0-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4d1f0-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="4d1f0-159">-RootCertificate</span></span>
<span data-ttu-id="4d1f0-160">切換以使用根憑證更新 X509 服務。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="4d1f0-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="4d1f0-161">-SecondaryCAName</span></span>
<span data-ttu-id="4d1f0-162">次要根 CA 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="4d1f0-163">如果需要使用根 CA 憑證表示，則必須提供根 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="4d1f0-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="4d1f0-164">-SecondaryCertificate</span></span>
<span data-ttu-id="4d1f0-165">包含次要憑證之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="4d1f0-166">X509 憑證 .cer 檔案或 .pem 檔案路徑的 Base-64 標記法。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="4d1f0-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4d1f0-167">-SecondaryKey</span></span>
<span data-ttu-id="4d1f0-168">以 base64 格式儲存的次要對稱共用便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="4d1f0-169">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="4d1f0-169">-StorageRootKey</span></span>
<span data-ttu-id="4d1f0-170">TPM 裝置 TPM 儲存根鍵。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="4d1f0-171">-標記</span><span class="sxs-lookup"><span data-stu-id="4d1f0-171">-Tag</span></span>
<span data-ttu-id="4d1f0-172">初始標記。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="4d1f0-173">-Web上Url</span><span class="sxs-lookup"><span data-stu-id="4d1f0-173">-WebhookUrl</span></span>
<span data-ttu-id="4d1f0-174">用於自訂配置要求的網頁連結 URL。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="4d1f0-175">-確認</span><span class="sxs-lookup"><span data-stu-id="4d1f0-175">-Confirm</span></span>
<span data-ttu-id="4d1f0-176">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1f0-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1f0-177">-WhatIf</span></span>
<span data-ttu-id="4d1f0-178">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1f0-179">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1f0-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1f0-180">CommonParameters</span></span>
<span data-ttu-id="4d1f0-181">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1f0-182">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4d1f0-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1f0-183">輸入</span><span class="sxs-lookup"><span data-stu-id="4d1f0-183">INPUTS</span></span>

### <span data-ttu-id="4d1f0-184">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4d1f0-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4d1f0-185">System.String</span><span class="sxs-lookup"><span data-stu-id="4d1f0-185">System.String</span></span>

## <span data-ttu-id="4d1f0-186">輸出</span><span class="sxs-lookup"><span data-stu-id="4d1f0-186">OUTPUTS</span></span>

### <span data-ttu-id="4d1f0-187">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="4d1f0-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="4d1f0-188">筆記</span><span class="sxs-lookup"><span data-stu-id="4d1f0-188">NOTES</span></span>

## <span data-ttu-id="4d1f0-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d1f0-189">RELATED LINKS</span></span>
