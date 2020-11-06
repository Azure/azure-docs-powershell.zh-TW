---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: 45afd8c7f690be7785a14d336fabe7ac52a6f44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455300"
---
# <span data-ttu-id="11764-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="11764-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="11764-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11764-102">SYNOPSIS</span></span>
<span data-ttu-id="11764-103">驗證 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="11764-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11764-104">句法</span><span class="sxs-lookup"><span data-stu-id="11764-104">SYNTAX</span></span>

### <span data-ttu-id="11764-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11764-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11764-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11764-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11764-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11764-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11764-108">說明</span><span class="sxs-lookup"><span data-stu-id="11764-108">DESCRIPTION</span></span>
<span data-ttu-id="11764-109">透過上傳包含由 Cmdlet AzureRmIotHubCertificateVerificationCode 取得之驗證碼的驗證憑證來驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="11764-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="11764-110">這是已擁有的程式證明中的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="11764-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="11764-111">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="11764-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="11764-112">示例</span><span class="sxs-lookup"><span data-stu-id="11764-112">EXAMPLES</span></span>

### <span data-ttu-id="11764-113">範例1</span><span class="sxs-lookup"><span data-stu-id="11764-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="11764-114">驗證 MyCertificate 私用金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="11764-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="11764-115">參數</span><span class="sxs-lookup"><span data-stu-id="11764-115">PARAMETERS</span></span>

### <span data-ttu-id="11764-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="11764-116">-CertificateName</span></span>
<span data-ttu-id="11764-117">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="11764-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="11764-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11764-118">-DefaultProfile</span></span>
<span data-ttu-id="11764-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11764-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11764-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="11764-120">-Etag</span></span>
<span data-ttu-id="11764-121">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="11764-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="11764-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11764-122">-InputObject</span></span>
<span data-ttu-id="11764-123">憑證物件</span><span class="sxs-lookup"><span data-stu-id="11764-123">Certificate Object</span></span>

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

### <span data-ttu-id="11764-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="11764-124">-Name</span></span>
<span data-ttu-id="11764-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="11764-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="11764-126">-Path</span><span class="sxs-lookup"><span data-stu-id="11764-126">-Path</span></span>
<span data-ttu-id="11764-127">X509 certificate .cer 檔案或 pem 檔案路徑的 base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="11764-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="11764-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11764-128">-ResourceGroupName</span></span>
<span data-ttu-id="11764-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="11764-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11764-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11764-130">-ResourceId</span></span>
<span data-ttu-id="11764-131">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="11764-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="11764-132">-確認</span><span class="sxs-lookup"><span data-stu-id="11764-132">-Confirm</span></span>
<span data-ttu-id="11764-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11764-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11764-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11764-134">-WhatIf</span></span>
<span data-ttu-id="11764-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11764-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11764-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11764-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11764-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11764-137">CommonParameters</span></span>
<span data-ttu-id="11764-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11764-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11764-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11764-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11764-140">輸入</span><span class="sxs-lookup"><span data-stu-id="11764-140">INPUTS</span></span>

### <span data-ttu-id="11764-141">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="11764-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="11764-142">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="11764-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="11764-143">System.object</span><span class="sxs-lookup"><span data-stu-id="11764-143">System.String</span></span>

## <span data-ttu-id="11764-144">輸出</span><span class="sxs-lookup"><span data-stu-id="11764-144">OUTPUTS</span></span>

### <span data-ttu-id="11764-145">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="11764-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="11764-146">筆記</span><span class="sxs-lookup"><span data-stu-id="11764-146">NOTES</span></span>

## <span data-ttu-id="11764-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="11764-147">RELATED LINKS</span></span>
