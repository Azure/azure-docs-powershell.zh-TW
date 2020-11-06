---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 923852448f96ddc59de7a1c1562d6665b00e25ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612225"
---
# <span data-ttu-id="b54eb-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="b54eb-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="b54eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b54eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b54eb-103">產生 Azure IoT 中樞憑證的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="b54eb-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="b54eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b54eb-104">SYNTAX</span></span>

### <span data-ttu-id="b54eb-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b54eb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b54eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b54eb-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b54eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b54eb-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b54eb-108">說明</span><span class="sxs-lookup"><span data-stu-id="b54eb-108">DESCRIPTION</span></span>
<span data-ttu-id="b54eb-109">此驗證碼是用來完成憑證的已保管步驟證明。</span><span class="sxs-lookup"><span data-stu-id="b54eb-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="b54eb-110">使用此驗證碼作為使用 [根憑證私密金鑰] 簽署的新憑證的 CN。</span><span class="sxs-lookup"><span data-stu-id="b54eb-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="b54eb-111">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b54eb-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b54eb-112">示例</span><span class="sxs-lookup"><span data-stu-id="b54eb-112">EXAMPLES</span></span>

### <span data-ttu-id="b54eb-113">範例1</span><span class="sxs-lookup"><span data-stu-id="b54eb-113">Example 1</span></span>
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

<span data-ttu-id="b54eb-114">產生 MyCertificate 的驗證碼</span><span class="sxs-lookup"><span data-stu-id="b54eb-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="b54eb-115">參數</span><span class="sxs-lookup"><span data-stu-id="b54eb-115">PARAMETERS</span></span>

### <span data-ttu-id="b54eb-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b54eb-116">-CertificateName</span></span>
<span data-ttu-id="b54eb-117">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="b54eb-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="b54eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54eb-118">-DefaultProfile</span></span>
<span data-ttu-id="b54eb-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b54eb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b54eb-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="b54eb-120">-Etag</span></span>
<span data-ttu-id="b54eb-121">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="b54eb-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b54eb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b54eb-122">-InputObject</span></span>
<span data-ttu-id="b54eb-123">憑證物件</span><span class="sxs-lookup"><span data-stu-id="b54eb-123">Certificate Object</span></span>

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

### <span data-ttu-id="b54eb-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b54eb-124">-Name</span></span>
<span data-ttu-id="b54eb-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="b54eb-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b54eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="b54eb-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b54eb-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b54eb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b54eb-128">-ResourceId</span></span>
<span data-ttu-id="b54eb-129">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b54eb-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="b54eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54eb-130">CommonParameters</span></span>
<span data-ttu-id="b54eb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b54eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54eb-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b54eb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54eb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b54eb-133">INPUTS</span></span>

### <span data-ttu-id="b54eb-134">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b54eb-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="b54eb-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b54eb-135">System.String</span></span>

## <span data-ttu-id="b54eb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b54eb-136">OUTPUTS</span></span>

### <span data-ttu-id="b54eb-137">PSCertificateWithNonceDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b54eb-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="b54eb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b54eb-138">NOTES</span></span>

## <span data-ttu-id="b54eb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b54eb-139">RELATED LINKS</span></span>
