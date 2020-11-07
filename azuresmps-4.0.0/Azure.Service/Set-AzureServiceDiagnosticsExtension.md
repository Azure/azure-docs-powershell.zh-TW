---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967493"
---
# <span data-ttu-id="a911e-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a911e-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="a911e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a911e-102">SYNOPSIS</span></span>
<span data-ttu-id="a911e-103">在已部署服務或部署上的指定角色或所有角色上啟用 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="a911e-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="a911e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a911e-104">SYNTAX</span></span>

### <span data-ttu-id="a911e-105">SetExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="a911e-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a911e-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="a911e-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a911e-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="a911e-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a911e-108">說明</span><span class="sxs-lookup"><span data-stu-id="a911e-108">DESCRIPTION</span></span>
<span data-ttu-id="a911e-109">**AzureServiceDiagnosticsExtension** Cmdlet 可在已部署服務或部署上的指定角色或所有角色上啟用 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="a911e-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="a911e-110">示例</span><span class="sxs-lookup"><span data-stu-id="a911e-110">EXAMPLES</span></span>

### <span data-ttu-id="a911e-111">範例1：啟用 Azure Diagnostics 延伸</span><span class="sxs-lookup"><span data-stu-id="a911e-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="a911e-112">這個命令會針對所有角色啟用 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="a911e-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="a911e-113">範例2：啟用指定角色的 Azure 診斷延伸</span><span class="sxs-lookup"><span data-stu-id="a911e-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="a911e-114">這個命令會啟用指定角色的 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="a911e-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="a911e-115">參數</span><span class="sxs-lookup"><span data-stu-id="a911e-115">PARAMETERS</span></span>

### <span data-ttu-id="a911e-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a911e-116">-CertificateThumbprint</span></span>
<span data-ttu-id="a911e-117">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a911e-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="a911e-118">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="a911e-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="a911e-119">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="a911e-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="a911e-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="a911e-121">指定 Azure Diagnostics 的配置陣列。</span><span class="sxs-lookup"><span data-stu-id="a911e-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="a911e-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="a911e-123">指定 Azure 診斷的配置。</span><span class="sxs-lookup"><span data-stu-id="a911e-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="a911e-124">您可以使用下列命令來下載架構：</span><span class="sxs-lookup"><span data-stu-id="a911e-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="a911e-125">-ExtensionId</span></span>
<span data-ttu-id="a911e-126">指定延伸識別碼</span><span class="sxs-lookup"><span data-stu-id="a911e-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a911e-127">-InformationAction</span></span>
<span data-ttu-id="a911e-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a911e-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a911e-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a911e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a911e-130">持續</span><span class="sxs-lookup"><span data-stu-id="a911e-130">Continue</span></span>
- <span data-ttu-id="a911e-131">理會</span><span class="sxs-lookup"><span data-stu-id="a911e-131">Ignore</span></span>
- <span data-ttu-id="a911e-132">看</span><span class="sxs-lookup"><span data-stu-id="a911e-132">Inquire</span></span>
- <span data-ttu-id="a911e-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a911e-133">SilentlyContinue</span></span>
- <span data-ttu-id="a911e-134">停止</span><span class="sxs-lookup"><span data-stu-id="a911e-134">Stop</span></span>
- <span data-ttu-id="a911e-135">封存</span><span class="sxs-lookup"><span data-stu-id="a911e-135">Suspend</span></span>

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

### <span data-ttu-id="a911e-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a911e-136">-InformationVariable</span></span>
<span data-ttu-id="a911e-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a911e-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a911e-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a911e-138">-Profile</span></span>
<span data-ttu-id="a911e-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a911e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a911e-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a911e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a911e-141">-角色</span><span class="sxs-lookup"><span data-stu-id="a911e-141">-Role</span></span>
<span data-ttu-id="a911e-142">指定要指定 Azure 診斷設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="a911e-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="a911e-143">如果您沒有指定此參數，則會將診斷設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="a911e-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a911e-144">-ServiceName</span></span>
<span data-ttu-id="a911e-145">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a911e-145">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-146">-槽</span><span class="sxs-lookup"><span data-stu-id="a911e-146">-Slot</span></span>
<span data-ttu-id="a911e-147">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="a911e-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="a911e-148">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="a911e-148">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="a911e-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="a911e-150">指定儲存空間帳戶端點。</span><span class="sxs-lookup"><span data-stu-id="a911e-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a911e-151">-StorageAccountKey</span></span>
<span data-ttu-id="a911e-152">指定儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="a911e-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a911e-153">-StorageAccountName</span></span>
<span data-ttu-id="a911e-154">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a911e-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-155">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a911e-155">-StorageContext</span></span>
<span data-ttu-id="a911e-156">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="a911e-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a911e-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="a911e-158">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="a911e-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="a911e-159">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="a911e-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-160">-版本</span><span class="sxs-lookup"><span data-stu-id="a911e-160">-Version</span></span>
<span data-ttu-id="a911e-161">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="a911e-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="a911e-162">-X509Certificate</span></span>
<span data-ttu-id="a911e-163">指定會自動上傳到雲端服務的 x.509 憑證，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="a911e-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a911e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a911e-164">CommonParameters</span></span>
<span data-ttu-id="a911e-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a911e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a911e-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a911e-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a911e-167">輸入</span><span class="sxs-lookup"><span data-stu-id="a911e-167">INPUTS</span></span>

## <span data-ttu-id="a911e-168">輸出</span><span class="sxs-lookup"><span data-stu-id="a911e-168">OUTPUTS</span></span>

## <span data-ttu-id="a911e-169">筆記</span><span class="sxs-lookup"><span data-stu-id="a911e-169">NOTES</span></span>

## <span data-ttu-id="a911e-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="a911e-170">RELATED LINKS</span></span>

[<span data-ttu-id="a911e-171">AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a911e-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="a911e-172">移除-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a911e-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


