---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135995"
---
# <span data-ttu-id="a8ae0-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="a8ae0-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="a8ae0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ae0-103">針對 Azure IoT 中樞裝置提供服務憑證產生驗證碼。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="a8ae0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8ae0-104">SYNTAX</span></span>

### <span data-ttu-id="a8ae0-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a8ae0-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8ae0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8ae0-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ae0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a8ae0-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ae0-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8ae0-108">DESCRIPTION</span></span>
<span data-ttu-id="a8ae0-109">此驗證碼是用來完成憑證的已保管步驟證明。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="a8ae0-110">使用此驗證碼作為使用 [根憑證私密金鑰] 簽署的新憑證的 CN。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="a8ae0-111">如需 Azure IoT 中樞裝置提供服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="a8ae0-112">示例</span><span class="sxs-lookup"><span data-stu-id="a8ae0-112">EXAMPLES</span></span>

### <span data-ttu-id="a8ae0-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a8ae0-113">Example 1</span></span>
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

<span data-ttu-id="a8ae0-114">產生「mycertificate」的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="a8ae0-115">範例2</span><span class="sxs-lookup"><span data-stu-id="a8ae0-115">Example 2</span></span>
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

<span data-ttu-id="a8ae0-116">使用管道產生「mycertificate」的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="a8ae0-117">參數</span><span class="sxs-lookup"><span data-stu-id="a8ae0-117">PARAMETERS</span></span>

### <span data-ttu-id="a8ae0-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a8ae0-118">-CertificateName</span></span>
<span data-ttu-id="a8ae0-119">Iot 裝置預配服務憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="a8ae0-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="a8ae0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ae0-120">-DefaultProfile</span></span>
<span data-ttu-id="a8ae0-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ae0-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="a8ae0-122">-Etag</span></span>
<span data-ttu-id="a8ae0-123">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="a8ae0-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a8ae0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ae0-124">-InputObject</span></span>
<span data-ttu-id="a8ae0-125">IoT 裝置預配服務憑證物件</span><span class="sxs-lookup"><span data-stu-id="a8ae0-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="a8ae0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8ae0-126">-Name</span></span>
<span data-ttu-id="a8ae0-127">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="a8ae0-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a8ae0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ae0-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8ae0-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a8ae0-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a8ae0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8ae0-130">-ResourceId</span></span>
<span data-ttu-id="a8ae0-131">IoT 裝置預配服務憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a8ae0-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="a8ae0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a8ae0-132">-Confirm</span></span>
<span data-ttu-id="a8ae0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ae0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ae0-134">-WhatIf</span></span>
<span data-ttu-id="a8ae0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ae0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ae0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ae0-137">CommonParameters</span></span>
<span data-ttu-id="a8ae0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ae0-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ae0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a8ae0-140">INPUTS</span></span>

### <span data-ttu-id="a8ae0-141">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="a8ae0-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a8ae0-142">System.String</span></span>

## <span data-ttu-id="a8ae0-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a8ae0-143">OUTPUTS</span></span>

### <span data-ttu-id="a8ae0-144">PSVerificationCodeResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a8ae0-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="a8ae0-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a8ae0-145">NOTES</span></span>

## <span data-ttu-id="a8ae0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8ae0-146">RELATED LINKS</span></span>
