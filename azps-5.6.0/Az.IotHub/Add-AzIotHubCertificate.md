---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 7796dae8d9eac66c3dd5b8fa22ed92c2c3c0b232
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913897"
---
# <span data-ttu-id="321ec-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="321ec-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="321ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="321ec-102">SYNOPSIS</span></span>
<span data-ttu-id="321ec-103">建立/更新 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="321ec-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="321ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="321ec-104">SYNTAX</span></span>

### <span data-ttu-id="321ec-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="321ec-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="321ec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="321ec-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="321ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="321ec-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="321ec-108">描述</span><span class="sxs-lookup"><span data-stu-id="321ec-108">DESCRIPTION</span></span>
<span data-ttu-id="321ec-109">上傳新的憑證，或以相同的名稱取代現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="321ec-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="321ec-110">有關 Azure IoT Hub 中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="321ec-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="321ec-111">例子</span><span class="sxs-lookup"><span data-stu-id="321ec-111">EXAMPLES</span></span>

### <span data-ttu-id="321ec-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="321ec-112">Example 1</span></span>
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

<span data-ttu-id="321ec-113">將 CA 憑證 CER 檔案上傳至 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="321ec-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="321ec-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="321ec-114">Example 2</span></span>
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

<span data-ttu-id="321ec-115">上傳新的 CER 檔案，以更新 IoT 中心中的 CA 憑證。</span><span class="sxs-lookup"><span data-stu-id="321ec-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="321ec-116">參數</span><span class="sxs-lookup"><span data-stu-id="321ec-116">PARAMETERS</span></span>

### <span data-ttu-id="321ec-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="321ec-117">-CertificateName</span></span>
<span data-ttu-id="321ec-118">憑證名稱</span><span class="sxs-lookup"><span data-stu-id="321ec-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="321ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321ec-119">-DefaultProfile</span></span>
<span data-ttu-id="321ec-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="321ec-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="321ec-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="321ec-121">-Etag</span></span>
<span data-ttu-id="321ec-122">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="321ec-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="321ec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="321ec-123">-InputObject</span></span>
<span data-ttu-id="321ec-124">憑證物件</span><span class="sxs-lookup"><span data-stu-id="321ec-124">Certificate Object</span></span>

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

### <span data-ttu-id="321ec-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="321ec-125">-Name</span></span>
<span data-ttu-id="321ec-126">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="321ec-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="321ec-127">-路徑</span><span class="sxs-lookup"><span data-stu-id="321ec-127">-Path</span></span>
<span data-ttu-id="321ec-128">base-64 表示 X509 憑證 .cer 檔案或 .pem 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="321ec-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="321ec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="321ec-129">-ResourceGroupName</span></span>
<span data-ttu-id="321ec-130">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="321ec-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="321ec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="321ec-131">-ResourceId</span></span>
<span data-ttu-id="321ec-132">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="321ec-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="321ec-133">-確認</span><span class="sxs-lookup"><span data-stu-id="321ec-133">-Confirm</span></span>
<span data-ttu-id="321ec-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="321ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="321ec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="321ec-135">-WhatIf</span></span>
<span data-ttu-id="321ec-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="321ec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="321ec-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="321ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="321ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321ec-138">CommonParameters</span></span>
<span data-ttu-id="321ec-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="321ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321ec-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="321ec-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321ec-141">輸入</span><span class="sxs-lookup"><span data-stu-id="321ec-141">INPUTS</span></span>

### <span data-ttu-id="321ec-142">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="321ec-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="321ec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="321ec-143">System.String</span></span>

## <span data-ttu-id="321ec-144">輸出</span><span class="sxs-lookup"><span data-stu-id="321ec-144">OUTPUTS</span></span>

### <span data-ttu-id="321ec-145">Microsoft.Azure.Commands.management.IotHub.models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="321ec-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="321ec-146">筆記</span><span class="sxs-lookup"><span data-stu-id="321ec-146">NOTES</span></span>

## <span data-ttu-id="321ec-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="321ec-147">RELATED LINKS</span></span>
