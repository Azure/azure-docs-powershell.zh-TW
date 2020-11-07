---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967342"
---
# <span data-ttu-id="ad4b9-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="ad4b9-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="ad4b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4b9-103">為部署建立雲端服務擴充配置。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="ad4b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad4b9-104">SYNTAX</span></span>

### <span data-ttu-id="ad4b9-105">NewExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="ad4b9-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad4b9-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ad4b9-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad4b9-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ad4b9-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad4b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad4b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ad4b9-109">**新的-AzureServiceExtensionConfig** Cmdlet 會為部署建立雲端服務擴充配置。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="ad4b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad4b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ad4b9-111">範例1：建立延伸設定</span><span class="sxs-lookup"><span data-stu-id="ad4b9-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="ad4b9-112">這個命令會指定延伸設定。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="ad4b9-113">範例2：為角色建立延伸設定</span><span class="sxs-lookup"><span data-stu-id="ad4b9-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="ad4b9-114">這個命令會指定角色 WebRole1 的延伸設定。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="ad4b9-115">參數</span><span class="sxs-lookup"><span data-stu-id="ad4b9-115">PARAMETERS</span></span>

### <span data-ttu-id="ad4b9-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ad4b9-116">-CertificateThumbprint</span></span>
<span data-ttu-id="ad4b9-117">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="ad4b9-118">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="ad4b9-119">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ad4b9-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="ad4b9-120">-ExtensionId</span></span>
<span data-ttu-id="ad4b9-121">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b9-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ad4b9-122">-ExtensionName</span></span>
<span data-ttu-id="ad4b9-123">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b9-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="ad4b9-124">-ExtensionState</span></span>
<span data-ttu-id="ad4b9-125">指定延伸的狀態。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="ad4b9-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ad4b9-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad4b9-127">啟用</span><span class="sxs-lookup"><span data-stu-id="ad4b9-127">Enable</span></span> 
- <span data-ttu-id="ad4b9-128">禁止</span><span class="sxs-lookup"><span data-stu-id="ad4b9-128">Disable</span></span> 
- <span data-ttu-id="ad4b9-129">卸下</span><span class="sxs-lookup"><span data-stu-id="ad4b9-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b9-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ad4b9-130">-InformationAction</span></span>
<span data-ttu-id="ad4b9-131">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ad4b9-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ad4b9-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad4b9-133">持續</span><span class="sxs-lookup"><span data-stu-id="ad4b9-133">Continue</span></span>
- <span data-ttu-id="ad4b9-134">理會</span><span class="sxs-lookup"><span data-stu-id="ad4b9-134">Ignore</span></span>
- <span data-ttu-id="ad4b9-135">看</span><span class="sxs-lookup"><span data-stu-id="ad4b9-135">Inquire</span></span>
- <span data-ttu-id="ad4b9-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ad4b9-136">SilentlyContinue</span></span>
- <span data-ttu-id="ad4b9-137">停止</span><span class="sxs-lookup"><span data-stu-id="ad4b9-137">Stop</span></span>
- <span data-ttu-id="ad4b9-138">封存</span><span class="sxs-lookup"><span data-stu-id="ad4b9-138">Suspend</span></span>

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

### <span data-ttu-id="ad4b9-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ad4b9-139">-InformationVariable</span></span>
<span data-ttu-id="ad4b9-140">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ad4b9-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4b9-141">-PrivateConfiguration</span></span>
<span data-ttu-id="ad4b9-142">指定私人配置文字。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b9-143">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ad4b9-143">-Profile</span></span>
<span data-ttu-id="ad4b9-144">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad4b9-145">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad4b9-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ad4b9-146">-ProviderNamespace</span></span>
<span data-ttu-id="ad4b9-147">指定副檔名的提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b9-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4b9-148">-PublicConfiguration</span></span>
<span data-ttu-id="ad4b9-149">指定公用配置文字。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b9-150">-角色</span><span class="sxs-lookup"><span data-stu-id="ad4b9-150">-Role</span></span>
<span data-ttu-id="ad4b9-151">指定要為其指定遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="ad4b9-152">如果未指定，遠端桌面設定會套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="ad4b9-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ad4b9-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ad4b9-154">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="ad4b9-155">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="ad4b9-156">-版本</span><span class="sxs-lookup"><span data-stu-id="ad4b9-156">-Version</span></span>
<span data-ttu-id="ad4b9-157">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="ad4b9-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="ad4b9-158">-X509Certificate</span></span>
<span data-ttu-id="ad4b9-159">指定在指定的 x509 憑證會自動上傳到雲端服務，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="ad4b9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4b9-160">CommonParameters</span></span>
<span data-ttu-id="ad4b9-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4b9-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad4b9-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4b9-163">輸入</span><span class="sxs-lookup"><span data-stu-id="ad4b9-163">INPUTS</span></span>

## <span data-ttu-id="ad4b9-164">輸出</span><span class="sxs-lookup"><span data-stu-id="ad4b9-164">OUTPUTS</span></span>

## <span data-ttu-id="ad4b9-165">筆記</span><span class="sxs-lookup"><span data-stu-id="ad4b9-165">NOTES</span></span>

## <span data-ttu-id="ad4b9-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad4b9-166">RELATED LINKS</span></span>

[<span data-ttu-id="ad4b9-167">AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ad4b9-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="ad4b9-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ad4b9-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


