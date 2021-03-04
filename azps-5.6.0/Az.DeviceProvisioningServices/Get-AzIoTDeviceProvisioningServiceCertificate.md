---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 788759abe543d3bddf3c67abe2ed37aafca6be3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908558"
---
# <span data-ttu-id="14c2b-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="14c2b-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="14c2b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="14c2b-103">列出 Azure IoT Hub 裝置設置服務中包含的所有憑證或特定憑證。</span><span class="sxs-lookup"><span data-stu-id="14c2b-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="14c2b-104">語法</span><span class="sxs-lookup"><span data-stu-id="14c2b-104">SYNTAX</span></span>

### <span data-ttu-id="14c2b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14c2b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c2b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="14c2b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c2b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="14c2b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c2b-108">描述</span><span class="sxs-lookup"><span data-stu-id="14c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="14c2b-109">有關 Azure IoT Hub 裝置設置服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates 。</span><span class="sxs-lookup"><span data-stu-id="14c2b-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="14c2b-110">例子</span><span class="sxs-lookup"><span data-stu-id="14c2b-110">EXAMPLES</span></span>

### <span data-ttu-id="14c2b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="14c2b-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="14c2b-112">顯示 Azure IoT Hub 裝置布布服務中「mycertificate」的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="14c2b-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="14c2b-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="14c2b-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="14c2b-114">使用管線列出「myiotdps」中所有的憑證。</span><span class="sxs-lookup"><span data-stu-id="14c2b-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="14c2b-115">參數</span><span class="sxs-lookup"><span data-stu-id="14c2b-115">PARAMETERS</span></span>

### <span data-ttu-id="14c2b-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="14c2b-116">-CertificateName</span></span>
<span data-ttu-id="14c2b-117">憑證名稱</span><span class="sxs-lookup"><span data-stu-id="14c2b-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="14c2b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c2b-118">-DefaultProfile</span></span>
<span data-ttu-id="14c2b-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14c2b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c2b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="14c2b-120">-DpsObject</span></span>
<span data-ttu-id="14c2b-121">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="14c2b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="14c2b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="14c2b-122">-Name</span></span>
<span data-ttu-id="14c2b-123">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="14c2b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="14c2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="14c2b-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="14c2b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="14c2b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14c2b-126">-ResourceId</span></span>
<span data-ttu-id="14c2b-127">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="14c2b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="14c2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c2b-128">CommonParameters</span></span>
<span data-ttu-id="14c2b-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14c2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c2b-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="14c2b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c2b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="14c2b-131">INPUTS</span></span>

### <span data-ttu-id="14c2b-132">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="14c2b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="14c2b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="14c2b-133">System.String</span></span>

## <span data-ttu-id="14c2b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="14c2b-134">OUTPUTS</span></span>

### <span data-ttu-id="14c2b-135">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="14c2b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="14c2b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="14c2b-136">NOTES</span></span>

## <span data-ttu-id="14c2b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="14c2b-137">RELATED LINKS</span></span>
