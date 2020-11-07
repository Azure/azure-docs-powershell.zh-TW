---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 87c7dea7e5cde48d6de6b9e9b756caf9cd2f2626
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787585"
---
# <span data-ttu-id="decf4-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="decf4-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="decf4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="decf4-102">SYNOPSIS</span></span>
<span data-ttu-id="decf4-103">建立/更新 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="decf4-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="decf4-104">句法</span><span class="sxs-lookup"><span data-stu-id="decf4-104">SYNTAX</span></span>

### <span data-ttu-id="decf4-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="decf4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="decf4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="decf4-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="decf4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="decf4-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="decf4-108">說明</span><span class="sxs-lookup"><span data-stu-id="decf4-108">DESCRIPTION</span></span>
<span data-ttu-id="decf4-109">上傳新憑證或使用相同名稱取代現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="decf4-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="decf4-110">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="decf4-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="decf4-111">示例</span><span class="sxs-lookup"><span data-stu-id="decf4-111">EXAMPLES</span></span>

### <span data-ttu-id="decf4-112">範例1</span><span class="sxs-lookup"><span data-stu-id="decf4-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="decf4-113">將 CA 憑證 CER 檔案上傳到 IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="decf4-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="decf4-114">範例2</span><span class="sxs-lookup"><span data-stu-id="decf4-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="decf4-115">透過上傳新的 CER 檔案，更新 IoT 中樞中的 CA 憑證。</span><span class="sxs-lookup"><span data-stu-id="decf4-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="decf4-116">參數</span><span class="sxs-lookup"><span data-stu-id="decf4-116">PARAMETERS</span></span>

### <span data-ttu-id="decf4-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="decf4-117">-CertificateName</span></span>
<span data-ttu-id="decf4-118">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="decf4-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="decf4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decf4-119">-DefaultProfile</span></span>
<span data-ttu-id="decf4-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="decf4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="decf4-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="decf4-121">-Etag</span></span>
<span data-ttu-id="decf4-122">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="decf4-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="decf4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="decf4-123">-InputObject</span></span>
<span data-ttu-id="decf4-124">憑證物件</span><span class="sxs-lookup"><span data-stu-id="decf4-124">Certificate Object</span></span>

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

### <span data-ttu-id="decf4-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="decf4-125">-Name</span></span>
<span data-ttu-id="decf4-126">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="decf4-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="decf4-127">-Path</span><span class="sxs-lookup"><span data-stu-id="decf4-127">-Path</span></span>
<span data-ttu-id="decf4-128">X509 certificate .cer 檔案或 pem 檔案路徑的 base-64 表示。</span><span class="sxs-lookup"><span data-stu-id="decf4-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="decf4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="decf4-129">-ResourceGroupName</span></span>
<span data-ttu-id="decf4-130">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="decf4-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="decf4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="decf4-131">-ResourceId</span></span>
<span data-ttu-id="decf4-132">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="decf4-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="decf4-133">-確認</span><span class="sxs-lookup"><span data-stu-id="decf4-133">-Confirm</span></span>
<span data-ttu-id="decf4-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="decf4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decf4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decf4-135">-WhatIf</span></span>
<span data-ttu-id="decf4-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="decf4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decf4-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="decf4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decf4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decf4-138">CommonParameters</span></span>
<span data-ttu-id="decf4-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="decf4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decf4-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="decf4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decf4-141">輸入</span><span class="sxs-lookup"><span data-stu-id="decf4-141">INPUTS</span></span>

### <span data-ttu-id="decf4-142">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="decf4-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="decf4-143">System.object</span><span class="sxs-lookup"><span data-stu-id="decf4-143">System.String</span></span>

## <span data-ttu-id="decf4-144">輸出</span><span class="sxs-lookup"><span data-stu-id="decf4-144">OUTPUTS</span></span>

### <span data-ttu-id="decf4-145">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="decf4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="decf4-146">筆記</span><span class="sxs-lookup"><span data-stu-id="decf4-146">NOTES</span></span>

## <span data-ttu-id="decf4-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="decf4-147">RELATED LINKS</span></span>
