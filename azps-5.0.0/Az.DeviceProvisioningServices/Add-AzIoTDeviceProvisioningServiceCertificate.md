---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136981"
---
# <span data-ttu-id="acf81-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="acf81-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="acf81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acf81-102">SYNOPSIS</span></span>
<span data-ttu-id="acf81-103">建立/更新 Azure IoT 中樞裝置置備服務憑證。</span><span class="sxs-lookup"><span data-stu-id="acf81-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="acf81-104">句法</span><span class="sxs-lookup"><span data-stu-id="acf81-104">SYNTAX</span></span>

### <span data-ttu-id="acf81-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="acf81-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf81-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="acf81-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="acf81-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acf81-108">說明</span><span class="sxs-lookup"><span data-stu-id="acf81-108">DESCRIPTION</span></span>
<span data-ttu-id="acf81-109">上傳新憑證或使用相同名稱取代現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="acf81-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="acf81-110">如需 Azure IoT 中樞裝置提供服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 。</span><span class="sxs-lookup"><span data-stu-id="acf81-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="acf81-111">示例</span><span class="sxs-lookup"><span data-stu-id="acf81-111">EXAMPLES</span></span>

### <span data-ttu-id="acf81-112">範例1</span><span class="sxs-lookup"><span data-stu-id="acf81-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="acf81-113">將 CA 憑證 CER 檔案上傳到 Azure IoT 中心裝置的提供服務。</span><span class="sxs-lookup"><span data-stu-id="acf81-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="acf81-114">範例2</span><span class="sxs-lookup"><span data-stu-id="acf81-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="acf81-115">透過上傳新的 CER 檔案，更新 IoT 中樞裝置提供服務中的 CA 憑證。</span><span class="sxs-lookup"><span data-stu-id="acf81-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="acf81-116">參數</span><span class="sxs-lookup"><span data-stu-id="acf81-116">PARAMETERS</span></span>

### <span data-ttu-id="acf81-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="acf81-117">-CertificateName</span></span>
<span data-ttu-id="acf81-118">Iot 裝置預配服務憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="acf81-118">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf81-119">-DefaultProfile</span></span>
<span data-ttu-id="acf81-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acf81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf81-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="acf81-121">-Etag</span></span>
<span data-ttu-id="acf81-122">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="acf81-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="acf81-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf81-123">-InputObject</span></span>
<span data-ttu-id="acf81-124">IoT 裝置預配服務憑證物件</span><span class="sxs-lookup"><span data-stu-id="acf81-124">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acf81-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="acf81-125">-Name</span></span>
<span data-ttu-id="acf81-126">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="acf81-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="acf81-127">-Path</span><span class="sxs-lookup"><span data-stu-id="acf81-127">-Path</span></span>
<span data-ttu-id="acf81-128">X509 certificate .cer 檔案或 pem 檔案路徑的基本64表示形式</span><span class="sxs-lookup"><span data-stu-id="acf81-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf81-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf81-129">-ResourceGroupName</span></span>
<span data-ttu-id="acf81-130">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="acf81-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="acf81-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf81-131">-ResourceId</span></span>
<span data-ttu-id="acf81-132">IoT 裝置預配服務憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="acf81-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="acf81-133">-確認</span><span class="sxs-lookup"><span data-stu-id="acf81-133">-Confirm</span></span>
<span data-ttu-id="acf81-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acf81-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf81-135">-WhatIf</span></span>
<span data-ttu-id="acf81-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acf81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf81-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acf81-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf81-138">CommonParameters</span></span>
<span data-ttu-id="acf81-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acf81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf81-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acf81-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf81-141">輸入</span><span class="sxs-lookup"><span data-stu-id="acf81-141">INPUTS</span></span>

### <span data-ttu-id="acf81-142">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="acf81-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="acf81-143">System.object</span><span class="sxs-lookup"><span data-stu-id="acf81-143">System.String</span></span>

## <span data-ttu-id="acf81-144">輸出</span><span class="sxs-lookup"><span data-stu-id="acf81-144">OUTPUTS</span></span>

### <span data-ttu-id="acf81-145">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="acf81-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="acf81-146">筆記</span><span class="sxs-lookup"><span data-stu-id="acf81-146">NOTES</span></span>

## <span data-ttu-id="acf81-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="acf81-147">RELATED LINKS</span></span>
