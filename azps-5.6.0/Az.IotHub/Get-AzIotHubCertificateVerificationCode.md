---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 5cad5da87b15430c33d748250501862dae77a38e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911093"
---
# <span data-ttu-id="40cc0-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="40cc0-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="40cc0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="40cc0-103">產生 Azure IoT 中心憑證的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="40cc0-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="40cc0-104">語法</span><span class="sxs-lookup"><span data-stu-id="40cc0-104">SYNTAX</span></span>

### <span data-ttu-id="40cc0-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="40cc0-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40cc0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40cc0-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40cc0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="40cc0-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40cc0-108">描述</span><span class="sxs-lookup"><span data-stu-id="40cc0-108">DESCRIPTION</span></span>
<span data-ttu-id="40cc0-109">此驗證碼是用來完成憑證的驗證步驟。</span><span class="sxs-lookup"><span data-stu-id="40cc0-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="40cc0-110">使用此驗證碼做為使用根憑證私人金鑰簽署之新憑證的 CN。</span><span class="sxs-lookup"><span data-stu-id="40cc0-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="40cc0-111">有關 Azure IoT Hub 中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="40cc0-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="40cc0-112">例子</span><span class="sxs-lookup"><span data-stu-id="40cc0-112">EXAMPLES</span></span>

### <span data-ttu-id="40cc0-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="40cc0-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="40cc0-114">產生 MyCertificate 的驗證碼</span><span class="sxs-lookup"><span data-stu-id="40cc0-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="40cc0-115">參數</span><span class="sxs-lookup"><span data-stu-id="40cc0-115">PARAMETERS</span></span>

### <span data-ttu-id="40cc0-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="40cc0-116">-CertificateName</span></span>
<span data-ttu-id="40cc0-117">憑證名稱</span><span class="sxs-lookup"><span data-stu-id="40cc0-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="40cc0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cc0-118">-DefaultProfile</span></span>
<span data-ttu-id="40cc0-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40cc0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40cc0-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="40cc0-120">-Etag</span></span>
<span data-ttu-id="40cc0-121">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="40cc0-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="40cc0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40cc0-122">-InputObject</span></span>
<span data-ttu-id="40cc0-123">憑證物件</span><span class="sxs-lookup"><span data-stu-id="40cc0-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40cc0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="40cc0-124">-Name</span></span>
<span data-ttu-id="40cc0-125">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="40cc0-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cc0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cc0-126">-ResourceGroupName</span></span>
<span data-ttu-id="40cc0-127">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="40cc0-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cc0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40cc0-128">-ResourceId</span></span>
<span data-ttu-id="40cc0-129">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="40cc0-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="40cc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cc0-130">CommonParameters</span></span>
<span data-ttu-id="40cc0-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40cc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cc0-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="40cc0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cc0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="40cc0-133">INPUTS</span></span>

### <span data-ttu-id="40cc0-134">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="40cc0-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="40cc0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="40cc0-135">System.String</span></span>

## <span data-ttu-id="40cc0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="40cc0-136">OUTPUTS</span></span>

### <span data-ttu-id="40cc0-137">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateWithNouvDescription</span><span class="sxs-lookup"><span data-stu-id="40cc0-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="40cc0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="40cc0-138">NOTES</span></span>

## <span data-ttu-id="40cc0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="40cc0-139">RELATED LINKS</span></span>
