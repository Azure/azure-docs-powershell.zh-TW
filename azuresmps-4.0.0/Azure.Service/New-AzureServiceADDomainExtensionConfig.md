---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967343"
---
# <span data-ttu-id="b89d7-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="b89d7-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="b89d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b89d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b89d7-103">為雲端服務的 AD 網域延伸產生配置。</span><span class="sxs-lookup"><span data-stu-id="b89d7-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="b89d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b89d7-104">SYNTAX</span></span>

### <span data-ttu-id="b89d7-105">JoinDomainUsingEnumOptions (預設) </span><span class="sxs-lookup"><span data-stu-id="b89d7-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b89d7-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="b89d7-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b89d7-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="b89d7-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b89d7-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="b89d7-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b89d7-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="b89d7-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b89d7-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="b89d7-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b89d7-111">說明</span><span class="sxs-lookup"><span data-stu-id="b89d7-111">DESCRIPTION</span></span>
<span data-ttu-id="b89d7-112">**AzureServiceADDomainExtensionConfig** Cmdlet 會為雲端服務的 Active DIRECTORY (AD) 網域延伸產生配置。</span><span class="sxs-lookup"><span data-stu-id="b89d7-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="b89d7-113">示例</span><span class="sxs-lookup"><span data-stu-id="b89d7-113">EXAMPLES</span></span>

### <span data-ttu-id="b89d7-114">範例1：指定廣告網域配置</span><span class="sxs-lookup"><span data-stu-id="b89d7-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="b89d7-115">這個命令會產生 AD 網域延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="b89d7-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="b89d7-116">參數</span><span class="sxs-lookup"><span data-stu-id="b89d7-116">PARAMETERS</span></span>

### <span data-ttu-id="b89d7-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b89d7-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b89d7-118">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="b89d7-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="b89d7-119">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="b89d7-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="b89d7-120">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="b89d7-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-121">-認證</span><span class="sxs-lookup"><span data-stu-id="b89d7-121">-Credential</span></span>
<span data-ttu-id="b89d7-122">指定要用來加入 AD 網域的認證。</span><span class="sxs-lookup"><span data-stu-id="b89d7-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="b89d7-123">認證包括使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="b89d7-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-124">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="b89d7-124">-DomainName</span></span>
<span data-ttu-id="b89d7-125">指定 AD 網功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b89d7-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="b89d7-126">-ExtensionId</span></span>
<span data-ttu-id="b89d7-127">指定延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="b89d7-127">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b89d7-128">-InformationAction</span></span>
<span data-ttu-id="b89d7-129">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b89d7-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b89d7-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b89d7-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b89d7-131">持續</span><span class="sxs-lookup"><span data-stu-id="b89d7-131">Continue</span></span>
- <span data-ttu-id="b89d7-132">理會</span><span class="sxs-lookup"><span data-stu-id="b89d7-132">Ignore</span></span>
- <span data-ttu-id="b89d7-133">看</span><span class="sxs-lookup"><span data-stu-id="b89d7-133">Inquire</span></span>
- <span data-ttu-id="b89d7-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b89d7-134">SilentlyContinue</span></span>
- <span data-ttu-id="b89d7-135">停止</span><span class="sxs-lookup"><span data-stu-id="b89d7-135">Stop</span></span>
- <span data-ttu-id="b89d7-136">封存</span><span class="sxs-lookup"><span data-stu-id="b89d7-136">Suspend</span></span>

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

### <span data-ttu-id="b89d7-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b89d7-137">-InformationVariable</span></span>
<span data-ttu-id="b89d7-138">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b89d7-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b89d7-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="b89d7-139">-JoinOption</span></span>
<span data-ttu-id="b89d7-140">指定 join 選項列舉。</span><span class="sxs-lookup"><span data-stu-id="b89d7-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-141">-選項</span><span class="sxs-lookup"><span data-stu-id="b89d7-141">-Options</span></span>
<span data-ttu-id="b89d7-142">指定不帶正負號的整數聯結選項。</span><span class="sxs-lookup"><span data-stu-id="b89d7-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="b89d7-143">-OUPath</span></span>
<span data-ttu-id="b89d7-144">指定 (OU 的組織單位) 加入 AD 網域加入作業的路徑。</span><span class="sxs-lookup"><span data-stu-id="b89d7-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-145">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b89d7-145">-Profile</span></span>
<span data-ttu-id="b89d7-146">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b89d7-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b89d7-147">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b89d7-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b89d7-148">-重新開機</span><span class="sxs-lookup"><span data-stu-id="b89d7-148">-Restart</span></span>
<span data-ttu-id="b89d7-149">指定如果加入作業成功，是否要重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="b89d7-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-150">-角色</span><span class="sxs-lookup"><span data-stu-id="b89d7-150">-Role</span></span>
<span data-ttu-id="b89d7-151">指定角色的選擇性陣列，以指定 AD 網域設定的遠端桌面配置。</span><span class="sxs-lookup"><span data-stu-id="b89d7-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="b89d7-152">如果您沒有指定此參數，則會將 AD 網域設定套用為所有角色的預設設定。</span><span class="sxs-lookup"><span data-stu-id="b89d7-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b89d7-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b89d7-154">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="b89d7-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="b89d7-155">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="b89d7-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="b89d7-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="b89d7-157">指定 ([使用者名稱] 和 [密碼]) 的認證，以脫離 AD 網域。</span><span class="sxs-lookup"><span data-stu-id="b89d7-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-158">-版本</span><span class="sxs-lookup"><span data-stu-id="b89d7-158">-Version</span></span>
<span data-ttu-id="b89d7-159">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="b89d7-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="b89d7-160">-WorkgroupName</span></span>
<span data-ttu-id="b89d7-161">指定工作組名稱。</span><span class="sxs-lookup"><span data-stu-id="b89d7-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="b89d7-162">-X509Certificate</span></span>
<span data-ttu-id="b89d7-163">指定會自動上傳到雲端服務的 x.509 憑證，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="b89d7-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89d7-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89d7-164">CommonParameters</span></span>
<span data-ttu-id="b89d7-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b89d7-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89d7-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b89d7-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89d7-167">輸入</span><span class="sxs-lookup"><span data-stu-id="b89d7-167">INPUTS</span></span>

## <span data-ttu-id="b89d7-168">輸出</span><span class="sxs-lookup"><span data-stu-id="b89d7-168">OUTPUTS</span></span>

## <span data-ttu-id="b89d7-169">筆記</span><span class="sxs-lookup"><span data-stu-id="b89d7-169">NOTES</span></span>

## <span data-ttu-id="b89d7-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="b89d7-170">RELATED LINKS</span></span>

[<span data-ttu-id="b89d7-171">AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b89d7-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="b89d7-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b89d7-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


