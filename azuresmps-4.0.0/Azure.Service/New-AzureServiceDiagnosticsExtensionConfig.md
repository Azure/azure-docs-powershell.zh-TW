---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967344"
---
# <span data-ttu-id="6d43d-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="6d43d-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="6d43d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d43d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d43d-103"> (s) 或所有角色，為指定角色的診斷延伸產生配置。</span><span class="sxs-lookup"><span data-stu-id="6d43d-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="6d43d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d43d-104">SYNTAX</span></span>

### <span data-ttu-id="6d43d-105">NewExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="6d43d-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d43d-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="6d43d-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d43d-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="6d43d-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d43d-108">說明</span><span class="sxs-lookup"><span data-stu-id="6d43d-108">DESCRIPTION</span></span>
<span data-ttu-id="6d43d-109">**新的-AzureServiceDiagnosticsExtensionConfig** Cmdlet 會針對指定角色或所有角色的診斷延伸產生配置。</span><span class="sxs-lookup"><span data-stu-id="6d43d-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="6d43d-110">示例</span><span class="sxs-lookup"><span data-stu-id="6d43d-110">EXAMPLES</span></span>

### <span data-ttu-id="6d43d-111">範例1：為雲端服務中的所有角色建立 Azure 診斷延伸</span><span class="sxs-lookup"><span data-stu-id="6d43d-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="6d43d-112">這個命令會為雲端服務中的所有角色建立 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="6d43d-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="6d43d-113">範例2：為角色建立 Azure 診斷延伸</span><span class="sxs-lookup"><span data-stu-id="6d43d-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="6d43d-114">這個命令會為雲端服務中的角色 WebRole01 建立 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="6d43d-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="6d43d-115">參數</span><span class="sxs-lookup"><span data-stu-id="6d43d-115">PARAMETERS</span></span>

### <span data-ttu-id="6d43d-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6d43d-116">-CertificateThumbprint</span></span>
<span data-ttu-id="6d43d-117">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="6d43d-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="6d43d-118">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="6d43d-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="6d43d-119">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="6d43d-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="6d43d-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="6d43d-121">指定診斷配置路徑。</span><span class="sxs-lookup"><span data-stu-id="6d43d-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="6d43d-122">-ExtensionId</span></span>
<span data-ttu-id="6d43d-123">指定延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="6d43d-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6d43d-124">-InformationAction</span></span>
<span data-ttu-id="6d43d-125">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="6d43d-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6d43d-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6d43d-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d43d-127">持續</span><span class="sxs-lookup"><span data-stu-id="6d43d-127">Continue</span></span>
- <span data-ttu-id="6d43d-128">理會</span><span class="sxs-lookup"><span data-stu-id="6d43d-128">Ignore</span></span>
- <span data-ttu-id="6d43d-129">看</span><span class="sxs-lookup"><span data-stu-id="6d43d-129">Inquire</span></span>
- <span data-ttu-id="6d43d-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6d43d-130">SilentlyContinue</span></span>
- <span data-ttu-id="6d43d-131">停止</span><span class="sxs-lookup"><span data-stu-id="6d43d-131">Stop</span></span>
- <span data-ttu-id="6d43d-132">封存</span><span class="sxs-lookup"><span data-stu-id="6d43d-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6d43d-133">-InformationVariable</span></span>
<span data-ttu-id="6d43d-134">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="6d43d-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-135">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6d43d-135">-Profile</span></span>
<span data-ttu-id="6d43d-136">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6d43d-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d43d-137">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6d43d-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-138">-角色</span><span class="sxs-lookup"><span data-stu-id="6d43d-138">-Role</span></span>
<span data-ttu-id="6d43d-139">指定要指定其診斷設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="6d43d-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="6d43d-140">如果未指定，則會將診斷設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="6d43d-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d43d-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="6d43d-142">指定 [儲存空間帳戶] 端點。</span><span class="sxs-lookup"><span data-stu-id="6d43d-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6d43d-143">-StorageAccountKey</span></span>
<span data-ttu-id="6d43d-144">指定儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="6d43d-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6d43d-145">-StorageAccountName</span></span>
<span data-ttu-id="6d43d-146">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6d43d-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-147">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="6d43d-147">-StorageContext</span></span>
<span data-ttu-id="6d43d-148">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6d43d-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6d43d-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6d43d-150">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6d43d-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="6d43d-151">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="6d43d-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="6d43d-152">-X509Certificate</span></span>
<span data-ttu-id="6d43d-153">指定會自動上傳到雲端服務的 x.509 憑證，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="6d43d-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d43d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d43d-154">CommonParameters</span></span>
<span data-ttu-id="6d43d-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d43d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d43d-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d43d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d43d-157">輸入</span><span class="sxs-lookup"><span data-stu-id="6d43d-157">INPUTS</span></span>

## <span data-ttu-id="6d43d-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6d43d-158">OUTPUTS</span></span>

## <span data-ttu-id="6d43d-159">筆記</span><span class="sxs-lookup"><span data-stu-id="6d43d-159">NOTES</span></span>

## <span data-ttu-id="6d43d-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d43d-160">RELATED LINKS</span></span>

[<span data-ttu-id="6d43d-161">AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6d43d-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="6d43d-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6d43d-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


