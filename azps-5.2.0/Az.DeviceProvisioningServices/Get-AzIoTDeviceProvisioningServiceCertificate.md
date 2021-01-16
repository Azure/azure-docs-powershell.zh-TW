---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278689"
---
# <span data-ttu-id="f7955-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="f7955-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="f7955-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7955-102">SYNOPSIS</span></span>
<span data-ttu-id="f7955-103">列出 Azure IoT 中心裝置提供服務中包含的所有憑證或特定憑證。</span><span class="sxs-lookup"><span data-stu-id="f7955-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f7955-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7955-104">SYNTAX</span></span>

### <span data-ttu-id="f7955-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f7955-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7955-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f7955-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7955-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f7955-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7955-108">說明</span><span class="sxs-lookup"><span data-stu-id="f7955-108">DESCRIPTION</span></span>
<span data-ttu-id="f7955-109">如需 Azure IoT 中樞裝置提供服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 。</span><span class="sxs-lookup"><span data-stu-id="f7955-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="f7955-110">示例</span><span class="sxs-lookup"><span data-stu-id="f7955-110">EXAMPLES</span></span>

### <span data-ttu-id="f7955-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f7955-111">Example 1</span></span>
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

<span data-ttu-id="f7955-112">在 Azure IoT 中心裝置的 [提供服務] 中顯示「mycertificate」的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f7955-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="f7955-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f7955-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="f7955-114">使用管線列出 "myiotdps" 中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="f7955-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="f7955-115">參數</span><span class="sxs-lookup"><span data-stu-id="f7955-115">PARAMETERS</span></span>

### <span data-ttu-id="f7955-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="f7955-116">-CertificateName</span></span>
<span data-ttu-id="f7955-117">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="f7955-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="f7955-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7955-118">-DefaultProfile</span></span>
<span data-ttu-id="f7955-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7955-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7955-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f7955-120">-DpsObject</span></span>
<span data-ttu-id="f7955-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="f7955-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f7955-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7955-122">-Name</span></span>
<span data-ttu-id="f7955-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="f7955-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f7955-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7955-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7955-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f7955-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f7955-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7955-126">-ResourceId</span></span>
<span data-ttu-id="f7955-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f7955-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f7955-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7955-128">CommonParameters</span></span>
<span data-ttu-id="f7955-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7955-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7955-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7955-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7955-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f7955-131">INPUTS</span></span>

### <span data-ttu-id="f7955-132">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="f7955-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f7955-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f7955-133">System.String</span></span>

## <span data-ttu-id="f7955-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f7955-134">OUTPUTS</span></span>

### <span data-ttu-id="f7955-135">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="f7955-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="f7955-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f7955-136">NOTES</span></span>

## <span data-ttu-id="f7955-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7955-137">RELATED LINKS</span></span>
