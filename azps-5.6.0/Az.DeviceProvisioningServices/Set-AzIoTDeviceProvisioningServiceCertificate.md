---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 1678202d02f25ea8ffa2ed14a859aaf5965776b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910225"
---
# <span data-ttu-id="d19b8-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="d19b8-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="d19b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d19b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d19b8-103">驗證 Azure IoT Hub 裝置設置服務憑證。</span><span class="sxs-lookup"><span data-stu-id="d19b8-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="d19b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="d19b8-104">SYNTAX</span></span>

### <span data-ttu-id="d19b8-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d19b8-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19b8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d19b8-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19b8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d19b8-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19b8-108">描述</span><span class="sxs-lookup"><span data-stu-id="d19b8-108">DESCRIPTION</span></span>
<span data-ttu-id="d19b8-109">上傳包含呼叫產生驗證碼所取得驗證碼的驗證憑證，以驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="d19b8-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="d19b8-110">這是驗證程式的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d19b8-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="d19b8-111">有關 Azure IoT Hub 裝置設置服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="d19b8-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="d19b8-112">例子</span><span class="sxs-lookup"><span data-stu-id="d19b8-112">EXAMPLES</span></span>

### <span data-ttu-id="d19b8-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="d19b8-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d19b8-114">確認「mycertificate」私密金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="d19b8-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="d19b8-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="d19b8-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d19b8-116">使用管線驗證「mycertificate」私密金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="d19b8-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="d19b8-117">參數</span><span class="sxs-lookup"><span data-stu-id="d19b8-117">PARAMETERS</span></span>

### <span data-ttu-id="d19b8-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d19b8-118">-CertificateName</span></span>
<span data-ttu-id="d19b8-119">Iot 裝置設置服務憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="d19b8-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d19b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19b8-120">-DefaultProfile</span></span>
<span data-ttu-id="d19b8-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d19b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d19b8-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="d19b8-122">-Etag</span></span>
<span data-ttu-id="d19b8-123">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="d19b8-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d19b8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d19b8-124">-InputObject</span></span>
<span data-ttu-id="d19b8-125">IoT 裝置設置服務憑證物件</span><span class="sxs-lookup"><span data-stu-id="d19b8-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="d19b8-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d19b8-126">-Name</span></span>
<span data-ttu-id="d19b8-127">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="d19b8-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d19b8-128">-路徑</span><span class="sxs-lookup"><span data-stu-id="d19b8-128">-Path</span></span>
<span data-ttu-id="d19b8-129">base-64 表示 X509 憑證 .cer 檔案或 .pem 檔案路徑</span><span class="sxs-lookup"><span data-stu-id="d19b8-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="d19b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="d19b8-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="d19b8-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d19b8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d19b8-132">-ResourceId</span></span>
<span data-ttu-id="d19b8-133">IoT 裝置提供服務憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d19b8-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d19b8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d19b8-134">-Confirm</span></span>
<span data-ttu-id="d19b8-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d19b8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19b8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19b8-136">-WhatIf</span></span>
<span data-ttu-id="d19b8-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d19b8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19b8-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d19b8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19b8-139">CommonParameters</span></span>
<span data-ttu-id="d19b8-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d19b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19b8-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d19b8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19b8-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d19b8-142">INPUTS</span></span>

### <span data-ttu-id="d19b8-143">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d19b8-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="d19b8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d19b8-144">System.String</span></span>

## <span data-ttu-id="d19b8-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d19b8-145">OUTPUTS</span></span>

### <span data-ttu-id="d19b8-146">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d19b8-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="d19b8-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d19b8-147">NOTES</span></span>

## <span data-ttu-id="d19b8-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="d19b8-148">RELATED LINKS</span></span>
