---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 659998a6a82c08ab57697767276e2357002a4182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612515"
---
# <span data-ttu-id="a6286-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a6286-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a6286-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6286-102">SYNOPSIS</span></span>
<span data-ttu-id="a6286-103">驗證 Azure IoT 中樞裝置置備服務憑證。</span><span class="sxs-lookup"><span data-stu-id="a6286-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="a6286-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6286-104">SYNTAX</span></span>

### <span data-ttu-id="a6286-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a6286-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6286-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6286-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6286-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6286-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6286-108">說明</span><span class="sxs-lookup"><span data-stu-id="a6286-108">DESCRIPTION</span></span>
<span data-ttu-id="a6286-109">透過上傳包含呼叫產生驗證程式代碼所取得之驗證碼的驗證憑證來驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="a6286-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="a6286-110">這是已擁有的程式證明中的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="a6286-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="a6286-111">如需 Azure IoT 中樞裝置置備服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="a6286-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="a6286-112">示例</span><span class="sxs-lookup"><span data-stu-id="a6286-112">EXAMPLES</span></span>

### <span data-ttu-id="a6286-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a6286-113">Example 1</span></span>
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

<span data-ttu-id="a6286-114">確認「mycertificate」私用金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="a6286-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="a6286-115">範例2</span><span class="sxs-lookup"><span data-stu-id="a6286-115">Example 2</span></span>
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

<span data-ttu-id="a6286-116">使用管線驗證「mycertificate」私用金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="a6286-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="a6286-117">參數</span><span class="sxs-lookup"><span data-stu-id="a6286-117">PARAMETERS</span></span>

### <span data-ttu-id="a6286-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a6286-118">-CertificateName</span></span>
<span data-ttu-id="a6286-119">Iot 裝置預配服務憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="a6286-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="a6286-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6286-120">-DefaultProfile</span></span>
<span data-ttu-id="a6286-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6286-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6286-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="a6286-122">-Etag</span></span>
<span data-ttu-id="a6286-123">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="a6286-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a6286-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6286-124">-InputObject</span></span>
<span data-ttu-id="a6286-125">IoT 裝置預配服務憑證物件</span><span class="sxs-lookup"><span data-stu-id="a6286-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="a6286-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6286-126">-Name</span></span>
<span data-ttu-id="a6286-127">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="a6286-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a6286-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a6286-128">-Path</span></span>
<span data-ttu-id="a6286-129">X509 certificate .cer 檔案或 pem 檔案路徑的基本64表示形式</span><span class="sxs-lookup"><span data-stu-id="a6286-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="a6286-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6286-130">-ResourceGroupName</span></span>
<span data-ttu-id="a6286-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a6286-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6286-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6286-132">-ResourceId</span></span>
<span data-ttu-id="a6286-133">IoT 裝置預配服務憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a6286-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="a6286-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a6286-134">-Confirm</span></span>
<span data-ttu-id="a6286-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6286-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6286-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6286-136">-WhatIf</span></span>
<span data-ttu-id="a6286-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6286-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6286-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6286-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6286-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6286-139">CommonParameters</span></span>
<span data-ttu-id="a6286-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6286-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6286-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6286-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6286-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a6286-142">INPUTS</span></span>

### <span data-ttu-id="a6286-143">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a6286-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="a6286-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a6286-144">System.String</span></span>

## <span data-ttu-id="a6286-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a6286-145">OUTPUTS</span></span>

### <span data-ttu-id="a6286-146">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="a6286-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a6286-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a6286-147">NOTES</span></span>

## <span data-ttu-id="a6286-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6286-148">RELATED LINKS</span></span>
