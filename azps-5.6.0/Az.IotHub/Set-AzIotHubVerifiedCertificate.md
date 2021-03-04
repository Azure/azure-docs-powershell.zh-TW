---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 5e887dc2f608dd7e26c05e3b7ca73036efe2595a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915478"
---
# <span data-ttu-id="3eabe-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="3eabe-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="3eabe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3eabe-102">SYNOPSIS</span></span>
<span data-ttu-id="3eabe-103">驗證 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="3eabe-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="3eabe-104">語法</span><span class="sxs-lookup"><span data-stu-id="3eabe-104">SYNTAX</span></span>

### <span data-ttu-id="3eabe-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3eabe-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eabe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3eabe-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eabe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3eabe-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eabe-108">描述</span><span class="sxs-lookup"><span data-stu-id="3eabe-108">DESCRIPTION</span></span>
<span data-ttu-id="3eabe-109">上傳包含 Cmdlet Get-AzIotHubCertificateVerificationCode 所取得驗證碼的驗證憑證，以驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="3eabe-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="3eabe-110">這是驗證程式的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="3eabe-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="3eabe-111">有關 Azure IoT Hub 中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="3eabe-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="3eabe-112">例子</span><span class="sxs-lookup"><span data-stu-id="3eabe-112">EXAMPLES</span></span>

### <span data-ttu-id="3eabe-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="3eabe-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="3eabe-114">驗證 MyCertificate 私密金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="3eabe-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="3eabe-115">參數</span><span class="sxs-lookup"><span data-stu-id="3eabe-115">PARAMETERS</span></span>

### <span data-ttu-id="3eabe-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3eabe-116">-CertificateName</span></span>
<span data-ttu-id="3eabe-117">憑證名稱</span><span class="sxs-lookup"><span data-stu-id="3eabe-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="3eabe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eabe-118">-DefaultProfile</span></span>
<span data-ttu-id="3eabe-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3eabe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eabe-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="3eabe-120">-Etag</span></span>
<span data-ttu-id="3eabe-121">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="3eabe-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="3eabe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eabe-122">-InputObject</span></span>
<span data-ttu-id="3eabe-123">憑證物件</span><span class="sxs-lookup"><span data-stu-id="3eabe-123">Certificate Object</span></span>

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

### <span data-ttu-id="3eabe-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3eabe-124">-Name</span></span>
<span data-ttu-id="3eabe-125">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="3eabe-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3eabe-126">-路徑</span><span class="sxs-lookup"><span data-stu-id="3eabe-126">-Path</span></span>
<span data-ttu-id="3eabe-127">base-64 表示 X509 憑證 .cer 檔案或 .pem 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3eabe-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="3eabe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eabe-128">-ResourceGroupName</span></span>
<span data-ttu-id="3eabe-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="3eabe-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3eabe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eabe-130">-ResourceId</span></span>
<span data-ttu-id="3eabe-131">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3eabe-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="3eabe-132">-確認</span><span class="sxs-lookup"><span data-stu-id="3eabe-132">-Confirm</span></span>
<span data-ttu-id="3eabe-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3eabe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eabe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eabe-134">-WhatIf</span></span>
<span data-ttu-id="3eabe-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3eabe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eabe-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eabe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eabe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eabe-137">CommonParameters</span></span>
<span data-ttu-id="3eabe-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3eabe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eabe-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3eabe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eabe-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3eabe-140">INPUTS</span></span>

### <span data-ttu-id="3eabe-141">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="3eabe-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="3eabe-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3eabe-142">System.String</span></span>

## <span data-ttu-id="3eabe-143">輸出</span><span class="sxs-lookup"><span data-stu-id="3eabe-143">OUTPUTS</span></span>

### <span data-ttu-id="3eabe-144">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="3eabe-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="3eabe-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3eabe-145">NOTES</span></span>

## <span data-ttu-id="3eabe-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eabe-146">RELATED LINKS</span></span>
