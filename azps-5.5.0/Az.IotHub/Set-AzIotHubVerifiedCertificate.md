---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131822"
---
# <span data-ttu-id="94ba6-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="94ba6-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="94ba6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="94ba6-103">驗證 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="94ba6-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="94ba6-104">句法</span><span class="sxs-lookup"><span data-stu-id="94ba6-104">SYNTAX</span></span>

### <span data-ttu-id="94ba6-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="94ba6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94ba6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94ba6-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ba6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94ba6-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94ba6-108">說明</span><span class="sxs-lookup"><span data-stu-id="94ba6-108">DESCRIPTION</span></span>
<span data-ttu-id="94ba6-109">透過上傳包含由 Cmdlet AzIotHubCertificateVerificationCode 取得之驗證碼的驗證憑證來驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="94ba6-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="94ba6-110">這是已擁有的程式證明中的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="94ba6-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="94ba6-111">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="94ba6-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="94ba6-112">示例</span><span class="sxs-lookup"><span data-stu-id="94ba6-112">EXAMPLES</span></span>

### <span data-ttu-id="94ba6-113">範例1</span><span class="sxs-lookup"><span data-stu-id="94ba6-113">Example 1</span></span>
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

<span data-ttu-id="94ba6-114">驗證 MyCertificate 私用金鑰的擁有權。</span><span class="sxs-lookup"><span data-stu-id="94ba6-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="94ba6-115">參數</span><span class="sxs-lookup"><span data-stu-id="94ba6-115">PARAMETERS</span></span>

### <span data-ttu-id="94ba6-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="94ba6-116">-CertificateName</span></span>
<span data-ttu-id="94ba6-117">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="94ba6-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="94ba6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ba6-118">-DefaultProfile</span></span>
<span data-ttu-id="94ba6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94ba6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ba6-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="94ba6-120">-Etag</span></span>
<span data-ttu-id="94ba6-121">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="94ba6-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="94ba6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94ba6-122">-InputObject</span></span>
<span data-ttu-id="94ba6-123">憑證物件</span><span class="sxs-lookup"><span data-stu-id="94ba6-123">Certificate Object</span></span>

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

### <span data-ttu-id="94ba6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="94ba6-124">-Name</span></span>
<span data-ttu-id="94ba6-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="94ba6-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="94ba6-126">-Path</span><span class="sxs-lookup"><span data-stu-id="94ba6-126">-Path</span></span>
<span data-ttu-id="94ba6-127">X509 certificate .cer 檔案或 pem 檔案路徑的 base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="94ba6-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="94ba6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ba6-128">-ResourceGroupName</span></span>
<span data-ttu-id="94ba6-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="94ba6-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="94ba6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94ba6-130">-ResourceId</span></span>
<span data-ttu-id="94ba6-131">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="94ba6-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="94ba6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="94ba6-132">-Confirm</span></span>
<span data-ttu-id="94ba6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94ba6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ba6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ba6-134">-WhatIf</span></span>
<span data-ttu-id="94ba6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94ba6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94ba6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94ba6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ba6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ba6-137">CommonParameters</span></span>
<span data-ttu-id="94ba6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94ba6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ba6-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94ba6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ba6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="94ba6-140">INPUTS</span></span>

### <span data-ttu-id="94ba6-141">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="94ba6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="94ba6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="94ba6-142">System.String</span></span>

## <span data-ttu-id="94ba6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="94ba6-143">OUTPUTS</span></span>

### <span data-ttu-id="94ba6-144">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="94ba6-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="94ba6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="94ba6-145">NOTES</span></span>

## <span data-ttu-id="94ba6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="94ba6-146">RELATED LINKS</span></span>
