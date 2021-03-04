---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 999fa5d697feb8eab6edb83816763ed6cf49523c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915497"
---
# <span data-ttu-id="0abc3-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="0abc3-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="0abc3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0abc3-102">SYNOPSIS</span></span>
<span data-ttu-id="0abc3-103">產生 Azure IoT Hub 裝置設置服務憑證的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="0abc3-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="0abc3-104">語法</span><span class="sxs-lookup"><span data-stu-id="0abc3-104">SYNTAX</span></span>

### <span data-ttu-id="0abc3-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0abc3-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0abc3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0abc3-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0abc3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0abc3-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0abc3-108">描述</span><span class="sxs-lookup"><span data-stu-id="0abc3-108">DESCRIPTION</span></span>
<span data-ttu-id="0abc3-109">此驗證碼是用來完成憑證的驗證步驟。</span><span class="sxs-lookup"><span data-stu-id="0abc3-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="0abc3-110">使用此驗證碼做為使用根憑證私人金鑰簽署之新憑證的 CN。</span><span class="sxs-lookup"><span data-stu-id="0abc3-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="0abc3-111">有關 Azure IoT Hub 裝置設置服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates 。</span><span class="sxs-lookup"><span data-stu-id="0abc3-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="0abc3-112">例子</span><span class="sxs-lookup"><span data-stu-id="0abc3-112">EXAMPLES</span></span>

### <span data-ttu-id="0abc3-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="0abc3-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0abc3-114">產生「mycertificate」的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="0abc3-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="0abc3-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="0abc3-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0abc3-116">使用管線產生「mycertificate」的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="0abc3-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="0abc3-117">參數</span><span class="sxs-lookup"><span data-stu-id="0abc3-117">PARAMETERS</span></span>

### <span data-ttu-id="0abc3-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0abc3-118">-CertificateName</span></span>
<span data-ttu-id="0abc3-119">Iot 裝置設置服務憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="0abc3-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="0abc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abc3-120">-DefaultProfile</span></span>
<span data-ttu-id="0abc3-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0abc3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0abc3-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="0abc3-122">-Etag</span></span>
<span data-ttu-id="0abc3-123">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="0abc3-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="0abc3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0abc3-124">-InputObject</span></span>
<span data-ttu-id="0abc3-125">IoT 裝置設置服務憑證物件</span><span class="sxs-lookup"><span data-stu-id="0abc3-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="0abc3-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0abc3-126">-Name</span></span>
<span data-ttu-id="0abc3-127">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="0abc3-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0abc3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abc3-128">-ResourceGroupName</span></span>
<span data-ttu-id="0abc3-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="0abc3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0abc3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0abc3-130">-ResourceId</span></span>
<span data-ttu-id="0abc3-131">IoT 裝置提供服務憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0abc3-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="0abc3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0abc3-132">-Confirm</span></span>
<span data-ttu-id="0abc3-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0abc3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0abc3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0abc3-134">-WhatIf</span></span>
<span data-ttu-id="0abc3-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0abc3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0abc3-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0abc3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0abc3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abc3-137">CommonParameters</span></span>
<span data-ttu-id="0abc3-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0abc3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abc3-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0abc3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abc3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0abc3-140">INPUTS</span></span>

### <span data-ttu-id="0abc3-141">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="0abc3-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="0abc3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0abc3-142">System.String</span></span>

## <span data-ttu-id="0abc3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0abc3-143">OUTPUTS</span></span>

### <span data-ttu-id="0abc3-144">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="0abc3-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="0abc3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0abc3-145">NOTES</span></span>

## <span data-ttu-id="0abc3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0abc3-146">RELATED LINKS</span></span>
