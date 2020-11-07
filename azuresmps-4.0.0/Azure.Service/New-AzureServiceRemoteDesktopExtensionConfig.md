---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967341"
---
# <span data-ttu-id="b7c26-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="b7c26-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="b7c26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7c26-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c26-103">為部署產生遠端桌面延伸設定。</span><span class="sxs-lookup"><span data-stu-id="b7c26-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="b7c26-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7c26-104">SYNTAX</span></span>

### <span data-ttu-id="b7c26-105">NewExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="b7c26-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b7c26-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="b7c26-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b7c26-107">說明</span><span class="sxs-lookup"><span data-stu-id="b7c26-107">DESCRIPTION</span></span>
<span data-ttu-id="b7c26-108">**新的-AzureServiceRemoteDesktopExtensionConfig** Cmdlet 會針對部署的遠端桌面延伸產生配置。</span><span class="sxs-lookup"><span data-stu-id="b7c26-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="b7c26-109">示例</span><span class="sxs-lookup"><span data-stu-id="b7c26-109">EXAMPLES</span></span>

### <span data-ttu-id="b7c26-110">範例1：產生遠端桌面延伸設定</span><span class="sxs-lookup"><span data-stu-id="b7c26-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="b7c26-111">這個命令會針對指定的認證產生遠端桌面延伸設定。</span><span class="sxs-lookup"><span data-stu-id="b7c26-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="b7c26-112">範例2：針對指定的角色產生遠端桌面延伸設定</span><span class="sxs-lookup"><span data-stu-id="b7c26-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="b7c26-113">這個命令會針對指定的認證及 WebRole01 角色產生遠端桌面延伸設定。</span><span class="sxs-lookup"><span data-stu-id="b7c26-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="b7c26-114">參數</span><span class="sxs-lookup"><span data-stu-id="b7c26-114">PARAMETERS</span></span>

### <span data-ttu-id="b7c26-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b7c26-115">-CertificateThumbprint</span></span>
<span data-ttu-id="b7c26-116">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="b7c26-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="b7c26-117">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="b7c26-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="b7c26-118">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="b7c26-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="b7c26-119">-認證</span><span class="sxs-lookup"><span data-stu-id="b7c26-119">-Credential</span></span>
<span data-ttu-id="b7c26-120">指定要為遠端桌面啟用的認證。</span><span class="sxs-lookup"><span data-stu-id="b7c26-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="b7c26-121">認證包括使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="b7c26-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c26-122">-到期日</span><span class="sxs-lookup"><span data-stu-id="b7c26-122">-Expiration</span></span>
<span data-ttu-id="b7c26-123">指定 **DateTime** 物件，讓使用者在使用者帳戶到期時指定。</span><span class="sxs-lookup"><span data-stu-id="b7c26-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c26-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="b7c26-124">-ExtensionId</span></span>
<span data-ttu-id="b7c26-125">指定延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="b7c26-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c26-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b7c26-126">-InformationAction</span></span>
<span data-ttu-id="b7c26-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b7c26-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b7c26-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b7c26-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7c26-129">持續</span><span class="sxs-lookup"><span data-stu-id="b7c26-129">Continue</span></span>
- <span data-ttu-id="b7c26-130">理會</span><span class="sxs-lookup"><span data-stu-id="b7c26-130">Ignore</span></span>
- <span data-ttu-id="b7c26-131">看</span><span class="sxs-lookup"><span data-stu-id="b7c26-131">Inquire</span></span>
- <span data-ttu-id="b7c26-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b7c26-132">SilentlyContinue</span></span>
- <span data-ttu-id="b7c26-133">停止</span><span class="sxs-lookup"><span data-stu-id="b7c26-133">Stop</span></span>
- <span data-ttu-id="b7c26-134">封存</span><span class="sxs-lookup"><span data-stu-id="b7c26-134">Suspend</span></span>

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

### <span data-ttu-id="b7c26-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b7c26-135">-InformationVariable</span></span>
<span data-ttu-id="b7c26-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b7c26-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b7c26-137">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b7c26-137">-Profile</span></span>
<span data-ttu-id="b7c26-138">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7c26-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7c26-139">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b7c26-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7c26-140">-角色</span><span class="sxs-lookup"><span data-stu-id="b7c26-140">-Role</span></span>
<span data-ttu-id="b7c26-141">指定要指定其遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="b7c26-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="b7c26-142">如果未指定此參數，則會將遠端桌面設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="b7c26-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="b7c26-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b7c26-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b7c26-144">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="b7c26-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="b7c26-145">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="b7c26-145">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="b7c26-146">-版本</span><span class="sxs-lookup"><span data-stu-id="b7c26-146">-Version</span></span>
<span data-ttu-id="b7c26-147">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="b7c26-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c26-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="b7c26-148">-X509Certificate</span></span>
<span data-ttu-id="b7c26-149">指定在指定的 x509 憑證會自動上傳到雲端服務，並用於加密延伸私人配置。</span><span class="sxs-lookup"><span data-stu-id="b7c26-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="b7c26-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c26-150">CommonParameters</span></span>
<span data-ttu-id="b7c26-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7c26-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c26-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7c26-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c26-153">輸入</span><span class="sxs-lookup"><span data-stu-id="b7c26-153">INPUTS</span></span>

## <span data-ttu-id="b7c26-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b7c26-154">OUTPUTS</span></span>

## <span data-ttu-id="b7c26-155">筆記</span><span class="sxs-lookup"><span data-stu-id="b7c26-155">NOTES</span></span>

## <span data-ttu-id="b7c26-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7c26-156">RELATED LINKS</span></span>

[<span data-ttu-id="b7c26-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="b7c26-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


