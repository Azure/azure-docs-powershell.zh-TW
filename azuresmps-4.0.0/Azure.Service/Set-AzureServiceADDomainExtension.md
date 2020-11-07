---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967494"
---
# <span data-ttu-id="0effd-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0effd-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="0effd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0effd-102">SYNOPSIS</span></span>
<span data-ttu-id="0effd-103">啟用雲端服務的 AD 網域延伸。</span><span class="sxs-lookup"><span data-stu-id="0effd-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="0effd-104">句法</span><span class="sxs-lookup"><span data-stu-id="0effd-104">SYNTAX</span></span>

### <span data-ttu-id="0effd-105">JoinDomainUsingEnumOptions (預設) </span><span class="sxs-lookup"><span data-stu-id="0effd-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0effd-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="0effd-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0effd-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="0effd-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0effd-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="0effd-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0effd-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="0effd-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0effd-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="0effd-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0effd-111">說明</span><span class="sxs-lookup"><span data-stu-id="0effd-111">DESCRIPTION</span></span>
<span data-ttu-id="0effd-112">**AzureServiceADDomainExtension** Cmdlet 可讓 AD (Active Directory) 雲端服務的網域延伸。</span><span class="sxs-lookup"><span data-stu-id="0effd-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="0effd-113">示例</span><span class="sxs-lookup"><span data-stu-id="0effd-113">EXAMPLES</span></span>

### <span data-ttu-id="0effd-114">sr-1</span><span class="sxs-lookup"><span data-stu-id="0effd-114">1:</span></span>
```

```

## <span data-ttu-id="0effd-115">參數</span><span class="sxs-lookup"><span data-stu-id="0effd-115">PARAMETERS</span></span>

### <span data-ttu-id="0effd-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0effd-116">-CertificateThumbprint</span></span>
<span data-ttu-id="0effd-117">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="0effd-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="0effd-118">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="0effd-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="0effd-119">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="0effd-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-120">-認證</span><span class="sxs-lookup"><span data-stu-id="0effd-120">-Credential</span></span>
<span data-ttu-id="0effd-121">指定要加入 AD 網域的認證。</span><span class="sxs-lookup"><span data-stu-id="0effd-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="0effd-122">認證包括使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="0effd-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-123">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="0effd-123">-DomainName</span></span>
<span data-ttu-id="0effd-124">指定 AD 網功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="0effd-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="0effd-125">-ExtensionId</span></span>
<span data-ttu-id="0effd-126">指定延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="0effd-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0effd-127">-InformationAction</span></span>
<span data-ttu-id="0effd-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0effd-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0effd-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0effd-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0effd-130">持續</span><span class="sxs-lookup"><span data-stu-id="0effd-130">Continue</span></span>
- <span data-ttu-id="0effd-131">理會</span><span class="sxs-lookup"><span data-stu-id="0effd-131">Ignore</span></span>
- <span data-ttu-id="0effd-132">看</span><span class="sxs-lookup"><span data-stu-id="0effd-132">Inquire</span></span>
- <span data-ttu-id="0effd-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0effd-133">SilentlyContinue</span></span>
- <span data-ttu-id="0effd-134">停止</span><span class="sxs-lookup"><span data-stu-id="0effd-134">Stop</span></span>
- <span data-ttu-id="0effd-135">封存</span><span class="sxs-lookup"><span data-stu-id="0effd-135">Suspend</span></span>

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

### <span data-ttu-id="0effd-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0effd-136">-InformationVariable</span></span>
<span data-ttu-id="0effd-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0effd-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0effd-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="0effd-138">-JoinOption</span></span>
<span data-ttu-id="0effd-139">指定 join 選項列舉。</span><span class="sxs-lookup"><span data-stu-id="0effd-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-140">-選項</span><span class="sxs-lookup"><span data-stu-id="0effd-140">-Options</span></span>
<span data-ttu-id="0effd-141">指定不帶正負號的整數聯結選項。</span><span class="sxs-lookup"><span data-stu-id="0effd-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="0effd-142">-OUPath</span></span>
<span data-ttu-id="0effd-143">針對 AD 網域加入作業，指定組織單位 (OU) 路徑。</span><span class="sxs-lookup"><span data-stu-id="0effd-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-144">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0effd-144">-Profile</span></span>
<span data-ttu-id="0effd-145">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0effd-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0effd-146">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0effd-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0effd-147">-重新開機</span><span class="sxs-lookup"><span data-stu-id="0effd-147">-Restart</span></span>
<span data-ttu-id="0effd-148">指定如果加入作業成功，是否要重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="0effd-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-149">-角色</span><span class="sxs-lookup"><span data-stu-id="0effd-149">-Role</span></span>
<span data-ttu-id="0effd-150">指定要指定其遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="0effd-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="0effd-151">如果未指定，AD 網域設定會套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="0effd-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0effd-152">-ServiceName</span></span>
<span data-ttu-id="0effd-153">指定雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0effd-153">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="0effd-154">-槽</span><span class="sxs-lookup"><span data-stu-id="0effd-154">-Slot</span></span>
<span data-ttu-id="0effd-155">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="0effd-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="0effd-156">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="0effd-156">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="0effd-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0effd-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="0effd-158">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="0effd-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="0effd-159">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="0effd-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="0effd-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="0effd-161">指定 ([使用者名稱] 和 [密碼]) 的認證，以脫離 AD 網域。</span><span class="sxs-lookup"><span data-stu-id="0effd-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-162">-版本</span><span class="sxs-lookup"><span data-stu-id="0effd-162">-Version</span></span>
<span data-ttu-id="0effd-163">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="0effd-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="0effd-164">-WorkgroupName</span></span>
<span data-ttu-id="0effd-165">指定工作組名稱。</span><span class="sxs-lookup"><span data-stu-id="0effd-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="0effd-166">-X509Certificate</span></span>
<span data-ttu-id="0effd-167">指定在指定的 x509 憑證會自動上傳到雲端服務，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="0effd-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0effd-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0effd-168">CommonParameters</span></span>
<span data-ttu-id="0effd-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0effd-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0effd-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0effd-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0effd-171">輸入</span><span class="sxs-lookup"><span data-stu-id="0effd-171">INPUTS</span></span>

## <span data-ttu-id="0effd-172">輸出</span><span class="sxs-lookup"><span data-stu-id="0effd-172">OUTPUTS</span></span>

## <span data-ttu-id="0effd-173">筆記</span><span class="sxs-lookup"><span data-stu-id="0effd-173">NOTES</span></span>

## <span data-ttu-id="0effd-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="0effd-174">RELATED LINKS</span></span>

[<span data-ttu-id="0effd-175">AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0effd-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="0effd-176">移除-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0effd-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="0effd-177">新-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="0effd-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


